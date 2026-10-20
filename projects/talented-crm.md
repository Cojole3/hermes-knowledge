# Talented CRM (folder "Talent Agency Software")

A CRM/ERP for talent agencies. Its core output is deal memos: one-page booking agreements as French/English PDFs.
Updated: 2026-10-20

## What it is
- **Multi-tenant:** the first tenant is a Paris agency representing Directors of Photography.
- **Manages:** talents, organisations, people, projects and documents.
- **Main job:** creating deal memos fast and without errors:
  - fee, commission and VAT calculation;
  - versioning, with draft and final states;
  - the agency's real memo PDFs serve as reference fixtures.

## Status
**Active, in progress.** Phase 1 covers steps 0–19; step 20.5 is done (last commit 13 Aug 2026, 236 tests passing).

**Next:**
- **Top priority:** Leon tests step 20 by hand in a browser, because no browser test tool is installed in the repo.
- Pixel-diff tests against the reference PDFs.
- Test coverage for the snapshot write path.

**Later:**
- **Phase 2:** AI drafting from emails, Pennylane invoicing, availability calendar, tracking signed memos.
- **Phase 3:** e-signatures and portals.

## How it's built
Next.js (React 19, TypeScript) in a Turborepo, with Supabase Postgres (row-level security), `@react-pdf/renderer` for the PDFs, and Vitest for tests. No deployment URL is documented.

## Connections
Architecture reused from **LacandERP**: agency clients correspond to Lacande "contacts", and bookings to "orders".

## Where things are
- **Repo:** https://github.com/Cojole3/Talented-CRM
- **Local:** `C:\Vibe coding\Talent Agency Software`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/STATE.md`
  - `docs/ROADMAP.md`
  - `docs/DECISIONS.md`
  - `docs/SCHEMA.md`
  - `TALENTED_CRM_BRIEF.md`
  - `AGENCY_ERP_BLUEPRINT.md`
