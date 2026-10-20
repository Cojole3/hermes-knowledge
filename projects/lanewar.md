# LANEWAR (working title, folder "Video game")

A desktop-first, real-time lane-strategy wargame where doctrine wins rather than unit stats.
Updated: 2026-10-20

## What it is
- **Board:** 5 lanes × 32 columns.
- **Players:** two, sharing an 18-unit roster from the pike-and-shot era. No magic, no upgrades.
- **Actions:** only four: Spawn, Release, Stance, Eco.
- **Graphics:** deliberately minimal in version 1.
- **Planned tools:**
  - a "Battle Lab" for AI-vs-AI balancing;
  - a sandbox map editor.

## Status
**Design and spec stage only:** two Markdown files and no code yet (16 Jul 2026). Planned build order: phase 0 (skeleton simulation) through phase 6 (multiplayer).

⚠️ **Leon doesn't remember this project** (20 Oct 2026). The file name `CLAUDE (1).md` suggests it was downloaded, probably from a chat. **Open question:** keep or archive?

## Planned build
TypeScript in a pnpm monorepo (sim, bots, lab, client), with Vitest, Vite and PixiJS. The simulation is deterministic and runs without graphics. Multiplayer over WebSockets comes much later.

## Where things are
- **Repo:** none.
- **Local:** `C:\Vibe coding\Video game`
- **Key docs:**
  - `DESIGN.md` (the rules; single source of truth)
  - `CLAUDE (1).md` (build instructions)
