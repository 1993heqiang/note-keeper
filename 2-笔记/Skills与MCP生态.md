## Skills

> Skills 是一组可复用的指令/提示词/工具组合，让 AI Agent 在特定领域表现更好。理论上不绑定特定 Agent，只要支持 Skill 协议即可加载。

### 按领域分类

#### 元技能

**skill-creator**

> 引导式 Skill 创建向导，帮你写出高质量的 Skill 定义。

- 类型：`独立` 来源：`anthropics/skills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/anthropics/skills/blob/main/skills/skill-creator)

**find-skills**

> 在 skills.sh 生态中搜索和发现 Skill。

- 类型：`独立` 来源：`vercel-labs/skills` 适配：`skills.sh 生态`
- 安装：—
- 地址：[Link](https://github.com/vercel-labs/skills/tree/main/skills/find-skills)

#### 编码

**Anthropic Skills**

> Anthropic 官方 Skill 仓库，含 canvas-design、frontend-design、skill-creator 等。

- 类型：`合集` 来源：`anthropics 官方` 适配：`Claude Code`
- 安装：`/plugin marketplace add anthropics/skills`
- 地址：[Link](https://github.com/anthropics/skills)

**awesome-claude-skills**

> ComposioHQ 维护的 Claude 生态精选 Skill 索引（Awesome List）。

- 类型：`索引` 来源：`ComposioHQ` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/ComposioHQ/awesome-claude-skills)

**superpowers**

> 可组合的 Skills 与硬约束，让 AI 像资深工程师一样按流程写代码。

- 类型：`合集` 来源：`独立仓库` 适配：`Claude Code`
- 安装：`/plugin marketplace add obra/superpowers`
- 地址：[Link](https://github.com/obra/superpowers)

**mattpocock/skills**

> TypeScript 大神 Matt Pocock 的 AI 编程工程化技能库。

- 类型：`合集` 来源：`skills.sh` 适配：`Claude Code` `Codex` `Cursor`
- 安装：`npx skills add mattpocock/skills`
- 地址：[Link](https://github.com/mattpocock/skills)

**baoyu-skills**

> 宝玉分享的 Claude Code 技能集，提升日常开发效率。

- 类型：`合集` 来源：`skills.sh` 适配：`Claude Code`
- 安装：`npx skills add JimLiu/baoyu-skills`
- 地址：[Link](https://github.com/JimLiu/baoyu-skills)

**andrej-karpathy-skills**

> 源自 Andrej Karpathy 的 LLM 编码陷阱总结（单一 CLAUDE.md）。

- 类型：`独立` 来源：`独立仓库` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/forrestchang/andrej-karpathy-skills)

#### 设计

**canvas-design**

> 从哲学美学运动汲取灵感，创作海报、封面、视觉设计，输出 PDF/PNG。

- 类型：`独立` 来源：`anthropics/skills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/anthropics/skills/tree/main/skills/canvas-design)

**frontend-design**

> 前端 UI 设计，生成生产级前端代码。

- 类型：`独立` 来源：`anthropics/skills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/anthropics/skills/tree/main/skills/frontend-design)

**ui-ux-pro-max**

> 跨平台 UI/UX 设计智能，支持多框架（React/Vue/Flutter 等）。

- 类型：`合集` 来源：`独立仓库` 适配：`Claude Code`
- 安装：`/plugin marketplace add nextlevelbuilder/ui-ux-pro-max-skill`
- 地址：[Link](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill)

#### 角色

**nuwa-skill**

> 女娲：蒸馏任何人的思维方式（乔布斯、马斯克、芒格、费曼等）。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/alchaincyf/nuwa-skill)

**Product-Manager-Skills**

> 产品经理专用 Skills，覆盖需求分析、PRD 撰写、竞品调研等场景。

- 类型：`合集` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/deanpeters/Product-Manager-Skills)

**Scientific Agent Skills**

> 140+ 专业科研技能，覆盖生物、化学、医学、材料、数据科学等。

- 类型：`合集` 来源：`skills.sh` 适配：`Claude Code` `Codex` `Cursor`
- 安装：`npx skills add K-Dense-AI/scientific-agent-skills`
- 地址：[Link](https://github.com/K-Dense-AI/scientific-agent-skills)

#### 营销

**copywriting**

> 为首页、着陆页、定价页等撰写以转化为导向的营销文案。

- 类型：`独立` 来源：`marketingskills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/coreyhaines31/marketingskills/tree/main/skills/copywriting)

**marketing-psychology**

> 营销心理学，让 AI 在营销场景中运用心理学原理。

- 类型：`独立` 来源：`marketingskills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/coreyhaines31/marketingskills/tree/main/skills/marketing-psychology)

**marketingskills**

> 营销领域 Skills 合集，含文案、心理学等多个子技能。

- 类型：`合集` 来源：`skills.sh` 适配：`Claude Code` `Codex`
- 安装：`npx skills add coreyhaines31/marketingskills`
- 地址：[Link](https://github.com/coreyhaines31/marketingskills)

#### 其他

**browser-act-skill-forge**

> 专为 AI Agent 打造的浏览器自动化 CLI 技能包。

- 类型：`合集` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/browser-act/skills)

**claude-seo**

> 免费开源全能 SEO 工具包，覆盖关键词研究、内容优化、技术 SEO。

- 类型：`合集` 来源：`独立仓库` 适配：`Claude Code`
- 安装：`/plugin marketplace add AgricIDaniel/claude-seo`
- 地址：[Link](https://github.com/AgricIDaniel/claude-seo)

---

### 平台与市场

> 便捷入口。安装示例以各平台文档为准。

| 平台           | 描述                                                            | 安装示例                               |
| -------------- | --------------------------------------------------------------- | -------------------------------------- |
| `skills.sh`    | Vercel 官方 AI Skill 市场，最大的 Skills 分发平台之一。         | `npx skills add <发布者>/<技能包>`     |
| `clawhub.ai`   | OpenClaw 生态 Skill 市场，适配 Claude Code / Codex / OpenClaw。 | 详见 [Link](https://clawhub.ai/)       |
| `skillsmp.com` | 多平台聚合发现引擎，覆盖 Claude Code、Codex、ChatGPT 等。       | 浏览安装 [Link](https://skillsmp.com/) |
| `skiload.com`  | 聚合 SkillHub、OpenClaw 索引及公开仓库，含 AI 审核评分。        | 浏览评估 [Link](https://skiload.com/)  |

---

## MCP 生态

> MCP（Model Context Protocol）是 Anthropic 推出的开放协议，让 AI 模型通过标准化接口连接外部工具和数据源。类似于 AI 的「USB 协议」。

| 名称          | 描述                                             | 地址                                            |
| ------------- | ------------------------------------------------ | ----------------------------------------------- |
| `blender-mcp` | 通过 MCP 协议连接 Blender，AI 直接操控 3D 建模。 | [Link](https://github.com/ahujasid/blender-mcp) |

> 更多 AI 编码工具和 Agent 框架见：[3-发现/AI开发技术栈.md](../3-发现/AI开发技术栈.md)
