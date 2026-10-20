# LacandERP

Lacande's internal back office (ERP/CRM): products, contacts, orders, stock, finance, invoices, analytics.
Updated: 2026-10-20

## What it is
A staff tool built around an audited ledger that can't be edited after the fact.

**Modules:**
- products and SKUs, contacts, pricing (EUR/CHF), inventory;
- orders: B2B, direct-to-consumer, Shopify webhook;
- finance and invoices: French e-invoicing (Factur-X), ready for the 2027 requirement;
- fixed assets, accounting, VAT;
- expenses with AI receipt reading, procurement;
- website analytics.

**Added in September 2026:** website commerce settings, a stock-check API, and a Stripe webhook.

## Status
- **Live.** Latest patch: 19 Oct 2026. A security review ("Fable") was fully fixed in July 2026.
- **Not built yet:**
  - NFC Tags screens and NFC tag analytics;
  - Staff/permissions;
  - Settings;
  - distributor portal.
- **Planned address:** `erp.lacanderecords.fr`, not set up yet.

## How it's built
Next.js 16 and React 19 in a Turborepo, on Vercel, with a Supabase database.

## Connections
- **From the website:** receives its analytics and its commerce/stock data.
- **With the NFC app:** an ERP↔NFC API is planned. The ERP would own products, batches and the chip-to-product mapping.
- **Talented CRM:** reuses its architecture.

## Where things are
- **Repo:** https://github.com/Cojole3/LacandERP
- **Local:** `C:\Vibe coding\LacandERP`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/CHANGELOG.md`
  - `docs/analytics/ANALYTICS-ROADMAP.md`
  - `docs/FABLE_REVIEW_ROADMAP.md`
  - each module's `docs/<module>/CONTEXT.md`
  - (`README.md` is outdated)
