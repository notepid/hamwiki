# HAM Radio Wiki — Project Instructions

## About This Project

An open-source amateur radio wiki built on Wiki.js. The content lives in markdown files with Wiki.js frontmatter. The wiki is international in scope, covers all skill levels, and is organized by topic area across 16 categories.

## Repository Structure

```
hamwiki/
├── home.md                    # Main landing page / navigation hub
├── CLAUDE.md                  # This file — project instructions
├── CONTENT-STATUS.md          # Tracks every page's content status
├── README.md                  # GitHub repo readme
├── getting-started/           # 16 topic-based category folders
├── licensing/                 #   each containing markdown pages
├── operating/                 #   with Wiki.js frontmatter
├── digital-modes/
├── equipment/
├── antennas/
├── propagation/
├── electronics/
├── emergency-communications/
├── satellites/
├── contesting/
├── awards/
├── software/
├── diy-projects/
├── history/
└── community/
```

## Wiki.js Page Format

Every page must use this frontmatter format:

```markdown
---
title: Page Title
description: Brief description of the page content
published: true
date: 2026-04-05T09:30:00.000Z
tags: comma, separated, tags
editor: markdown
dateCreated: 2026-04-05T09:30:00.000Z
---
```

## AI-Generated Content Banner

**All AI-generated content MUST include this banner** immediately after the frontmatter and before any other content:

```markdown
> **Notice:** This page was initially generated with the assistance of AI and is pending human review. The information may contain errors or omissions. Amateur radio operators are encouraged to verify all technical details independently. Help improve this page by submitting corrections and additions. [Learn how to contribute](/contributing) *Remove this banner after human review is complete.*
{.is-warning}
```

The `{.is-warning}` class renders as a yellow warning box in Wiki.js.

When a human reviewer has verified and approved the content, they should:
1. Remove the banner from the page
2. Update CONTENT-STATUS.md to change the page status from `ai-draft` to `reviewed`

## Content Status Tracking

All page statuses are tracked in `CONTENT-STATUS.md` at the repo root. Pages go through these stages:

| Status | Meaning |
|--------|---------|
| `stub` | Placeholder only — no real content yet |
| `ai-draft` | AI-generated content written, awaiting human review |
| `reviewed` | Human-reviewed and approved (AI banner removed) |

**When generating content for a page, always update CONTENT-STATUS.md** to change its status from `stub` to `ai-draft`.

## Content Writing Guidelines

When writing wiki content:

- **Be accurate.** Prioritize correctness over completeness. If unsure about something, note it or omit it.
- **Be international.** Don't assume a US-only audience. When discussing regulations, licensing, or practices, cover multiple countries or note which country is being discussed.
- **Be beginner-friendly.** Start each page with accessible explanations. Add depth as the page progresses.
- **Use practical examples.** Where possible, include real-world examples, typical setups, and common use cases.
- **Link to other wiki pages.** Cross-reference related topics using Wiki.js internal links (e.g., `/getting-started/your-first-radio`).
- **Avoid product endorsements.** Mention product categories and features, not specific brand recommendations.
- **Use metric and imperial.** Include both measurement systems where relevant.
- **Include safety warnings.** For topics involving RF exposure, high voltage, tower climbing, etc., always include appropriate safety information.

## Git Workflow

- Work on the `main` branch
- Always ask the user for review before committing
- Write clear, descriptive commit messages
- Push to origin after committing
