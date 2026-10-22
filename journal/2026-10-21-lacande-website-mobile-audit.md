# Lacande Website: the site on a phone, audited against nineteen stores
Session note · Date: 2026-10-21 · Project: Lacande Website · Session 130 · Repo: Cojole3/lacande-website (docs commit e6dd01a)

## Done
- Every page of the site captured on an iPhone 15 viewport with Playwright from the current build: first screens, scrolled screens, full pages, the menu open, the cart with an item. Type sizes, tap targets and page weights read from the rendered CSS.
- Nineteen candle, perfume and fashion stores captured the same way (landing, catalogue, product, menu, cart) by three agents: Diptyque, Trudon, Le Labo, Ex Nihilo, Buly, Astier de Villatte, Aesop, Frédéric Malle, Loewe, Jacques Marie Mage, Lido, The Row, Lemaire, Totême, Jil Sander, Bottega Veneta usable; Byredo, Jacquemus, Celine, Kurkdjian and Aimé Leon Dore blocked by maintenance pages or bot walls, and named as such.
- The report published as one page, "Lacande on the Phone": https://claude.ai/artifact/CtFAaNcPf1Mg4Hq7i62j14. Benchmark table and site-by-site phones, Lacande measured, nine shortcomings, seven proposals rendered on the real site before and after (override CSS injected, same scroll), six notes, the September audit reconciled, the build order.
- No site code changed. Docs updated and committed: LOG (Session 130), STATE, ROADMAP.

## Found
- Lacande already reads as premium on a phone: no promo bar, popup, chat bubble or five-icon header, and the candle page's first screen holds the price and the button, which Diptyque's and The Row's do not.
- The shortcomings are of scale and density: one candle a screen on the homepage éditions and the Candles catalogue (eleven of fifteen readable catalogues run two a row at 170 to 197 px); eight lines of intro before the first candle; the crumb truncating every candle's name to "ja…"; 49 px menu items that collide when "Matchbox Archive" wraps; the cart's checkout an underlined word; the disabled Add to cart the only filled button on the candle page.

## Proposals (Claude's picks in bold)
- P1 homepage first screen: caption 2 rem higher (**a**) or 3 rem and the picture inset (b). Leon's observation.
- P2 éditions on the homepage 2 × 2: **without lines (a)** or with (b).
- P3 **Candles intro clamped to three lines with "More +"** (Leon's, after Diptyque; the Matchbox Archive's intro-more snippet reused).
- P4 Candles catalogue one a row (Lido) beside **two a row** (the others).
- P5 menu at min(6.2vh, 10.5vw), line-height 1.08, (a) alone or **(b) with a foot: Cart · Shipping & returns · Contact**.
- P6 crumb on candle pages: **(a) shows the section, the name is the page** or (b) the name wraps under the brand.
- P7 **the cart's checkout as the candle page's filled button**.

## Open / next steps
- Leon chooses among the variants on the page.
- Build order: P3 + P4 (Candles), P2 + N1 (éditions, the disabled Add to cart styled as disabled or "Notify me"), P6a + P5b (crumb, menu), P7 + N5 (cart button, playlist link row), P1a, then the Music page's 11 px texts and 31 px chips, the Matchbox filters' 18 px targets, Isola's running text in the house ink.

## Key files and docs touched
- `Lacande Website/docs/LOG.md`, `docs/STATE.md`, `docs/ROADMAP.md`. Capture and render scripts in the session scratchpad only (`pw/capture-lacande.mjs`, `pw/bench.mjs`, `pw/proposals.mjs`).

## Session 130.1 (2026-10-22): the choices built
- Leon chose: P1a with one fixed shape for the first frame on every phone (369 : 441), P2a, P3, P4 two a row, P5a with the record centred under the last item; the crumb (P6) visualised only, three strips to pick from; and a new ask: more air at the end of a candle and a ruled line naming the next one, like the Matchbox Archive's pager, on phones and desktop.
- All built on the site and verified on three phone sizes and desktop; committed. The "Next" line had existed but the sequence script hid it once the next candle loaded; it stays now.
- The audit page corrected (phone viewport 393 × 659, not 852) and extended with part 7: https://claude.ai/artifact/CtFAaNcPf1Mg4Hq7i62j14.
- Open: the crumb's size (Claude's pick c, 18 px, no space round the slash), P7 the cart button, N1 the disabled Add to cart before launch.

## Session 130.2 (2026-10-22): two corrections after Leon's phone
- The first frame: Leon's rule is that the line is always at the bottom of the screen and the picture takes a fixed part of the screen (the crop varies). Built so: the picture is 75 % of the height under the band on every phone, verified on four sizes. The fixed-shape version of 130.1 is undone.
- The candle's "Next" line: a small thing under the picto (13 px desktop, 11 px phone), no ruled box.
- The audit page got a table of contents, a dated band and the four options for the first frame (A built, B the old frame with the caption higher, C fixed shape, D screen units).

## Session 130.3 (2026-10-22): round 3
- Built: the first frame as option B (the frame takes what the caption leaves, the line at the fold on every phone); the Candles intro's "… More +" at the end of the third line, as Diptyque.
- To decide, rendered as whole phone screens: the crumb (a no space round the slash, b the same at 20 px, c at 18 px; Claude's pick c) and "Add to cart" (a drawn disabled with "Available soon", b a Notify me link, c the filled button reading "Notify me" with the matchboxes' email field; Claude's pick c).
- The audit page is now newest-first: part A the latest round, part B rounds 1 and 2, then the audit. Version 5.

## Session 130.4 (2026-10-22): the crumb built
- Leon chose c: the crumb and cart count at 18 px on phones, no space round the slashes, and the band shrunk in proportion (58 px instead of 73, the text still centred). Built and committed; the menu's masthead follows.
- "Add to cart": Leon's decision, nothing changes; the button stays as it will work once the shop opens.
- Audit page version 6, part A updated. Open: P7 the cart button, N5, N2 to N4.

## Session 130.5 (2026-10-22): live
- The phone work of Sessions 130 to 130.4 is live on lacanderecords.fr (871bbd5, 22 Oct 14:26), pushed to GitHub and installed with `sudo website-update` over SSH (dry run first: 5 files, no content touched; backup taken; live tests passed). Noindex still on. Verified on a phone viewport against the public site.
- Note for later: SSH from this PC works through the Windows OpenSSH agent (`C:\Windows\System32\OpenSSH\ssh.exe`), not Git Bash's ssh.
