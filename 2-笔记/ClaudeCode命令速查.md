# Claude Code 常用命令速查

## 启动

- 日常开发用：`claude --permission-mode acceptEdits`
- 完全自动化用：`claude --permission-mode auto`
- 沙箱 / CI 用：`claude --permission-mode bypassPermissions`
- 恢复最近：`claude -c`
- 命名会话：`claude -n "feature-name"`
- 单次问答：`claude -p "问题"`
- 后台运行：`claude --bg "任务描述"`

---

## 斜杠命令

### 会话管理

| 命令                | 说明                                                 |
| ------------------- | ---------------------------------------------------- |
| `/clear`            | 清空会话历史，切换任务前使用（脏上下文不如没上下文） |
| `/compact`          | 压缩上下文释放 token，超过 70% 时用                  |
| `/rewind` (Esc+Esc) | 回滚到之前的步骤                                     |
| `/fork`             | 从当前会话分支新会话，用于尝试不同方向               |
| `/resume`           | 切换已保存的会话                                     |

### 模型与性能

| 命令                       | 说明                          |
| -------------------------- | ----------------------------- |
| `/model sonnet/opus/haiku` | 实时切换模型                  |
| `/fast`                    | Fast Mode，Opus 2.5 倍速      |
| `/effort low/medium/high`  | 设置推理深度                  |
| `/cost`                    | 查看当前会话 token 消耗和费用 |

### 配置与调试

| 命令           | 说明                       |
| -------------- | -------------------------- |
| `/config`      | 打开 settings.json 编辑器  |
| `/init`        | 扫描项目自动生成 CLAUDE.md |
| `/permissions` | 管理工具调用的自动批准规则 |
| `/doctor`      | 验证配置文件并建议修复     |
| `/statusline`  | 自定义终端状态栏显示       |
| `/memory`      | 在会话中编辑 CLAUDE.md     |

### 任务与自动化

| 命令                    | 说明                               |
| ----------------------- | ---------------------------------- |
| `/todos`                | 持久化任务列表，跨会话保留         |
| `/loop 5m check status` | 每 5 分钟执行一次检查              |
| `/plan`                 | 切换到 Plan Mode（只读，仅出方案） |

### 其他

| 命令          | 说明                        |
| ------------- | --------------------------- |
| `/help`       | 列出所有可用命令和 skill    |
| `/vim`        | 切换 Vim 键绑定             |
| `/voice`      | 语音输入（按空格开始/停止） |
| `/btw "why?"` | 快速旁提问，不干扰主上下文  |

---

## 快捷键

| 快捷键      | 作用                                 |
| ----------- | ------------------------------------ |
| `Esc`       | 立即停止执行                         |
| `Esc+Esc`   | 调出回滚菜单                         |
| `Ctrl+B`    | 后台当前 bash 命令                   |
| `Ctrl+S`    | 暂存输入，先问另一个问题             |
| `Ctrl+R`    | 模糊搜索历史命令                     |
| `Ctrl+G`    | 在外部编辑器打开 plan                |
| `Shift+Tab` | 切换权限模式（Normal / Auto / Plan） |
| `Enter`     | 发送（执行中也可排队新消息）         |

---

## 对话快捷操作

- `!git status` — `!` 前缀直接执行 shell，比让 Claude 执行更快
- `@./src/auth.ts` — `@` 引用文件，Claude 自动读取
- 拖放文件到终端 — 自动识别处理

### 管道模式（最实用的调试方式）

```bash
cat error.log | claude -p "解释这个错误并给出修复方案"
npm test 2>&1 | claude -p "修复失败的测试"
```

直接把原始输出喂给 Claude，比自己转述更准确。

---

## 配置体系

### 三件套

| 文件                          | 作用                     | 是否提交  |
| ----------------------------- | ------------------------ | --------- |
| `CLAUDE.md`                   | 项目记忆，每会话自动读取 | ✅ 提交   |
| `.claude/settings.json`       | 权限规则 + 钩子          | ✅ 提交   |
| `.claude/settings.local.json` | 个人覆盖                 | ❌ 不提交 |

### 优先级（高 → 低）

`Managed Settings` > `CLI 参数` > `settings.local.json` > `settings.json（项目）` > `~/.claude/settings.json（用户）`

### settings.json 示例

```json
{
  "permissions": {
    "allow": ["Bash(npm *)", "Bash(git *)", "Bash(gh *)"],
    "deny": ["Bash(git push *)", "Read(./.env)"]
  },
  "hooks": {
    "preToolUse": "npm run lint-staged",
    "postToolUse": "prettier --write"
  }
}
```

- `allow` — 预批准常用命令，减少弹窗
- `deny` — 禁止危险命令（优先级永远最高）
- `hooks` — 工具调用前后自动执行脚本

---

## 权限模式

| 模式              | 说明                                   |
| ----------------- | -------------------------------------- |
| Normal            | 首次使用需确认                         |
| acceptEdits       | 自动接受文件修改和常用命令（日常推荐） |
| Plan              | 只读模式，仅出方案不执行               |
| Auto              | 自动批准（适合自动化场景）             |
| dontAsk           | 除非预批准否则一律拒绝                 |
| bypassPermissions | 跳过所有确认（仅容器/VM 环境）         |

`/fewer-permission-prompts` 可自动扫描使用记录，生成常用命令的预批准规则。

---

## 会话最佳实践

1. **不同功能用不同命名会话** — 避免上下文污染
2. **切换任务前 `/clear`** — 脏上下文比没上下文更糟糕
3. **同一个问题纠正两次后 `/clear` 重新写 prompt** — 干净会话优于被错误拖累的会话
4. **超过 70% token 用 `/compact`**
5. **按场景选模型**：日常 Sonnet，复杂推理 Opus，样板代码 Haiku
6. **管道模式调试**：把原始输出喂给 Claude，不要转述
