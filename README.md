# Matt Pocock Skills — Kimi 适配版

> 基于 [Matt Pocock](https://github.com/mattpocock/skills) 的 `skills` 仓库，为 **Kimi Work** 和 **Kimi Claw (OpenClaw)** 环境进行本地化适配。
>
> 核心理念不变：small, easy to adapt, composable — 用经过验证的软件工程实践，让 AI 辅助编码更可靠、更可维护。

---

## 与原版的关系

| | 原版 (mattpocock/skills) | 本仓库 (mattpocock-skills-kimi) |
|---|---|---|
| 目标平台 | Claude Code / Claude Desktop | Kimi Work, Kimi Claw (OpenClaw) |
| 触发方式 | `/command` 手动命令 | Model-invoked 自动触发 |
| 工具调用 | `run` / `gh` CLI 等 | `Bash` / `PythonRun` / GitHub MCP / 通用指令 |
| Issue Tracker | `gh issue create` | 抽象层：GitHub MCP / Token / CLI / 本地 Markdown |
| 配置文件 | `CLAUDE.md` / `AGENTS.md` | `IDENTITY.md` + Vault Memory + 项目内 `CONTEXT.md` |

本仓库保留 Matt Pocock 的所有核心方法论和思维框架，仅对工具调用、路径、触发机制进行 Kimi 生态的本地化适配。

---

## 已适配 Skill 列表

按实施顺序排列，逐步上线：

| # | Skill | 状态 | 说明 |
|---|-------|------|------|
| 1 | `grilling` | ✅ 已完成 |  relentlessly interview，对齐需求的底层循环 |
| 2 | `handoff` | ✅ 已完成 | 跨会话交接，压缩上下文 |
| 3 | `domain-modeling` | ⏳ 待实现 | 维护项目术语表 `CONTEXT.md` + ADR |
| 4 | `codebase-design` | ⏳ 待实现 | 深模块设计词汇与原则 |
| 5 | `tdd` | ⏳ 待实现 | 红绿重构，垂直切片 |
| 6 | `diagnosing-bugs` | ⏳ 待实现 | 六阶段 Bug 诊断 |
| 7 | `grill-with-docs` | ⏳ 待实现 | 有代码库时的对齐 + 文档维护 |
| 8 | `to-prd` | ⏳ 待实现 | 合成 PRD + Issue Tracker 发布 |

---

## 快速开始（Kimi Work）

1. 在 Kimi Work 中打开本仓库所在目录
2. 将 `skills/` 下的 skill 目录复制到 Kimi Work 的 skill 目录，或使用 `SkillManage` 安装
3. 开始编码，skill 会在合适场景自动触发

## 快速开始（Kimi Claw / OpenClaw）

1. 将本仓库 skill 文件按 OpenClaw 规范放入 skill 目录
2. 工具调用描述已适配为通用指令，兼容 OpenClaw 的执行环境

---

## 本地化修改说明

详见 [`docs/ADAPTATION-NOTES.md`](./docs/ADAPTATION-NOTES.md)。

---

## 致谢与许可

- 原作者：**Matt Pocock** — [github.com/mattpocock/skills](https://github.com/mattpocock/skills)
- 核心方法论、词汇、设计原则全部来自 Matt Pocock 的原创工作
- 本仓库仅做 Kimi 生态的本地化适配

Licensed under the **MIT License** — 保留 Matt Pocock 版权声明。
