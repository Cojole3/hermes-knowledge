# Hermes Docker — central Lacande design document (v1 draft)
Session note · Date: 2026-10-20 · Project: Hermes Docker · Repo: local only

## Done
- Followed `briefs/lacande-design-consolidation.md`. Read the 16 Lacande design sources (website, NFC app, Render tool, Serigrafia, playlist tool, Design Atelier, LacandERP, Lettera, the old summary), plus the website's live CSS, its Panel settings and its `content-studio/foundations/`.
- Wrote four files in `design/` and pushed them (`58caa66`):
  - `LACANDE-DESIGN.md`: the central rules (type, colour, layout, pictures, print, motion, naming, do/don't, notes per surface, sources). Status: DRAFT v1, waiting for Leon's decisions.
  - `tokens.css`: the decided colours, fonts, sizes and spacing as CSS variables.
  - `templates/html-output.html`: the Lacande template for Hermes and Claude Code documents. Checked on desktop, on a true 390px phone, and with fallback fonts.
  - `DECISIONS-NEEDED.md`: 31 contradictions and gaps, each with a recommendation.
- No project repository was changed.

## Decided (and why)
- Until Leon decides, the draft follows the website's `GUIDELINES.md` and marks open points "(pending decision #n)", as the brief says.
- The template embeds no fonts: Hermes writes HTML as text, and base64 font data is error-prone. It uses Spectral and Mattone when installed, otherwise Georgia and Arial.

## Open / next steps
- Leon decides the 31 rows. The 5 most important: #1 NFC customer pages in the house look; #2 one near-black (#111); #3 social formats (square vs 4:5); #4 typefaces beyond Spectral and Mattone on boards; #5 print inks, board and fonts for matchboxes.
- Then: remove the DRAFT line (v1), turn `design/lacande-design-language.md` into a pointer, and point each project's design doc here through pull requests.
- Found along the way: the Render tool and Serigrafia design docs are copies of the NFC app's June doc; the Panel sets LC-002's typeface to Cormorant Garamond, not Basteleur; the playlist tool and Lettera are local only, so Hermes can't read them.

## Key files and docs touched
- `hermes-knowledge/design/` (the four files above)
- `Hermes Docker/SETUP-LOG.md` (log entry)
