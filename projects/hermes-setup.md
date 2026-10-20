# Hermes setup

This assistant: Hermes Agent running on the OVH VPS, reachable only through Leon's VPN.
Updated: 2026-10-20

## What it is
- **Hermes Agent v0.22.2** runs in a Docker container on the VPS that also hosts the Lacande website. It's isolated from the website.
- **Access:** through WireGuard only (Leon's PC and phone), using Hermes Desktop or the dashboard at `http://10.8.0.1:9119`.
- **Models:**
  - Opus 5.5: main;
  - Sonnet 5.5: helpers and judgment jobs;
  - Haiku 5.5: side jobs.
- **Limits:** 1.5 GB memory, 1 CPU, 10 GB data area, 512 processes.
- **Network:**
  - **reachable:** the internet and the public website;
  - **blocked:** the server's internal services, SSH, CloudPanel, the database, private networks and email.
- **Approvals:**
  - dangerous commands need Leon's OK;
  - force-push is blocked;
  - "ask first" rules are in the standing instructions.

## Status
**Being set up.**

**Next:**
- standing instructions and this knowledge base;
- tests, including a server restart;
- backups, updates and alerts;
- the FileZilla key;
- the GitHub `knowledge` repo and the Claude Code connection (routines);
- later, Leon's own interface.

## Where things are
- **Plan and log, on Leon's PC:** `C:\Vibe coding\Hermes Docker\` (`NOTES.md`, `SETUP-LOG.md`, `vps/`).
- **On the server:** `/srv/hermes` (compose, data, workspace).
