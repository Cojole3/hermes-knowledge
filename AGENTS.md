# Knowledge base: rules

Read these rules before writing anything in this folder.

This folder is Leon's long-term memory.
- **Hermes** maintains it.
- **Leon** reads it, later through his own interface.
- **Claude Code** adds session notes to `journal/`.

It will live in a private GitHub repository (`knowledge`), so every change has a history.

## Folders

| Folder | What goes in it |
|---|---|
| `about-me/` | Leon: who he is, his preferences, how he works. Short and factual. |
| `projects/` | One page per project, plus `INDEX.md`, the map of all projects and how they connect. |
| `thoughts/` | Leon's ideas and reflections, one file per topic, refined over time. |
| `design/` | Design language and templates: the Lacande design language, and later the HTML output template. |
| `outputs/` | Every finished document Hermes produces, dated, plus `INDEX.md`. |
| `journal/` | Session notes written by Claude Code. Hermes reads them but doesn't edit them. |
| `imports/claude/` | Leon's exported Claude history, sorted by topic. |
| `skills/` | Later: how-to manuals shared with Claude Code. |

## Writing rules
- **Format:** Markdown, plain language, short sections, headings a non-programmer understands.
- **File names:** `lowercase-with-dashes.md`. Dates are written `YYYY-MM-DD`.
- **Page header:** every page starts with a one-line summary and `Updated: YYYY-MM-DD`.
- **Update, don't duplicate:** search first, then extend the existing page.
- **Links:** link related pages with relative links.
- **Facts vs. guesses:** mark assumptions and inferences as such. A project's own repository and docs win over this knowledge base.
- **Secrets:** never put passwords, API keys, tokens, or personal data about third parties beyond what's needed.
- **The map:** when a project's status changes or an important decision is made, update its page, and update `projects/INDEX.md` too if the overview changes.

## Project pages
Use these sections: **Summary · What it is · Status · Next steps · Decisions · Connections · Where things are · Open questions.**

## Outputs
- **Path:** `outputs/YYYY/YYYY-MM-DD-short-title.html` (or `.md`).
- **Index:** add one line to `outputs/INDEX.md` with the date, title, type, project, and a one-line description.
- **HTML outputs** follow the design in `design/`. The output template comes later.

## Thoughts
- One file per topic: `thoughts/topic-name.md`.
- Add dated entries at the bottom.
- Keep a short **"Current view"** at the top, and refine it when Leon's thinking changes.
