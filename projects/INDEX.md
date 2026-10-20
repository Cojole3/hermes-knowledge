# Projects: map

All of Leon's projects, how important each one is, and how they connect.
Updated: 2026-10-20 (first version, written from each project's own docs)

## Priority
1. **Lacande** ([lacande.md](lacande.md)). Within it, the **website** comes first.
2. The other Lacande tools, which make content, images, prints and playlists for the brand.
3. Other projects.

## The Lacande system

```
                 Customers
                     │
      ┌──────────────┴───────────────┐
      ▼                              ▼
 Website (lacanderecords.fr)    NFC Candle app (tap.lacanderecords.fr)
 Kirby, on the OVH VPS          candle label → playlist
      │ analytics, stock,             │ (ERP ↔ NFC API planned)
      ▼ orders                        ▼
              LacandERP (back office, Vercel)

 Brand and content tools (local, on Leon's PC):
   Corpus (brand knowledge) → Lettera (social posts) ← Photothèque (photos)
   Playlist atelier (CP- playlists) → website Music pages, NFC app
   Design Atelier · Serigrafia (print) · Render tool (3D renders) → visuals, labels, matchboxes
```

## All projects

| Project | What it is | Status | Page |
|---|---|---|---|
| **Lacande** | The brand: listening candles, matchboxes, playlists | Pre-launch | [lacande.md](lacande.md) |
| **Lacande Website** | Public editorial site and future shop | Live with an old build (noindex); local work far ahead | [lacande-website.md](lacande-website.md) |
| **LacandERP** | Back office: orders, stock, finance, invoices, analytics | Live | [lacanderp.md](lacanderp.md) |
| **NFC Candle app** | Turns a candle tap into the right playlist | Deployed, no production chips yet | [nfc-candle-app.md](nfc-candle-app.md) |
| **Lacande Lettera** | Writes Lacande social posts with Claude | Built (June); paused | [lacande-lettera.md](lacande-lettera.md) |
| **Lacande Corpus** | Brand knowledge base and thinking partner | Built (June); paused | [lacande-corpus.md](lacande-corpus.md) |
| **Photothèque** | Leon's photo/video archive with AI tagging | Working, active | [phototheque.md](phototheque.md) |
| **Playlist atelier** | Makes Lacande's numbered playlists | Working, active | [playlist-atelier.md](playlist-atelier.md) |
| **Design Atelier** (+ small generators) | Generates Lacande design variants (matchbox, poster) | Phases 1–8 done | [design-atelier.md](design-atelier.md) |
| **Serigrafia** | Template studio + print simulation lab | Active | [serigrafia.md](serigrafia.md) |
| **Render tool** | 3D renders of candles, boxes, matchbox; label templates | Active | [render-tool.md](render-tool.md) |
| **Le Bureau des Énigmes** | French puzzle magazine web app | Active, waiting on Leon | [bureau-des-enigmes.md](bureau-des-enigmes.md) |
| **Talented CRM** | CRM/ERP for talent agencies (deal memos) | Active | [talented-crm.md](talented-crm.md) |
| **LANEWAR** | Lane-strategy wargame (folder "Video game") | Design only. Leon doesn't remember it: keep or archive? | [lanewar.md](lanewar.md) |
| **Training tools** | Camera practice simulator | Single finished tool | [training-tools.md](training-tools.md) |
| **Recipe app** | Recipe/cookbook app | Empty folder; old prototype archived | [recipe-app.md](recipe-app.md) |
| **Hermes setup** | This assistant: Hermes on the VPS | Being set up | [hermes-setup.md](hermes-setup.md) |

## What Hermes can reach
- **GitHub repos (since 2026-10-20):** read-only copies of all of them are in `/workspace/repos/<name>`, refreshed hourly. New repos appear automatically.
  - Folder names: `Lacande-Website`, `LacandERP`, `NFC-Candle-app`, `Phototheque`, `Render-tool`, `Serigrafia`, `Lacande-Design-Atelier`, `Carnet-enigmes` (Bureau des Énigmes), `Talented-CRM`, `OpenCookbook` (recipe prototype).
  - Code changes go through Claude Code, after Leon's OK.
- **Local-only projects** (no GitHub remote: Lettera, Corpus, Playlist atelier, Training tools, LANEWAR): Hermes can't see them until Leon pushes them to GitHub.
