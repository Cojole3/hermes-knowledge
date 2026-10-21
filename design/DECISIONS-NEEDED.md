# Lacande design: decisions

The questions found while writing the central design document, and Leon's answers.
**Decided: 25 of 31** (Leon, 2026-10-21). **Open: 6**, to be seen visually before a decision.
Updated: 2026-10-21

## How to use this page
- **Open questions come first.** Leon decides them by looking at the options, not by reading them.
- **To decide,** tell Hermes or a Claude Code session the number and your answer: "#10 B", "#12 as recommended", or "all as recommended except #3 and #9".
- **Until a question is decided,** [LACANDE-DESIGN.md](LACANDE-DESIGN.md) follows the website's `GUIDELINES.md` and marks the point "(pending decision #n)".
- Contrast figures are computed with the standard WCAG formula. The rule is 4.5:1 for text and 3:1 for large titles (G III).

---

## Still open (to see visually)

### #10. Reading width (the measure)
- **Option A:** 40em on reading pages (DD §4).
- **Option B:** 37em (website CLAUDE.md; DD §4 calls it an open decision). G II and DD §11 say about 73 characters a line.
- **Recommendation:** about 73 characters a line for every long read. The em value follows from the text size. Remove 37em.
- **Leon:** "It depends already on phone vs desktop, and I would need to visualise the things to take a decision."
- **Next:** a visual comparison, on a phone and on a desktop.

### #11. Phone sizes for titles and subtitles
- **Option A:** titles 29px, subtitles 16px (G II; PNL, the live site).
- **Option B:** titles 32px, subtitles 18px (DD §4).
- **Recommendation:** A (live). Update DD §4.
- **Leon:** "Is the website's design doctrine newer? But is the site using A? Again, I need to compare and understand visually."
- **Next:** check which is newer; a visual comparison of both sizes on a phone.

### #12. Labels and kickers: capitals and letter-spacing
- **Option A:** labels 14px in capitals (G II). The Panel's caption style is 14px, 0.02em, no capitals (PNL).
- **Option B:** kickers in Mattone capitals at 0.08em (PL §2; CS rules.md). The internal tools use heavy capitals at 0.2 to 0.3em (NFC 1.3).
- **Recommendation:** one rule for public surfaces: labels and kickers in Mattone capitals, 0.08em, 14px (phones 13px). Captions that are sentences stay in sentence case at 0.02em. Internal tools keep theirs (#18).
- **Leon:** "I need to really understand what the scope of this change is, what messages are meant, and then visualise."
- **Next:** list the messages that use labels and kickers, and show them before and after.

### #15. Line weight on boards
- **Option A:** one weight: 2px on screen, about 1pt in print (G IV).
- **Option B:** 4px on 1080px boards, 2px between the rows of a list (PL §4; CS rules.md).
- **Recommendation:** B, written as "2px as the reader sees it": a 1080px board is shown much smaller on a phone, so 4px there reads like the site's 2px.
- **Leon:** "I need to check visually."
- **Next:** one board at 1080px and on a phone, with 2px and 4px lines.

### #20. Motion on the NFC pages
- **Option A:** a closed list: rotation, drift, flood (about 200 ms), cross-fade, and the moving crop. No scroll-snap, no full-screen (100dvh) panels (DD §9; WDS §6).
- **Option B:** the "Nudge" (a pulse, wobble or peek after 3 to 30 s), flip cards, slideshows that move on by themselves, one-screen pages at 100dvh (NFC 2.3, 2.11).
- **Recommendation:** for Lacande's presets, no pulse and no wobble; a peek at most. Flip cards and slideshows are fine (a turn and a cross-fade). The one-screen page serves the tap moment and stays.
- **Leon:** "It depends a lot on how it will look. The NFC page uses a sort of template system: a top part that shows the design and a bottom part to choose the music provider, so not much to move. We could try and see how it looks if, instead of the square at the top, we just have the turning record (a bit like before in the playlist part of the website)."
- **Next:** a mock-up of the NFC page with the turning record at the top.

### #21. The voice for music
- **Option A:** say what it is, plainly: facts, sources instead of qualities; "warm" is on the avoid list (G VII; POS §7.2).
- **Option B:** "A radio host who knows the records. Warm, specific, names artists and songs, says when to play it" (PL §8; CS rules.md).
- **Recommendation:** B, without the word "warm".
- **Leon:** neither. "It should feel more like a curator, a sort of professor explaining something, but without being boring. It's more context dependent." He judged "Put it on after dinner, while the table is still full." bad.
- **Direction now in the document** (§1): a curator explaining, not boring, depends on context.
- **Next:** new example sentences, to validate with Leon.

---

## Decided (25)

| # | Topic | Decision | Leon's note (2026-10-21) |
|---|---|---|---|
| 1 | NFC pages a customer sees | **A**: the house look | Any change to the NFC page is first proposed visually and validated by Leon. It should carry the Lacande look. |
| 2 | One near-black | **A**: `#111` everywhere | Internal tools included. `#1A1A1A` stays only as the name of the riso black ink. |
| 3 | Social post shapes | **Changed from the recommendation**: 4:5 is the default for all Instagram posts, playlist boards included; square as an option | "The standard insta post is 4/5, so focus firstly on this, with the option for square." |
| 4 | Typefaces beyond Spectral and Mattone | **Recommendation**: named exceptions | Spectral and Mattone by default. Exceptions allowed, for example playlists, and the scent cards with their own design. |
| 5 | Print: inks, board and type | **Recommendation** (B: house rules, three steps) | More freedom for typefaces in print. The guidelines are a fallback; what matters is that it looks homogeneous. Few inks and riso are a Lacande trademark. |
| 6 | LC-002 typeface | **B**: Cormorant Garamond (the Panel's value stays) | Follow-up: the website's `GUIDELINES.md` and `CLAUDE.md` still say Basteleur. |
| 7 | Hover colour on candle pages | **Recommendation** (B: each candle's own ink) | none |
| 8 | LC-003 Isola Paradiso ink | **A**: keep `#F54317` (3.0:1) | Leon's choice. Noted in one line: below 4.5:1, so it suits titles and lines better than long text. |
| 9 | Long-read text size | **Recommendation** (B: 20px, phones 17px) | none (live setting; the website's CLAUDE.md agrees) |
| 13 | House paper | **Recommendation**: white for screens and documents; cream `#FFF9ED` for boards and riso pictures; label white `#F7F5F0` for labels and the Matchbox Archive | none |
| 14 | Two colour pairs per candle | **Recommendation**: keep both, as two kinds | "The website colours and candle label colours optimise for different things and thus are different." |
| 16 | Matchbox Archive colours | **Recommendation**: added to G III, `#F7F5F0` with Select red | none |
| 17 | Grey for secondary text | **A**: `#6B6B6B` everywhere | none |
| 18 | Internal tools look | **A**: keep their own practical look | Before any change to harmonise their design, Leon must see and approve it. "The main aim of tools is always clarity and ease of use, and then only to be coherent with our design." |
| 19 | Render tool and Serigrafia docs | **Recommendation**: replace with a pointer and Serigrafia's plate rules, through pull requests | A later step, not now. |
| 22 | Em dashes | **A**: never, in public texts and internal documents | none |
| 23 | Lettera's voice | **Recommendation**, low priority | Lettera is on hold. |
| 24 | Label line | **A**: "Tap for music" | Not design-guideline material. Kept out of the document, except one line. |
| 25 | LC-001 name | **A**: Jazz Impressions, one name everywhere | Tournant Jazz was the old name. The name is the main identifier; the catalogue number is secondary, only for cataloguing, and not emphasised. |
| 26 | Playlist numbers | **A**: `CP-`, with the nuance below | A playlist with a candle is that candle's édition and carries its LC number. Never a CP and an LC number for the same thing. A playlist without perfume that later gets one is promoted to LC, and its CP number is retired. So the four candle playlists carry LC numbers. Other early playlists: CP in issue order, excluding the candle playlists. |
| 27 | Logos | **B**: the NFC app's four names: Short, Extended, Logo + picto, Picto | Colours are not strict: ink, paper or accent, depending on the situation. Which logo is used depends on the situation. The old names map as wordmark = Short, lockup = Extended, picto = Picto (to confirm). |
| 28 | Cart and checkout typeface | **A**: one typeface | The July brief names no face, so it is written as "one typeface (Mattone) (to confirm)". |
| 29 | Three kinds of picture (plein, planche, signe) | **Removed** from the document | "Remove this, I can't wrap my head around it; I will add it back if needed." |
| 30 | Dark mode for documents | **A**: documents light only | B stays for the playlist tool's own screens. |
| 31 | Type in documents | **A** for reports, briefs, dashboards and tables; **B** for essays | Plus: Spectral Medium (500) for document titles, with SemiBold (600) as the alternative to compare. Applied in `tokens.css` and the template. |

Each decided row's full options (A and B with their sources) are in the git history of this file, before the commit of 2026-10-21.
