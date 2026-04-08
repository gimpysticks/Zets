# The Claude Code Cheatsheet
**Updated March 2026**

60+ Commands | 6 Environments | 1M Token Context | 20 Voice Languages

---

## 📥 INSTALLATION

| macOS | Windows | npm |
| :--- | :--- | :--- |
| `brew install claude-code` | `winget install Anthropic.ClaudeCode` | `npm i -g @anthropic-ai/claude-code` |

**Then:** `cd your-project && claude`

---

## 🛠️ CLI FLAGS

* **claude "prompt"** — start with a prompt
* **claude -p** — (one-shot, non-interactive)
* **claude -c** — (continue last session)
* **claude --resume** — (resume by ID or name)
* **claude -n "name"** — (name new session)
* **claude --worktree** — (run in isolated git worktree)
* **claude --effort high** — (set max reasoning effort)
* **claude --remote-control** — (remote terminal access)
* **claude --debug** — (enable debug logging)

---

## 📜 CLAUDE.md — AGENT'S CONSTITUTION

**Where:**
* `~/.claude/CLAUDE.md` (global)
* `./CLAUDE.md` (project)
* `./src/CLAUDE.md` (folder overrides)

**What:**
* build/lint/test commands
* code conventions and patterns
* commit message format
* architecture decisions and tech stack
* what NOT to do (anti-patterns)

> **Pro tip:** Use `/init` to scaffold, then curate manually.

---

## 🔌 EXTENSIBILITY STACK

* **Skills (`.claude/skills/`)** — AI-driven skill definitions, automatically invoked when Claude matches the task, YAML frontmatter.
* **Subagents (`.claude/agents/`)** — instances with isolated context windows, Explore (read-only) and Code (tool access) types.
* **Hooks (`settings.json` → `hooks{}`)** — deterministic code that runs at specific events, e.g., `PreToolUse`, `PostToolUse`.
* **MCP Servers (`claude mcp add`)** — connects Claude Code to external tools/data via Model Context Protocol, e.g., GitHub, Jira, Slack, linear, postgres, notion, lazy-loads tools.

---

## 💻 6 ENVIRONMENTS

* Terminal CLI
* VS Code Extension
* JetBrains Plugin
* Jenkins Plugin
* Desktop App
* Web
* claude.ai/code
* iOS App

---

## ⌨️ SLASH COMMANDS

| Col 1 - Session | Col 2 - Model | Col 2 - Workflow |
| :--- | :--- | :--- |
| `/compact` | `/model` | `/plan` |
| `/clear` | `/effort low\|med\|high` | `/voice` |
| `/rewind` | `"ultrathink" keyword` | `/loop` |
| `/diff` | | `/btw` |
| `/cost` | | `/init` |
| `/usage` | | |
| `/context` | | |

* **/review** — multi-agent code review pipeline
* **/simplify** — 3-agent architecture review before PR
* **/batch** — parallel changes across multiple isolated worktrees
* **/debug** — systematic debugging workflow
* **/loop** — scheduled cron-like tasks in-session
* **/claude-api** — API and SDK documentation, patterns, SDK examples on demand

---

## ⌨️ KEYBOARD SHORTCUTS

* **Shift+Tab:** cycle permission modes (normal, auto-accept, plan mode)
* **Option+T:** toggle extended thinking on/off
* **Option+P:** open model picker
* **Ctrl+G:** open current file/diff in external editor
* **Esc+Esc:** open rewind/undo menu
* **Tab:** toggle extended thinking for current turn only

---

## 💰 COST TIPS

* **/effort low** for quick iteration — save thinking tokens
* **/model haiku** for mechanical/repetitive tasks (formatting, renaming)
* **/compact** proactively — larger contexts cost more per token
* **Batch API 50% off** for non-urgent async workloads
* **Prompt Caching 90% savings** for repetitive inputs

---

## 📣 WHAT'S NEW MARCH 2026

* **Opus 4.6 Default [NEW]:** Opus 4.6 is now the default model, effort defaults to medium.
* **1M Token Context [NEW]:** Supports 1 million token context window for Max/Team/Enterprise plans.
* **Voice Mode [NEW]:** Native voice interaction via /voice, push-to-talk, 20 languages.
* **/loop Command [NEW]:** Scheduled recurring tasks (cron) within a session, e.g., for monitoring.
* **ultrathink [NEW]:** Special keyword for maximum possible reasoning on the next turn only.
* **Remote Control [NEW]:** Terminal access from claude.ai, code, iPhone, iPad, Mac, code stays local.
* **Computer Use [NEW]:** Enhanced visual reasoning for desktop automation, research preview for Pro/Max.
* **HTTP Hooks [NEW]:** Deterministic hooks can POST JSON to any URL, custom headers, env var interpolation.

---
`code.claude.com` | `github.com/anthropics/claude-code`
Created by Brij Pandey • @brijpandeyji
