# Design generation tools (Lacande Design Atelier and small generators)

Tools that generate Lacande design variants, plus two small one-page generators.
Updated: 2026-10-20

## Lacande Design Atelier
**What it is:** generates nine design variants at a time and shows them on a labelled contact sheet. It then narrows down toward what Leon picks, e.g. "02 and 07", or "04 but less busy".
- **Generators:** matchbox and poster.
- **Formats:** 50×35 matchbox, A3 poster, 1080×1350 Instagram portrait.

**Status:**
- Phases 1–8 are done (12 Aug 2026).
- Phase 9, an automated critic, hasn't started.
- Phase 1 is still waiting for Leon to look at `work/matchbox_run01.png`.
- Open questions:
  - font files: `assets/fonts` is empty;
  - named inks;
  - printer and paper stock;
  - the exact matchbox die-line.

**How it's built:** Python 3.11 (resvg-py, fonttools), with a SQLite history of every run. Runs locally from the command line, plus a local window.

**Where:**
- **Repo:** https://github.com/Cojole3/Lacande-Design-Atelier
- **Local:** `C:\Vibe coding\1. Design generation tools\Lacande Design Atelier`
- **Key docs:**
  - `CLAUDE.md`
  - `ROADMAP.md`
  - `DECISIONS.md`
  - `docs/how-it-works.md`
  - `docs/print-brief.md`
  - `docs/handoff-next-session.md`

## Small generators (no docs, no Git)
- **Jazz-Type Studio:** generates mid-century jazz album covers in the style of Reid Miles and Blue Note. Inferred to be for Lacande's jazz playlists.
- **Riso filter:** an early one-page risograph filter. Inferred to be replaced by Serigrafia's lab and the website's riso tools.

## Connections
- **Serigrafia and the Render tool:** they share the matchbox work.
- **Photothèque:** a read-only link is planned.
