# Render tool (`lacande-render`)

Internal Lacande tool for 3D renders of the candles, boxes and matchbox, and for printer-ready curved label templates.
Updated: 2026-10-20

## What it is
- **Stage 1, browser app:**
  - pick a glass, place the label artwork, and view it in 3D;
  - export a transparent PNG, plus the correct curved label template for tapered glasses, to send to the printer.
- **Stage 2, Blender:** photorealistic stills and turntable videos.
- **"Turntable hero":** a candle staged in front of a record turntable.

## Status
**Active** (session 10, 15 Oct 2026).
- **First finished picture:** the Jazz Impressions homepage image, 3200×1800.
- **Done:** sessions 1–7 and 9.
- **Open:**
  - session 8 (props and pairs);
  - session 10 (props and décor): the proposal is waiting for Leon's answers (OPEN-019), and "Shoot 01 – listening room" is in progress.
- **Next:**
  - a way to add downloaded props, and a catalogue browser;
  - lighting described in photographer's terms;
  - still-life arrangements;
  - table and wall décor;
  - shoot tools.

## How it's built
Vite and TypeScript, with three.js, zod, pdf-lib and Vitest. Blender 4.5 LTS and ffmpeg live in `tools/`. Local only, with no backend.

## Connections
- **Saved projects:** candle-3, candle-box-4, the Arles matchbox, sonata-v1/v2 and jazz-impressions-v2.
- **Playlist atelier:** plans to put disc artwork on the turntable's record label.
- **Lacande website:** its images are used there.

## Where things are
- **Repo:** https://github.com/Cojole3/Render-tool
- **Local:** `C:\Vibe coding\Render tool`
- **Key docs:**
  - `CLAUDE.md`
  - `STATE.md`
  - `ROADMAP.md`
  - `LOG.md`
  - `DECISIONS.md`
  - `docs/BLENDER.md`
  - `docs/DESIGN_SYSTEM.md`
