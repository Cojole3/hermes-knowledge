---
processed: 2026-10-24
---
# Lacande Website · Playlist names in Mattone
Session note · Date: 2026-10-23 · Project: Lacande Website · Repo: https://github.com/Cojole3/Lacande-Website

## Done
- On the website's Music page, the playlist names are now set in Mattone (the house typeface, regular weight) in all three places they appear: under the record sleeves, on the back of the sleeve (the tracklist) and as the title of the About card.
- Before, each name used its candle's own display typeface (for example Tournant Jazz in Bauhaus 93, Nuit d'Amour in Federo - Amour).
- Checked in a browser on a phone size and a desktop size, before and after switching playlists: Mattone everywhere, nothing broken.
- Also fixed: clicking a record sleeve turns it over to show the tracklist, but clicking again did nothing. Now a click (or a tap on a phone) on the tracklist turns it back to the cover, as often as you like. Scrolling the tracklist or selecting a song title does not turn it (Session 134.1).
- Also fixed: with the sleeve turned over, the mouse wheel did not scroll the tracklist; the page moved or the sleeves slid sideways. Now the wheel anywhere on the turned sleeve scrolls the tracklist, and the sleeves stay put until the cover is back (Session 134.2). Phones were already fine.
- Committed in the website repo (Sessions 134 to 134.2), not yet put live on lacanderecords.fr.

## Decided (and why)
- Leon prefers the playlist titles in the plain Mattone typeface. Each candle's own typeface is kept for the candle page only.
- A typeface chosen in the Panel (Music page, Typography tab) for those names still takes priority; left empty, it is Mattone.
- Candle names on the homepage (the first picture's caption, the candle tiles) keep their own typeface, since they name candles, not playlists.

## Open / next steps
- Goes live with the next server update.
- Check the tracklist scrolling once on Leon's iPhone (Safari could not be tested on the PC).

## Key files and docs touched
- site/snippets/music-stage.php, assets/js/music-grid.js, site/models/playlist.php, site/blueprints/pages/music.yml
- docs/LOG.md, docs/STATE.md, docs/ROADMAP.md
