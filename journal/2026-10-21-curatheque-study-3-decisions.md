# Curathèque — Study N° 3 and Leon's decisions
Session note · Date: 2026-10-21 · Project: Curathèque · Repo: local only (no git yet)

## Done
- Leon redirected the brief: Curathèque is a standalone music social app (people publish playlists with notes, listeners follow them), not the Lacandothèque with tenants. Nothing is read from the Kirby website.
- Six research strands ran in parallel (profiles, discovery and feeds, the item page, playlist import, data and hosting, library and the listener's pages). Official App Store screenshots of 25 apps plus mobile web captures of Spotify, Bandcamp, Substack, Medium, NTS, Letterboxd, song.link and Pitchfork were reviewed.
- Study N° 3 published: https://claude.ai/artifact/VvbAT4ikyNE9SjAoE1Fyaz (source `docs/study-3/`, with the six reports and the screenshots attached).

## Decided (and why)
- Every playlist exists in the house's own accounts on every reachable service (Spotify, Apple Music, Deezer, YouTube Music), created automatically at publish from ISRC numbers. Reason: Spotify only lets 25 people sign in to a new app and gives a playlist's tracks only to its owner, so curators cannot be asked to connect or to make copies themselves.
- Curators give a playlist by link, by pasted text, or by screenshots; one match list to confirm.
- Profile: P1 (stacked), without the bar repeating the name. Item page: a variation of I2 (square at half width, "Listen" button that asks the service once, Save with groups, note in three lines plus Read more). Feed: the cards, plus a browse-by-niche view in Discover. Addresses like Medium: /@handle/slug-id.
- Sign-in with a password first; email links later. The database is not chosen yet: plain SQL, SQLite locally, Postgres when real people arrive.
- All nine decisions are in `docs/DECISIONS.md` (C1 to C9).

## Open / next steps
- Tests before building: a Spotify single-track lookup with a plain developer key; whether an API-made Apple Music playlist can be public; Deezer's public playlist read; screenshot reading accuracy.
- Then the first local build: the wordmark page, the data layer, the publishing flow with one real import, the four pages with the chosen variants.

## Key files and docs touched
- `C:\Vibe coding\Curatheque\docs\study-3\` (index.html, refimg/, research/), `docs/DECISIONS.md`, `docs/LOG.md`.
