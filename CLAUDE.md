# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库性质

这不是软件项目，是个人技术知识库。所有内容为 Markdown 文件，中文为主，技术名词保留英文。

## 目录结构

按**使用深度**四层分层，而非技术领域：

- `1-工具箱/` — 日常使用的工具，上限 20 条，一进一出
- `2-笔记/` — 自己写的配置、学习笔记（可自由编辑）
- `3-发现/` — 感兴趣但未必用的工具和项目，同类超过 5 个时精简
- `4-归档/` — 已废弃或停维护的项目，只增不减

## 常用命令

```bash
# 首次克隆后必须执行（激活 pre-commit 钩子）
git config core.hooksPath .githooks

# 手动格式化所有 Markdown
npx prettier --write "**/*.md"
```

## Pre-commit 钩子

`.githooks/pre-commit` 在每次 `git commit` 前自动运行 Prettier 格式化所有 `.md` 文件。如果 prettier 未安装会打警告但不会阻止提交。

## 格式规范

工具/库条目使用统一表格：

```markdown
| 名称        | 描述             | 地址        | 状态               |
| ----------- | ---------------- | ----------- | ------------------ |
| `tool-name` | 一句话中文描述。 | [Link](url) | :star::star::star: |
```

状态标记：`:white_check_mark:` 正在使用 / `:star:` 推荐程度 / 空 未评估 / `:x:` 不推荐

## 操作约束

- **绝对禁止**在用户未明确确认的情况下执行 `git commit` 或 `git push`
- 改动完成后告知用户改了什么，等用户说「提交」再提交
- 文件重命名时同步更新 README.md 和各层 README.md 中的引用
- 归档内容移至 `4-归档/`，同时在 `4-归档/INDEX.md` 登记
