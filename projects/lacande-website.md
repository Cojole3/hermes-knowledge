# Lacande Website

The public editorial website and future shop of Lacande, at lacanderecords.fr. **Top priority.**
Updated: 2026-10-20

## What it is
**Pages:**
- homepage and candle catalogue, with a page per candle;
- Matchbox Archive (`/allumettes`);
- Music and playlist pages;
- Journal;
- "Lacande wing" pages about the house;
- cart and checkout (placeholders for now).

**Also:** a library of 194 ingredient "scent cards" and a content studio for social media templates.

## Status
- **Live but outdated:** the domain shows an **old build** (from about session 9) with **noindex** on.
- **Local work is far ahead:** session 129 on 20 Oct 2026.
- **Launch gate**, everything that must happen before launch:
  - deploy the current build;
  - ~~update Kirby on the server~~ (done 2026-10-20, Kirby 5.6.1);
  - write real candle copy and prices;
  - connect the newsletter;
  - point analytics at a public ERP address;
  - buy the Kirby licence;
  - remove noindex.

## Security note
**Fixed 2026-10-20:** Kirby on the live server went from 5.5.2 to **5.6.1** (security release; repo and server verified identical). The live site is still an old design build, but the CMS is patched. Also new: `tools/snapshot` (offline copy of the site as a zip) and an updated server doc (`docs/lacande-infrastructure-v4.md`) covering the hardened server.

## How it's built and deployed
- **Stack:** Kirby CMS (flat files, PHP, no database).
- **Hosting:** the OVH VPS in Strasbourg, with CloudPanel, nginx and Varnish.
- **Deploy:** by hand, over SFTP with FileZilla. A Git- or rsync-based deploy is planned.
- **Important:** the nginx security rules live **only on the server** (CloudPanel vhost). A copy is saved in the Hermes setup project.

## Connections
- **To LacandERP:** sends an anonymous analytics beacon (off in production for now) and matchbox stock data.
- **Shared numbers:** uses the same catalogue numbers as the NFC app.
- **Design guidelines:** apply to every Lacande surface.
- **Playlist atelier:** reads genres, fonts and the riso tools from this site.

## Where things are
- **Repo:** https://github.com/Cojole3/Lacande-Website (private)
- **Local:** `C:\Vibe coding\Lacande Website`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/STATE.md`
  - `docs/ROADMAP.md` (the launch gate is at the top)
  - `docs/lacande-infrastructure-v4.md`
  - `docs/GUIDELINES.md`
  - `docs/for Leon/lacande-positioning.md`
  - `docs/LOG.md`

## Open questions
- Launch date.
- Which deploy method replaces FileZilla.
- When the ERP gets its public address (`erp.lacanderecords.fr`).
