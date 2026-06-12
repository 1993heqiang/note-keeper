## Skills

> Skills 是一组可复用的指令/提示词/工具组合，让 Claude Code 等 AI 编码工具在特定领域表现更好。类似于给 AI 安装「职业技能包」。

### 优质Skill

| 名称                      | 描述                                                       | 地址                                                         |
| ------------------------- | ---------------------------------------------------------- | ------------------------------------------------------------ |
| `nuwa-skill`              | 女娲：蒸馏任何人的思维方式（乔布斯、马斯克、芒格、费曼）。 | [Link](https://github.com/alchaincyf/nuwa-skill)             |
| `Product-Manager-Skills`  | 产品经理专用 Skills                                        | [Link](https://github.com/deanpeters/Product-Manager-Skills) |
| `browser-act-skill-forge` | 专为 AI Agents打造的浏览器自动化 CLI                       | [Link](https://github.com/browser-act/skills)                |
|                           |                                                            |                                                              |

### Claude Code

> **命令**: `/plugin marketplace add <发布者>/<插件名>`

| 名称                     | 描述                                                           | 地址                                                           |
| ------------------------ | -------------------------------------------------------------- | -------------------------------------------------------------- |
| `Anthropic Skills`       | Anthropic 官方 Agent Skills 仓库。                             | [Link](https://github.com/anthropics/skills)                   |
| `superpowers`            | 可组合的 Skills 与硬约束，让 AI 像资深工程师一样按流程写代码。 | [Link](https://github.com/obra/superpowers)                    |
| `andrej-karpathy-skills` | 源自 Andrej Karpathy 的 LLM 编码陷阱总结（单一 CLAUDE.md）。   | [Link](https://github.com/forrestchang/andrej-karpathy-skills) |
|                          |                                                                |                                                                |

- `awesome-claude-skills`: [Link](https://github.com/ComposioHQ/awesome-claude-skills)

  一个由 Composio 维护的、面向 Claude 生态的精选技能集合（Awesome List），也是目前最主流、最全面的 Claude 技能开源仓库之一

-

### Skills 市场

| 平台         | 描述                                                                                                                                                                                       | 地址                          |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------- |
| skills.sh    | Vercel 官方推出的 AI 技能市场                                                                                                                                                              | [Link](https://skills.sh/)    |
| clawhub.ai   | clawhub skill市场.  [OpenClaw Skill精选](https://github.com/VoltAgent/awesome-openclaw-skills)                                                                                             | [Link](https://clawhub.ai/)   |
| skillsmp.com | 发现适用于 Claude Code、Codex、ChatGPT 以及所有 SKILL.md 工具的开源 agent skills                                                                                                           | [Link](https://skillsmp.com/) |
| skiload.com  | Skiload 汇总 SkillHub、OpenClaw 索引和公开仓库中的技能条目，覆盖 Claude、Codex、OpenClaw 等不同 Agent 生态。这里会展示 AI 审视结果、评分信号和源仓库链接，帮助你在安装前先做一轮风险判断。 | [Link](https://skiload.com/)  |

- **skills.sh**

  > **命令**: `npx skills add K-Dense-AI/scientific-agent-skills`

  | 名称                      | 描述                                                                                                                                                       | 地址                                                          |
  | ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
  | `Scientific Agent Skills` | 它是一套140+ 个专业科研技能，能把你的 AI 助手（ClaudeCode、Cursor、Codex 等）变成AI 科研助手，直接处理生物、化学、医学、材料、数据科学等领域的复杂工作流。 | [Link](https://github.com/K-Dense-AI/scientific-agent-skills) |
  | `mattpocock/skills`       | TypeScript 大神 Matt Pocock 的 AI 编程工程化技能库。                                                                                                       | [Link](https://github.com/mattpocock/skills)                  |
  | `baoyu-skills`            | 宝玉分享的 Claude Code 技能集，提升日常工作效率。                                                                                                          | [Link](https://github.com/JimLiu/baoyu-skills)                |
  |                           |                                                                                                                                                            |                                                               |

- ***

## MCP 是什么

> MCP（Model Context Protocol）是 Anthropic 推出的开放协议，让 AI 模型通过标准化接口连接外部工具和数据源。类似于 AI 的「USB 协议」——一套接口，插什么都能用。

| 名称               | 描述                                                          | 地址                                                     |
| ------------------ | ------------------------------------------------------------- | -------------------------------------------------------- |
| `blender-mcp`      | 通过 MCP 协议连接 Blender 与 Claude AI，AI 直接操控 3D 建模。 | [Link](https://github.com/ahujasid/blender-mcp)          |
| `awesome-llm-apps` | 精心整理的 RAG、AI 智能体、MCP、语音智能体等 LLM 应用集合。   | [Link](https://github.com/Shubhamsaboo/awesome-llm-apps) |
|                    |                                                               |                                                          |

---

## CodingAgent

| 名称         | 描述                                                                                                                                                                                     | 地址                                              |
| ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| `rtk-ai/rtk` | rtk 在命令输出到达 LLM 上下文之前进行过滤和压缩。单一 Rust 二进制文件，零依赖，<10ms 开销。                                                                                              | [Link](https://github.com/rtk-ai/rtk)             |
| `CodeGraph`  | CodeGraph 是专为 AI 编程助手（如 ClaudeCode、Cursor）打造的本地代码知识图谱工具，核心是把代码库提前解析成可查询的结构化图谱，让 AI 不用反复扫描文件，大幅减少 Token 消耗、提升响应速度。 | [Link](https://github.com/colbymchenry/codegraph) |
| `OpenSpec`   | Spec-driven development (SDD) for AI coding assistants.                                                                                                                                  | [Link](https://github.com/Fission-AI/OpenSpec)    |
|              |                                                                                                                                                                                          |                                                   |

- CodeWhale: [Link](https://github.com/Hmbown/CodeWhale)

  面向 DeepSeek V4 和开放模型的本地 Agent 运行框架：自我、权威、证据闭环。

- Warp: [Link](https://github.com/warpdotdev/warp)

  Warp 是一个基于终端的智能体开发环境。

- DeepSeek-Reasonix: [Link](https://github.com/esengine/DeepSeek-Reasonix)

  面向终端的 DeepSeek 原生 AI coding agent。

- claude-code-best/claude-code: [Link](https://github.com/claude-code-best/claude-code)

  原汁原昧 Claude Code 可运行,可构建, 可调试版; 生产级工程化, 企业级可靠性; 安全无毒, 内存泄露修复.

-

---

## Agents

### Hermes Agent

- 地址: [Link](https://github.com/NousResearch/hermes-agent)

- **由 [Nous Research](https://nousresearch.com/) 构建的自进化 AI Agent。** 它是唯一内置学习闭环的智能代理——从经验中创建技能，在使用中改进技能，主动持久化知识，搜索过往对话，并在跨会话中逐步构建对你的深度理解。可以在 $5 的 VPS 上运行，也可以在 GPU 集群上运行，或者使用几乎零成本的 Serverless 基础设施。它不绑定你的笔记本——你可以在 Telegram 上与它对话，而它在云端 VM 上工作.

### Clowder AI

- 代码地址: [Link](https://github.com/zts212653/clowder-ai), 教程: [Link](https://github.com/zts212653/cat-cafe-tutorials)

- **Clowder AI** 是把孤立的 AI agent 变成真正团队的平台层 — 持久身份、跨模型互审、共享记忆、协作纪律。
