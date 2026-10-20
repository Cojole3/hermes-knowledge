# Lacande Lettera

Leon's tool for writing Lacande social media posts with Claude.
Updated: 2026-10-20

## What it is
- **Bench:** a cheap chat for thinking ideas through.
- **Drafting table:** picks an idea and writes the copy first, then imagines the ideal images. It searches the Photothèque for them: each image comes back as have it, close, or missing. Missing images become a shot list.
- **Archive:** saves each final post with Leon's 1–5 rating and his edits. These feed future drafts as examples.
- **Ratings stay separate** from Instagram/Meta engagement data, on purpose.

## Status
- **Built:** phases 1–5, from 8 to 10 June 2026, including a carousel format and a hook-first flow.
- **Paused:** no work documented after 10 June.
- **Placeholders:** `VOICE.md` (the brand voice) is still a placeholder, and the look is a placeholder to be replaced by Lacande branding.

## How it's built
Node, Express, TypeScript, React/Vite and SQLite, using the Anthropic API. Runs locally, built so it can move to the cloud later.

## Connections
- **Photothèque:** uses it for images (connected).
- **Corpus:** designed to take ideas from it and export the archive to it. Not built yet.
- **Claude Design:** produces a design brief for it.

## Where things are
- **Repo:** none; Git is local only, so Hermes can't see it yet.
- **Local:** `C:\Vibe coding\Lacande Lettera`
- **Key docs:**
  - `CLAUDE.md`
  - `MIGRATION.md`
  - `docs/AUDIT.md`
  - `docs/VOICE.md`
  - `docs/CONVENTIONS.md`
