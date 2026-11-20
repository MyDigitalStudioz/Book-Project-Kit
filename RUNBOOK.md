# Runbook — "New book project"

The standing command is **"New book project: \<Title\>"**. Whoever runs it (Trinity, or a desk Jon designates) executes this runbook end to end and hands back ONE checklist: what is scaffolded, and which slots await story and artwork. Nothing below needs Jon's legwork beyond the kickoff answers.

Proven on: *Harlow's Accidental Journey* (Book 1, 2026) and *Harlow's Helping Paws* (Book 2, Nov 2026).

## Kickoff — confirm with Jon in one round
1. Title (working title is fine) and author
2. Repo name (org: **MyDigitalStudioz**)
3. Trim size (default: Square 8.5 × 8.5 — see docs/LULU-SPECS.md)
4. Series? If Book N, which prior books join this book's shelf (contained — never linked out)
5. Manuscript status (draft in hand / coming)

## Step 1 — Drive homebase
Create the folder tree exactly per **docs/DRIVE-TREE-SPEC.md**. Write the START-HERE doc (project, author, status, where things live). Create the shared notes inbox doc (ONE doc, newest first).

## Step 2 — GitHub repo
- Create `MyDigitalStudioz/<repo>` (public), GitHub Pages on from `main`.
- Working branch: `<repo-slug>-v1`. **Branch policy: work happens on the working branch; `main` is the Pages/shipping line; merges happen on Jon's go.** Never assume the default branch is the working line.
- Repo settings per the standing template lock: description, 3–5 topics, labels (GitHub defaults + `blocked` + `needs-jon`), `.nojekyll`. Badges are shields.io only — never hand-made SVGs.
- Seed `docs/STORY-VERSIONS.md` (version tracker: drafts, dates, where each lives).

## Step 3 — Flipbook (bookshelf)
- Copy `templates/flipbook/` into the repo at `flipbook/`.
- Set `images/manifest.js` to the new book (cover + about placeholders until art locks) and the CATALOG to this book only — then import prior series books as contained shelf books (pages under `flipbook/shelf/<slug>/`, catalog id = the book's slug, `source: "built-in"`, `textBaked: true`, text + info carried from the book's final manifest).
- Set the `#shelfShowcase` href to the new showcase URL; set a project-unique storage-key prefix.
- **Port gate (mandatory, every flipbook change):** byte census of the change; cold-boot behavior probe in Chromium AND WebKit against the exact bytes (shelf renders, every book opens and turns a page, deep links boot, error set = baseline only); push; re-verify the LIVE bytes (md5) after the merge. A failed probe stops the ship.

## Step 4 — Showcase + spread review pages
- Start from `templates/repo/`; apply `templates/TEMPLATING-NOTES.md`.
- The shared ☰ menu ships from day one, same destinations in the same order on every surface: **bookshelf (gold) → spread review → showcase**. One menu button for everything — no separate gear/settings buttons in page chrome.
- Spread review pages are FROZEN snapshots (`spread-options-vN.html` + `review-assets/vN/`); the flipbook is always "current". Every version page carries the version dropdown listing all versions.
- Screenshots: refresh the repo hero/gallery whenever visuals change; stamp `?v=` on README image URLs (GitHub's image cache ignores same-path updates).

## Step 5 — Dashboard Space
Build the Muse dashboard from **docs/DASHBOARD-SPEC.md** in one pass — sections, actions, chrome, and the hard-won data rules (seed discipline, idempotent syncs, verify from data). Wire every link row to its live URL and audit the full list before calling it done.

## Step 6 — Cast system
- One recipe per character from `templates/CHARACTER-RECIPE-TEMPLATE.md`, filed in Drive (Recipes & Standards + Working Canonicals) and the repo's `cast/`.
- Portrait lock first, then the character board per **docs/CHARACTER-BOARD-STANDARD.md** (Harlow grid is the layout standard; decorated exemplar dress; footer finish line).
- Canonical naming: `<name>-cast-portrait-CANONICAL.png`, `<name>-cast-fullbody-CANONICAL.png`, `<name>-character-board.png`.
- Hi-res finals: real AI upscale only (Topaz High Fidelity V2, face enhancement OFF) → Drive Cast Finals. A plain resize is a preview, never a deliverable.

## Step 7 — Production (the part that stays human)
Story, author wording passes, cast locks, spread art — per **docs/BOOK-BUILD-BIBLE.md** and **docs/MASTER-PROCESS.md**. Standing commands from the Book 1 desk carry over: "Build new book" (local only) / "Patch book" / "Publish book" / "Flipbook: \<name\>" — see docs/BUILD-NEW-BOOK-SPEC.md and docs/FLIPBOOK-COMMAND-SPEC.md.
- Review passes run on **docs/REVIEW-CHECKLIST.md** + the spread-options system (**docs/SPREAD-OPTIONS-SYSTEM.md**); interior text follows **docs/TYPESET-STYLE-CARD.md** and is verified with **docs/TEXT-PASS-CHECKLIST.md**.
- Print masters are made and moved per **docs/HIRES-PIPELINE.md** (AI upscale only; md5 manifest on every set).
- Optional but recommended before ordering proofs: build the **physical mockup viewer** per **docs/PHYSICAL-MOCKUP-SPEC.md** — the bound-book reading experience, proofed on screen.
- Every page publish follows **docs/PAGE-POLISH.md** and the **docs/PUBLISH-GATE.md** four-part diff.

## Step 8 — Print (Lulu)
Covers designed on Lulu geometry from day one per **docs/COVER-START-SPEC.md** + **docs/LULU-SPECS.md** (Matte locked; full pack: **docs/PRINT-SPEC-PACK.md**). Only the spine band moves when the real template returns. The run itself follows **docs/LULU-RUN-CHECKLIST.md** with **docs/LULU-RUN-KNOWLEDGE.md** open beside it; open a per-book project sheet on the pattern of **docs/LULU-PROJECT-SHEET-EXAMPLE.md**. Proofs are ordered and checked per **docs/PROOF-ORDER-CHECKLIST.md**. At go-live, send the announcement from **templates/ANNOUNCEMENT-EMAIL-TEMPLATE.md**.

## Handoff checklist (what "done scaffolding" means)
- [ ] Drive homebase + START-HERE + shared inbox
- [ ] Repo + Pages + working branch + STORY-VERSIONS
- [ ] Flipbook live, port gate passed, prior books on the shelf if a series
- [ ] Showcase + spread review V1 live with the shared menu
- [ ] Dashboard built, links audited, log started
- [ ] Recipe files opened for every known character
- [ ] The only open items are story and artwork
