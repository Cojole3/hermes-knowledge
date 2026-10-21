# Curathèque — the first build
Session note · Date: 2026-10-21 · Project: Curathèque · Repo: local only (no git yet)

## Done
- Curathèque now runs as a standalone app on port 3400: a music platform where listeners follow people. Nothing is read from the Lacande website any more; Lacande is one curator among others and its sleeves are uploads.
- Built in one session: the wordmark page (five faces for CURATHÈQUE, at `/wordmark`); the database (SQLite built into Node, no server) with the seed (Lacande plus three invented curators, 15 entries, the House list of 31 niches, the six moments); every page of Study N° 3 with Leon's chosen variants: Discover (the feed as cards, the five doors, the niches), a niche page, the profile (stacked, in the curator's colours), the entry page (square at half width, Listen that asks the service once, Save with groups, the note in three lines, the tracklist), Search, Library (saved, groups, objects), You, Settings, About; accounts with passwords; the curator's publishing desk with the three import doors (a link, pasted text, screenshots), matching by ISRC on Spotify, Apple Music, Deezer and YouTube, and the house's copies in the house's accounts.
- Verified: type-check clean, every route answers, the listener's and the curator's flows walked with a cookie jar, 24 screenshots looked at. A quick audit fixed two open redirects, an upload without a ceiling and a per-request scan of all people.

## Decided (and why)
- Build decisions B1 to B9 in `docs/DECISIONS.md`: SQLite through `node:sqlite` (no dependency); passwords with scrypt, sessions in a cookie; the listener's library on the server under a device key, merged into the person at sign-in; forms that work without JavaScript; uploads re-encoded on the server; the mark's candidate faces from Google Fonts; screenshots read through the Claude API; Deezer and Tidal marked unverified; a development-only route for screenshots.

## Open / next steps
- Leon picks the wordmark face and looks at the pages on a phone.
- Keys for Spotify, YouTube, Deezer and Apple, then the live tests: a Spotify track lookup returns the ISRC; YouTube's and Deezer's public playlist reads; the house's OAuth connections and copies; Apple's public visibility of an API-made playlist; screenshot reading.
- Later: a sign-in link by email, rate limiting on sign-in, Lacande's real links per service, the notes rewritten by Leon, git init.

## Key files and docs touched
- `C:\Vibe coding\Curatheque\server\src\*` (new), `public/app.css`, `public/app.js`, `data/seed/*`, `docs/wordmark/`, `docs/shots/`, `CLAUDE.md`, `README.md`, `.env.example`, `docs/STATE.md` (rewritten), `docs/DECISIONS.md` and `docs/LOG.md` (appended).
