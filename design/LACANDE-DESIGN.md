Status: DRAFT v1, waiting for Leon's decisions

# Lacande design

The central design document for everything Lacande makes: the website, the NFC pages, playlists and covers, prints and matchboxes, renders, social posts, and every document Hermes and Claude Code produce.
Updated: 2026-10-20

## How to use this document
- **What it is.** The rules every Lacande surface follows, gathered from the projects' own design documents. Each rule names its source in brackets: (G III) means the website's `GUIDELINES.md`, part III. All the codes are in [Sources](#sources).
- **Agreed rules** are written here as rules.
- **Open points.** Where the sources disagree or say nothing, the question is in [DECISIONS-NEEDED.md](DECISIONS-NEEDED.md). Until Leon decides, this document follows the website's `GUIDELINES.md` and marks the point **(pending decision #n)**.
- **What wins.** While this is a draft, the website's `GUIDELINES.md` settles any doubt. From v1 on, this document is the authority, and each project's design doc points here.
- **Changing it.** Leon tells Hermes (or a Claude Code session) "change X in the design". The change is made here, with its date; GitHub keeps the history.
- **Files next to it:**
  - [tokens.css](tokens.css): the decided values as CSS variables.
  - [templates/html-output.html](templates/html-output.html): the template for documents and reports.
  - [DECISIONS-NEEDED.md](DECISIONS-NEEDED.md): the open questions.

**Making something new? Five questions, in this order (G VIII):**
1. What must the reader understand first? Make that the clearest thing.
2. Which world is it? Take its background and its accent.
3. Which text is a title? Spectral. The rest is Mattone. A product's name is in its own typeface. (Long reads turn this round: see §3.)
4. Where does one part end and the next begin? Mark it with a line, and let space do the rest.
5. Which one picture carries the feeling?

---

# Basics

## 1. Positioning and voice

### Who the house is
- **Lacande is a maison d'édition. It edits things that have no body.** (POS §1)
- It publishes **listening candles**: a perfume and a playlist in one object, numbered like a record and credited like a book (G, opening).
- **The house is an éditeur:** it commissions the perfume, chooses the music, and signs work it did not make itself. The word *éditeur* is never translated. Never "curator", "creative director" or "label" as a self-description (POS §2.1).
- **The dry line** for footers, colophons, the legal page and meta descriptions: *Éditeur d'objets, de parfums et de musique.* The longer declaration appears only at the top of the maison page (POS §2.2).
- **Doctrine: le modernisme humaniste.** The clarity of modern form without the worship of the machine; industry and the hand reconciled, each named where it does the work (POS §5, §10).
- **References for the grammar:** ECM, Blue Note, Gallimard NRF: colophon, catalogue number, série, liner notes (POS §4quater, §9; HK). For the website: lido-lido.com for tempo and full-bleed pictures, Jacques Marie Mage for the maison page and the apparatus, Italy Segreta for the Journal (WDS §1).
- **Provence** is where the house is and where the candles are poured. The positioning leans towards treating it as a plain fact rather than one of the "territories"; that is not settled yet (POS §5).
- **Hyperrealism.** The world is won on the surfaces nobody treats as design: order emails, invoices, the 404, alt text, tab titles, file names. No vendor default is allowed to name anything. The test: *would this object exist if the house were real?* An invoice would; a tote bag would not (POS §6).

Full texts: `Lacande Website/docs/for Leon/lacande-positioning.md` (the positioning) and `docs/for Leon/lacande-website-design-system.md` §11–18 (the maison page, editorial mechanics, editions).

### How the house writes
Say what it is, plainly. Facts are clearer than adjectives, and they age better. Lacande writes like a catalogue: numbers, names, places and sources (G VII).

- **Describe a scent by what it comes from.** "Damask rose, aged harpsichord spruce, saline lagoon air." (G VII)
- **No pyramid.** A candle burns all at once, so its notes are one plain list, never top, heart and base (G VII).
- **Give the facts:** number, place, weight, burn time, price (G VII).
- **Nothing is urgent.** No countdowns, no "only 3 left", no "hurry". Out of stock is *épuisé, réimpression en cours*, never "sold out" (G VII; WDS §18).
- **One idea per paragraph**, in short sentences: 40 to 60 words a paragraph, up to about 90 in essays (POS §7.1).
- **The chronicle register** (POS §7.2):
  1. Name sources, never qualities.
  2. Use lists as evidence.
  3. State judgement flatly.
  4. One figure of speech per section, placed last.
  5. Never tell the reader what to feel: no sentence beginning "you will".
  6. Give coordinates: places, periods, traditions.
  7. Define by absence where possible.
- **The register test:** could a competitor put their name on this sentence? If yes, cut it (POS §7.4).
- **Never:** *warm, enveloping, luxurious, sophisticated* (G VII; POS §7.2); *synesthesia*; "we combine music and fragrance" (POS §3.2, §8); *curator* as a noun (POS §2.1); *discover, elevate, the perfect* (LET).
- **People:** places, periods and traditions may be named anywhere; persons only in the Journal, the Bibliothèque and the credits (POS §11.4).
- **First person** only in the Journal, signed (POS §4ter).
- **Each language is written from scratch**, never translated (WDS §16.5).
- **Music has a presenter's voice:** specific, names artists and songs, says when to play it, no exclamation marks, no superlatives (PL §8). Whether it may be called "warm": (pending decision #21).
- **Em dashes in public copy:** (pending decision #22).

**Real lines (G VII)**

| | |
|---|---|
| Kind | Perfumed candle · LC-002 |
| Scent | Damask rose, aged harpsichord spruce, saline lagoon air. |
| Facts | 250 g · 60 hours · Ø 8.5 × 9.5 cm |
| Credits | Perfume Jean-Michel Duriez · Direction Léon Windorfer |
| Price | 85€ |
| On the label | Tap for music (pending decision #24) |
| Avoid | warm, enveloping, luxurious · only 3 left · hurry · top / heart / base notes |

## 2. Principles
- **Clear first, then beautiful.** A reader should understand at a glance what they are looking at and where to go next. When clarity and beauty pull apart, clarity wins (G I; NFC Part 0).
- **Several things are shown as several things:** a list, separate lines, columns (G I).
- **The accent points at what matters,** a few times per page (G I).
- **Whatever doesn't help the reader is removed.** Nothing decorative; every element carries weight (G I; COM §0).
- **Then the care:** exact spacing, a good picture, the right typeface (G I).
- **Same function, same look.** A reader must see at once what is clickable, what is selected and what is only explanation (NFC 0.2).
- **One surprise per page, not five.** Surprises work only when they are rare (WDS §10).
- **A fixed frame, a free world.** The header, type and grid never move; inside them, each product may be designed from its own world (WDS §15.2).
- **The print test:** if it would look wrong printed in two inks on uncoated paper, it is wrong on screen too (NFC 1.1).

## 3. Typography
**Spectral for titles, Mattone for everything else, a typeface of its own for each product** (G II). Two house typefaces are enough for one voice; because the house stays quiet, each product can be noticed.

### The typefaces

| Role | Typeface | Weights in use | Source |
|---|---|---|---|
| Titles | **Spectral** | Regular 400 for titles; Bold 700 and Medium 500 in long reads | G II; PNL |
| Everything else: text, navigation, labels, prices, buttons | **Mattone** | Regular 400 (Bold 700 and Black 900 exist) | G II; PNL |
| A product's name, its opening line, a post or card about it | **the product's own face** | as the face comes | G II |
| The brand marks | **lacande-mark** (a font holding the marks) | one weight, 400 | G VI; PL §3 |

**Product typefaces today (G II)**

| Product | Typeface |
|---|---|
| LC-001 Jazz Impressions | Bauhaus 93 |
| LC-002 Sonata in Venetian Rose | Basteleur (pending decision #6) |
| LC-003 Isola Paradiso | Struggle |
| LC-004 Nuit d'Amour | Federo |

- A product's typeface names the product. It stays out of running text and interface (G II).
- Outside long reads, a heading is never in Mattone (PL §2).
- The marks are set at weight 400 with no fake bold (`font-synthesis: none`); a synthesised bold fills the counters and the mark looks blurred (PL §3).
- **Font files:** the website's `content/spectral-*.woff2`, `content/mattone-*.woff2`, the product faces in `content/`, and `assets/fonts/lacande-mark.otf` (PL §2).
- **Fallbacks** when the fonts are missing: Mattone → Arial, Helvetica, sans-serif (the website's own fallback, CSS). Spectral → Georgia, "Times New Roman", serif (proposed here; the website only says "a serif").

### Sizes
Every size is set twice, for desktop and for phones, and the phone size is never larger (DD §4). Phones are screens up to 768px wide.

| Style | Typeface | Desktop | Phone | Line height | Letter-spacing | Source |
|---|---|---|---|---|---|---|
| Title | Spectral Regular | 42px | 29px (pending decision #11) | 1.15 | 0 | G II; PNL |
| Subtitle | Spectral Regular | 18px | 16px (pending decision #11) | 1.35 | 0 | PNL |
| Lead | Mattone Regular | 22px | 18px | 1.4 | 0 | PNL; DD §4 |
| Text (body) | Mattone Regular | 18px | 15px | 1.55 | 0 | G II; DD §4; PNL |
| Quote | Mattone Regular | 22px | 18px | 1.4 | 0 | PNL; DD §4 |
| Label, kicker | Mattone, capitals | 14px | 13px | 1.4 | (pending decision #12) | G II |
| Caption (a sentence) | Mattone Regular | 14px | 13px | 1.4 | 0.02em | PNL; DD §4 |
| Navigation | Mattone Regular | 16px | 16px | 1.2 | 0.05em | PNL |
| Footer | Mattone Regular | 14px | 14px | 1.3 | 0.02em | PNL |
| Breadcrumb and cart count | Mattone | 36px (2 × text) | 22.5px (1.5 × text) | 1.1 | | DD §8 |

- On the website, text sizes come from these styles, never from a raw px value in the CSS (DD §4).
- On desktop everything grows with the window: × 1 at 1280px wide up to × 1.33 at 1920px. Phones always stay × 1. At × 1, 1rem = 18px (DD §10).

### Long reads (journal articles, the Lacande pages)
The other way round (G II; sizes from PNL and the website's CLAUDE.md):

| Part | Typeface | Desktop / phone |
|---|---|---|
| Big title | Mattone Regular | 46 / 32px |
| Standfirst | Mattone Regular | 22 / 18px |
| Section titles | Spectral Bold | 34 / 28px |
| Text | Spectral Medium | 18 / 16px (pending decision #9) |

- About 73 characters a line (pending decision #10). Red (the section's accent) only on the titles (G II).

### Boards and scent cards
On music boards and scent cards, a few more faces are in use: Cormorant Garamond Medium Italic for subtitles, questions and song titles; Spectral for paragraphs; Jost for scent-card names; five vintage sans as heading trials (PL §2; CS type.md). (pending decision #4)

### Money
One format everywhere: **85€**. The number, then €, no space, no decimals for whole euros. An amount with cents keeps them: 1.50€ (DD §6; G VII).

## 4. Colour
**Each world has one background and one accent** (G III). A world is anything the reader should recognise: a section of the site, a product, a series of posts. Its two colours tell the reader where they are before they read a word.

### The rules
- **House pages:** near-black text `#111` (pending decision #2) on white (pending decision #13). The accent marks only what matters: where you are, what you can click, a key sentence (G III).
- **A product's page:** the product's accent becomes the ink for everything, text and lines included (G III).
- **Online:** the same pairs; a post about a product wears that product's colours (G III) (pending decision #14).
- **Contrast:** text at least 4.5:1 on its background; large titles at least 3:1 (G III).
- **Clean edges:** worlds change at a clean edge, with no blends or gradients (G III).
- **One accent:** needing a second accent usually means a second world (G III).
- **Grey for secondary text:** `#6B6B6B` (5.3:1 on white), never below 4.5:1. On a tinted ground, use a grey worked out for that ground (at least 4.6:1), never a transparency (DD §4, §8) (pending decision #17).
- **One red:** Select red `#C50141` is the one red of the house (Leon, 16 October 2026). It replaced `#C5222F` and `#DC001C`. The menu's spinning record keeps its riso reds, `#C43C2C` and `#9F2E22` (G IX; CSS).

### Four kinds of combination (G III, Leon 15 October 2026)
Every combination is one of four kinds, and each colour in it has one job.

| Kind | Its colours | Rule | Use it for |
|---|---|---|---|
| **Tone on tone** | Ground · Ink: two tones of one colour; the ink does everything | ink on ground 4.5:1 | a product's world: its page, the label, the packaging |
| **Ground, text and accent** | Ground · Text (near-black) · Accent, for a few marks | text 4.5:1; accent 3:1, or 4.5:1 if it writes links | the site's sections, the Journal, emails, Note d'ascolto, Disque |
| **Triad** | three colours that look good together, in large areas | at least one pair 4.5:1, for the words | social media, covers, matchboxes, stickers |
| **Riso colours** | Paper · Light colour (light and middle tones) · Key colour (shadows, the name, the text) | key colour on paper 4.5:1; the light colour only has to show | the riso look of pictures and animations: Sovrastampa, scent cards, playlist covers |

**Black changes the kind.** When a pair's dark colour is a real colour (a blue, a red), black can take the text and the lines; the colour steps back to accent, and the pair becomes ground, text and accent (Music is one). When the dark colour is already close to black, the pair stays tone on tone (G III).

The combinations Leon likes are kept, sorted by kind, in *Lacande Colours*: `Lacande Website/docs/colours/index.html` (shared copy https://claude.ai/artifact/6A7vuUjn4ftkPPiaTpYPaU) (G III).

### The worlds today
Text is `#111` in all of these (G III).

| World | Kind | Ground | Accent | Accent on ground | Source |
|---|---|---|---|---|---|
| The house | ground, text and accent | `#FFFFFF` | Select red `#C50141` | 6.1:1 | G III |
| Lacande wing | ground, text and accent | `#ECEAF3` | `#C50141` | 5.1:1 | G III |
| Candles catalogue | ground, text and accent | `#FFF3EF` | `#C50141` | 5.6:1 | G III |
| Journal | ground, text and accent | `#F1F4F5` | `#C50141` | 5.5:1 | G III |
| Music | ground, text and accent | Quicksilver `#E0E2E5` | Ultramarine `#1F45C2` | 6.0:1 | G III |
| Matchbox Archive | ground, text and accent | `#F7F5F0` | `#C50141` | 5.6:1 | PNL (pending decision #16) |

### The candles: two pairs each
The site pair is the candle's tone-on-tone world (G III; PNL). The riso pair is used for print-looking pictures on posts and covers, printed on cream `#FFF9ED` (CS colours.md). The two are "not the same values" on purpose (pending decision #14).

| Candle | Site ground | Site ink | Ink on ground | Riso light colour | Riso key colour |
|---|---|---|---|---|---|
| LC-001 Jazz Impressions | `#A9CBE0` | `#14213D` | 9.4:1 | `#2D87BE` | `#24244A` |
| LC-002 Sonata in Venetian Rose | `#F9E6E1` | `#9F0920` | 6.9:1 | `#F7B7BD` | `#A80A24` |
| LC-003 Isola Paradiso | `#D8EDF4` | `#F54317` | 3.0:1 (pending decision #8) | `#A8E2FF` | `#CD3A14` |
| LC-004 Nuit d'Amour | `#4D1A28` | `#EBADCB` | 7.6:1 | `#F9BCE7` | `#511C2E` |

- On posters, the Jazz word stays dark blue (CS colours.md).
- Hovers on candle pages use the house red today (pending decision #7).

### The music family (PL §1; CS colours.md)

| Role | Value |
|---|---|
| Music grey (ground) | `#E0E2E5` |
| Ink (text, lines) | `#111111` |
| Ultramarine (kickers, numbers, charts, illustrations) | `#1F45C2` |
| Label white (boxes) | `#F7F5F0` |
| Charcoal ground (Disque's dark setting, off-white text) | `#262628` |

The playlist tool's own screens in dark mode: charcoal `#262628`, off-white `#F7F5F0`, ultramarine lifted to `#8FA6F2`. Boards never change with the viewer's theme (PL §1).

### Other colours with a fixed job
- **Matchbox Archive cards:** forthcoming `#F9E6E1`, out of print `#E4E2DE`, "in stock" green `#1E7B34` (4.9:1 on its ground) (CSS).
- **Each website section's accent** is a Site setting; a page takes its top-level section's colour (DD §8).

## 5. Layout and spacing

### Lines (G IV)
A few lines give the page its order. A single line in the ink marks where one part ends and the next begins. It replaces boxes, shadows and rounded corners.
- **One weight:** 2px on screen, about 1pt in print. Square corners, no shadows (G IV). Boards: (pending decision #15).
- **When in doubt, try space first** (G IV).
- On the website, a border width is never typed in px; it uses the `--rule` token (DD §8).
- **Lines are never doubled:** where a list meets a picture there is one line, the picture's (PL §4; DD §11).

| A line helps | Space is enough |
|---|---|
| Under the header | Between paragraphs |
| Between two parts of a page | Between the items of a list |
| Between rows of facts | Around titles and captions |
| Between two buttons | |

### Spacing values (DD §5, §8; CSS)

| What | Desktop | Phone |
|---|---|---|
| Text margin, left and right (`--pad`) | 1rem (18px at × 1) | 12px |
| Between blocks (`--space`) | 6rem | 6rem |
| Between a picture and the text beside it (`--space-media`) | 2.5rem | 2.5rem |
| Above and below the breadcrumb in the band (`--band-pad`) | 23px × scale | 23px |
| First line of text under the band (`--page-top`) | band + 23px × scale | band + 16px |
| Line weight (`--rule`) | 2px | 2px |

- **Desktop widths are in rem, never px.** A px value is only for a line, a tap target, or a phone value (DD §10).
- **Reading width:** about 73 characters a line (pending decision #10).

### Page structure (DD §1–3, §8, §12)
- **Five kinds of page:** Catalogue (a grid of objects), Édition (a stage: picture on one side, name and buying on the other), Reading (centred title, prose at the reading width), Door (panels that send the reader somewhere), Utility (cart, checkout, 404: one quiet written column).
- **The feed on phones:** one column in reading order: name → one line → image → the rest. Nothing pinned, nothing side by side.
- **The first screen:** at 375 × 667, every landing shows the page's name, one sentence and an image, never a screen of text alone. A long intro shrinks to one paragraph of 40–60 words plus a quiet "More +" (never on reading pages).
- **The first screen is exactly the window:** nothing cut by the fold.
- **The band:** breadcrumb and cart count sit in a fixed band in the page's own ground colour, with equal space above and below and a 2px ink line edge to edge underneath. The page scrolls under it. The band never sits over pictures and the header never moves.
- **No sideways scrolling on phones, ever**, except the tape row and the row of scent cards, each inside itself.
- **The split article:** the photo column 40–45% wide, the text always on the larger side, 1.5rem margins, lines capped at about 73 characters (DD §11).

### Tap targets (DD §7)
- At least 24 × 24px everywhere.
- 44px for buying and navigation controls (quantity, Remove, Add, the menu ×, the cart count).
- The target grows through padding; what you see stays small.

## 6. Imagery and photography
**Large pictures, quiet words** (G V). The picture carries the feeling, so it gets the space. The words around it stay plain and never sit on top of it.

### Rules
- **Edge to edge, in portrait (4:5)** unless there is a reason not to (G V).
- **Cropped around what matters**, centred on the picture's focus point (G V; DD §5).
- **A product render is shown whole**, on its own background, standing on a line (G V).
- **Show things that can be named:** a street, an awning, a table (G V). Source nouns give the camera something to shoot; adjectives give it nothing (POS §7.2).
- **No words on pictures, no dark veils (scrims):** the breadcrumb sits in the band, never over a picture (G V; DD §5).
- **Phones:** every picture full width, one column; pairs stack; pictures sit flush against each other; one 2.5rem gap between a picture and its text (DD §5).
- **Desktop:** portrait pictures default to 4:5; landscape pictures keep their shape; "original shape" never crops (DD §5).
- **Thumbnails** inside components (matchbox renders, ingredient pictures, cart and archive) are the one exception to full width (DD §5).
- **One clear subject per picture**, recognisable at thumbnail size: tobacco leaves drying on poles, not a cigarette (CS pictures.md; PL §7).
- **A photograph never stands for someone it is not** (CS pictures.md).

### Three kinds of picture (WDS §5) (pending decision #29)
- **Plein:** an untreated photograph, full width. Leon's own photography.
- **Planche (plate):** a photograph turned into a halftone print in the candle's ink (the Serigrafia treatment). Used regularly, not as the default.
- **Signe:** a flat geometric mark in the ink: disc, arc, bar, rule, repeated glyph. Never a picture of a candle, a flame or a musical note. The Olivetti and Pintori register.
- Treatment rises as the text becomes abstract.

### Where pictures come from (CS pictures.md; PL §7)
1. **Leon's photothèque**, searched in physical terms (light, surface, hour, material), because its descriptions carry no mood words.
2. **Wikimedia Commons**, free licences only, with credits kept.
3. **A picture Leon supplies**, marked "source to check before posting" until its rights are known.

- CC BY and CC BY-SA pictures carry their credit wherever they are posted. Each board keeps the picture's file name, date and author.
- Old record labels, sleeves and covers are **links, never pictures**. A board may borrow their grammar (flat grounds, round labels, condensed capitals), never their marks (PL §7).

### Halftone plates on screen (WDS §5)
- Made at screen resolution with a coarser dot, exported at 1x and 2x, never shrunk from print files (fine print screens shimmer on screens).
- Placed on the page's own paper colour, never in a white box.

---

# Print

## 7. Riso, inks, paper, matchbox and die-lines

### The riso look
Pictures that look printed use the **riso colours** kind: paper, a light colour, a key colour (G III).
- **Every print is real:** the picture is separated into plates and printed with named inks on a named paper. **No CSS filter stands in for a print** (PL §7).
- The key plate sits a hair off register: 0.4mm on a 110mm print (PL §7), 3px on a 1080px card (CS pictures.md).
- The tools: `riso-drums.mjs` (one ink, many tones: mono, key, flood) and `riso-separate.mjs` (two or three inks that look like the subject), in the website's `tools/riso/` (CS pictures.md).
- If a subject is not recognisable after separation, change the picture, not the inks (CS pictures.md).

**Riso inks** (catalogue of `riso-separate.mjs`, CS colours.md): black `#1A1A1A`, federalBlue `#3D5588`, mediumBlue `#3255A4`, teal `#00838A`, fluoPink `#FF48B0`, brightRed `#F15060`, crimson `#962B44`, sunflower `#FFB511`, yellow `#FFE800`, green `#00A95C`, mint `#82D8D5`, flatGold `#BB8B41`, violet `#9D7AD2`, fluoOrange `#FF7443`.

**Riso papers:** gesso `#F1EBE0`, neve `#F8F5F0`, crema `#EDE5D3`. The paper of playlist boards: cream `#FFF9ED` (CS colours.md).

**Olivetti inks** for the scent cards (Leon's choice, Session 94; CS colours.md):

| Ink | Hex | Ink | Hex |
|---|---|---|---|
| Valentine red | `#D2232A` | Pintori blue | `#1D57A5` |
| Spool orange | `#F28C1E` | Pintori yellow | `#F6D21C` |
| Lettera sea green | `#9EC3B5` | Pintori red | `#D9381E` |
| Lettera blue-grey | `#5F7A8A` | Pintori green | `#2A8C4A` |
| Lettera 32 blue | `#A8BFCB` | Carbon blue | `#2E3B8C` |
| Lexikon grey | `#6E7470` | Olivetti ink | `#23262B` |
| Programma red | `#C8102E` | Divisumma yellow | `#F2C318` |
| Teak | `#7A4A26` | | |

- Olivetti papers: ivory `#F1EBDD`, Lettera beige `#E6DCC6`.
- A black-and-white photograph on a sleeve may take two Olivetti inks: the darker on the key plate, the lighter on the flood, on crema. Teak keeps a sepia picture clear (PL §7).
- The scent card G′ is Olivetti card G on the Candles paper `#FFF3EF` with Select red: the default since Session 95 (CS colours.md).

### Printing matchboxes, posters and other printed matter (AT print-brief.md, inks.json)
- **Spot colours, not four-colour (CMYK)** (Leon, 2026-08-12): named Pantone inks, one plate each. Flat solids, sharp edges, the same colour on every run.
- **The board is free.** The ground is the unprinted board and costs no plate, so a "three-ink" matchbox (ground, black, one colour) is a two-plate job. The board's own colour is a design choice.
- **Choose the board first.** It decides the Pantone book: uncoated board → the **U** book, whose colours print duller and softer. Accept that as the design.
- **Choose from paper, not from a screen:** a printed Pantone guide (uncoated) in daylight, then a **drawdown** (a smear of the real ink on the real board) before the run.
- **Never send a hex code to a printer.** Hex values are screen stand-ins only (`hex_proxy`); the Pantone reference is what the printer receives.
- **Which black** is a brand decision: pure black, a warm black, or a very dark brown or grey (pending decision #5).
- **What the printer gets:** one PDF per ink (artwork in 100% black, the Pantone in the file name); a proof picture stamped "PROXY — not a colour reference"; the die-line on its own layer, with cut and fold lines told apart; all text turned into outlines; a spec sheet (sizes, bleed, safe area, board, finish, inks, thinnest line, smallest type).
- **The thinnest line** each ink holds comes from the printer; it limits the line weights in the design.

### Sizes (AT surfaces/*.json)

| Piece | Trim | Bleed | Safe area | Inks | Note |
|---|---|---|---|---|---|
| Matchbox (worked default) | 50 × 35mm | 3mm | 3.5mm | black + one colour | sizes vary by project; the proportions drive the composition |
| Poster A3 | 297 × 420mm | 3mm | 15mm | black + one colour | 15mm is visual air, not cutter tolerance |
| Instagram portrait | 1080 × 1350px | | 120 top, 180 bottom, 60 sides | screen | see social formats, pending decision #3 |

- **The matchbox die-line is not drawn yet.** It waits for the supplier: is the matchbox a printed sleeve over a tray? (AT ROADMAP O5)
- The Atelier sizes everything as a fraction of a grid module, so the same values produce a 50mm matchbox and a 1080px slide (AT brand.json).
- The Atelier's inks and fonts are still placeholders (pending decision #5).

### The marks in print (AT identity.json; G VI)
Never recolour a mark outside its allowed inks, never stretch it, never rotate it, never crowd it inside its clear space, never print it below its minimum size, never redraw it: place the file.

### Printed éditions
- The letterpress print édition of Sonata in Venetian Rose, in rosa Tiepolo, from the stamperia at Cornuda (WDS §4; POS §7.5).
- Matchbox éditions carry AS- numbers (§9).
- Printed matter is the lasting counterpart to a candle that burns and a track that ends (POS §3.3).

---

# Behaviour and naming

## 8. Motion and interaction

### Motion: a closed list (WDS §6; DD §9)
Anything not listed is out.

| Motion | Use |
|---|---|
| Rotation | constant, slow, never set off by scrolling: the vinyl, a signe turning beside a section |
| Drift | carousels that move by themselves in the Journal: a pan, not a slideshow |
| Flood | colour arriving, about 200 ms, on hover or on entry |
| Cross-fade | page transitions |
| The moving crop (the one exception to "no parallax", Session 124) | a photograph drifts 1.5% of its frame's height inside a frame that never moves. Never on covers, candles, matchboxes, sleeves, cards, posters or illustrations |

- **Banned:** parallax, scroll-jacking, fade-up on scroll, scroll-snap, full-screen (100dvh) panels (DD §9; WDS §6).
- **Reduce motion** on the reader's device turns movement off (DD §9; NFC 2.3).
- Done in CSS and a little plain JavaScript, no motion library (WDS §6).
- The NFC pages' Nudge, flip cards and slideshows: (pending decision #20).

### Interaction
- **What you can click** is marked by the accent (G III). In a row of sibling pages, the current page is bold in the section's accent, with no underline (DD §8).
- **Feedback stays on the page:** no toast, no drawer, no pop-up. After "Add to cart" the label becomes a text link, "In the cart — view cart" (COM §3).
- **A button never carries the price** (DD §2).
- **Fields** are underlined, with no box and the label inside the field (COM §5.2).
- **Messages** are a plain sentence in the house voice: no error boxes, no red, no icons (COM §8.2).
- **It works without JavaScript.** The content is in the page itself; scripts only add to it (COM §0).
- **A normal visit sets zero cookies** (COM §2.2).
- **Availability** is either available or *épuisée*, never a count (COM §7.2).
- **Codes** come by link; there is no discount field anywhere (COM §5.4).
- **Every interface string is the house's own**, translated per language; no vendor default names anything (POS §6; COM §0).
- **Design questions are decided on the real page:** the options are built side by side, Leon picks, the losing option is deleted and the decision is logged with the rejected option and the reasons (DV §4).

## 9. Naming and numbering

### Catalogue numbers
| Prefix | What | Example | Source |
|---|---|---|---|
| **LC-** | candles (perfumed candles) | LC-001 Jazz Impressions | G II; PNL |
| **AS-** | matchbox éditions | AS-001 | PNL; HK |
| **CP-** | curated playlists | CP-007 Calypso Blues | PL D023; HK (pending decision #26) |

- Three digits. **The number is a fact,** set small in capitals, never a hero, never big (CS rules.md).
- **Name a playlist with its candle:** "Jazz Impressions · LC-001" (CS rules.md). One name per édition (pending decision #25).
- **A hors-série** is a playlist with no candle: listed after the éditions, more plainly (WDS §9; POS §0).
- **Candle names never translate** (CS rules.md).
- **The kind line:** "Perfumed candle · LC-002" (G VII).
- **A catalogue number is not an edition size.** The tirage is stated after the fact (*première édition, imprimée en N exemplaires*). A reissue may change the picture, never the perfume. Refills carry no number (WDS §18).

### Credits and the lexicon
- **The colophon:** three credit lines on every object, naming who did what. *Sous la direction de* is a field that can name someone other than Leon (POS §0, §4quater).
- **Names are functional and specific**, never evocative and modern; for materials, papers, match séries and prints, the origin lives in the name (POS §7.6).

| Term | Meaning (POS §0) |
|---|---|
| maison d'édition | the house |
| éditeur | the person who commissions, chooses and signs; never translated |
| édition | one issued work: a candle with its music, numbered; also the print éditions |
| série | a group of éditions issued together |
| hors-série | a playlist with no candle |
| mise en parfum | composing the scent half of an atmosphere to a brief |
| souscription | a reader asks for a hors-série to become a perfume; the count is never shown |
| achevé d'imprimer | the closing statement of the tirage |
| épuisé | out of print, and coming back |

### Links, facts and formats
- **The link** is the real address from the NFC app: `tap.lacanderecords.fr/LC-00x-XXXXX/music`. Never "On Spotify". A post's last slide carries the QR of the same address and "Or light LC-00x and tap its label." (CS rules.md)
- **The line on the label:** "Tap for music" (G VII) (pending decision #24).
- **Facts** are separated by "·": "250 g · 60 hours · Ø 8.5 × 9.5 cm". Metric units only (G VII; COM §0).
- **Money:** 85€ (§3).
- **Document editions** carry a number and a date: "N° 6 · 16 October 2026" (G; PL).

---

# Practice

## 10. Do and don't

| Do | Don't |
|---|---|
| One idea per paragraph, short sentences | Three ideas in one sentence |
| Name what a scent comes from: "damask rose, saline lagoon air" | *warm, enveloping, luxurious, sophisticated*; *synesthesia*; *curated* |
| Scent notes as one plain list | Top, heart and base notes |
| Facts with "·": number, place, weight, burn time, price | Countdowns, "only 3 left", "hurry", "sold out" |
| A 2px line between parts; space inside them | Boxes, shadows, rounded corners, gradients |
| Pictures edge to edge, 4:5, one clear subject | Words on pictures, dark veils over pictures |
| The accent a few times per page | The accent as decoration, or a second accent in one world |
| Spectral titles, Mattone text, the product's face for its name | A product's face in running text; Mattone for a title outside long reads |
| Check contrast: 4.5:1 for text, 3:1 for large titles | Grey text below 4.5:1; transparent text on tinted grounds |
| The mark in one colour, on a calm background | The mark in the accent, outlined, stretched, rotated or redrawn |
| Real riso prints, with named inks and papers | A CSS filter pretending to be a print |
| Pantone references for the printer | A hex code sent to a printer |
| Credit pictures; keep file name, date and author | Pictures of other labels' sleeves or marks |
| The real tap address and its QR | "On Spotify", vendor default strings, a discount field |
| Rotation, drift, flood, cross-fade | Parallax, scroll-jacking, fade-up on scroll |
| One column on phones, no sideways scrolling | A page wider than the phone |

## 11. Notes per surface

### The website (the reference surface)
- Everything in §1–9 comes first from here. The detailed build rules are in the website's `docs/DESIGN-DOCTRINE.md` and `CLAUDE.md` (G, opening).
- New CSS: desktop widths in rem; text sizes from the type styles; lines with `--rule` (DD §4, §8, §10).
- Pictures go through the image component (focus point, srcset, width and height) (DD §5).
- Vinyls and motifs are separate SVG files, shown with `<img>` so their repeated letters never enter the page text; their main colour is `#C43C2C`, repainted by the server to the Panel's chosen colour; 300 × 300 (VIN).
- Check at 1920 × 1080, 1440 × 900 and 393 × 852, and at a true 390px phone width (DD §8, §10).

### Cart, checkout and order emails
- Written, not decorated: one quiet column, `#111` on white, no boxes, badges, icons or reassurance furniture, no urgency (COM §0). Titles in Spectral (pending decision #28).
- The cart row is name · × quantity · line price · Remove; no thumbnails (COM §4.2).
- The breadcrumb is replaced by the bare wordmark linking home (COM §4.1).
- The confirmation links to the playlist of each candle bought, so the music arrives before the candle (COM §8.1).
- The confirmation email is a small editorial object in the house voice, not a receipt (COM §9.3).

### NFC pages (what a customer sees after tapping)
- The only piece of the brand a customer sees from the app (NFC 2.1).
- **A customer standing over a candle never scrolls** to reach the streaming choice: the one-screen rule (NFC 2.11).
- The streaming services keep their official colours (NFC 2.10, Leon 2026-06-12).
- The footer (language and privacy) is fixed on every page (NFC 2.3).
- Photos sit inside their box and never behind text, except a page background photo with a veil (NFC 2.5).
- Lacande's own presets: Spectral, Mattone, the candle's colours, no shadow (pending decision #1). Motion: (pending decision #20).

### Playlist covers and boards
- Square boards, designed for the square first; 4:5 and 9:16 made from it (PL §6) (pending decision #3).
- Two registers: the music grey family for the app, proposals and unnamed playlists; a playlist's own world (cream paper, its key and light inks) once it has a name (PL §1).
- Templates: Sovrastampa, Disque, Grille, Manifesto, Ritornello, Note d'ascolto, Spec sheet, Sweep (PL §6). Each template's full rule is in the website's `content-studio/templates/`.
- Marks on boards: the wordmark top left in the ink; the lockup once, in the footer; the picto bottom right of the footer row, 0.6 of its height (PL §3).
- A fixed footer: a line edge to edge and a 106px row with the address or credit on the left and the picto on the right (PL §4; CS rules.md).
- A name that can't be read on its picture goes on a paper band; words are never cut, never shrunk below what can be read (PL §6; CS rules.md).
- The era first: look at the music's years and places before choosing pictures, inks and faces (PL §7).

### Social posts
- A post about a product wears that product's colours; the triad kind is for social media (G III).
- Formats: (pending decision #3). Stories keep text out of the top 220px and the bottom 230px (CS rules.md).
- Inner slides name themselves (About the playlist, Tracklist · 2 / 5, What it smells like, Listen); the address appears only on the last slide (CS rules.md).
- Before posting: facts checked · pictures credited · the NFC code set (no `XXXXX`) · formats exported · caption written from the playlist page (CS rules.md).
- Lettera writes the cultural posts and never names the brand (LET) (pending decision #23).

### Prints and matchboxes
See §7. Matchboxes use the triad kind (G III). Their inks and board are still to be chosen (pending decision #5).

### Renders
- A product render is shown whole, on its own background, standing on a line (G V).
- On the candle page the candle stands on the line where the first screen ends (DD §8).
- The Render tool's own design doc is a copy of the NFC app's (pending decision #19).

### Documents and HTML outputs (Hermes and Claude Code)
- Start from [templates/html-output.html](templates/html-output.html). It carries the tokens and the components.
- White paper, `#111` text, Select red as the one accent: where you are, links, a key number. A few times per page.
- Titles in Spectral, text in Mattone (pending decision #31). Fallbacks: Georgia for Spectral, Arial for Mattone.
- One line weight (2px on screen, 1pt in print); lines between parts and between rows of facts; space everywhere else. No boxes, shadows, rounded corners or coloured badges: a state is a word.
- "Needs Leon" goes first, as a short list.
- Dates as "20 October 2026" in the text; `YYYY-MM-DD` in file names (AGENTS.md).
- Light only (pending decision #30).
- The voice of §1: facts, short sentences, no adjectives doing a fact's job.

### Internal tools (NFC console, LacandERP, the Render tool, Serigrafia, the Atelier's sheets, the playlist tool's app)
Staff tools look different **on purpose** (pending decision #18):
- System font; labels in heavy capitals, tracked wider the smaller they are (NFC 1.3).
- Colour carries meaning, one meaning each: ink fill = the main action; amber `#D97706` = selected, "which one"; green `#15803D` = on, live; red `#DC2626` = off, blocked or destructive; in LacandERP also blue `#1D4ED8` = issued and grey `#57534E` = not started (NFC 0.4, 1.2; ERP 1b). A switch always carries its word (ON / OFF) as well as its colour (NFC 0.2).
- Five roles, never mixed: action (2px ink border), selection (amber), container (hairline `#DAD7CF`), input (pale fill, 2px line under), text to read (no box) (NFC 0.2).
- Sentences are sentence case at 12–13px; nothing a person must read is under 11px; fields on phones are 16px (NFC 0.3, 3.4).
- The one decorative move: a hard offset shadow under dialogs, with no blur (NFC 1.4).
- **Shared with the house:** clear first; square corners; 2px lines; the print test. Near-black and grey: (pending decisions #2 and #17).
- The playlist tool's colour codes (PL §5): cities Berlin `#1F45C2`, Turin `#D2232A`, Paris `#00838A`; verdicts keep `#2A8C4A`, cut `#C43C2C`; an unknown value is hatched or hollow with "—", never a guess.

---

# Sources
Each rule above names its source with one of these codes. Paths are on Leon's PC under `C:\Vibe coding\`; Hermes reads the same repositories in `/workspace/repos/<GitHub name>`.

| Code | Document | GitHub repo | What it gave |
|---|---|---|---|
| **G** | `Lacande Website/docs/GUIDELINES.md`, Edition N° 6, 16 October 2026 | Lacande-Website | the principles, type, colour, lines, pictures, marks, voice; the tie-breaker while this is a draft |
| **DD** | `Lacande Website/docs/DESIGN-DOCTRINE.md` | Lacande-Website | page kinds, phones, type law, images, money, tap targets, the band, motion limits, desktop scale |
| **WDS** | `Lacande Website/docs/for Leon/lacande-website-design-system.md` | Lacande-Website | references, picture register, motion list, editorial mechanics, editions. Its §2–4 (cream paper, provisional inks) predate G III (decision #13) |
| **POS** | `Lacande Website/docs/for Leon/lacande-positioning.md` | Lacande-Website | positioning, lexicon, the chronicle register, hyperrealism |
| **DV** | `Lacande Website/docs/design-variants.md` | Lacande-Website | how design options are compared and decided |
| **VIN** | `Lacande Website/docs/VINYL-GUIDELINES.md` | Lacande-Website | vinyl and motif SVG files, their colour |
| **COM** | `Lacande Website/docs/commerce-design-brief.md`, 2026-07-23 | Lacande-Website | cart, checkout, availability, messages |
| **CSS** | `Lacande Website/assets/css/base.css` | Lacande-Website | the values really used: `--color-ink`, `--rule`, `--pad`, `--space`, reds, matchbox states |
| **PNL** | `Lacande Website/content/site.en.txt` and `content/candles/*/candle.en.txt` (the Panel's live settings) | Lacande-Website | live type sizes, section grounds and accents, candle colours and faces |
| **CS** | `Lacande Website/content-studio/foundations/` (`colours.md`, `type.md`, `rules.md`, `pictures.md`); read because PL builds on them | Lacande-Website | riso and Olivetti inks, papers, candle riso pairs, post rules, picture sources |
| **NFC** | `NFC Candle app/docs/DESIGN_SYSTEM.md` | NFC-Candle-app | customer pages, five roles, internal-tool look |
| **A7** | `NFC Candle app/docs/audits/AUDIT_7_DESIGN_SYSTEM.md`, 2026-09-10 | NFC-Candle-app | state of the customer-page design system; no fonts uploaded |
| **RT** | `Render tool/docs/DESIGN_SYSTEM.md` | Render-tool | identical to SER and to the NFC app's June doc (decision #19) |
| **SER** | `Serigrafia/docs/DESIGN_SYSTEM.md` | Serigrafia | identical to RT (decision #19) |
| **PL** | `Spotify playlist tool/docs/DESIGN-GUIDE.md`, N° 6, 16 October 2026; D019, D023 in its `DECISIONS.md` | none (local only; Hermes can't read it) | boards, music registers, marks on boards, riso workflow, colour codes |
| **AT** | `1. Design generation tools/Lacande Design Atelier/brand.json`, `docs/print-brief.md`, `assets/inks/inks.json`, `assets/identity/identity.json`, `surfaces/*.json`, `ROADMAP.md` | Lacande-Design-Atelier | print method, sizes, bleed, spec sheet, open print questions |
| **ERP** | `LacandERP/docs/DESIGN_SYSTEM.md` | LacandERP | internal-tool look and status colours |
| **LET** | `Lacande Lettera/docs/VOICE.md` (still a placeholder) | none (local only) | the voice of the cultural posts |
| **HK** | `hermes-knowledge/design/lacande-design-language.md` | hermes-knowledge | the earlier short summary; from v1 on it should point here |

- The website's `CLAUDE.md` was read only where it disagrees with G (decisions #9 and #10).
- **Not used**, as the brief says: Settimana enigmistica (Bureau des Énigmes has its own brand), Talent Agency Software, Video game, any `AGENCY_ERP_DESIGN_SYSTEM.md`, and the placeholder looks in `Lacande Lettera/docs/design-guidelines.md` and `Lacande Corpus/docs/design-guidelines.md`.
