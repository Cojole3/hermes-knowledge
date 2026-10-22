# Lacande Website · Note de l'éditeur, How it works, candle care
Session note · Date: 2026-10-22 · Project: Lacande Website · Repo: https://github.com/Cojole3/Lacande-Website

## Done
- Proposal page first: https://claude.ai/artifact/XAUbo8okoKqzushpHboSk6
- Built (Session 133, commit 4a1c733, local, not pushed yet). Every candle page now has a third text part, "Note de l'éditeur", after The perfume composition. Each playlist has the same note in its About card.
- Each note is signed LÉON WINDORFER in capitals in the Michroma typeface (newly installed), then the month. The name and its typeface are set in Site → Options.
- The candle page's "The label" row is now "How it works": light it, tap the label (hold your phone to the Lacande logo and open the link that appears), listen on your own streaming service.
- A new row, "Caring for your candle":
  - First burn: about three hours, until the whole surface melts.
  - After that: no more than four hours at a time, wick at 5 mm.
  - Stop at 1 cm of wax.
  - Safety line.
- Both rows are editable in Site → Options. The homepage's "Tap the label" step uses the same words.
- Each note holds one test sentence for now (four candles and Tournant Jazz).

## Decided (and why)
- Leon: the note is a part of the page, not a row that opens, because a signed text is for reading.
- Leon: the name is "Note de l'éditeur", the house's own word, chosen over "Liner notes" and "Curator's note".
- Leon: the note is in the same typeface as the parts above it (Mattone). The signature is in Michroma for now; Leon may choose another face later.
- Leon writes every note himself in Kirby. No AI-written notes.
- Music and candle care are two separate rows, because burning the candle well is its own thing to explain.

## Open / next steps
- Leon writes the notes (four candles, seven playlists) and sets each month.
- Check the care facts with the manufacturer.
- Push to GitHub and put live when Leon says so. Four ingredient commits from a parallel session are also waiting.
- If the notes are written in "I", record the first-person exception in the positioning.
- Michroma, as the signature typeface, should go into the design documents.

## Key files and docs touched
- site/snippets/candle-section.php, site/snippets/note-signature.php (new), site/snippets/music-stage.php, assets/js/music-grid.js, assets/css/base.css
- Blueprints: site, candle, playlist, music. Language strings: site/languages/en.php.
- Content: site settings, the four candles, Tournant Jazz, the homepage.
- docs/LOG.md, docs/STATE.md, docs/ROADMAP.md, CLAUDE.md
