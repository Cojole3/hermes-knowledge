# Lacande Website

The public editorial website and future shop of Lacande, at lacanderecords.fr. **Top priority.**
Updated: 2026-10-24

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
- **Live build:** `main` up to c0032d5 (2026-10-23); later Music page commits wait for the next update. Base since 2026-10-21: 162973f, installed by the server's update from GitHub. Debug off, analytics off, **noindex on** every page, secrets set (source: repo `docs/STATE.md`, checked 2026-10-22).
- **Launch gate**, everything that must happen before launch:
  - ~~deploy the current build~~ (done 2026-10-21);
  - ~~update Kirby on the server~~ (done 2026-10-20, Kirby 5.6.1);
  - write real candle copy and prices;
  - connect the newsletter;
  - point analytics at a public ERP address;
  - buy the Kirby licence;
  - remove noindex.

## Latest (2026-10-23)
- **PHP2Shell patched** (server session, e24c1d7): all ten PHP versions updated (site on 8.3.36), no sign of attack or compromise in 7 days of logs; backups first. Exploited in the wild since 17 Oct.
- **Pushed, partly live:** the 9 local commits (Sessions 131 to 134, incl. Note de l'éditeur) are on GitHub. The server update put c0032d5 live: the Jazz Impressions perfume text edited in the Panel on 22 Oct, merged into Git so it is not lost.
- **Music page** (Sessions 134 to 134.2, pushed, not yet live): playlist names in Mattone (candle typeface kept for the candle page; a Panel choice still wins); a click on the turned sleeve flips it back; the wheel over it scrolls the tracklist.
- **Access documented** (infrastructure doc 2.1): the key file is the only door; Hermes has no server access by design; SFTP retired.

## Latest (2026-10-22)
- **Phone work live** (commit 871bbd5, docs ceb50c0, Session 130): first frame one shape on every phone with the line at the fold; éditions and catalogue two a row; Candles intro clamped to three lines with "More +"; menu smaller with the record centred; crumb at 18 px; candle's Next line small under the picto.
- **Note de l'éditeur** (Session 133, commit 4a1c733, local, not pushed): third text part on every candle page and playlist, signed in Michroma; "How it works" and "Caring for your candle" rows, editable in Site > Options. Leon writes every note himself.
- **Scent cards** (Sessions 131, 132): Ingredient Library and Scent Cards pages link to each other; the 194 card backs proofread (1 wrong fact, 45 unproven, 114 new texts proposed) on the page "Scent Card Proof".
- Server docs (2026-10-21): password login off for every account; crawl files held back while noindex is on.

## Next steps
- Leon writes the Notes de l'éditeur (four candles, seven playlists) and sets the months.
- Leon answers five scent questions (rose, black olive, oak and rockrose in Jazz Impressions, myrrh and opoponax) and the "isolate" kind; then the choices are applied in the Panel.
- Check the candle-care facts with the manufacturer.
- Put the pushed work live (Sessions 131 to 134) when Leon asks.
- Check the tracklist scrolling on Leon's iPhone (Safari not testable on the PC).
- Consider disabling CloudPanel's FTP service (firewalled but listening).
- Record Michroma in the design documents; record the first-person exception if notes use "I".
- Remaining mobile proposals: menu foot, cart button, playlist link row.

## Earlier (2026-10-20 evening)
- Commit 162973f: production settings file for the live host (debug off, analytics off, noindex on). Secrets live only on the server (gitignored).
- Prepared updates where the server pulls from GitHub. Adopted 2026-10-21: FileZilla retired.

## Security note
**Fixed 2026-10-20:** Kirby on the live server went from 5.5.2 to **5.6.1** (security release; repo and server verified identical). Since 2026-10-21 the live site also runs the current build. Repo notes say debug was probably on in production until that update. Also new: `tools/snapshot` (offline copy of the site as a zip) and an updated server doc (`docs/lacande-infrastructure-v4.md`) covering the hardened server.

## How it's built and deployed
- **Stack:** Kirby CMS (flat files, PHP, no database).
- **Hosting:** the OVH VPS in Strasbourg, with CloudPanel, nginx and Varnish.
- **Deploy:** the server pulls from GitHub (`website-update`), only when Leon asks (skill `website-live`). FileZilla retired 2026-10-21.
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

## Decisions
- Playlist titles in plain Mattone; each candle's own typeface for the candle page only (2026-10-23).
- Content rule: local is authoritative; a Panel edit is merged into Git before the next update (`website-update --accept-live`).

## Open questions
- Launch date.
- When the ERP gets its public address (`erp.lacanderecords.fr`).
