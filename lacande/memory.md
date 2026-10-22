# Lacande

Lacande is Leon's main business: a small French house that makes listening candles. Each candle pairs a scent with a playlist.
Updated: 2026-10-22

## What it is
- **The idea:** each candle is a perfume and a music playlist in one object. An NFC tag in the label opens the playlist. The customer's steps are: light it, tap the label, listen.
- **Positioning:** a maison d'édition. It commissions and signs its work.
- **Team:** Leon (founder, product owner, direction) and one co-founder. Leon directs the candles; the perfumes are by Jean-Michel Duriez.

## Products
- **Candles:** 250 g each, about 60 hours of burn time. The 85 euro price is a placeholder. The candles are Jazz Impressions (formerly Tournant Jazz), Sonata in Venetian Rose, Isola Paradiso and Nuit d'Amour.
- **Matchbox editions:** numbered, for example Arles. The first real print job is matchbox model BX-L50.
- **Playlists:** numbered, the latest being Calypso Blues. A hors-série is a playlist without a candle.
- **Journal:** editorial writing on the website.
- **Catalogue numbers** (LC-, AS- and CP- prefixes) are shared across the website, the NFC app and LacandERP. Names come first in all writing.

## Key decisions
- The design rules live in [foundations](foundations/). LACANDE-DESIGN.md is the authority for anything visual. 25 of its 31 points were decided on 2026-10-21.
- Hermes never writes to GitHub. Code changes go through Claude Code.
- The website updates from GitHub, on request. FileZilla is retired (2026-10-21).
- The website goes live only when Leon asks. LacandERP and the NFC Candle app wait for Leon's OK before going live.

## Status
- **Pre-launch.**
- **Website:** the session notes of 2026-10-21 say the current build went live that day. The older project page still describes the old build with noindex. The website's own repository is the authority.
- **NFC Candle app:** deployed, but no production chips exist yet.
- **LacandERP:** live.
- **Launch gate, what remains:** real candle copy and prices; the newsletter; the analytics address; the Kirby licence; removing noindex.

## Connections
- The Lacande tools and sites are in [coding](coding/). The website's live server and its updates are in [operations](operations/).
- Leon's wider setup is in [systems](../systems/).

## Open questions
- Final prices and candle copy.
- Launch date.
- The public address for LacandERP (erp.lacanderecords.fr) is not set up yet.
- Whether Lacande Corpus and Hermes's knowledge base should be connected, merged or kept apart.
