# Dashboard Space — Build Spec

The per-book Muse dashboard, specified from the Harlow's Helping Paws dashboard (Nov 2026) so a new book's dashboard is one build from this brief, not a day of passes.

## Sections / tabs
- **Overview** — project summary; phase tiles (Story · Edit · Cast · Illustration · Layout · Publish) that open the task list pre-filtered to the tapped phase — the tile outline follows the *selected filter*, and the current phase shows only as a small "● NOW" label; an "ecosystem" link list (repo, Drive homebase, Manuscripts, Knowledge Base, Cast Finals, showcase, bookshelf, spread review, shared inbox) rendered as live links, never static text.
- **Tasks** — the production checklist by phase, with owner and status (todo / doing / done). Seed with the standard pipeline tasks from the runbook.
- **Cast** — one card per character: name, kind, status (returning / new), description, and the character's **approved cast image** (the web-sized portrait the showcase serves) once art locks. Characters without locked art show an honest **"Art pending"** state — the tab doubles as the cast-completion tracker.
- **Storyboard** — the approved character boards first, then one slot per story beat/scene in story order. Until spread art is approved, slots read **"No spreads approved yet"** — the section is the approval shelf, ready to fill; never invent placeholder art.
- **Links** — every project destination, categorized (Repo · Manuscript · Bridge · Drive · Showcase · Bookshelf · Review · Reference). Every row carries a working URL from day one; audit all rows after any build pass.
- **Notes** — the project log, newest first: locks, milestones, shipped changes, with author + category.

## Chrome (same as the web pages)
- Slim sticky top bar with ONE ☰ button opening a slide-in menu: the same destinations in the same order as the showcase/review menus (bookshelf link in gold first), with the dashboard marked "you're here", plus links to the dashboard's own sections.
- Fade-in back-to-top button.

## Data actions the app must expose
`getdashboard`, `addtask` / `updatetask`, `addlink` / `updatelink` / `deletelink`, `addnote`, `addcharacter` / `updatecharacter`, `addscene` — full-row updates (read a row back after writing to verify).

## Hard-won rules (learned on the HHP dashboard — do not relearn)
- **Seed discipline:** a deleted row that still exists in the app's seed data WILL resurrect on the next sync/build. A deletion is not done until the seed entry is struck too. (Bit twice on Nov 20, 2026 with a dead reference link.)
- **Data fixes ride an idempotent sync:** when a build must correct stored data (a wrong label, a stale note), ship it as a post-submit sync function that changes a row only if it still holds the wrong value, and verify: first run changes N, second run changes 0.
- **Label matching is fragile:** any code that finds a row by its label text breaks silently when the label changes. Prefer ids; when matching by label, verify the match found a row.
- **Verify from the data, not the builder's summary:** after every pass, read the dashboard back and check counts and the specific rows the pass touched.
