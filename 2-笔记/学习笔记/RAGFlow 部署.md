# RAGFlow 单独部署

## 软件介绍

**RAGFlow** 是 [infiniflow](https://github.com/infiniflow/ragflow) 开源的 RAG（检索增强生成）引擎，基于 Apache-2.0 协议。核心卖点是**深度文档理解**——能识别页眉页脚、表格、多栏排版、公式和图片中的语义信息，将复杂非结构化数据精准切块后送入 LLM。

### 核心特性

- **深度文档解析**：按文档类型（论文/书籍/法律/简历/PPT/表格/QA）智能切块，保留结构语义
- **混合检索 + 重排序**：BM25 关键词 + 向量相似度 + 融合重排序，支持跨语言检索
- **Agent 编排**：可视化画布拖拽编排工作流，内置翻译/SEO/研究报告等模板，支持 MCP、代码执行器、Memory
- **GraphRAG**：自动抽取实体关系构建知识图谱，文件增删时动态维护
- **接地气引用**：回答直接链接回原始文档段落，减少幻觉
- **异构数据源**：支持 PDF/Word/PPT/Excel/图片/扫描件/网页/邮件等

### 技术架构

- 后端 Python（DeepDoc 文档引擎 + RAGFlow Agent 编排引擎 + LLM 对接层）
- 前端 React + TypeScript
- 默认向量数据库 Infinity（自研），可选 Elasticsearch
- Docker Compose 微服务部署，自带 MySQL / Redis / MinIO / Elasticsearch

> 最低建议 4 核 CPU + 16GB 内存。LLM 需自行对接（支持 OpenAI / DeepSeek / 通义千问 / Ollama 等 30+ 模型提供商）。

## 1. 克隆仓库

```bash
git clone https://github.com/infiniflow/ragflow.git
cd ragflow/docker
```

## 2. 修改配置

编辑 `.env` 文件：

```env
# 修改 HTTP 端口，避免与其他服务冲突（默认 80 改为 8090）
SVR_WEB_HTTP_PORT=8090

# 关闭开放注册，仅允许 admin 用户
REGISTER_ENABLED=0
```

## 3. 启动服务

```bash
docker compose -f docker-compose.yml up -d
```

## 4. 重置 admin 密码

本地部署时 admin 密码无法通过 `.env` 预置（`DEFAULT_SUPERUSER_*` 变量不生效），需进入容器手动重置：

```bash
docker exec -it ragflow-ragflow-cpu-1 bash
cd /ragflow && quart --app api.apps reset-password
```

按提示输入新密码。

## 5. 验证

```bash
curl http://127.0.0.1:9380/api/v1/system/healthz
```

## 6. 停止

```bash
docker compose down          # 保留数据
docker compose down -v       # 清理数据卷（谨慎）
```

> 更多详情：[GitHub](https://github.com/infiniflow/ragflow) | [官网](https://ragflow.io/)

---

## 常用 API 接口

所有接口需要在 Header 中携带 API Key：`Authorization: Bearer <RAGFLOW_API_KEY>`

### 系统

| 方法  | 路径                     | 说明         |
| ----- | ------------------------ | ------------ |
| `GET` | `/api/v1/system/healthz` | 健康检查     |
| `GET` | `/api/v1/models`         | 列出可用模型 |

### 知识库

| 方法     | 路径                    | 说明           |
| -------- | ----------------------- | -------------- |
| `POST`   | `/api/v1/datasets`      | 创建知识库     |
| `GET`    | `/api/v1/datasets`      | 列出知识库     |
| `PUT`    | `/api/v1/datasets/{id}` | 更新知识库     |
| `DELETE` | `/api/v1/datasets`      | 批量删除知识库 |

```bash
# 列出知识库
curl -H "Authorization: Bearer $API_KEY" \
  http://127.0.0.1:9380/api/v1/datasets
```

### 文件

| 方法     | 路径            | 说明     |
| -------- | --------------- | -------- |
| `POST`   | `/api/v1/files` | 上传文件 |
| `GET`    | `/api/v1/files` | 列出文件 |
| `DELETE` | `/api/v1/files` | 删除文件 |

```bash
# 上传文件到知识库
curl -X POST -H "Authorization: Bearer $API_KEY" \
  -F "file=@doc.pdf" \
  http://127.0.0.1:9380/api/v1/files
```

### 文档

| 方法     | 路径                              | 说明             |
| -------- | --------------------------------- | ---------------- |
| `GET`    | `/api/v1/datasets/{id}/documents` | 列出知识库下文档 |
| `POST`   | `/api/v1/datasets/{id}/documents` | 添加文档到知识库 |
| `DELETE` | `/api/v1/datasets/{id}/documents` | 批量删除文档     |

```bash
# 将已有文件关联到知识库并开始解析
curl -X POST -H "Authorization: Bearer $API_KEY" \
  http://127.0.0.1:9380/api/v1/datasets/{dataset_id}/documents \
  -d '{"file_ids": ["file_id_1"], "name": "doc-name"}'
```

### Chat 对话

| 方法   | 路径                          | 说明                         |
| ------ | ----------------------------- | ---------------------------- |
| `POST` | `/api/v1/chat/completions`    | 发起对话（RAGFlow 原生格式） |
| `POST` | `/api/v1/chat/recommandation` | 获取推荐问题                 |

```bash
# 对话
curl -X POST -H "Authorization: Bearer $API_KEY" \
  http://127.0.0.1:9380/api/v1/chat/completions \
  -d '{
    "chat_id": "<chat_id>",
    "session_id": "<session_id>",
    "question": "你好"
  }'
```

### Agent

| 方法   | 路径                              | 说明              |
| ------ | --------------------------------- | ----------------- |
| `POST` | `/api/v1/agents/{id}/sessions`    | 创建 Agent 会话   |
| `POST` | `/api/v1/agents/{id}/completions` | 向 Agent 发送消息 |

```bash
# 创建 Agent 会话
curl -X POST -H "Authorization: Bearer $API_KEY" \
  http://127.0.0.1:9380/api/v1/agents/{agent_id}/sessions

# 对话
curl -X POST -H "Authorization: Bearer $API_KEY" \
  http://127.0.0.1:9380/api/v1/agents/{agent_id}/completions \
  -d '{"session_id": "<id>", "question": "你好"}'
```

### OpenAI 兼容接口

| 方法   | 路径                                                | 说明                     |
| ------ | --------------------------------------------------- | ------------------------ |
| `POST` | `/api/v1/openai/{chat_id}/chat/completions`         | Chat 助手（OpenAI 格式） |
| `POST` | `/api/v1/agents_openai/{agent_id}/chat/completions` | Agent（OpenAI 格式）     |

```python
from openai import OpenAI

client = OpenAI(
    api_key="your-ragflow-api-key",
    base_url="http://127.0.0.1:9380/api/v1/openai/{chat_id}"
)

completion = client.chat.completions.create(
    model="model-name",
    messages=[{"role": "user", "content": "你好"}],
    stream=True
)
for chunk in completion:
    print(chunk.choices[0].delta.content, end="")
```

> `chat_id` 从 UI 嵌入功能获取；`agent_id` 从 Agent 列表 URL 获取。
