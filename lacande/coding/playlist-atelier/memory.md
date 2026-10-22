# Playlist atelier ("Spotify playlist tool", `lacande-playlists`)

Makes Lacande's numbered, curated playlists, which are paired with candles or published as hors-série.
Updated: 2026-10-20

## What it is
- **Library:** a local copy of Leon's 110 Spotify playlists, sorted into families.
- **Track facts:** from Deezer, MusicBrainz and AcousticBrainz.
- **Proposals:** documents that turn a draft into a publishable playlist: track selection, name, story, riso-printed boards, sleeve and scent.
- **Division of work:** Leon looks and points in the web app; the creative work happens in Claude Code sessions.

## Status
- **Working,** started 15 Oct 2026.
- **First release:** **CP-007 Calypso Blues**, on 16 Oct 2026.
- **Leon still has to:** put Calypso Blues' cover and description on Spotify, and add it to the NFC app.
- **Next:**
  - a release board in the app;
  - fetching facts for the whole library;
  - Leon's verdicts on the open proposals;
  - export to the website;
  - hand-off sheets for the NFC app and the ERP.
- **Open decisions:** whether playlist numbers use PL- or CP-, and whether the tool may ever write to Spotify (today it only reads).

## How it's built
Node 24, TypeScript, Express, and React/Vite. Runs locally on port 3200. Data is stored in JSON files, with no database.

## Connections
- **Lacande Website:** reads genres, fonts and the riso tools from it.
- **Links to:** Photothèque, Serigrafia, Lettera, Corpus, the NFC Candle app, LacandERP and the Render tool.

## Where things are
- **Repo:** none yet; Git is local only. **Leon plans to push it to GitHub** (20 Oct 2026). After that, Hermes can read it.
- **Local:** `C:\Vibe coding\Spotify playlist tool`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/STATE.md`
  - `docs/ROADMAP.md`
  - `docs/DECISIONS.md`
  - `docs/DESIGN-GUIDE.md`
  - `docs/PROPOSAL-SPEC.md`
  - `docs/RELEASE.md`
