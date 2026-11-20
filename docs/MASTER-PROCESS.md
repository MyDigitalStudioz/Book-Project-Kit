# Harlow's Accidental Journey — master process

Final merged record, 2026-11-05 (Cursor draft + Trinity pass). Where a deeper file owns the detail, the rule is here in a few lines and the file is named. This document does not replace those files.

---

## 1. The book and the current state

Title: **Harlow's Accidental Journey**. Author Lois Farrell. Illustrator Jon Farrell. Two print formats, two Lulu projects, one interior.

| | Hardcover | Softcover |
|---|---|---|
| Project | `rmq8eyw` | `v854g55` |
| Lulu version | 4 | 3 |
| State | COMPLETE, Select Access | COMPLETE, Select Access |
| List / print | $26.00 / $22.58 | $16.00 / $13.76 |
| Binding | Hardcover Case Wrap, Matte | Paperback Perfect Bound, Matte |
| Buy link | https://www.lulu.com/shop/lois-farrell-and-jon-farrell/harlows-accidental-journey/hardcover/product-rmq8eyw.html | https://www.lulu.com/shop/lois-farrell-and-jon-farrell/harlows-accidental-journey/paperback/product-v854g55.html |

Both: Square 8.5 × 8.5 in, Premium Color, 80# White — Coated, 54 pages, no ISBN, no Global Distribution. Payee Jon Farrell, id `yjpmy9`, 100%. Buy links are bound to the project, not the version. A revision does not mint a new URL. Strip `?page=&pageSize=` before sharing.

Repo: `D:\Hermes\projects\Harlows-Big-Adventure`. Deliverables of record: `Xtraz\LuLu-Master-Deliverables\v3`. Upload only from `v3\03-Deliverables-PDF`.

Flipbook (56 pages). Current book: `flipbook-gold-v10` and `flipbook-master-v2`. Live gold URL: https://mydigitalstudioz.github.io/Harlows-Accidental-Journey/flipbook-gold-v10.html. `flipbook-master.html` is frozen at gold-v9 by Jon's call. It is not the current book. `LATEST.txt` in `Xtraz\Master-Review` says latest build and latest published are `2026-11-05-best23`.

v3 layout: `01` Photoshop sources, `02` packaged InDesign, `03` upload PDFs, `04` Lulu templates and previews, `05` project sheets and `HAJ-Links.md` (the links index), `06` flipbook gold-v10 and master-v2, `07-Proofs` proof copies, order records, and print notes. File list: `MANIFEST.md`. This run: `BUILD-REPORT.md`.

Open gate: physical proof copies have not been ordered. Files built, uploaded, held, and used for print match. The printed object is still unchecked.

**Deliverables version rule (Jon, 2026-11-05):** cutting a NEW version of this folder set (v4, v5, …) is a CLEAN REMAKE — newest-best files only, and every preview, render, and document inside is regenerated or updated to match the new state. Never carry forward copies of superseded art or stale docs (scar: v3\04 inherited v2's colon-byline cover previews because the folder was copied wholesale; fixed in place later the same day). A task that specifically targets an update inside the CURRENT version updates in place — that is the only exception.

A second copy of the three current PDFs sits in the Drive folder "LuLu-Deliverables" (root). Trinity hash-verified them on 2026-11-05: identical to the files Lulu holds.

## Standing commands — Jon's words

Four phrases are standing orders. Whoever hears one runs it as defined here and in `BUILD-NEW-BOOK.md`; the phrases never need re-explaining.

- **"Build new book Harlow"** — LOCAL ONLY. Full rebuild from the Photoshop sources (InDesign + both PDFs), flipbook staged under a provisional next gold number. Never pushes, never uploads.
- **"Publish book Harlow"** — pushes the latest build per `LATEST.txt` to the live gold + master-v2 lines. If latest build = latest published, it does nothing.
- **"Patch book Harlow"** — swap only the changed spread(s) into the published build, archive the set as `…-patchN-<spread>`, republish under the SAME gold version.
- **"Flipbook: <name>"** — Jon names it and supplies a folder of his own spread-width exports; Trinity writes the paste-ready Cursor prompt (spec: `FLIPBOOK-COMMAND-SPEC-2026-11-02.md`, Trinity's goal files).

Standing rider for all build work: Cursor may toggle layer and group visibility during a build; the saved visibility state of Jon's Photoshop files is never a stop condition, and visibility changes are never saved back into them.

## 2. Sources

The PSB is the only text authority. Lois's edits reach the book through Jon, including call edits that exist in no other file. Diff the PDF against the PSB. Do not "correct" the PSB from an older doc. Full rule: `BUILD-NEW-BOOK.md`.

| File | Where this build read it | Bytes | Saved |
|---|---|---|---|
| `HAJ-Interior-Spread-BEST-23.psb` | `Xtraz\Adobe-Photoshop\` (copy also in `v3\01-Source-Photoshop`) | 3,141,726,402 | 2026-11-05 12:23:58 |
| `HAJ-Cover-HARDCOVER-DESIGN-TEMPLATE-v3.psd` | `v2\01-Source-Photoshop\` (copy in `v3\01`) | 189,767,663 | 2026-11-05 11:25:45 |
| `HAJ-Cover-SOFTCOVER-DESIGN-TEMPLATE-v1.psd` | `v2\01-Source-Photoshop\` (copy in `v3\01`) | 203,194,740 | 2026-11-05 11:19:49 |

Never save Jon's Photoshop files. Toggle visibility only on a duplicate. A spread group's own eyeball is ignored. Renaming excludes a spread. Hiding it does not.

Build order, by name: Inside-Peek, then Spread-01 through Spread-24, then End-Dedication-Spread, then Cast-Spread. BEST-23 has all of those. Page count is 54. Anything else with picture or text layers stops the build, unless it is a known utility or a green or red label.

Labels, from the Action Manager `color` key. Green reads as `grain`. Red reads as `red`. Orange and none have no include or exclude meaning.

- Green on a top-level group: composite it into every plate, in panel order. It is not a spread.
- Red: never use, eyeball or not. Not a spread, not a plate, not a text frame.
- No label: the saved eyeball governs.

BEST-23: Default BG is the green include. Red exclusions are Seem-Shadow, 3D-FlipBook-Guides, Guides, Covers-BEST, and Spread-Pages-L-R-Sizes. The book groups are orange. Full table: `BUILD-REPORT.md`.

Plates are flattened composites, 5250×2625 at 300 ppi, type hidden. One plate per opening, from a duplicate, through Photoshop COM. The UXP bridge can be down and COM still works.

## 3. InDesign and tools

A full build makes a brand-new document. Do not open or patch an earlier indd. Patch mode is the only time the indd of record is relinked, and only for the named spread. Spec: `BUILD-NEW-BOOK.md`. Mechanics desk: `Xtraz\LuLu-Master-Deliverables\BOOK-BUILD-BIBLE.md` (its header still describes gold-v8; use this file for current state).

This run's documents, packaged with links and fonts (Andika, Caveat):

- `02-InDesign\Interior\HAJ-Interior-FROM-PHOTOSHOP-BEST-23.indd` — 27 plates, 94 live frames.
- `02-InDesign\Cover-HC-FINAL-JON\HAJ-Cover-HARDCOVER-FINAL-JON-v2.indd` — colon removed in the live frames, nothing else.
- `02-InDesign\Cover-SC-FINAL\HAJ-Cover-SOFTCOVER-FINAL.indd` — same.

Live type, from the character style (`textStyleRange`), never the paragraph default. A blind walk returns Myriad Pro and is wrong. Read the color from that same style. Do not fall through to Black. Story color in this PSB is RGB 46, 42, 36.

| Frame | Spec |
|---|---|
| Story | Andika 17/22 |
| Peek | Caveat 22, plus Andika 14 and Andika 12. This run: byline Caveat 22, intro Andika 14/22, copyright Andika 12/18 |
| Cover byline, front and back | Caveat 17/22. Published string: "Written By Lois Farrell" |
| Edition and design | Andika 13/18. Exactly two lines |
| Spine title | Andika 9/18, white, bottom to top |

Lift 7.65 pt. No extra nudges. Text frames follow the Photoshop line breaks.

Tools this pipeline actually uses:

- Photoshop COM on a duplicate, for plate export. Named in `BUILD-NEW-BOOK.md`. The Photoshop UXP bridge is optional. COM still works if that bridge is down.
- InDesign UXP MCP bridge on ports 19300 and 19301, for live frames and export. Named in `.cursor/docs/BOOK-2-TEMPLATE.md`.
- `tools\layout-mcp`, a junction to the TNIMS layout tools. Named in `.cursor/docs/CONTINUE-HERE.md`.
- InDesign exec (ExtendScript in the running app) is the other InDesign door. Never name an ExtendScript variable `name`.

PDF gates before a flipbook is staged: text diff against the PSB (words and forced breaks; extractor soft wraps are noise); every plate 5250×2625 from this PSB; quote codepoint sweep (this interior: U+2019 ×83, U+201C ×72, U+201D ×72, U+2014 ×16, no straight quotes, no U+FFFD); cover text counts; spine glyph margins equal within ±3 px at 300 dpi. `pdffonts` is the font gate when it is installed. It was not installed for BEST-23. The embedded names were read instead: Andika and Caveat on all three PDFs. This run's report does not include a new spine-margin measurement. The revision did not touch the spine frames; margins stand as verified on the original cover builds (softcover spine ink margins 10/9 px at 300 dpi).

## 4. Geometry

Interior page 2625×2625 at 300 dpi. Spread 5250×2625. PDF MediaBox 630×630 pt. TrimBox inset 9 pt, which is the 8.5 in trim. Bleed 0.125 in. Safety 0.5 in inside the trim. One plate across the opening, centered on the fold. Do not place left and right halves separately.

Hardcover wrap, from Lulu's template for `rmq8eyw`: 19 × 10.25 in, spine 0.25 in, page count 54. PDF MediaBox 1368 × 738 pt. The template's "book trim" line (8.75 × 9 in) is the case-wrap window, not the 8.5 in page trim.

Softcover wrap, from the project sheet for `v854g55`: 17.432 × 8.75 in, spine 0.182 in, centered. PDF MediaBox 1255.08 × 630 pt. Trim 8.5 × 8.5 in. Bleed 0.125 in.

Cover-start rule (checklist addendum, 2026-11-04): design on Lulu's real geometry. The spine is estimated and stamped ESTIMATE until the template returns. When a template returns, only the spine band moves. Art is never rescaled. The paragraph is in `05-Lulu-Project-Info\LULU-RUN-CHECKLIST-2026-11-04.md`. The longer spec it names (`COVER-START-SPEC-2026-11-04.md`) was not in this repo.

Spine: deep-blue gradient from the design file. Title "Harlow's Accidental Journey", apostrophe U+2019, Andika 9 pt, bottom to top. A returned spine at or above about 0.17 in keeps that title. Under 0.17 in, stop for Jon. Do not shrink or drop it unasked. Both current spines are above that line.

## 5. Covers

The plate hides all type. Every cover word is a live InDesign frame. The HAJ logo lockup is the one baked exemption. It is a painted graphic and is not re-typeset.

Wording, punctuation, and line breaks come from the PSD text layers, verbatim. BEST-23 then removed the colon in the live frames only: "Written By Lois Farrell" on front and back, twice per cover, "Written By:" zero times. The Covers-BEST group still contains the colon and is excluded. It is not an interior frame.

Place a rotated spine frame by its center, never by a corner. Centering the frame box does not center the glyphs. Judge the rendered PDF at 300 dpi. Pass is equal blue margins within ±3 px.

Back cover edition block is exactly two lines: "First illustrated edition - 2026." and "Book design by Jon Farrell."

## 6. Flipbooks

Build from the new interior PDF plus the cover faces. 56 pages, each 1750×1750: front, peek, spreads 01–24, end-dedication, cast, back. Front and back are the hardcover wrap windows (back x 188–2812, front x 2888–5512, y 188–2887 on the 5700×3075 render), scaled to the square. Interior pages are trim crops. `pages-data.js` is in the set and is loaded before `startFlipbook()`. Header on this gold: "Updated HAJ Print-Review v10".

Gold versions freeze. A new publish adds the next `flipbook-gold-vN` and does not rewrite older gold folders. `LATEST.txt` has two lines. "Latest build" moves on every build. "Latest published" moves only when a gold version is pushed.

Publish target: `MyDigitalStudioz/Harlows-Accidental-Journey`. Working branch `Harlows-v2`. `main` is the published branch, synced from `Harlows-v2`. Note from the BEST-23 run: the flipbook sets were published straight to `main` (commit 9397c08) — the flipbook does not live on `Harlows-v2`, so there was nothing to merge. Treat direct-to-main as the flipbook publish lane unless the branch layout changes. Do not commit to `Harlows-v1`. Stage with `git add --sparse` or the new images never commit. Verify by a hash match after the Pages status is "built", not by a page load. Full command: `BUILD-NEW-BOOK.md`. Book builds never touch the 3D-Flip-BookVizon repo.

## 7. Lulu

Creation goal gates the forms. "Print Copies for Your Own Use" has no metadata, no pricing step, and Private Access only. The forms are absent, not locked. A book that will be sold from a link is created under **Publish Your Book** plus **Lulu Bookstore**, with Global Distribution off. Switching later is Revise, then Start, then Select a Goal, then price, then Select Access. Harlow hardcover was created under personal printing and switched on 2026-11-05. Future projects start on the final goal. Two clauses this desk could not open a file for are CONFIRMED by Trinity from the Drive record (Playbook §35 + `LULU-RUN-KNOWLEDGE-2026-11-05.md`): **payees do not inherit into a new project** — the softcover project had none until Jon Farrell was attached explicitly at publish; and **Lulu did not auto-convert the softcover's prices** — USD alone did not persist, and all five were hand-filled from the print minimums (list USD 16.00 / EUR 15.41 / AUD 24.16 / GBP 12.47 / CAD 24.47). The hardcover's goal-switch pass DID auto-convert — behavior varies by path, so always read all five before publishing.

Specs, both projects: Square 8.5 × 8.5, Premium Color, 80# White — Coated, Matte, 54 pages. Hardcover Case Wrap. Softcover Perfect Bound. The ink warning on an illustrated book is normal. Stay on Premium Color.

Upload from `03` only. Replace the interior, then the cover. Do not click ahead while a bar is moving. A green "uploaded" banner and a page count are not proof the file is normalized. Confirm and Publish once, then wait. The cart that works is https://www.lulu.com/cart. If a run dies, open My Projects before creating anything.

Revision traps, from the BEST-23 publish. Full write-up: `.cursor/docs/LULU-BOOKSTORE-SELECT-PLAYBOOK.md`, section "Revising a book that is already published." Vault copy: `H:\Vader_Vault\02_Knowledge\Patterns\Lulu-Bookstore-Select-Playbook.md`.

- Revise is the navy button. Retire is the cyan button under it. Cancel a Retire dialog. Nothing is retired if you cancel.
- A new interior clears the spec radios and sets the cover back to pending. Re-select the same spec. Do not upload the cover again if the filename is already right.
- Validated is not normalized. Softcover needed a second upload of the same interior, then the spec again, then Confirm List Price on the unchanged numbers.
- Read the print cost before leaving Design. It must be $22.58 or $13.76.
- The My Projects card is the proof: new version, COMPLETE, Select Access, same prices. The success banner is not the proof. Do not click Order Copies.

Select Access means unlisted. The link works. The book is not in Bookstore search. General Access is the public switch. Private has no share link.

## 8. Verification

Before upload: the byte size is the identity. Upload the verified file. Do not export a fresh PDF and upload that instead.

After publish, project pages do not show file names or sizes. Download the files back.

| Button | What it is |
|---|---|
| Source Files | The original uploads. Original names. Byte-exact sizes. |
| Print-Ready Files | What the press prints. Renamed to the project id. Part of the check. |

Then: sizes exact; SHA-256, and a shared interior must match in both projects; a token-diff against the previous published interior, limited to the approved changes; cover text counts; `pdfinfo` page count and geometry; render spot-checks trim-aligned. The MediaBox includes the 9 pt bleed. An unaligned diff false-alarms. An identical S09-L read 31.7 raw and 6.7 trim-aligned. The aligned figure is recompression noise. Normalization here was a few KB and at most 0.12 pt. Content-identical is the standard.

BEST-23, checked by Trinity on 2026-11-05. Source interior 65,008,627 bytes in both projects. SHA-256 `d6a8807af1dcb8277b1fc3abc8823090d873db91b79f25255ab3700ed8ccfea6`. Hardcover cover 5,027,947 bytes. Softcover cover 4,091,305 bytes. Print-ready text against published BEST-22: exactly two tokens, in both multiset and ordered comparisons. Peek `By:` became `By`. Spread 22 left `sites` became `sights`. All four cover PDFs: byline twice, colon byline zero. Interiors 54 pages, 54 images, 630×630 pt. S09-L from the print-ready file matches Jon's new plate.

Vader's browser publishes. Trinity's browser is the read-only check. Cloudflare can block either one.

## 9. Pointers

| Doc | Owns |
|---|---|
| Playbook on Drive, Trinity | Design, canon, and the system. Drive file `1KuYAx5e1SRfaKGJKBTIVWzYAOhKbMeYQ`; §35 + Addendum 2 carry the Lulu publish + revision law. Local mirror in Trinity's Harlow goal files. |
| `Xtraz\LuLu-Master-Deliverables\BOOK-BUILD-BIBLE.md` | Build mechanics. Header is behind this run. |
| `.cursor/docs/LULU-BOOKSTORE-SELECT-PLAYBOOK.md` and the vault copy of that note | Store process, revision traps, Trinity's download-back. |
| `BUILD-NEW-BOOK.md` | The build, publish, and patch command. |
| `v3\BUILD-REPORT.md` and `v3\MANIFEST.md` | This run's record and file list. |
| `LULU-RUN-KNOWLEDGE-2026-11-05.md` | The Lulu run + revision knowledge note. Drive bridge inbox, file `1hIefKeVeZcARbUgKYawUSkEorXi9yvYk`; copy in Trinity's Harlow goal files. |
| `COVER-START-SPEC-2026-11-04.md` | The cover-start rule in full. Trinity's Harlow goal files; summarized in Playbook §34 and the v3 checklist addendum. |
| `v3\05-Lulu-Project-Info\` | The two project sheets, the run checklist, and the note to Lois. |

## 10. Canon, style, and the people side (Trinity's desks)

- **Canon source:** the Drive Character Recipes folder is the ONLY cast authority. Never brief, render, or typeset from a name or from memory. Cast briefs attach the character's approved portrait and paste the recipe's NEVER CHANGE lines verbatim; when two approved sources conflict, flag it to Jon BEFORE generating (JJ's likeness = the approved author's-note porch art — dark brown curls, freckles — over the recipe text; the cast page's label for the boy reads "Jon" by Jon's deliberate choice — never flag it).
- **Style governance:** govern every revision directly off that spread's original approved keeper frame; never chain revisions off sibling takes; compare at whole frame before delivery. Restraint is the book's hand — gentle, believable expressions, no over-animation.
- **Failed-patch rule (locked):** patch only isolated damage. If a patch round still leaves errors, or the damage is in several places, stop patching and generate a new image; audit the whole element at 1:1 before calling anything final.
- **Hi-res rule:** deliverables are 5250×2625 (spreads) from a real AI upscale (Topaz High Fidelity V2, face enhancement off — or Jon's Gigapixel). A plain resize is a preview, never a deliverable. Soft/washy end-matter art is the one exception: Topaz at 30% over the plain upscale ("Soft 30").
- **Provenance guard:** never brief, typeset, render, publish, or email from a text or image claim that has not been re-read in its source file in the same session.
- **People:** Lois's role is deliberately light — she gets finished things to enjoy and one simple list for notes; all decisions run through Jon. Lois-facing sales talk is Lulu, Amazon, retail only — BookVizion is never mentioned to her. Future Amazon lane (discussed, not locked): paperback via KDP with Lois's own ISBN as publisher of record; KDP cannot print this hardcover (no 8.5×8.5; 75-page minimum vs 54).

## Retired, one line each

- Temp-spine canvas (17.5 × 8.75 in, 5250×2625 cover page): retired 2026-11-04. Covers now start on the real Lulu geometry. The standing spec still describes the old canvas. Do not use it for a new cover.
- Personal-printing goal ("Print Copies for Your Own Use"): retired for any book that will be sold from a link. It hides metadata, pricing, and Select Access.
- Paste-to-publish board flows: retired. The PSB is the text authority. Older paste packets and Rev.19 are history, not checkers.
- BEST-3 as a cover BUILD source: retired 2026-11-04. It and its softcover twin survive as temp-spine references only; covers build from Jon's design-template PSDs.
- Wholesale folder copies for a new deliverables version: retired 2026-11-05 (see the version rule in §1).
