# Lacande Website: the backs of the 194 scent cards, proofread
Session note · Date: 2026-10-22 · Project: Lacande Website · Session 132 · Repo: Cojole3/lacande-website (commit 830fc8f)

## Done
- Every text on the back of the 194 scent cards (written by AI, never reviewed) was checked claim by claim against sources: Kew, IFRA, the perfume makers' own pages, papers, Wikipedia.
- Found: 1 wrong fact (rose oil's main molecules) and 45 unproven ones, mostly legends told as history (Hungary water, the princess of Nerola) and dates or figures nobody can trace.
- Proposed 114 new texts; 80 cards stay as they are. Every accord now says why it is an accord (no extract, too costly, banned by IFRA, taken from an animal).
- Built the page Scent Card Proof (https://claude.ai/artifact/VUzoegxKCDYNaJLnJQ36dJ): wrong and unproven facts first, then the kinds, then every card with today's text beside the new one. Leon picks keep, new text or his own; his choices are saved on the page.

## Decided (and why)
- Writing rule for the backs (Leon): hyphens in compound words are fine (hay-like); only a dash used as punctuation is out. Up to about 280 characters. An accord must explain itself.
- "Synthetic" means made by chemistry (Leon). 42 of the 43 synthetic cards are indeed made that way; only limonene is taken from orange peel. Proposed: a fourth kind, "isolate". Leon decides.
- Rose is described as rose oil, not an accord, until Leon checks what the candle uses.

## Open / next steps
- Leon chooses on the page and answers five questions: rose, black olive, oak and rockrose in Jazz Impressions (oil, absolute or accord?), and where myrrh and opoponax belong.
- Then apply his choices in the Panel, fix three Wikidata links (muscone, Tolu balsam, rockrose) and redraw the cards.

## Key files and docs touched
- tools/ingredients/seeds/backs-proof.json (the full review), content-studio/templates/scent-card.md and site/blueprints/pages/ingredient.yml (the writing rule)
- docs/LOG.md (Session 132), docs/STATE.md, docs/ROADMAP.md
