# NFC Candle app

Turns a tap on a candle's label (NFC chip or QR code) into the right playlist on the customer's streaming service.
Updated: 2026-10-20

## What it is
**For customers:** a chip or QR code leads to a choice page. The customer picks a streaming service, and the choice is remembered.

**For admins:**
- manage products and content;
- design the customer pages;
- create chip links;
- encode chip rolls from a phone;
- see tap analytics.

**Built as multi-tenant software:** Lacande is the first tenant.

## Status
**Pre-launch:** deployed to production, but no production chips exist yet.

**Recent work (13 Oct):** an encoding station for chip rolls, and a phone version of the admin console.

**Open items:**
- **The database has no backup** until a Supabase Pro upgrade.
- Rate-limiting decision on the redirect.
- Uptime monitoring.
- Two-factor login and other login hardening.
- Legal and privacy sign-off.
- Checks on a real iPhone with Safari.
- The final chip-lock step on the SLIX2 chips is unproven.
- The docs don't confirm that the Edge Function holding the new product addresses has been deployed.

**Note:** test data still uses the old name "Tournant Jazz" (now Jazz Impressions).

## How it's built
React, Vite, TypeScript and Tailwind on Vercel, with Supabase (database and Edge Functions). Public address: `tap.lacanderecords.fr/<CODE>`.

## Connections
- **ERP↔NFC API (planned):** the NFC app owns chip IDs, destinations and anonymous taps; customer identity never reaches it.
- **Shared numbers:** the same catalogue numbers as the website.
- **Playlist atelier:** new playlists get added here.

## Where things are
- **Repo:** https://github.com/Cojole3/NFC-Candle-app
- **Local:** `C:\Vibe coding\NFC Candle app`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/STATE.md`
  - `docs/ARCHITECTURE.md`
  - `docs/SECURITY.md`
  - `docs/DECISIONS.md`
  - `docs/GLOSSARY.md`
  - `docs/LAUNCH_TODO.md`
  - `docs/api/CONTEXT.md`
