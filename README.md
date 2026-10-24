# Local AI Search & Review Engineering (Kirby Local SEO)

[![Kirby Skills Collection](https://img.shields.io/badge/Kirby_Skills-Collection-blue?style=flat-square&logo=github)](https://github.com/markkirby125/kirby-skills-collection)

You have a Google Business Profile and are trying to rank in the local map pack. For years, it was completely reasonable to just build standard NAP citations, stuff a few keywords into your GMB description, and passively collect 5-star reviews. 

**However, Google Ask Maps and generative AI agents have fundamentally broken that model.** Conversational agents (ChatGPT, Gemini) don't just look at proximity or link volume—they read the exact semantic attributes inside your reviews and service pages. If your content doesn't explicitly satisfy an AI's highly constrained query parameters, you are filtered out of the candidate pool before traditional rankings are even calculated.

By ignoring AI attribute matching, you are silently bleeding high-intent, hyper-local conversion traffic to competitors who have adapted to semantic local architecture.

**The Solution:** The `kirby-local-seo` skill enforces the strict 4+1 Local Content Classification Engine and Google Ask Maps review engineering protocols. It forces your AI coding agent to generate local content and schema that guarantees your business entity passes the LLM attribute-matching phase.

## 🆕 October 2026 — Review Engineering Doctrine (Matt Hammerton, Ep. 1135)

- **§3.14** Star-rating math: the baseline-dependent offset ratio `x=(a−1)/(5−a)` (7:1 at 4.5 → 79:1 at 4.95) and the illegitimate-review removal SOP (4-removal map-pack unfreeze benchmark)
- **§3.15** The GBP "super-link" effect — verified GBP → city landing page, gated by the §3.8 routing tree
- **§3.16** Review gating marked compliance-restricted (Google policy + FTC 16 CFR 465) with the policy-safe unconditional-survey alternative
- **§3.17** Standalone brand review summary sites (`[Brand]Reviews.com`) for LLM review corroboration (canonical twin shipped in `kirby-decision-engine-optimization` Module 4)
- **§3.18** Offline-asset digitization for established 30–40 year businesses into verified review/proof nodes
- **§3.19** Ask Maps SAB address revelation, restored GBP Product links & Whitespark 1.8M Study correlations
- **§3.20** EXIF metadata reality check (no measurable Map Pack lift vs. +90% Lens visual search appearance) & Local Context Saturation for Google Ask Maps (The SEO Meta Study / Ep. 1191/1207)
- **§3.3.1** Primary-category niche-down one-way door (+3.4/−30) and DBA video-verification readiness

## 🆕 October 2026 — Location-Page Differentiation (Sept 24 Spam Update)

- **Module 7** Gate 0 Doorway Defense (service-area truth test for dispatch and non-dispatch professions alike) + the 10-Rule Differentiation Checklist: 50% Substance Variance with the Swap Test, per-page Service JSON-LD (`areaServed`/canonical `@id`), geo-photographs with honest alt text, polygon map embeds, transit-time commitments, landmark weaving, hyperlocal neighbor linking, suburb+job review harvesting, on-site short-video proof, and GSC indexation hygiene
- Cross-routes: 7-phase spam-update audit in `kirby-seo-telemetry` Module 11; metadata fact-check + SRA boundaries in `kirby-aiseo-skill` Module 15; pre-deploy Swap-Test lint gate in `kirby-seo-deployment` Module 19; Astro templates in `kirby-scrappy-local-launch` Module 1

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
