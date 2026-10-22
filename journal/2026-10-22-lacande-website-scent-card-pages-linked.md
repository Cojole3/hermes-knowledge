# Lacande Website: the two scent card pages now link to each other
Session note · Date: 2026-10-22 · Project: Lacande Website · Session 131 · Repo: Cojole3/lacande-website (commit 2738578)

## Done
- Reopened the page with all the olfactory notes for Leon: the Lacande Ingredient Library, 194 smells as cards.
- Explained the two pages that show those same 194 cards, by Jean-Claude Ellena's families, front and back:
  - **Ingredient Library** (https://claude.ai/artifact/Y7yYsF5TqWdY7un1bLMDjU): the working reference. Filters (natural, accord, synthetic, Jazz Impressions), search by English, French or botanical name, a switch between fronts and backs, and each card opens on its names, its two Olivetti inks, its description and the photo credit. Ends with "How the list was made".
  - **Scent Cards** (https://claude.ai/artifact/P8KX2Vc5YxnmS2sZu5A5Tx): the version made to send. Built for a phone, a tap turns a card over, two or one a row, "turn all over". Also exists as a single file (about 13 MB) for WhatsApp, AirDrop or mail.
- Both read the same data, the ingredient library in the Kirby Panel, so their content never disagrees.
- Added a link between them, in the accent red, at the top of each page: "The scent cards →" on the library, "The full library →" on the scent cards. Both live pages were updated, and the scripts that rebuild them now write the link too.

## Decided (and why)
- Linked, not merged: the page to send must work without scripts (phones often preview attachments without them), while the library needs scripts for its search and filters.
- The single file to send carries no link to the library, because the people it goes to cannot open the private library page.

## Open / next steps
- Both pages are private. Anyone the scent cards are shared with also needs the library shared for the link to work.

## Key files and docs touched
- tools/ingredients/batch/page.mjs (builds the library page), tools/ingredients/share.mjs (builds the scent cards), tools/ingredients/README.md
- docs/LOG.md (Session 131), docs/STATE.md
