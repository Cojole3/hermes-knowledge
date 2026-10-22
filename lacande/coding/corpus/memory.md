# Lacande Corpus

Lacande's brand knowledge base and thinking partner. Its answers come only from material Leon has fed it, and it cites sources.
Updated: 2026-10-20

## What it is
- **Input:** Leon pastes in conversations, notes, and passages from books and articles.
- **Indexing:** the material is split into chunks and indexed by meaning, using a small embedding model that runs locally.
- **Answers:** Sonnet answers using only the passages it finds, with sources. It says so when it has little material on a topic.
- **Purpose:** meant as **infrastructure that other tools query**, not mainly as an app.

## Status
- **Built:** 5 June 2026 (ingestion, search API, admin and settings, chat).
- **Paused:** no next phase documented after session 4.
- **Placeholder:** the look is a placeholder to be replaced by Lacande branding.

## How it's built
Node, Express, TypeScript and SQLite (sqlite-vec for search). Haiku splits messy text without rewriting it. The interface is React/Vite. Runs locally on port 3100.

## Connections
Meant to supply grounded brand context to Lettera, and later possibly to the ERP and a website chatbot. None of these links are wired yet.

**Overlap with Hermes's knowledge base:** both hold Lacande knowledge. Whether to connect, merge or keep them separate is an open question for Leon.

## Where things are
- **Repo:** none; Git is local only, so Hermes can't see it yet.
- **Local:** `C:\Vibe coding\Lacande Corpus`
- **Key docs:**
  - `CLAUDE.md`
  - `docs/CONTEXT.md`
  - `docs/SPEC.md`
  - `docs/WORKLOG.md`
  - `docs/prompts/`
