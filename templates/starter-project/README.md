# Starter Project — copy this whole folder to start a book

A working, bare-bones book project: showcase + spread review + 3D flipbook, wired together and running on placeholder art. Everything functions — menus, bookshelf, page turns, review lightbox with Lulu/seam guides — before a single real page exists.

The placeholder book follows the kit's universal shelf-book flow (BOOK-BUILD-BIBLE §6, kit v1.2.5): **front cover → flyleaf → title page → content → flyleaf → back cover**, with the © lines at the title page's foot — no standalone copyright page. Replace the placeholder flyleaf/title pages with your own typeset versions in the same slots.

## What's inside
| Path | What it is |
|---|---|
| `index.html` | The showcase — hero, story, cast, boards, roadmap, bookshelf links. Shared ☰ menu. |
| `spread-options-v1.html` + `review-assets/v1/` | The spread review page (V1) and its FROZEN snapshot images. Review pages never read live flipbook art. |
| `flipbook/index.html` | The BookVizion 3D flipbook (best build: two-book shelf machinery, icon back-button, phone-width toolbar fix). |
| `flipbook/images/` | The book's live pages + `manifest.js` (title, page list, roles). The flipbook is always "current" — swap art here. |
| `media/` | Showcase images (cast portraits, boards, hero). |
| `PRINT-SPECS.md` | The locked Lulu numbers, carried in-project. |

## Make it yours (in order)
1. **Copy the folder** into the new book's repo; rename nothing inside until it runs.
2. **Title + author:** `flipbook/images/manifest.js` (title), the CATALOG info block in `flipbook/index.html` (author/about/captions), `<title>`/headings in `index.html` + `spread-options-v1.html`.
3. **Storage prefix:** the flipbook uses the `bookproj-` localStorage prefix and the review page uses `bookproj-spreads-v1-settings` — change `bookproj` to a project-unique slug (all his books share one github.io origin; prefixes keep each book's device state separate).
4. **Placeholder art:** replace the plates in `flipbook/images/` (keep the filenames or update manifest + review SPREADS together), `review-assets/v1/`, and `media/`. Square pages, web-sized JPGs.
5. **Series shelf (optional):** to shelve a finished earlier book, add its CATALOG entry + contained page copies under `flipbook/shelf/<slug>/` — the pattern is proven in the kit's reference build (`templates/flipbook/`, the HHP two-book build).
6. **Run the gates** from the kit RUNBOOK before anything ships: port-gate probes on the flipbook (Chromium + WebKit), the publish gate's four-part diff on page changes, PAGE-POLISH for anything shared by link.

The full reference implementations (Harlow's Helping Paws, with real content) sit beside this folder in `templates/repo/` and `templates/flipbook/` — copy patterns from them freely.
