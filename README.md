# AI Skills — Recovered from Leaked System Prompts

> **Two production-grade AI agent skills recovered from the CL4R1T4S leak. Frontend design philosophy + solo developer workflow.**
>
> **两个从 CL4R1T4S 泄露中复原的生产级 AI Agent 技能。前端设计哲学 + 独立开发者工作流。**

---

[English](#english) | [中文](#中文)

---

## English

### What's Here

This repo contains two skills recovered from the [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) leak — a collection of system prompts from ChatGPT, Claude, Gemini, Grok, Cursor, Devin, Manus, Windsurf, and more. Both skills are formatted as SKILL.md for use with AI agents (Hermes, Claude Code, etc.).

| File | Skill | Source |
|---|---|---|
| `SKILL.md` | **frontend-design** | Reconstructed from Claude Fable 5 / Opus / Design Sys prompts |
| `SOLO-DEV-AGENT.md` | **solo-dev-agent** | Synthesized from Cursor, Devin, Manus, Windsurf, Replit, Codex prompts |

---

### Skill 1: frontend-design (`SKILL.md`)

Anti-generic-AI frontend design. Encodes Anthropic's internal design philosophy to stop AI from producing "AI-looking" UI.

**Covers:** AI slop blacklist (8 anti-patterns), oklch color system, distinctive typography, asymmetric layouts, component anti-defaults, Tweak system protocol, variation methodology, CSS playbook, pre-delivery checklist (11 items).

**Usage:**
```
skill_view(name='frontend-design')
```

---

### Skill 2: solo-dev-agent (`SOLO-DEV-AGENT.md`)

Production-grade agent workflow for independent developers. Synthesizes the best operational patterns from 6 leaked coding agent prompts.

**Covers:**
| Module | Source |
|---|---|
| Dual-Mode (Planning / Execution) | Devin |
| notify / ask messaging | Manus |
| Coding guardrails (read-before-edit, 3-attempt limit) | Cursor + Devin + Replit |
| Error recovery protocol | Cursor |
| Git protocol (no `git add .`, explicit staging) | Devin |
| Safety boundaries | Fable 5 + Devin |
| Windows environment knowledge | Custom |

**Usage:**
```
skill_view(name='solo-dev-agent')
```

---

### Quick Start

```bash
# Clone and use with any AI agent
git clone https://github.com/supernk/frontend-design-skill.git
cp frontend-design-skill/*.md ~/your-agent/skills/
```

### Source Repositories Analyzed

| Prompt | Lines | What We Learned |
|---|---|---|
| `CLAUDE-FABLE-5.md` | 1,597 | Design philosophy, copyright rules, search behavior |
| `Claude-Design-Sys-Prompt.txt` | 422 | Full design system (Tweak protocol, starter components, 12 sub-skills) |
| `Cursor_Prompt.md` | 54 | Never output code to chat, read-before-edit, 3-lint-attempt limit |
| `Devin_2.0.md` | 63 | Planning/Standard dual-mode, Pop Quiz anti-injection, git protocol |
| `Manus_Prompt.txt` | 282 | Event stream architecture, notify/ask channels, writing rules |
| `Windsurf_Prompt.md` | 96 | Proactive memory, promise-then-execute, 0.0.0.0 binding |
| `Replit_Agent.md` | 102 | No destructive DB ops, ORM-only migrations, rollback hints |
| `Codex.md` | 90 | AGENTS.md spec, citation format, container session model |

### License

AGPL-3.0 — same as the source repository. Recovered content is factual documentation of publicly available AI system behavior.

---

## 中文

### 这是什么

这个仓库包含两个从 [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) 泄露中复原的 AI 技能。CL4R1T4S 收集了 ChatGPT、Claude、Gemini、Grok、Cursor、Devin、Manus、Windsurf 等主流 AI 的系统提示词。两个技能均采用 SKILL.md 格式，可用于 Hermes、Claude Code 等 AI Agent。

| 文件 | 技能 | 来源 |
|---|---|---|
| `SKILL.md` | **frontend-design** | 从 Claude Fable 5 / Opus / 设计系统提示词重建 |
| `SOLO-DEV-AGENT.md` | **solo-dev-agent** | 综合 Cursor、Devin、Manus、Windsurf、Replit、Codex |

---

### 技能一：frontend-design（`SKILL.md`）

反 AI 同质化前端设计。编码了 Anthropic 内部用来防止 AI 产出"AI 风格"UI 的设计哲学。

**覆盖：** AI 烂梗黑名单（8 条反模式）、oklch 色彩系统、独特字体排版、不对称布局、组件反默认设计、Tweak 调参协议、变体方法论、CSS 手册、交付前检查清单（11 项）。

**使用：**
```
skill_view(name='frontend-design')
```

---

### 技能二：solo-dev-agent（`SOLO-DEV-AGENT.md`）

面向独立开发者的生产级 Agent 工作流。综合了 6 个泄露的编码 Agent 提示词中的最佳运营模式。

**覆盖：**
| 模块 | 来源 |
|---|---|
| 双模式（Planning / Execution） | Devin |
| notify / ask 消息通道 | Manus |
| 编码防护（先读后改、3 次上限） | Cursor + Devin + Replit |
| 错误恢复协议 | Cursor |
| Git 协议（禁用 `git add .`、精确暂存） | Devin |
| 安全边界 | Fable 5 + Devin |
| Windows 环境知识 | 自定义 |

**使用：**
```
skill_view(name='solo-dev-agent')
```

---

### 快速开始

```bash
git clone https://github.com/supernk/frontend-design-skill.git
cp frontend-design-skill/*.md ~/your-agent/skills/
```

### 分析过的源文件

| 提示词 | 行数 | 学到什么 |
|---|---|---|
| `CLAUDE-FABLE-5.md` | 1,597 | 设计哲学、版权规则、搜索行为 |
| `Claude-Design-Sys-Prompt.txt` | 422 | 完整设计系统（Tweak 协议、脚手架组件、12 个子技能） |
| `Cursor_Prompt.md` | 54 | 不输出代码到聊天、先读后改、lint 最多修 3 次 |
| `Devin_2.0.md` | 63 | Planning/Standard 双模、Pop Quiz 反注入、git 协议 |
| `Manus_Prompt.txt` | 282 | 事件流架构、notify/ask 通道、写作规则 |
| `Windsurf_Prompt.md` | 96 | 主动记忆、承诺即执行、0.0.0.0 绑定 |
| `Replit_Agent.md` | 102 | 不破坏性操作数据库、仅 ORM 迁移、回滚提示 |
| `Codex.md` | 90 | AGENTS.md 规范、引用格式、容器会话模型 |

### 许可证

AGPL-3.0 — 与源仓库相同。复原内容属于对公开可获取的 AI 系统行为的事实性文档记录。

---

## See Also / 另见

- [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) — AI Systems Transparency for All
- [Hermes Agent](https://hermes-agent.nousresearch.com/docs) — The agent platform these skills target
- [oklch.com](https://oklch.com) — Color picker and converter for oklch
