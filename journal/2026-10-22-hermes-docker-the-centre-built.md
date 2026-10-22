# Hermes Docker: the centre built, stages 0 to 3
Session note · Date: 2026-10-22 · Project: Hermes Docker · Repo: local only (the centre: C:\Vibe coding\hermes-centre, GitHub repo to create)

## Done
- The knowledge base is now a tree (stage 0): GLOBAL.md, CONVENTIONS.md, about-leon.md, journal/ as inbox; domains, categories, boxes, each with memory.md, log.md, docs/. Every old page moved with its history. Hermes switched over; it reads GLOBAL.md and writes task files.
- Additions: the Curathèque box, the coding playbook, a nightly catalogue (CATALOG.md), a weekly tidy-up job (Sundays), Hermes writes what it learns about Leon into about-leon.md, every memory correction gets a log line.
- Hermes may write in its workspace again (a container setting, Leon's explicit OK).
- The centre (stages 1 to 3): a small Python web app in its own container next to Hermes, VPN only, same login as the dashboard; reads the knowledge base read-only; tasks are files in their box written by Hermes (skill centre-task); each task's conversation is a Hermes session through Hermes's official API; a Documents inbox that opens a filing task in Lacande › Admin. The page: Home (Dashboard, Needs you, Documents, Workers, Activity), Tasks (New task, Active, Recurring), The tree (Global, domains, boxes).

## Decided (and why)
- No second database: the knowledge base and Hermes's sessions hold everything; the centre only reads and relays.
- Only Leon closes a task; closing triggers the housekeeping.
- Hermes files tasks; it asks when unsure.

## Open / next steps
- Leon runs hermes-set-centre-key, then tests with TESTING-THE-CENTRE.md.
- Create the GitHub repo hermes-centre; then centre-update --mirror deploys from it.
- The Admin workflow (Dropbox, the ERP) to design; the phone layout; the Claude export import.

## Key files and docs touched
- hermes-knowledge: the whole tree; GLOBAL.md; CONVENTIONS.md.
- hermes-centre: backend/app.py, static/index.html, Dockerfile, CONTRACT.md, README.md.
- Hermes Docker: vps/docker-compose.yml, vps/ops/centre-update, hermes-catalog, the watchdog, SOUL.md, hermes-skills/centre-task; NOTES.md; SETUP-LOG.md; TESTING-THE-CENTRE.md.
