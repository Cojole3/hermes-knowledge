# Lacande Website · Playlist names in Mattone
Session note · Date: 2026-10-23 · Project: Lacande Website · Repo: https://github.com/Cojole3/Lacande-Website

## Done
- On the website's Music page, the playlist names are now set in Mattone (the house typeface, regular weight) in all three places they appear: under the record sleeves, on the back of the sleeve (the tracklist) and as the title of the About card.
- Before, each name used its candle's own display typeface (for example Tournant Jazz in Bauhaus 93, Nuit d'Amour in Federo - Amour).
- Checked in a browser on a phone size and a desktop size, before and after switching playlists: Mattone everywhere, nothing broken.
- Committed in the website repo (Session 134), not yet put live on lacanderecords.fr.

## Decided (and why)
- Leon prefers the playlist titles in the plain Mattone typeface. Each candle's own typeface is kept for the candle page only.
- A typeface chosen in the Panel (Music page, Typography tab) for those names still takes priority; left empty, it is Mattone.
- Candle names on the homepage (the first picture's caption, the candle tiles) keep their own typeface, since they name candles, not playlists.

## Open / next steps
- Goes live with the next server update.

## Key files and docs touched
- site/snippets/music-stage.php, assets/js/music-grid.js, site/models/playlist.php, site/blueprints/pages/music.yml
- docs/LOG.md, docs/STATE.md, docs/ROADMAP.md
