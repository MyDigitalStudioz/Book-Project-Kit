# Book Project Kit — Manifest

Version **1.2.3** · Assembled 2026-11-20 (Pass 2 harvest + starter project added the same day) · 1.2.1 refinement pass 2026-11-20: board pre-flight self-check + likeness governance folded back from the live Book 2 board rebuild · 1.2.2 refinement pass 2026-11-20: the production-notes sweep system (starter ships a blank PRODUCTION-NOTES.md; the currency rule below names it as the sweep input), cast folder roles completed (Archive + one-master rule, DRIVE-TREE-SPEC), real-person reference authority + upload banking check (CHARACTER-BOARD-STANDARD) — all from Harlow's Helping Paws · 1.2.3 refinement pass 2026-11-20: the full HHP cast-production sweep — the full-body gate, cast tiers incl. group/family sets, pair differentiation at reading size, board profile-orientation check, per-face board carry-over + printed-trait re-typeset, terminal marks taper/fade, recipe-scrub + designer-invention + copy-matches-art rules, author's-placeholder-art rule, cast census (search wide, then ask), hi-res lock + single end-of-cast batch (HIRES-PIPELINE), review lightbox guides (SPREAD-OPTIONS-SYSTEM), shelf tile identity + curated shelf order + flatPairs real-cover rule (BOOK-BUILD-BIBLE), environment scenes + two-space governance (DASHBOARD-SPEC), showcase presentation — portrait-lead + full-body toggle, place cards, same-site/external link rule, manuscript button (PAGE-POLISH), Drive-mirror-as-homing (DRIVE-TREE-SPEC) — all from Harlow's Helping Paws · Proven on *Harlow's Accidental Journey* (Book 1) and *Harlow's Helping Paws* (Book 2)

One index of every component in the system, where its canonical copy lives, and what it's for. The kit has two homes that mirror each other: this repo (code + specs) and the **Book Project Kit** folder in Google Drive (the document side). The master Playbook's canonical copy is the Google Doc; a copy rides in the Drive kit folder.

## Start here
| Component | Where | Purpose |
|---|---|---|
| RUNBOOK.md | repo root | The "New book project" procedure — the automation, step by step |
| MANIFEST.md | repo root + Drive kit folder | This index |
| Picture-Book Production Playbook | Google Doc (master) · copy in Drive kit folder | The production method end to end |

## Specs (docs/)
| File | What it governs |
|---|---|
| MASTER-PROCESS.md | The overall book-production process from the Book 1 desk |
| BOOK-BUILD-BIBLE.md | Build rules for layout, PDFs, and the flipbook line |
| BUILD-NEW-BOOK-SPEC.md | The "Build new book / Patch book / Publish book" standing commands |
| FLIPBOOK-COMMAND-SPEC.md | The "Flipbook: \<name\>" standing command |
| COVER-START-SPEC.md | Cover design on Lulu geometry from day one (locked) |
| LULU-SPECS.md | Verified Lulu numbers: trim, bleed, safety, finishes, viewer guide spec |
| CHARACTER-BOARD-STANDARD.md | Character Board format, grid lock, dress lock, footer line |
| DASHBOARD-SPEC.md | The per-book Muse dashboard: sections, actions, data rules |
| DRIVE-TREE-SPEC.md | The Drive homebase folder tree + manuscript rules |
| SPREAD-OPTIONS-SYSTEM.md | The system behind the final-pass / spread-options review pages (from the Book 1 repo) |
| REVIEW-CHECKLIST.md | The book-desk review pass checklist |
| TYPESET-STYLE-CARD.md | Typesetting style card for interior text |
| TEXT-PASS-CHECKLIST.md | Post-text-pass verification checklist (text of record discipline) |
| PHYSICAL-MOCKUP-SPEC.md | The bound-book mockup viewer: leaf order, flyleaves, turn checks |
| HIRES-PIPELINE.md | Print masters: AI-upscale route, byte-exact handling, md5 manifest rule |
| PRINT-SPEC-PACK.md | The full print specification pack behind the LULU-SPECS quick card |
| LULU-RUN-CHECKLIST.md | The Lulu publishing run, step by step |
| LULU-RUN-KNOWLEDGE.md | Hard-won Lulu knowledge from the Book 1 run |
| LULU-PROJECT-SHEET-EXAMPLE.md | A filled Lulu project sheet (Book 1 hardcover) — the pattern for per-book sheets |
| PROOF-ORDER-CHECKLIST.md | Ordering and checking printed proofs |
| PAGE-POLISH.md | Share-preview leanness, cache-busting, screenshot discipline for project pages |
| PUBLISH-GATE.md | The four-part pre-publish diff + one-source-of-truth rule |

## Templates (templates/)
| Path | What it is |
|---|---|
| **starter-project/** | **THE SCAFFOLD — copy this whole folder to start a book.** Bare-bones working project: skeleton showcase + spread review V1 + one-book flipbook on labeled placeholder art, Lulu specs carried in-project (PRINT-SPECS.md), generic storage prefix (`bookproj-`). Probed end-to-end before shipping; its README lists the make-it-yours steps in order. |
| repo/index.html | Showcase page — reference implementation (HHP) |
| repo/spread-options-v1.html | Spread review page — reference implementation (HHP) |
| flipbook/ | The COMPLETE BookVizion bookshelf build (two-book capable, top-bar icon fix included) + preview images + manifest + `vendor/` + `icons/` + `manifest.webmanifest` — the support files are part of the build; the app 404s without them |
| CHARACTER-RECIPE-TEMPLATE.md | Per-character recipe skeleton with the standing §5 look + background standard |
| ANNOUNCEMENT-EMAIL-TEMPLATE.md | The launch email (Jon's Book 1 wording, generalized): links, honest cost breakdown, flipbook twin |
| TEMPLATING-NOTES.md | Every per-book variable in the templates, marked |

## Referenced, not copied (living homes elsewhere)
| Component | Where it lives | Why it's a pointer, not a copy |
|---|---|---|
| BookVizion Admin app | `BookVizion-Admin` repo (hPanel deploy lane) | A living app with its own deploy discipline; the kit's flipbook is its data source |
| Book 1 final-pass pages | https://mydigitalstudioz.github.io/Harlows-Accidental-Journey/final-pass-v12.html | The review pages' ancestor implementation — the method is in SPREAD-OPTIONS-SYSTEM.md; the file itself is Book 1's frozen record |
| Sales & pricing picture | Book 1 desk files (HARLOW-SALES-AND-PRICING-PICTURE, SALES-LANES-PREP) | Business-side planning, partly superseded per book; the Playbook carries the durable parts |
| Gradient fade technique | Book 1 desk file GRADIENT-FADE-SPEC | A single layout technique, referenced from the build bible's world |
| START-HERE worked example | The HHP Drive homebase | DRIVE-TREE-SPEC states the pattern; HHP's folder is the living example |

## Standing rules that travel with the kit
- Bookshelf over links: series books live contained on the shelf, never linked out to another project.
- One ☰ menu, same destinations in the same order, on every surface.
- Port gate on every flipbook change; publish gate (four-part diff) on every design publish.
- "Hi-res" means a real AI upscale — never a plain resize.
- Review pages are frozen snapshots; the flipbook is always current.
- A full body locks only through the full-body gate: whole-frame style verdict against its portrait, measured proportions, build check (CHARACTER-BOARD-STANDARD).
- A book's shelf tile always shows that book's own cover; cover resolution never branches on which book is open (BOOK-BUILD-BIBLE §6).
- Hi-res masters run once, as a single batch, after the cast is locked — never piecemeal, never for un-locked work (HIRES-PIPELINE).
- The author's manuscript file is the manuscript of record; the author's side stays light.
- **Kit currency (Jon, 2026-11-20):** when a live project teaches a refinement — a new gate, a corrected method, a failure turned into a rule — fold it back into the kit's docs the same session, bump the patch version, and note the source project. **The mechanism:** every live project keeps a `PRODUCTION-NOTES.md` kit-feed log at its root — each refinement is entered there the session it is learned, with a status. A kit update SWEEPS that log: every PENDING KIT entry is folded into the kit docs or explicitly parked, then stamped in the log with the kit version that took it. Entries are never deleted; the log is the audit trail of how the kit got better. The kit must never lag the desks; a stale kit is how the next book regenerates the wrong boards.
