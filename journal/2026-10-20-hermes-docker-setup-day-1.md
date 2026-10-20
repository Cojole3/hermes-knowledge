# Hermes setup — day 1 (server, VPN, Hermes, Kirby, monitoring)
Session note · Date: 2026-10-20 · Project: hermes-docker · Repo: local only (`C:\Vibe coding\Hermes Docker`)

## Done
- **Hermes is running** on the OVH VPS in an isolated container. It's reachable only through the WireGuard VPN, from Leon's PC and Android phone.
- **The server is hardened:**
  - SSH: key only for the admin, root login off;
  - CloudPanel is reachable only through the VPN;
  - a firewall guard and fail2ban are in place.
- **Kirby on the live website** went from 5.5.2 to **5.6.1** (a security release), and the website repo was updated to match.
- **Monitoring:**
  - a watchdog every 5 minutes;
  - nightly Hermes backups;
  - a weekly update check;
  - phone alerts via ntfy;
  - automatic night-time restarts after security updates.
- **Knowledge base:** this repository syncs with Hermes every 15 minutes. The PC copy updates itself. `/wrap-up` writes notes like this one.

## Decided (and why)
- **Hermes never gets write access to GitHub.** Code changes go through Claude Code as pull requests, because that's safer and runs on the subscription.
- **Models:** Opus is the main brain, Sonnet the helper, Haiku does the side jobs. Budget: $100/month of API credits (Max 5x).
- **Interface:** start with Hermes's own interfaces; Leon's own interface comes later.

## Open / next steps
- **11c:** read-only access to the code repos for Hermes, plus a nightly review.
- **11d:** a Claude Code routine that Hermes can start.
- **Website deploys:** a FileZilla key or a server pull-deploy.
- **Local-only projects:** push them to GitHub, starting with the Playlist atelier.

## Key files and docs touched
- **Hermes Docker project:** `NOTES.md`, `SETUP-LOG.md`, `vps/`, `pc/`.
- **Lacande Website:** `docs/lacande-infrastructure-v4.md` (§15) and `kirby/`.
