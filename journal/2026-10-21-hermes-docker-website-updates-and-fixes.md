# Hermes Docker — website updates on request, and two security fixes
Session note · Date: 2026-10-21 · Project: Hermes Docker · Repo: local only

## Done
- **The website now updates from GitHub, on request.**
  - How to ask: Leon asks Hermes ("put the website live") or a Claude Code session. The server installs GitHub's main branch with checks, a backup, live tests and an automatic restore.
  - FileZilla is retired.
  - First update 2026-10-21: the current website build is live (commit `162973f`, then `ea907af`). Debug is off, statistics are off, and it is still hidden from search engines (noindex on every page).
- **Website, production settings:** a new live-only settings file. Leon created the server-only secrets with one command: the Panel login key, the link salt, and the shop's sync password.
- **Fix A (Hermes isolation):** the server now owns Hermes's top-level folders, so a hijacked Hermes can't trick the server's jobs. Tested as Hermes.
- **Fix B (website):** internal notes uploaded in July (`docs/`, `CLAUDE.md`, `README.md`, `composer.json`, `server.php`) were publicly downloadable. They're removed, and the logs show no one read them in the last 7 days.

## Decided (and why)
- **Claude Code changes merge automatically, on all GitHub projects.** A manual merge added nothing for a non-coder, and Git keeps history.
- **The website changes only when Leon asks, never automatically.** Updates will be rare later, and it gives a second safety gate.
- **Pages renamed or deleted on GitHub also disappear from the live site.** Anything the live site writes itself (sign-ups, Panel edits) is never touched.
- **The site stays hidden from search engines until launch.** Anyone with the link may see it.
- **Local-only projects stay off GitHub for now.**

## Open / next steps
- **Leon to decide:** keep `llms.txt`, `sitemap.xml` and the AI-crawler rules in `robots.txt` answering before launch, or hold them back.
- **Leon to decide:** switch off password login for the website user (FileZilla isn't needed any more).
- **11d:** Hermes starts Claude Code tasks (a routine on claude.ai), plus Hermes's "put the website live" skill.
- **Website code:** the shop sync should refuse requests when no secret is set (now on its ROADMAP).
- **Design:** the 31 decisions in `design/DECISIONS-NEEDED.md`.

## Key files and docs touched
- **Lacande Website:** `site/config/config.lacanderecords.fr.php`; `docs/lacande-infrastructure-v4.md` (§5 rewritten); LOG, STATE, ROADMAP.
- **Hermes Docker:** `vps/ops/website-update`, `website-set-secrets`, `website-units.txt`, the watchdog, the mirror and the knowledge sync; NOTES.md; SETUP-LOG.md.
