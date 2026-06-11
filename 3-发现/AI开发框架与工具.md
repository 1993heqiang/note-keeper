# AI 开发框架与工具

> 面向开发者的 AI 框架、库、SDK 和开发工具。从模型训练到推理部署的全栈工具链。

## 核心框架

| 名称 | 描述 | 地址 |
|---|---|---|
| `PyTorch` | 开源 Python 机器学习库，基于 Torch，底层由 C++ 实现，广泛应用于 CV 和 NLP。 | [Link](https://github.com/pytorch/pytorch) |
| `TensorFlow` | 开源软件库，用于各种感知和语言理解任务的机器学习。 | [Link](https://github.com/tensorflow/tensorflow) |
| `JAX` | Google 开发的用于变换数值函数的 Python 机器学习框架。 | [Link](https://github.com/jax-ml/jax) |
| `Transformers` | Hugging Face 出品，为 Jax、PyTorch 和 TensorFlow 打造的先进 NLP 库。 | [Link](https://github.com/huggingface/transformers) |
| `Keras` | 用 Python 编写的高级神经网络 API，支持 TensorFlow、CNTK 或 Theano 后端。 | [Link](https://github.com/keras-team/keras) |

## 数据处理与科学计算

| 名称 | 描述 | 地址 |
|---|---|---|
| `NumPy` | Python 扩展程序库，支持高阶大规模多维数组与矩阵运算。 | [Link](https://github.com/numpy/numpy) |
| `Pandas` | 数据操纵和分析库，建于 NumPy 之上。 | [Link](https://github.com/pandas-dev/pandas) |
| `SciPy` | 开源 Python 算法库和数学工具包。 | [Link](https://github.com/scipy/scipy) |
| `Datasets` | HuggingFace 提供的用于加载、处理、查询数据集的库。 | [Link](https://github.com/huggingface/datasets) |
| `scikit-learn` | 自由开源机器学习库，包含分类、回归、聚类算法。 | [Link](https://github.com/scikit-learn/scikit-learn) |
| `Pydantic` | Python 数据验证与解析库，通过数据模型实现自动类型校验和格式转换。 | [Link](https://github.com/pydantic/pydantic) |

## 模型训练与优化

| 名称 | 描述 | 地址 |
|---|---|---|
| `Megatron-LM` | NVIDIA 出品，大规模训练 Transformer 模型的 GPU 优化技术。 | [Link](https://github.com/NVIDIA/Megatron-LM) |
| `PyTorch Lightning` | 基于 PyTorch 的高级深度学习框架，简化研究流程。 | [Link](https://github.com/Lightning-AI/pytorch-lightning) |
| `DeepSpeed` | Microsoft 出品，深度学习优化库，简化分布式训练和推理。 | [Link](https://github.com/microsoft/DeepSpeed) |
| `FairScale` | Meta 出品，用于高性能和大规模训练的 PyTorch 扩展。 | [Link](https://github.com/facebookresearch/fairscale) |
| `Weights & Biases` | AI 开发者平台，实验跟踪与可视化。 | [Link](https://github.com/wandb/wandb) |
| `Optuna` | 专为机器学习设计的自动超参数优化框架。 | [Link](https://github.com/optuna/optuna) |
| `LightGBM` | Microsoft 出品，基于决策树算法的分布式梯度提升框架。 | [Link](https://github.com/microsoft/LightGBM) |
| `XGBoost` | 可扩展的分布式梯度提升决策树机器学习库。 | [Link](https://github.com/dmlc/xgboost) |
| `Dask` | Python 中并行和分布式计算的灵活开源库。 | [Link](https://github.com/dask/dask) |

## 微调与适配

| 名称 | 描述 | 地址 |
|---|---|---|
| `unsloth-studio` | 可视化微调工具，用最少显存、最短时间定制大模型。 | [官网](https://unsloth.ai/) |
| `PEFT` | HuggingFace 出品，参数高效微调技术。 | [Link](https://github.com/huggingface/peft) |
| `TRL` | HuggingFace 出品，用强化学习训练 Transformer 语言模型。 | [Link](https://github.com/huggingface/trl) |
| `LLaMA-Factory` | 零代码命令行与 Web UI 轻松微调百余种大模型。 | [Link](https://github.com/hiyouga/LLaMA-Factory) |

## 模型推理

| 名称 | 描述 | 地址 |
|---|---|---|
| `vLLM` | 快速且易用的 LLM 推理和服务库，与 HuggingFace 无缝集成（GPU 加速）。 | [Link](https://github.com/vllm-project/vllm) |
| `SGLang` | 面向 LLM 和多模态模型的高性能服务框架，低延迟高吞吐。 | [Link](https://github.com/sgl-project/sglang) |
| `llama.cpp` | C/C++ LLM 推理引擎（Ollama、LM Studio、LocalAI 的内核）。 | [Link](https://github.com/ggml-org/llama.cpp) |
| `ONNX-TensorRT` | 解析 ONNX 模型以便使用 TensorRT 执行推理。 | [Link](https://github.com/onnx/onnx-tensorrt) |
| `Accelerate` | HuggingFace 出品，方便将 PyTorch 模型迁移到 GPU/TPU 等硬件。 | [Link](https://github.com/huggingface/accelerate) |

## 辅助工具

| 名称 | 描述 | 地址 |
|---|---|---|
| `Gradio` | 快速构建机器学习 Web 演示应用。 | [Link](https://github.com/gradio-app/gradio) |
| `Matplotlib` | Python 的 NumPy 绘图库。 | [Link](https://github.com/matplotlib/matplotlib) |
| `Seaborn` | 基于 Matplotlib 的 Python 数据可视化库。 | [Link](https://github.com/mwaskom/seaborn) |
| `MLflow` | 开源机器学习生命周期管理平台。 | [Link](https://github.com/mlflow/mlflow) |
| `ZLUDA` | 在 AMD GPU 上运行 CUDA。 | [Link](https://github.com/vosen/ZLUDA) |
| `supervision` | 计算机视觉工具库。 | [Link](https://github.com/roboflow/supervision) |
| `firecrawl` | 网页转 LLM 结构化数据（商业产品）。 | [Link](https://github.com/mendableai/firecrawl) |

## Agent 框架

| 名称 | 描述 | 地址 |
|---|---|---|
| `composio` | AI Agent 的生产工具集。 | [Link](https://github.com/ComposioHQ/composio) |
| `mem0` | AI Agent 的记忆层。 | [Link](https://github.com/mem0ai/mem0) |
| `agno` | 构建 multi-modal Agent 的轻量化库。 | [Link](https://github.com/agno-agi/agno) |
| `CrewAI` | AI Agent 调度框架（多 Agent 协作）。 | [Link](https://github.com/crewAIInc/crewAI) |
| `OpenHands` | AI 开发平台：软件开发 Agent。 | [Link](https://github.com/All-Hands-AI/OpenHands) |
| `pydantic-ai` | 生成级 AI 应用开发框架。 | [Link](https://github.com/pydantic/pydantic-ai) |
| `agency-agents` | 将真实企业专业岗位打包成可直接调用的 AI 角色。 | [Link](https://github.com/msitarzewski/agency-agents) |
| `CLI-Anything` | 让所有软件都能被 Agent 驱动。 | [Link](https://github.com/HKUDS/CLI-Anything) |
| `hermes-agent` | 自进化、持久记忆型 AI 智能体，数据全本地、多平台触达。 | [Link](https://github.com/nousresearch/hermes-agent) |
| `oh-my-openagent` | 运行在 OpenCode 之上的多智能体编排框架，自动拆任务、选模型、并行执行。 | [Link](https://github.com/code-yeongyu/oh-my-openagent) |
| `Project N.O.M.A.D` | 开源、离线优先、Docker 容器化的本地知识/AI 服务器。 | [Link](https://github.com/Crosstalk-Solutions/project-nomad) |
| `pi-mono` | AI Agent 工具包：coding agent CLI、统一 LLM API、TUI 等（OpenClaw 核心）。 | [Link](https://github.com/earendil-works/pi) |
| `OpenViking` | AI 智能体的上下文数据库（字节跳动）。 | [Link](https://github.com/volcengine/OpenViking) |

## RAG

| 名称 | 描述 | 地址 |
|---|---|---|
| `RAGFlow` | 基于深度文档理解构建的开源 RAG 引擎。 | [Link](https://github.com/infiniflow/ragflow) |
| `graphrag` | Microsoft 出品，基于图的模块化 RAG 系统。 | [Link](https://github.com/microsoft/graphrag) |

## Skills 生态

| 名称 | 描述 | 地址 |
|---|---|---|
| `Anthropic Skills` | Anthropic 官方 Agent Skills 仓库。 | [Link](https://github.com/anthropics/skills) |
| `awesome-claude-skills` | Claude Skills 精选合集（多个仓库）。 | [Link](https://github.com/ComposioHQ/awesome-claude-skills) |
| `claude-scientific-skills` | 专注科学研究的 Skills，含 138 个科学领域 Skill。 | [Link](https://github.com/K-Dense-AI/claude-scientific-skills) |
| `awesome-openclaw-skills` | OpenClaw Skills 精选，5400+ 经过筛选分类。 | [Link](https://github.com/VoltAgent/awesome-openclaw-skills) |
| `mattpocock/skills` | TypeScript 大神 Matt Pocock 的 AI 编程工程化技能库。 | [Link](https://github.com/mattpocock/skills) |
| `Product-Manager-Skills` | 产品经理 Skills。 | [Link](https://github.com/deanpeters/Product-Manager-Skills) |
| `baoyu-skills` | 宝玉分享的 Claude Code 技能集。 | [Link](https://github.com/JimLiu/baoyu-skills) |
| `superpowers` | 可组合的 Skills 与硬约束，让 AI 像资深工程师一样写代码。 | [Link](https://github.com/obra/superpowers) |
| `andrej-karpathy-skills` | 源自 Andrej Karpathy 的 LLM 编码陷阱总结。 | [Link](https://github.com/forrestchang/andrej-karpathy-skills) |
| `nuwa-skill` | 女娲：蒸馏任何人的思维方式。 | [Link](https://github.com/alchaincyf/nuwa-skill) |

**Skills 发现平台：** [skills.sh](https://skills.sh/) · [clawhub.ai](https://clawhub.ai/) · [skillsmp.com](https://skillsmp.com/) · [skiload.com](https://skiload.com/)

## MCP

| 名称 | 描述 | 地址 |
|---|---|---|
| `blender-mcp` | 通过 MCP 协议连接 Blender 与 Claude AI。 | [Link](https://github.com/ahujasid/blender-mcp) |

## 网关/路由

| 名称 | 描述 | 地址 |
|---|---|---|
| `gateway` | Portkey AI 网关：通过统一 API 链接多个大语言模型。 | [Link](https://github.com/Portkey-AI/gateway) |
| `aisuite` | Andrew Ng 出品，为多平台 LLM 提供统一调用接口。 | [Link](https://github.com/andrewyng/aisuite) |
| `openrouter` | LLM 统一接口，找到最佳模型和价格。 | [官网](https://openrouter.ai/) |
| `llmgateway` | 一个 API 调用所有 LLM，任意模型任意提供商。 | [官网](https://llmgateway.io/) |

## Coding Agent 工具

| 名称 | 描述 | 地址 |
|---|---|---|
| `everything-claude-code` | Anthropic 黑客马拉松获奖者的完整 Claude Code 配置集合。 | [Link](https://github.com/affaan-m/everything-claude-code) |
| `claude-hud` | Claude Code 插件，实时显示上下文使用率、活跃 Agent 等。 | [Link](https://github.com/jarrodwatts/claude-hud) |
| `rtk` | 命令输出过滤和压缩，单一 Rust 二进制，<10ms 开销。 | [Link](https://github.com/rtk-ai/rtk) |

## 本地模型

| 名称 | 描述 | 地址 |
|---|---|---|
| `Fara-7B` | Microsoft 出品，专为计算机操作设计的轻量级多模态 CUA 模型。 | [Link](https://github.com/microsoft/fara) |
