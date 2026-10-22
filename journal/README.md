# Journal: the inbox

Session notes written by Claude Code at the end of a work session: what was done, what was decided, and what is still open. Claude Code's wrap-up command writes these notes.
Updated: 2026-10-22

## How it works
- Each note is one file: `journal/YYYY-MM-DD-project-short-title.md`.
- Hermes reads each new note and files its content into the right box: the box's memory.md, log.md or docs/.
- Once filed, the note is marked processed by adding `processed: YYYY-MM-DD` to its front matter.
- The notes stay here as the record. Nothing is deleted.
- Where the content ends up: the project's box in the tree, for example lacande/coding/website. CONVENTIONS.md has the details.
