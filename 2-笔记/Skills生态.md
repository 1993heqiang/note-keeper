## 简介

> Skills 是一组可复用的指令/提示词/工具组合，让 AI Agent 在特定领域表现更好。基于 [agentskills.io](https://agentskills.io) 开放标准（SKILL.md / AGENTS.md），理论上不绑定特定 Agent，Claude Code、Codex、Cursor、Copilot 等 30+ Agent 均可加载。

## 常用安装

| 平台           | 原生安装                         | 通用安装 (`npx skills add`)        |
| -------------- | -------------------------------- | ---------------------------------- |
| Claude Code    | `/plugin marketplace add <repo>` | `npx skills add <repo> -a claude`  |
| Codex CLI      | `$skill-installer <name>`        | `npx skills add <repo> -a codex`   |
| Gemini CLI     | `gemini skills install <url>`    | `npx skills add <repo> -a gemini`  |
| GitHub Copilot | `gh skill install <repo>`        | `npx skills add <repo> -a copilot` |

> 更多平台详见：[Skill平台与工具](Skill平台与工具.md)

## 领域分类

### 元技能

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

**Darwin Skill**

> 可让 Skill 自我进化的系统，通过评估→优化→测试→保留/回滚实现持续迭代。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/alchaincyf/darwin-skill)

**ralph-loop**

> 自动迭代优化循环插件，让 AI 持续自我修正、完善代码与方案直到达标。

- 类型：`独立` 来源：`anthropics 官方` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/ralph-loop)

### 编码

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

**planning-with-files**

> 基于项目文件结构进行结构化规划，自动生成任务清单、执行步骤与开发路线。

- 类型：`独立` 来源：`独立仓库` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/othmanadi/planning-with-files)

**code-review**

> Anthropic 官方代码审查插件，自动检查代码规范、潜在 Bug、性能与安全问题。

- 类型：`独立` 来源：`anthropics 官方` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/code-review)

**code-simplifier**

> 官方代码简化工具，重构冗余代码，提升可读性、简洁性与可维护性。

- 类型：`独立` 来源：`anthropics 官方` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/anthropics/claude-plugins-official/tree/main/plugins/code-simplifier)

**webapp-testing**

> Web 应用自动化测试技能，生成测试用例、执行流程检查与兼容性验证。

- 类型：`独立` 来源：`anthropics/skills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/anthropics/skills/tree/main/skills/webapp-testing)

**mcp-builder**

> MCP（模型上下文协议）快速构建工具，用于创建、调试和部署自定义模型插件。

- 类型：`独立` 来源：`anthropics/skills` 适配：`Claude Code` `Codex`
- 安装：—
- 地址：[Link](https://github.com/anthropics/skills/tree/main/skills/mcp-builder)

**Systematic Debugging**

> 系统化调试技能，按流程定位错误根源、分析日志、给出可复现修复方案。

- 类型：`独立` 来源：`obra/superpowers` 适配：`Claude Code`
- 安装：—
- 地址：[Link](https://github.com/obra/superpowers/tree/main/skills/systematic-debugging)

### 设计

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

**Taste Skill**

> 提升 AI 输出审美与风格，避免生成平庸、通用化、乏味的内容。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/leonxlnx/taste-skill)

**Impeccable**

> 强化 AI 的设计语言能力，让代码、界面、文案更具设计感与专业度。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/pbakaus/impeccable)

### 角色

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

### 营销

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

### 写作

**Humanizer-zh**

> 中文 AI 文本去痕迹工具，将 AI 生成内容润色得更自然、更贴近人类真实表达。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/op7418/Humanizer-zh)

### 其他

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

**AnySearch Skill**

> 为 AI Agent 提供统一的实时搜索引擎能力，支持多源聚合检索。

- 类型：`独立` 来源：`独立仓库` 适配：`通用`
- 安装：—
- 地址：[Link](https://github.com/anysearch-ai/anysearch-skill)

---

## 更多资源

> Skill 平台、聚合搜索引擎、安装工具等详见：[Skill平台与工具](Skill平台与工具.md)
