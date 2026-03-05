# Hugo Blog Skills

Five AI agent skills for managing a Hugo blog: writing, editing, auditing, planning, and promotion.

Reusable AI agent skills for managing any Hugo blog.

## Skills

| Skill | Purpose | Trigger phrases |
|---|---|---|
| **blog-writer** | Create new posts through an interview-driven workflow | "write a post", "new blog post", "draft a post" |
| **blog-editor** | Review and edit existing posts for tone, structure, and conventions | "review this post", "edit the blog post", "check my front matter" |
| **blog-keeper** | Audit internal links, cross-references, and "coming soon" teasers | "check blog links", "audit posts", "find broken links" |
| **blog-planner** | Discover and plan new topics by analyzing existing content | "new post idea", "what should I write about", "brainstorm posts" |
| **blog-marketer** | Generate LinkedIn and Twitter/X content to promote posts | "promote this post", "share on LinkedIn", "tweet about this" |

## Platform Support

These skills work with multiple AI coding agents. The repo includes symlinks for automatic discovery:

| Platform | Discovery path | How to install |
|---|---|---|
| **Claude Code** | `.claude/skills/` | Clone repo, or install as plugin |
| **GitHub Copilot** | `.github/skills/` | Clone repo into your project |
| **OpenAI Codex** | `.agents/skills/` | Clone repo into your project |
| **Gemini CLI** | `.gemini/skills/` or `.agents/skills/` | Clone repo, or install as extension |

All four paths are symlinks to the canonical `skills/` directory, so skills stay in sync.

## Quick Start

### Option 1: Clone into your project

```bash
git clone https://github.com/mdelapenya/blog-skills.git
```

The symlinks inside the repo handle platform discovery automatically.

### Option 2: Copy skills to your agent's discovery path

```bash
# For Claude Code
cp -r skills/* ~/.claude/skills/

# For Copilot
cp -r skills/* .github/skills/

# For Codex
cp -r skills/* .agents/skills/

# For Gemini CLI
cp -r skills/* .gemini/skills/
```

### Option 3: Symlink for single source of truth

```bash
REPO=/path/to/hugo-blog-skills/skills

# Claude Code (user-global)
ln -s $REPO/blog-writer ~/.claude/skills/blog-writer
ln -s $REPO/blog-editor ~/.claude/skills/blog-editor
ln -s $REPO/blog-keeper ~/.claude/skills/blog-keeper
ln -s $REPO/blog-planner ~/.claude/skills/blog-planner
ln -s $REPO/blog-marketer ~/.claude/skills/blog-marketer
```

## Repo Structure

```
blog-skills/
├── skills/                          # Canonical skill files
│   ├── blog-writer/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── front-matter-example.md
│   ├── blog-editor/
│   │   └── SKILL.md
│   ├── blog-keeper/
│   │   └── SKILL.md
│   ├── blog-planner/
│   │   ├── SKILL.md
│   │   └── references/
│   │       └── topic-map.example.md
│   └── blog-marketer/
│       ├── SKILL.md
│       └── references/
│           └── platform-guide.md
├── .agents/skills -> ../skills      # Codex + Gemini CLI
├── .claude/skills -> ../skills      # Claude Code
├── .github/skills -> ../skills      # Copilot
├── .gemini/skills -> ../skills      # Gemini CLI
├── .claude-plugin/
│   └── plugin.json                  # Claude Code plugin manifest
├── gemini-extension.json            # Gemini CLI extension manifest
├── LICENSE                          # MIT
└── README.md
```

## Setup

1. Copy the config template into your blog repo root:
   ```bash
   cp skills/blog-config.example.md /path/to/your-blog-repo/blog-config.md
   ```
2. Edit `blog-config.md` in your blog repo with your blog's domain, theme, social handles, topic areas, and publication settings
3. Optionally customize reference files:
   - `blog-writer/references/front-matter-example.md` — your site's front matter fields
   - `topic-map.md` in your blog repo — generate by running the planner against your content
   - `blog-marketer/references/platform-guide.md` — platform-specific guidance (mostly generic)

## License

MIT
