# Serigrafia

A graphic-design tool built on templates, with a print-simulation lab (riso, CMYK) that exports printer-ready files.
Updated: 2026-10-20

## What it is
**Template Studio:**
- reproduces premade layouts with photos, text, filters and grain;
- the original brief was the Jobim *Wave* album cover;
- can draft a template from a reference image using Claude.

**Image Treatment Lab:**
- WebGL simulation of riso inks and CMYK halftones;
- RAW file support and Pantone books;
- exports print plates and PDF/X files for printers.

## Status
- **Active:** 136 recorded decisions. Last commit 6 Oct 2026, plus uncommitted work from 8 Oct (a duotone curve per ink).
- **Image Lab gaps:** undo, more than two pictures per page, 16-bit RAW.
- **Next:** saved presets, splitting templates from outputs, hosting.

## How it's built
React 18, Vite 6 and TypeScript, with Konva, Zustand, Dexie/IndexedDB, pdf-lib/jsPDF, libraw-wasm and the Anthropic SDK. Runs locally in the browser, and is designed to be hosted later.

## Connections
- **Lacande design system:** the app uses it, and 4 brand marks are pre-loaded in its logo library.
- **First real print job:** a Lacande matchbox, model BX-L50, offset-printed at a carton printer using the printer's die-line.
- **Playlist atelier:** its riso scripts borrow Serigrafia's image libraries.
- **Photothèque:** a photo source.

## Where things are
- **Repo:** https://github.com/Cojole3/Serigrafia
- **Local:** `C:\Vibe coding\Serigrafia`
- **Key docs:**
  - `README.md`
  - `CLAUDE.md`
  - `docs/00-overview.md`
  - `docs/10-roadmap.md`
  - `docs/07-decision-log.md`
  - `docs/15-print-production-roadmap.md`
  - `docs/Serigrafia Description.md`
