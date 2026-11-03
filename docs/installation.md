# Installation Guide

Skill Santuy is designed to follow standard skill specifications and can be installed across multiple AI coding harnesses.

---

## 1. OpenCode

### Per-Project
Clone or link the skill into your project's `.opencode/skills/` directory:

```bash
mkdir -p .opencode/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .opencode/skills/santuy
rm -rf /tmp/skill-santuy
```

### Global (All Projects)
Install into OpenCode's global configuration directory:

```bash
mkdir -p ~/.config/opencode/skills/
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy ~/.config/opencode/skills/santuy
rm -rf /tmp/skill-santuy
```

---

## 2. Claude Code

Claude Code discovers skills placed in `.claude/skills/`:

```bash
mkdir -p .claude/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .claude/skills/santuy
rm -rf /tmp/skill-santuy
```

---

## 3. Cursor

Cursor supports skill directories located in `.cursor/skills/` or the interoperable `.agents/skills/` folder:

```bash
mkdir -p .agents/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .agents/skills/santuy
rm -rf /tmp/skill-santuy
```

---

## 4. Codex & Windsurf

Both harnesses natively support the canonical `.agents/skills/` hierarchy:

```bash
mkdir -p .agents/skills
git clone https://github.com/masambangawi/skill-santuy.git /tmp/skill-santuy
cp -r /tmp/skill-santuy/santuy .agents/skills/santuy
rm -rf /tmp/skill-santuy
```

---

## Verification

Once installed, test that the skill triggers properly by opening your assistant in the workspace and typing:

> "Halo rek, coba cek status workspace kita sekarang."

The assistant should greet you with `rek` / `cik` and respond in Santuy mode while keeping all executed tool commands and file operations strictly clean.
