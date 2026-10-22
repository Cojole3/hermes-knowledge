# Conventions: how this knowledge base works

Plain rules for how the knowledge base is organised. Read GLOBAL.md first.
Updated: 2026-10-22

## The levels
1. **Global:** GLOBAL.md, about-leon.md, CONVENTIONS.md and journal/. Everyone reads these.
2. **Domain:** one of five top-level areas: lacande, investments, private, other-ventures, systems. Each has README.md and memory.md. Lacande also has ideas.md.
3. **Category:** a group inside a domain, such as lacande/coding. Has README.md, memory.md, log.md and docs/INDEX.md.
4. **Box:** the lowest level, where the work happens, such as lacande/coding/website. Has memory.md, log.md and docs/INDEX.md.

## What each box holds
- **memory.md:** the current picture, always kept up to date. Short: what it is, status, key decisions, next steps, open questions, connections.
- **log.md:** a dated record, newest first. One line per thing done.
- **docs/:** finished documents, with their own files. docs/INDEX.md lists each one.
- **ideas.md** (optional): ideas not yet decided.
- **references/** (optional): facts to look up, which change rarely, such as specifications.
- **playbooks/** (optional): checklists for one kind of situation, such as a coding housekeeping review.

Categories also have README.md, which lists each child with its status: Active, Paused or Empty. Paused also covers finished or stopped work that still has an open question.

## Front matter for documents
Every document in docs/ starts with this block:

    ---
    date: 2026-10-21
    title: Short title
    type: report
    box: lacande/coding/website
    task: short name of the task
    tags: [website, mobile]
    ---

Documents that were already here before this layout (the nightly digests, for example) may lack the block. It is added when they are next edited.

## The index line
Each docs/INDEX.md has one line per document, newest first, in this format:

    - YYYY-MM-DD · Title · type · task · file

Example: `- 2026-10-21 · Lacande on the Phone · report · website mobile audit · lacande-on-the-phone.md`

## Housekeeping when a task closes
When Leon closes a task, Hermes:
1. updates the box's memory.md;
2. appends one or more dated lines to the box's log.md;
3. files each new document in docs/ with front matter and an index line;
4. updates the parent README if a child's status changed.

## Session notes in journal/
- journal/ is the inbox. Claude Code writes one note per work session: journal/YYYY-MM-DD-project-short-title.md.
- Hermes reads each new note, files its content into the right box (memory, log, docs), and marks the note processed by adding `processed: YYYY-MM-DD` to its front matter.
- The note itself stays in journal/ as the record. Notes are not deleted.

## Layers of knowledge
- Every box's memory.md is read first when working there.
- references/ is read when the task needs its facts.
- playbooks/ are followed when a situation matches.
- Reading order is always top-down: GLOBAL, domain memory, category memory, box memory.

## The catalogue
CATALOG.md at the top is rebuilt every night by the server from every document's front matter and every docs/INDEX.md. Nobody edits it by hand. To find a document, search CATALOG.md first.

## Weekly tidy-up
Every Sunday Hermes reviews the tree and writes a proposal in systems/hermes/routines/docs/ (stale memories, duplicates, boxes to archive, unprocessed journal notes) and tells Leon. Nothing is archived without his yes.

## Naming rules
- Folder names: kebab-case, meaning lowercase words joined by dashes, with no accents.
- Document file names in docs/: YYYY-MM-DD-short-title.md. Fixed names such as memory.md, log.md, README.md and INDEX.md are exceptions.
- Dates are always written YYYY-MM-DD.
- Names before catalogue numbers in text.
- Never use the long dash character.

## Who maintains what
- Hermes maintains everything in this knowledge base.
- Claude Code writes journal/ notes and changes project repositories, after Leon's OK where GLOBAL.md says so.
- Leon decides, and reads.
