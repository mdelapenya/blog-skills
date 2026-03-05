# CLAUDE.md

## Project Overview

Cross-platform AI agent skills for managing a Hugo blog. Contains five skills (writer, editor, keeper, planner, marketer) that work with Claude Code, GitHub Copilot, OpenAI Codex, and Gemini CLI.

The canonical skill files live in `skills/`. Platform-specific discovery paths (`.agents/skills`, `.claude/skills`, `.github/skills`, `.gemini/skills`) are symlinks to `../skills`.

Blog-specific settings live in `blog-config.md` in the blog repo root. Copy from `skills/blog-config.example.md` in this repo and place it in your blog repo.

## Repo Structure

```
skills/                          # Canonical skill files (edit here)
├── blog-writer/                 # Create new posts via interview workflow
│   ├── SKILL.md
│   └── references/
│       └── front-matter-example.md
├── blog-editor/                 # Review and edit existing posts
│   └── SKILL.md
├── blog-keeper/                 # Audit links and cross-references (read-only)
│   └── SKILL.md
├── blog-planner/                # Discover and plan new topics
│   ├── SKILL.md
│   └── references/
│       └── topic-map.example.md
└── blog-marketer/               # Generate social media content
    ├── SKILL.md
    └── references/
        └── platform-guide.md

.agents/skills -> ../skills      # Codex + Gemini CLI discovery
.claude/skills -> ../skills      # Claude Code discovery
.github/skills -> ../skills      # Copilot discovery
.gemini/skills -> ../skills      # Gemini CLI discovery
.claude-plugin/plugin.json       # Claude Code plugin manifest
gemini-extension.json            # Gemini CLI extension manifest
```

## Skill File Conventions

Each skill has a `SKILL.md` with YAML front matter:

```yaml
---
name: skill-name
description: One-line description. Include trigger phrases.
allowed-tools: Read Edit Write Grep Glob AskUserQuestion
metadata:
  author: blog-skills
  version: "1.0.0"
---
```

### Required sections in SKILL.md

1. **Title and purpose** — what the skill does, what it does NOT do
2. **Instructions** — numbered steps the agent follows
3. **Examples** — 2-3 concrete usage scenarios with expected actions
4. **Troubleshooting** — common failure modes and fixes

### Reference files

Place supporting data in `references/` inside the skill directory. Reference them from SKILL.md with relative paths (e.g., `references/front-matter-example.md`).

## Editing Skills

Always edit files in `skills/`. Never edit inside the symlinked directories (`.agents/`, `.claude/`, `.github/`, `.gemini/`). Changes in `skills/` propagate automatically through symlinks.

The user-global symlinks (`~/.claude/skills/blog-*`) also point here, so edits take effect immediately in all Claude Code sessions.

## Tone and Style Rules (shared across skills)

These conventions apply to all blog content the skills produce:

- First-person, conversational voice
- No em dashes (—) — use colons, periods, commas, semicolons, or parentheses
- No leading whitespace on paragraphs
- Practical over theoretical: CLI commands, code snippets, real examples
- Short paragraphs, one idea each
- Bold for key terms, bullet lists for enumerations

## Verification

```bash
# All platform paths show the same 5 skills
ls skills/ .agents/skills/ .claude/skills/ .github/skills/ .gemini/skills/

# User-global symlinks resolve correctly
ls -la ~/.claude/skills/blog-*
cat ~/.claude/skills/blog-keeper/SKILL.md | head -3

# Symlinks inside repo are relative
readlink .agents/skills   # should show ../skills
```

## Git Conventions

Follow conventional commits:

```
feat(skill): description      # new skill or major feature
fix(skill): description       # bug fix in a skill
chore: description            # maintenance, docs, config
```

Scope is the skill name without the `blog-` prefix (e.g., `feat(writer): add series detection step`).
