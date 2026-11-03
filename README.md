# Skill Santuy ☕🎭

> Universal Agent Skill for Indonesian casual chat, comedic banter, and Ngawi internet pop culture. Strictly functional, deeply technical, with an ironclad Golden Rule.

[![Validate Skill](https://github.com/masambangawi/skill-santuy/actions/workflows/validate.yml/badge.svg)](https://github.com/masambangawi/skill-santuy/actions/workflows/validate.yml)
[![skills.sh](https://img.shields.io/badge/skills.sh-masambangawi%2Fskill--santuy-black)](https://skills.sh)
[![Specification: Agent Skills](https://img.shields.io/badge/spec-Agent%20Skills-blue.svg)](https://agentskills.io/specification)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## What is Skill Santuy?

**Skill Santuy** is a portable, harness-agnostic skill following the [Agent Skills Specification](https://agentskills.io/specification). It transforms your AI coding agent's conversational tone into a hilarious, blak-blakan Indonesian internet persona (inspired by iconic Indonesian memes like Mas Rusdi, Amba, and Ngawi lore) while keeping **100% precision, productivity, and technical excellence**.

### ⚠️ The Golden Rule: Chat Only

```
┌─────────────────────────────────────────────────────────────┐
│                       THE GOLDEN RULE                       │
├──────────────────────────────┬──────────────────────────────┤
│ ✅ CHAT CONVERSATION ONLY    │ ❌ PRODUCTION ARTIFACTS     │
├──────────────────────────────┼──────────────────────────────┤
│ • Casual Indonesian banter   │ • Source code (.ts, .py, etc)│
│ • Absurdist comedic roasting │ • Unit tests & fixtures      │
│ • Playful meme references    │ • Git commit messages        │
│ • Direct technical feedback  │ • Pull Requests & Issues     │
│                              │ • Documentation & configs    │
└──────────────────────────────┴──────────────────────────────┘
```

When an agent with Skill Santuy writes to files or generates deliverables, the output is **100% clean, professional, modular, and unpolluted**.

---

## 🚀 Supported Harnesses

Skill Santuy works out of the box with any AI coding harness supporting skill directories or system instructions:

| Harness | Location / Method | Support Status |
|---|---|---|
| **OpenCode** | `.opencode/skills/santuy/` or `~/.config/opencode/skills/` | Native |
| **Claude Code** | `.claude/skills/santuy/` | Native |
| **Cursor** | `.cursor/skills/santuy/` or `.agents/skills/santuy/` | Native |
| **Codex** | `.agents/skills/santuy/` | Native |
| **Windsurf** | `.windsurf/skills/santuy/` | Native |

Read the full [Installation Guide](docs/installation.md) for quick setup commands.

---

## 📦 Quick Installation

### Option 1: Universal CLI via skills.sh (Recommended)

Install directly using Vercel's official Agent Skills CLI into any supported agent:

```bash
npx skills add masambangawi/skill-santuy
```

### Option 2: Per-Project Manual Install

Run inside your repository root:

```bash
# For OpenCode / Cursor / Codex standard:
mkdir -p .agents/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .agents/skills/santuy
rm -rf /tmp/skill-santuy
```

### Option B: Claude Code

```bash
mkdir -p .claude/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .claude/skills/santuy
rm -rf /tmp/skill-santuy
```

---

## 📖 How It Works

Once installed, triggering the skill is simple:
- Say: *"Santuy dulu rek"*, *"Mode santuy cik"*, or chat casually in Indonesian.
- The agent adapts its conversational register immediately.
- Ask it to write code, debug a race condition, or run tests: the technical solution will be crisp, correct, and completely professional inside the code files.

See [Scenarios and Test Cases](tests/scenarios.md) to inspect expected inputs and outputs.

---

## 🤝 Contributing

We welcome community contributions! Want to propose a new witty phrase formula, report harness compatibility, or refine boundaries?
- Check out [CONTRIBUTING.md](CONTRIBUTING.md) for our contribution guide.
- Review our community guidelines in [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
- Report security or privacy concerns via [SECURITY.md](SECURITY.md).

---

## 📄 License

Distributed under the [MIT License](LICENSE). Copyright (c) 2026 masambangawi.
