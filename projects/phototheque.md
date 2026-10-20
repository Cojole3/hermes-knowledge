# Photothèque

Leon's personal visual archive of photos, videos, screenshots and scans. Each item is automatically understood on import, then reviewed and explored.
Updated: 2026-10-20

## What it is
**On import, for each item:**
- reads the EXIF data;
- finds the place from GPS, offline;
- makes a CLIP visual fingerprint;
- runs AI passes: Haiku on every image, Sonnet only on selected ones. These judge whether a shot is a keeper and suggest labels, descriptions and a mood line.

**Areas:** Explore, Collections, Upload, Review (works on a phone) and Labels. The look is meant to feel like a printed catalogue.

## Status
- **Working and actively patched:** the latest is patch 29, last commit 8 Oct 2026.
- **Size:** about 4,300 images.
- **Uncommitted changes** to the upload flow.
- **Cloud migration:** documented but not started (see `MIGRATION.md`).

## How it's built
- **Server:** Express and TypeScript with SQLite, sharp, onnxruntime (CLIP), ffmpeg and the Anthropic SDK.
- **Client:** React/Vite.
- **Runs:** locally on port 3000.

## Connections
- **Lettera:** has an image search API (`GET /api/images/search`) built for it.
- **Playlist atelier:** searches it for pictures.
- **Design Atelier:** a read-only link to its database is planned.
- **Serigrafia:** names it as a photo source.

## Where things are
- **Repo:** https://github.com/Cojole3/Phototheque
- **Local:** `C:\Vibe coding\Phototheque`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/Phototheque Description.md`
  - `docs/PHOTOTHEQUE_BUILD_PROMPT.md`
  - `MIGRATION.md`
  - `docs/Patches/`
  - `docs/Phases/`

## Open questions
When and how to move it to the cloud. Photos are large, and they're private.
