# Website operations: memory

How the Lacande website goes live and how it is kept up. The code side is in [coding/website](../../coding/website/memory.md).
Updated: 2026-10-22

## How it goes live
- The website goes live only when Leon asks. He can ask Hermes ("put the website live") or a Claude Code session.
- The server takes GitHub's main branch. Before it switches, it runs checks and takes a backup. After it switches, it runs live tests, and it restores the backup automatically if something fails.
- FileZilla is retired. Nothing is uploaded by hand any more.
- Secrets (the admin login key, the link salt and the shop's sync password) live only on the server, never in the repository.

## Hidden from search until launch
- Every page carries noindex, so search engines do not list the site yet. Removing it is the last item of the launch gate.

## Keeping it up
- **Kirby** (the content system) runs version 5.6.1 on the server since 2026-10-20, after a security release.
- A weekly update check runs on Mondays at 10:00 (Paris time). It looks for new Kirby and Hermes releases and sends an alert. It installs nothing.
- A watchdog checks the site every 5 minutes and alerts Leon's phone if it fails.

## Still open before launch
- Real candle copy and prices.
- The newsletter.
- The address that analytics reports to (erp.lacanderecords.fr, not set up yet).
- Buying the Kirby licence.
- Removing noindex.
