# Templating Notes — what changes per book (Pass 1: reference implementation)

The files in `templates/` are the proven Harlow's Helping Paws implementations, shipped as the reference. Pass 1 keeps them as-is with the per-book variables marked here; full parameterization is Pass 2 work.

## templates/repo/index.html (showcase)
Per book, change:
- Title, author, story lede, phase blurbs
- Cast section: portrait images (`media/cast/`) + names/kinds
- Character Boards section: board images (`media/boards/`)
- The Bookshelf section copy (which books sit on the shelf)
- ☰ menu destinations (same order everywhere: bookshelf gold first, spread review, showcase)
- KEEP: the shared menu system, the charcoal/gold skin, back-to-top, the section rhythm.

## templates/repo/spread-options-v1.html (spread review)
Per book, change:
- Card set = the book's spreads (from the flipbook Overview)
- Frozen artwork copies under `review-assets/v1/` — a review page NEVER points at the live flipbook images
- The VERSIONS list (every version page lists every version; update all pages when a new one ships)
- KEEP: lightbox with seam + Lulu guides, Page Settings panel, shared ☰ menu, per-device settings persistence.

## templates/flipbook/ (BookVizion build)
Per book, change:
- `images/manifest.js` — the builtin book (title + page list) and `images/` page files
- CATALOG entries in `index.html` — one per book on the shelf; prior books in a series are imported contained (pages under `shelf/<slug>/`, entry shape per the runbook) rather than linked out
- The `#shelfShowcase` href — the new book's showcase URL
- Storage key prefix — isolate per project (HHP uses `hhp-`)
- KEEP: the top-bar layout including the 42px round back-arrow icon button and the ≤380px small-screen rules (the Settings-gear overflow fix, Nov 20 2026) — do not reintroduce a text pill in the top bar.
- Any change to this build goes through the port gate (see RUNBOOK): byte census, Chromium + WebKit cold-boot probes, live-byte verification after shipping.
