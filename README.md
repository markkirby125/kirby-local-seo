# Local AI Search & Review Engineering (Kirby Local SEO)

[![Kirby Skills Collection](https://img.shields.io/badge/Kirby_Skills-Collection-blue?style=flat-square&logo=github)](https://github.com/markkirby125/kirby-skills-collection)

You have a Google Business Profile and are trying to rank in the local map pack. For years, it was completely reasonable to just build standard NAP citations, stuff a few keywords into your GMB description, and passively collect 5-star reviews. 

**However, Google Ask Maps and generative AI agents have fundamentally broken that model.** Conversational agents (ChatGPT, Gemini) don't just look at proximity or link volume—they read the exact semantic attributes inside your reviews and service pages. If your content doesn't explicitly satisfy an AI's highly constrained query parameters, you are filtered out of the candidate pool before traditional rankings are even calculated.

By ignoring AI attribute matching, you are silently bleeding high-intent, hyper-local conversion traffic to competitors who have adapted to semantic local architecture.

**The Solution:** The `kirby-local-seo` skill enforces the strict 4+1 Local Content Classification Engine and Google Ask Maps review engineering protocols. It forces your AI coding agent to generate local content and schema that guarantees your business entity passes the LLM attribute-matching phase.

## 🪄 The Magic Prompt

Copy and paste this directly to your AI (Cursor, Windsurf, Claude Code, Antigravity):

```markdown
@agent Please install the kirby-local-seo skill into this workspace.
1. Read the `SKILL.md` file and `references/` directory from this repository: https://github.com/markkirby125/kirby-local-seo
2. Identify the correct rules system for our current environment (e.g., `.cursor/rules/` for Cursor, `.windsurfrules` for Windsurf, `.clinerules` for Cline, or `~/.agents/skills/` for Antigravity).
3. Save the contents appropriately. If our environment supports multi-file dispatcher skills, clone the directory structure exactly.
4. Confirm when the installation is complete.
```

## Manual Installation

- **Cursor**: Save `SKILL.md` to `.cursor/rules/kirby-local-seo.mdc` and copy `references/`
- **Windsurf**: Save `SKILL.md` to `.windsurfrules` and copy `references/`
- **Antigravity**: Clone this repository directly into `~/.agents/skills/kirby-local-seo`

## Tech Stack

- **Format**: Markdown / YAML
- **Compatibility**: Antigravity, Claude Code, Cursor, Windsurf, Cline
