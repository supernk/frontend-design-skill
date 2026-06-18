# Frontend Design — AI Skill

> **Distinctive, intentional UI that avoids templated defaults. Recovered from leaked Claude system prompts.**
>
> **独特的、有意图的 UI 设计，避免模板化的默认风格。从泄露的 Claude 系统提示词中复原。**

---

[English](#english) | [中文](#中文)

---

## English

### What This Is

This is a frontend design skill recovered from the [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) leak of Claude (Anthropic) system prompts. It encodes the design philosophy Anthropic uses internally to stop Claude from producing generic, "AI-looking" UI.

The original skill is named `frontend-design` and lives at `/mnt/skills/public/frontend-design/SKILL.md` in Claude's sandbox. While the SKILL.md file itself was not leaked verbatim, its description, trigger conditions, and the full design system prompt (Claude-Design-Sys-Prompt, 422 lines) were recovered. This skill is a faithful reconstruction of that system.

### What It Covers

| Module | Content |
|---|---|
| **AI Slop Blacklist** | 8 anti-patterns that scream "AI made this" (gradient backgrounds, rounded-card-left-border, Inter/Roboto/Arial fonts, emoji, etc.) |
| **Color System** | oklch-based derivation — derive harmonious palettes from one base color |
| **Typography** | Font pairing guide with 7 distinctive pairs — intentionally avoiding AI-default fonts |
| **Layout & Composition** | Asymmetric grids, broken-grid moments, oversized type, texture/noise |
| **Component Anti-Defaults** | How to make buttons, cards, heroes, and navbars that DON'T look like templates |
| **Tweak System** | PostMessage-based protocol for live design parameter panels in prototypes |
| **Variation Methodology** | 6 dimensions × 3+ variations — explore the possibility space |
| **CSS Playbook** | Modern CSS best practices (`text-wrap: pretty`, `oklch()`, `:has()`, etc.) |
| **Pre-Delivery Checklist** | 11-item verification before shipping any UI |

### Usage

Load this skill before writing any UI code (web components, landing pages, dashboards, React components, HTML/CSS layouts). It works with any AI agent that supports SKILL.md format.

**For Hermes Agent:**
```
skill_view(name='frontend-design')
```

**For other agents:** Copy `SKILL.md` into your skills directory.

### Quick Execution Rule

```
BEFORE writing any UI code:

1. State your design thesis: "This is [style] + [twist], executed with [technique]"
2. Pick fonts NOT in {Inter, Roboto, Arial, Fraunces}
3. Derive colors from one base using oklch
4. Add ONE bold move: oversized type / broken grid / unexpected color / heavy borders / texture
5. Provide 3 variations, not 1 "perfect" solution
6. Check the blacklist before shipping
```

### Source

Recovered from the [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) repository — an AI systems transparency project collecting leaked system prompts from ChatGPT, Claude, Gemini, Grok, Cursor, and more.

**Files analyzed for this reconstruction:**
- `CLAUDE-FABLE-5.md` (1,597 lines) — Fable 5 system prompt
- `Claude-Opus-4.7.txt` (1,408 lines) — Opus 4.7 system prompt
- `Claude_Opus_4.6.txt` (1,047 lines) — Opus 4.6 system prompt
- `Claude-4.5-Opus.txt` (1,222 lines) — 4.5 Opus system prompt
- `Claude-Design-Sys-Prompt.txt` (422 lines) — Full design system prompt

### License

AGPL-3.0 — same as the source repository. The recovered content is factual documentation of publicly available AI system behavior.

---

## 中文

### 这是什么

这是从 [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) 泄露的 Claude（Anthropic）系统提示词中复原的前端设计技能。它编码了 Anthropic 内部用来防止 Claude 产生千篇一律"AI 风格"UI 的设计哲学。

原始技能名称为 `frontend-design`，在 Claude 沙箱中位于 `/mnt/skills/public/frontend-design/SKILL.md`。虽然 SKILL.md 文件本身未被逐字泄露，但其描述、触发条件以及完整的设计系统提示词（Claude-Design-Sys-Prompt，422 行）均已被复原。此技能是对该系统的忠实重建。

### 覆盖内容

| 模块 | 内容 |
|---|---|
| **AI 设计烂梗黑名单** | 8 种暴露"这是 AI 做的"的反模式（渐变背景、圆角卡片左边框、Inter/Roboto/Arial 字体、emoji 等） |
| **色彩系统** | 基于 oklch 的派生方法 — 从一个基础色派生和谐配色 |
| **字体排版** | 7 组独特字体配对指南 — 刻意避开 AI 默认字体 |
| **布局与构图** | 不对称网格、破格瞬间、超大字号、纹理/噪点 |
| **组件反默认设计** | 如何让按钮、卡片、Hero 区和导航栏不像模板 |
| **Tweak 系统** | 基于 PostMessage 的原型实时调参协议 |
| **变体方法论** | 6 个维度 × 3+ 个变体 — 探索可能性空间 |
| **CSS 手册** | 现代 CSS 最佳实践（`text-wrap: pretty`、`oklch()`、`:has()` 等） |
| **交付前检查清单** | 11 项验收标准 |

### 使用方法

在编写任何 UI 代码（网页组件、落地页、仪表盘、React 组件、HTML/CSS 布局）之前加载此技能。适用于任何支持 SKILL.md 格式的 AI 代理。

**Hermes Agent：**
```
skill_view(name='frontend-design')
```

**其他代理：** 将 `SKILL.md` 复制到你的技能目录。

### 快速执行规则

```
写任何 UI 代码之前：

1. 说出你的设计论题："这是 [风格] + [变奏]，用 [技法] 执行"
2. 选择不在 {Inter, Roboto, Arial, Fraunces} 中的字体
3. 用一个基础色通过 oklch 派生配色
4. 加一个大胆动作：超大字号 / 破格布局 / 意外配色 / 粗边框 / 纹理
5. 提供 3 个变体，而非 1 个"完美"方案
6. 交付前对照黑名单
```

### 来源

从 [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) 仓库复原 — 这是一个 AI 系统透明度项目，收集了 ChatGPT、Claude、Gemini、Grok、Cursor 等泄露的系统提示词。

**本次重建分析的文件：**
- `CLAUDE-FABLE-5.md`（1,597 行）— Fable 5 系统提示词
- `Claude-Opus-4.7.txt`（1,408 行）— Opus 4.7 系统提示词
- `Claude_Opus_4.6.txt`（1,047 行）— Opus 4.6 系统提示词
- `Claude-4.5-Opus.txt`（1,222 行）— 4.5 Opus 系统提示词
- `Claude-Design-Sys-Prompt.txt`（422 行）— 完整设计系统提示词

### 许可证

AGPL-3.0 — 与源仓库相同。复原内容属于对公开可获取的 AI 系统行为的事实性文档记录。

---

## See Also / 另见

- [CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S) — AI Systems Transparency for All
- [Hermes Agent](https://hermes-agent.nousresearch.com/docs) — The agent this skill was built for
- [oklch.com](https://oklch.com) — Color picker and converter for oklch
