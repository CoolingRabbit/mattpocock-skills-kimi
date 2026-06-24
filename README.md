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
| 3 | `domain-modeling` | ✅ 已完成 | 维护项目术语表 `CONTEXT.md` + ADR |
| 4 | `codebase-design` | ✅ 已完成 | 深模块设计词汇与原则 |
| 5 | `tdd` | ✅ 已完成 | 红绿重构，垂直切片 |
| 6 | `diagnosing-bugs` | ✅ 已完成 | 六阶段 Bug 诊断 |
| 7 | `grill-with-docs` | ✅ 已完成 | 有代码库时的对齐 + 文档维护 |
| 8 | `to-prd` | ✅ 已完成 | 合成 PRD + Issue Tracker 发布 |

---

## 快速开始（Kimi Work）

方式一：通过 AI 安装（推荐）
1. 在 Kimi Work 中打开本仓库所在目录
2. 在对话中告诉 Kimi："帮我安装本仓库 `skills/` 目录下的所有 skill"
3. Kimi 会自动通过 `SkillManage` 工具完成安装

方式二：通过 `SkillManage` 命令安装（手动）
1. 在 Kimi Work 中打开本仓库
2. 运行 `SkillManage` 工具，逐个创建 `skills/` 下的 skill

安装完成后，开始编码，skill 会在合适场景自动触发。

## 快速开始（Kimi Claw / OpenClaw）

方式一：通用安装器（推荐）
```bash
npx skills add CoolingRabbit/mattpocock-skills-kimi
```

方式二：手动克隆到 skill 目录
```bash
# OpenClaw
git clone https://github.com/CoolingRabbit/mattpocock-skills-kimi.git ~/.openclaw/skills/mattpocock-skills-kimi

# 或 OpenClaw workspace 路径
git clone https://github.com/CoolingRabbit/mattpocock-skills-kimi.git ~/.openclaw/workspace/skills/mattpocock-skills-kimi
```

方式三：通过 ClawHub 安装（如果已发布）
```bash
npx clawhub@latest install mattpocock-skills-kimi
```

工具调用描述已适配为通用指令，兼容 OpenClaw 的执行环境。

---

## 本地化修改说明

详见 [`docs/ADAPTATION-NOTES.md`](./docs/ADAPTATION-NOTES.md)。

---

## 致谢与许可

- 原作者：**Matt Pocock** — [github.com/mattpocock/skills](https://github.com/mattpocock/skills)
- 核心方法论、词汇、设计原则全部来自 Matt Pocock 的原创工作
- 本仓库仅做 Kimi 生态的本地化适配

Licensed under the **MIT License** — 保留 Matt Pocock 版权声明。
