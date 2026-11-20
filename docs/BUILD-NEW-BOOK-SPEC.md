# BUILD NEW BOOK — standing build spec (Harlows-Big-Adventure project)

Keywords: **"Build new book"** = full rebuild (this spec), in this project. From Jon's JonBeatz window the trigger is **"Build new book Harlow"** (names the book); a plain "Build new book" there with a Harlow PSB open/active means this book too. **"Patch book — <what changed>"** = single-spread tweak (Patch mode, below). When Jon says either, run it end-to-end without asking for details. Seeded 2026-11-01.

## Amendments adopted 2026-11-01 (Cursor's recommendations, Jon approved)
1. Text verification compares WORDS + Photoshop's forced breaks and ignores PDF-extractor soft wraps ("Gideon the / pigeon" is extractor noise, not a change). A soft-wrap difference never stops a build.
2. Cover geometry: the cover page is 17.5 × 8.75 in, bleed 0 — bleed and the 0.25 in spine are already inside the Photoshop canvas; the cover PDF is the text-visible wrap edge to edge. NEVER use the Lulu interior preset (8.75 square) on the cover. Flipbook faces are trim crops of the wrap: back on the left, front on the right, spine excluded. Cover text frames get the same 7.65 pt lift.
3. Fonts are read from the character style (textStyleRange), never the layer/paragraph default (which falsely returns Myriad Pro). The set: story text Andika 17/22 · inside-peek Caveat 22 + Andika 14 and 12 · cover byline Caveat 17/22 · edition line Andika 13/18.
4. Plate export runs through Photoshop COM on a DUPLICATE of the file (the UXP bridge can be down while COM works). Never save the original, even when it's already dirty from toggles. In ExtendScript, never name a variable `name` — it resolves to "Adobe Photoshop" and kills the export.
5. InDesign runs are confirmed by the FILES ON DISK, not the tool's return — a long build may return a numeric COM code or time out while the document and PDF finish. Never start a second create while the first may still be running.
6. Publish verification is a HASH match, not a page load: wait until the Pages build status is "built", then match the live front-cover and S13 files to the local files. In the gold clone, stage with `git add --sparse` or new images never get committed. Never upload pages-data.js to that repo. Never commit the PSB, the PDFs, or the Master-Review folder unless Jon asks.

## How the build actually works (Cursor's Job 4 answers, 2026-11-01 — documented for Trinity)
- **Layer walk:** the PSB is read from the top level of the Layers panel. A spread = a top-level group named `Inside-Peek` or `Spread-<number>`; order is by that number with Inside-Peek first, NOT panel order. NOT spreads: `Spread-Pages-L-R-Sizes`, `Guides`, `Covers-BEST`, the shadow, the vignette, `Default BG`. A "plate" is not a layer — it's the JPEG rendered after showing that one group. A text layer = a real (non-outlined) text layer inside the group.
- **Visibility:** the GROUP's own eyeball is IGNORED; each layer INSIDE keeps Jon's saved eyeball. Default BG and the vignette are forced on for the composite. Consequence: hiding a spread group does NOT exclude it from the build — only its name does. The "genuinely broken" stop = with group + Default BG + vignette on and inner layers as saved, the composite still has no illustration.
- **Alternates:** NOTHING chooses between variants (e.g. `s02` vs `s02-NoLights`) — names are never read. If both are on, both print; the upper layer paints over the lower. **The visible composite is the selection.** What Jon sees in Photoshop is what prints.
- **Plate export:** a flattened JPEG of the visible composite at the file's native size — 5250×2625 @300dpi. The 0.125 in bleed IS the canvas (17.5×8.75 in already includes it). No cropping, no padding.
- **Text frames:** words from the text layer; a PS forced break becomes an InDesign forced LINE break (not a new paragraph). Frame corner = the text click point as a % of the 17.5×8.75 canvas; frame size = the paragraph box (~534×464 pt here), not the ink. Left edge left of the fold → left page, else right page. After snugging the frame to its last line, the 7.65 pt lift moves top and bottom up together. Cover frames: same lift. Plates are exported with type HIDDEN — text exists only as InDesign frames (no double-printing).
- **TEXT COLOR — GAP FOUND AND FIXED (2026-11-01):** the interior build originally read font/size/leading from the character style but NOT color, so builds through BEST-10 shipped interior text as InDesign Black vs Jon's PSB warm brown **RGB 46, 42, 36 (#2E2A24)**. **Jon adopted Cursor's fix the same night (spec: Interior build line 38 — per-frame color from textStyleRange, never hardcoded; Build verification line 55 — spot-check one frame and report both values; Report back line 95) and ordered an immediate rebuild → gold-v4.** The cover build already read color per frame.
- **Assembly:** ONE image per spread placed across facing pages (not two page images). Pages are facing 8.5 in squares + 0.125 bleed; numbering starts at 2 so the first page is a LEFT page. The fold = the left page's right edge; the image's center (PS fold, x=2625) is set on that edge; it hangs 0.125 past the outer bleed on both sides.
- **Cover face crops — FIXED GEOMETRY, hardcoded to the 5250×2625 wrap:** fold x=2625; spine 75 px (±37.5); bleed 37.5 px. Back face = x 37.5→2587.5, front = x 2662.5→5212.5 (2550 px each), resized to 1750. Faces come from the text-visible wrap. **A different-sized cover canvas would crop the wrong faces and still publish.**
- **Front matter:** same pipeline. Inside-Peek is first only because of its name; signature/intro/copyright are ordinary text layers; the painted title treatment is ART in the plate, not a live frame. No copyright-page detector exists.
- **Exported PDF internals (verified on BEST-10, 2026-11-01):** the Lulu PDF does NOT store 25 whole-spread images — InDesign splits each placed spread at the fold, so the PDF carries **50 page JPEGs at ~2634×2625 px each (300 dpi at the 8.75 in bleed page; the ~9 px extra width is fold overlap)**. Full resolution confirmed, no downsampling. BEST-10 interior PDF = 60,508,003 bytes (Windows: 59,090 KB) — that size is CORRECT for full-res plates JPEG-compressed (uncompressed would be ~1 GB). **Export preset (verified 2026-11-01): `Lulu-Interior-Print-PDF.joboptions` — JPEG quality Maximum (QFactor 0.15), 4:4:4 (no chroma subsampling), downsampling only above 450 ppi → 300 (plates are exactly 300, so NONE occurred); measured embedded quality 92–93 on all 50 pages. Cover PDF: not an InDesign-preset export; embedded JPEG quality 99. Both deliverables are at the top of what JPEG offers — lossless ZIP would only multiply file size with no visible print gain. Ship as-is.**
- **Silent-failure flags (Cursor, proposals only):** (1) a top-level group not named Inside-Peek/Spread-N is DROPPED and the build still finishes; (2) a lights layer left ON above a NoLights layer prints the lights — the name doesn't save it; (3) cover crops hardcoded per above; (4) outlined type has no text layer → never becomes a frame, and the text check still passes (the words print only if visible in the plate composite).
- **COLOR-LABEL RULES LIVE (Cursor confirmed 2026-11-01):** the export path CAN read PS layer color labels; Photoshop's green reads back as **"grain"** (internal enum) and the spec is written against the actual read values. GREEN (top-level group) = global include into every spread's plate in panel order + exempt from the unknown-group stop; never makes a spread. RED = never use: red top-level group excluded entirely (even if named Spread-NN) + exempt from the stop; red layer inside a spread treated as off even if eyeball on (red text layer = no frame, not counted). Report lists greens applied + reds excluded; merely-off layers get no line. Green inside a spread = no meaning. **Interior file only — the cover file's labels are NOT covered; cover needs its own spec line before labels mean anything there.** LABEL STATE of Jon's BEST-10 PSB at adoption: utility groups RED (correct — never use), Inside-Peek + Spread-01…24 ORANGE (no build meaning; name governs — correct), vignette ORANGE (not forced on under the new rules), **Default BG — FIXED by Jon 2026-11-01 ~21:50 (screenshot-verified): relabeled GREEN; its composite = the warm ivory layer (only inner layer with eyeball on). Vignette: Jon left it ORANGE and off — undecided; he'll green it if he wants it on every plate. Cover PSD: Jon directed 2026-11-01 that the color rules apply to the cover file too — **extension CONFIRMED LIVE by Cursor the same night with ZERO conflicts**: cover rules sit in Build—cover; red text layers are out of the cover frame count too; the label read on BEST-2 matched tonight's build exactly (red = 02-LULU-GUIDES, Spread-Pages-L-R-Sizes + its two pictures, all already excluded; no green labels on the cover, so nothing off gets forced in; eyeballs otherwise match — old front art, Amazon barcode, QR codes off).**
- **GUARDRAILS ADOPTED (Jon, 2026-11-01):** (a) the build report lists EVERY top-level group with its disposition (built as spread N / excluded by name); a top-level group that is not a recognized spread and not a known utility group (Guides, Covers-BEST, Spread-Pages-L-R-Sizes, Default BG, shadow, vignette, 3D-FlipBook-Guides — added 2026-11-01 after Cursor's dry check flagged it in BEST-10; it holds picture layers but is a guides group, not a page) but contains picture or text layers is a STOP condition; (b) the cover canvas must measure exactly 5250×2625 before face crops are taken — any other size stops the cover build; (c) the report carries per-spread text-frame counts and the total (BEST-10 baseline: 49).

## Sources
- The LATEST interior PSB and cover PSD in Xtraz\Adobe-Photoshop, by pattern: `HAJ-Interior-Spread-BEST-*.psb` and `HAJ-Cover-Front-Back-TempSpine-BEST-*.psd` (highest version number; tie-break by most recently modified). Never the Master-Review archive copies.
- State the exact filenames + modified times in the report. If the latest is ambiguous, stop and ask — that's the only source question allowed.

## Text authority (Jon, 2026-11-01)
- The PSB is the sole and final text authority for the book. Lois's edits reach the book through Jon — including edits from phone calls that exist in no email, doc, or PDF anywhere. A change with no paper trail is still a real change when it's in the PSB.
- NEVER flag, question, correct, or revert PSB text because it differs from Rev.19, the paste packet, the LF notes, or any older document. Those are historical references, not checkers. Differences from them are expected and legitimate.
- The build verification diffs the PDF against the PSB only — never the PSB against an older document.
- When Jon says a build includes call-entered edits, BUILD-NOTE.txt records it: "Includes text edits Jon entered directly from his call with Lois, <date>."

## Visibility (Jon's standing permission)
- Toggle layer / spread-group visibility freely during the build, as in previous builds: turn each spread set on, export it, move to the next.
- The saved visibility state is never a stop condition — Jon works with sets toggled; a picture layer off in the saved file is NOT excluded from the book.
- Toggle in your working session only; never save visibility changes back into Jon's Photoshop files. In general: work from copies / your own session — NEVER save over Jon's Photoshop files for any reason.
- The composite governs: each spread exports as it looks with its full set on.

## Build — interior (InDesign, brand new every time)
- New document named after the PSB: `HAJ-Interior-FROM-PHOTOSHOP-<ver>.indd`. Never open, copy, derive from, or patch an earlier .indd.
- Specs: 8.5in trim + 0.125in bleed; text frames matching the Photoshop line breaks; 7.65pt lift; no nudges.
- Place EVERY art plate from the PSB at full resolution, exactly as composited — no substitutions, no plates from archives or earlier builds.
- Set ALL text from the PSB only — every word, every line break, apostrophes as they stand in the file. Never retype from Rev.19, the paste packet, or any older document.
- Export `HAJ-Interior-FROM-PHOTOSHOP-<ver>-LULU.pdf`.
- Report the interior page count; never silently add or drop pages (no cast bonus page unless it's in the PSB).

## Build — cover (InDesign, brand new every time)
- New document named after the PSD: `HAJ-Cover-Front-Back-TempSpine-<ver>.indd` — front + back + spine from the PSD only.
- Export `HAJ-Cover-Front-Back-TempSpine-<ver>-LULU.pdf`.
- If an output filename already exists, move the old one aside as `*-superseded` (never silently overwrite) and note it in the report.

## Build verification (self-check, before anything publishes)
- Diff the exported interior PDF's text against the PSB's text, spread by spread. Any difference = stop condition.
- Confirm every placed plate is the full-resolution export from the PSB (dimensions 5250x2625 per spread). Any plate that isn't = stop condition.

## Flipbooks (from the new PDFs)
- Render the full page set at 1750x1750: front cover, inside-peek L/R, all spreads as L/R pages in book order, back cover.
- GOLD VIEWER (the only flipbook output): the build stages the viewer LOCALLY in the run folder under the PROVISIONAL next gold number (highest `flipbook-gold-v*.html` in MyDigitalStudioz/Harlows-Accidental-Journey + 1), same viewer as the current version, header exactly "Updated HAJ Print-Review v<N+1>", manifest = `<PSB version>-<date>` (e.g. BEST-10-2026-11-01). **BUILD/PUBLISH SPLIT (Jon, 2026-11-01 night): "Build new book" NEVER pushes to the repo — publishing is the separate "Publish book Harlow" command (see Publish). The provisional number becomes real only at publish; a discarded draft consumes nothing.**
- The standalone 3D-Flip-BookVizon repo/site is a SEPARATE project (Jon, 2026-11-01) — book builds and patches NEVER touch it, sync to it, or report on it.

## Publish — "Publish book Harlow" (separate command, Jon 2026-11-01)
- Publishing NEVER happens inside a build. "Publish book Harlow" takes the latest build (the "Latest build" line of LATEST.txt), and if it is not yet published, pushes its staged flipbook files to MyDigitalStudioz/Harlows-Accidental-Journey as `flipbook-gold-v<N+1>.html` + `flipbook-gold-v<N+1>/` (the provisional number the build staged under), appends a "Status: PUBLISHED as flipbook-gold-v<N+1> on <date> — <live URL>" line to that run's BUILD-NOTE.txt, and updates LATEST.txt's "Latest published" line.
- If the latest build is already published, there is nothing to do — report that, never publish the same build twice or burn a second number on it.
- Phrase rows for "Publish book Harlow" live in BOTH windows' maps (JonBeatz + Harlow project), same as the build phrases.

## Publish guards (hard)
- flipbook18.html: the freeze was LIFTED by Jon 2026-11-01 (Lois views the book on the new gold pages now). The file is retired, not protected — builds simply ignore it; no build step checks it. (It stays in the repo untouched as a courtesy, but nothing depends on it.)
- Previous gold versions stay exactly as-is. New versions are new files only.
- Verify live after pushing: gold page loads, correct "Updated HAJ Print-Review" header, full page count, spot-check the front cover and S13. Report each check by name.
- Pages stall remedy: if the new gold page still serves the stale build ~5 minutes after the push, push one trivial nudge commit to main and re-verify once before declaring a verification failure.

## Archive
- Copy ALL new files (interior .indd, cover .indd, both PDFs, the flipbook) to `D:\Hermes\projects\Harlows-Big-Adventure\Xtraz\Master-Review\<YYYY-MM-DD>-<psb version lowercase>\` (e.g. 2026-11-01-best10).
- ONE FOLDER PER BUILD RUN — never dump a build into an existing folder. If that folder name is already taken (same source version built again the same day), append a run number: `-r2`, then `-r3` (e.g. 2026-11-01-best10-r2). The highest run number is the newest build of that version. State the exact folder used in the report.
- Every run folder gets a BUILD-NOTE.txt: sources (names + modified times), versions, interior page count, PDF sizes, the run timestamp, and a Status line — "NOT PUBLISHED (provisional flipbook-gold-v<N+1>)" at build time; the publish step appends its PUBLISHED line. The folder explains itself.
- Maintain LATEST.txt in the Master-Review root with TWO lines: "Latest build: <run folder>" (updated on every build) and "Latest published: <run folder> — flipbook-gold-v<N> — <live URL>" (updated only by a publish). Patch mode reads the Latest-published line — it patches the build that's actually live; a patch run also archives its own run folder, which becomes Latest build, while the gold number stays put. **Split CONFIRMED INTEGRATED by Cursor 2026-11-01 ~22:43 (spec lines 7, 59–62, 65–73, 75–79, 84–85; phrase rows in both workflow.mdc files; LATEST.txt converted: Latest build + Latest published both = 2026-11-01-best10-r2 / flipbook-gold-v4).**

## Patch mode — "Patch book — <what changed>"
For a single-spread fix (a new image, a text tweak) after a good full build — do NOT rerun the whole book. (Precedent: the S13 patch on gold-v2.)
- Jon names the spread and the change; the change is already in the Photoshop source (he seats plates / edits text in the PSB himself) or he states the exact text change to make in the PSB first. The PSB stays the source of truth — never patch the InDesign file alone.
- Update ONLY the affected pieces:
  1. Re-export the affected spread from the PSB (visibility rules above apply).
  2. Interior InDesign of record (the one in the latest Master-Review run folder): replace that spread's plate/text, save.
  3. Interior PDF: re-export; only the changed pages should differ — verify that.
  4. Viewer: re-render just that spread's two page images (1750) and swap them IN PLACE in the current gold viewer version (same version, same URL, header unchanged — a fix to the current version, not a new version).
  5. Archive: a new Master-Review run folder (next `-rN` under the folder rule) holding the updated full file set + a PATCH-NOTE.txt naming the spread, the change, and the date — AND the replaced pre-patch page images saved as `*-before*` copies, so any patch can be rolled back in minutes. Update LATEST.txt.
- Verify live: the changed spread in the gold viewer; spot-check that a neighboring spread is untouched.
- Report: what changed, which files/pages were updated, the archive folder, live verification.
- If the "one change" actually touches more than two spreads, stop and say so — that's a full build, Jon's call.

## Stop conditions (the only ones)
- Source files missing or ambiguous.
- A spread's composite is genuinely broken (art missing even with its full set on).
- The build verification fails: PDF text differs from PSB text on any spread, or a placed plate is not the full-resolution PSB export.
- A live verification fails after the push (after the one nudge-commit remedy for a Pages stall).
Otherwise: run end-to-end, no mid-build questions.

## Report back
Source files (names + modified times) · interior page count · both PDF sizes · flipbook version published + page count · Master-Review folder path · live verification results for the gold page · any *-superseded files · anything that didn't match this spec.

---

## AMENDMENT 2026-11-04 — COVER LIVE TYPE (learned the hard way, gold-v7 cover saga)

The cover follows the SAME type rule as the interior: the plate is art with ALL type hidden, and every cover text element is re-set as a LIVE InDesign frame. (Before this amendment the cover exported as one flattened composite — every gold cover through v7 shipped with ZERO live text; pdffonts empty. The HAJ logo lockup is the one exception: it is a painted graphic, baked by design, never re-typeset.)

Cover live frames: spine title (Andika 9/18, white, bottom-to-top), "Written By: Lois Farrell" front + back (Caveat 17/22), edition + design lines (Andika 13/18).

Two placement laws for the spine frame:
1. Place rotated frames BY THEIR CENTER, never by a corner — rotating a corner-placed frame swings it off target.
2. Centering the frame BOX does not center the type (9pt on 18pt leading leaves the glyph column offset inside the box). Verify on the RENDERED PDF at 300dpi: measure the blue margins on both sides of the glyph column; PASS = equal within +/-3px. Shift by the measured delta if not.

Cover verification (required in every build report): pdffonts shows Andika + Caveat embedded; pdftotext extracts byline x2, edition lines, and the spine string character-for-character (apostrophe = U+2019 curly; title exactly "Harlow's Accidental Journey"); the spine margin measurement above. Trinity re-measures from the PDF independently.
