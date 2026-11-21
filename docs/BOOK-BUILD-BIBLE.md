# Book Build Bible

Living document — updated after every build, patch, or Lulu run; new lessons appended as dated entries; superseded guidance struck through, never silently deleted.

Filed 2026-11-04 beside the version folders in `Xtraz\LuLu-Master-Deliverables\`. This is the build desk: Photoshop, InDesign, covers, flipbooks, and Lulu. It is written from the standing spec, the Master-Review notes, the v1 manifest and project sheets, the Santa run of 2026-08-03, and the size locks. A fact with no file behind it is marked **(from session recall, unverified)** or left out.

Current book of record, from `Xtraz\Master-Review\LATEST.txt`: build `2026-11-04-best21`, published as flipbook-gold-v8. Two same-day patches sit on that line: S14 (peanut bag, published in place on gold-v7) and S09 (sky, published in place on gold-v8).

---

## 1. Pipeline overview

Photoshop is the design desk. InDesign is the print file. Lulu never receives a PSD or a PSB.

| Step | What it is | Who |
|---|---|---|
| Art and story type in the PSB / cover PSD | Jon's files. The PSB is the only text authority. | Jon edits. Cursor reads a duplicate and does not save the original. |
| Plate export | One 5250×2625 composite per spread, from a duplicate. Cover plate hides all type except the baked logo lockup. | Cursor |
| InDesign build | Brand-new interior document every full build. Live frames for every word. Cover document the same way. | Cursor |
| Deliverable PDFs | Interior `HAJ-Interior-FROM-PHOTOSHOP-<ver>-LULU.pdf`. Cover `HAJ-Cover-…-LULU.pdf`, later filed with a TEMP-SPINE name until Lulu's template exists. | Cursor |
| Flipbook | Local stage, then publish. Gold versions freeze. `flipbook-master.html` is the permanent current-best link. | Cursor publishes. Lois and Jon view. |
| Lulu project, interior upload, template download, cover upload | Two projects, hardcover and softcover. Files only from the highest version's `03-Deliverables-PDF`. | Trinity drives the site. Jon is logged out on this PC for that run. |
| Cover rebuilt on Lulu's returned template | Same art, same live-type method, real spine. | Cursor |
| Proof order, payment, the look of the soft-proof | One proof per format. Family copies wait until Jon has the physical proof. | Jon |

Trinity also holds the project sheets. Cursor does not retype metadata during a build.

---

## 2. Photoshop layer system

Sources: `BUILD-NEW-BOOK.md`, the BEST-21 build note, the 2026-10-29 size lock.

**Interior PSB.** One file, canvas 5250×2625 at 300 dpi (one opening: two 8.75 in pages). Spreads are recognized by name only:

- `Inside-Peek`
- `Spread-<number>`
- `End-Dedication-Spread`
- `Cast-Spread`

End matter sits immediately after the highest numbered spread, dedication then cast. A missing end-matter group is absent, not invented. Any other top-level group that holds picture or text layers stops the build, unless it is a known utility group or a green or red label.

Known utility groups, excluded and not a stop: Guides, 3D-FlipBook-Guides, Covers-BEST, Spread-Pages-L-R-Sizes, Default BG, the shadow, the vignette. On BEST-21 the red shadow group is named Seem-Shadow. Red utilities on that file were Seem-Shadow, 3D-FlipBook-Guides, Guides, Covers-BEST, and Spread-Pages-L-R-Sizes. Default BG was the green include. There was no vignette group.

**Labels.** Read the Action Manager `color` key. Red is `red`. The green swatch reads as `grain`, not the word green. Orange and none have no include or exclude meaning.

- GREEN (`grain`) on a **top-level** group is a global include. Its composite goes into every plate, in Layers-panel order: below the spreads it sits behind the art, above them it sits in front. Green does not make a group a spread. Green inside a spread has no build meaning.
- RED wins at its own level, eyeball or not. A red top-level group is never a spread and never composited. A red layer inside a spread is off for the plate and never becomes a text frame. Red inside a green group is left out of that composite.
- No label: the saved eyeball governs, except that a spread group's own eyeball is ignored. Hiding a spread does not exclude it. Renaming it does.

**Plates vs live type.** The plate is the art composite. Story text is read from the PSB and reset as InDesign frames. Alternate pictures are never chosen by name. The visible composite prints, and the top layer wins.

**Cover PSD.** No spreads, so green is not a global include. Green forces that group or layer into the wrap even if the eyeball is off. Red is never in the wrap and never becomes a frame. No label means the saved eyeball. The HAJ logo lockup is a painted graphic and stays in the plate. Every other cover text element is hidden on the plate and reset live (amendment 2026-11-04).

**Toggle permission.** During a build, turn each spread set on, export, move on. A picture layer that is off in the saved file is not excluded. Toggle only in the working session. Never save visibility, and never save Jon's Photoshop file for any reason. Work on a duplicate. In ExtendScript, never name a variable `name`.

---

## 3. InDesign build

Sources: `BUILD-NEW-BOOK.md`, `PRINT-SPEC-PACK-2026-10-24.md` §2B, project-log entries for BEST-6 and BEST-7, BEST-10-r2 and BEST-21 build notes, `PHOTOSHOP-TEXT-READ.md`.

**Interior, brand new every full build.** Document named `HAJ-Interior-FROM-PHOTOSHOP-<ver>.indd`. Do not open, copy, or patch an earlier indd on a full build. Patch mode is the only time the indd of record is relinked, and only for the named spread.

- Trim 8.5 in, bleed 0.125 in. Facing pages. One plate across the whole opening, 17.5 × 8.75 in, centered on the fold. Do not place left and right halves separately. That overlaps the gutter by 0.25 in. The print spec pack records that mistake as a mechanics test, not the build method.
- Every plate is the full-resolution composite from this PSB, 5250×2625. A plate from an archive fails the build.
- Plates are plain RGB with no alpha channel. An opaque PNG that still carries alpha made InDesign flatten Santa's PDF into low-resolution tiles. That is the standing warning in the print spec pack.
- Text frames follow the Photoshop line breaks. Lift 7.65 pt. No extra nudges. Forced breaks are real. Soft wraps that a PDF extractor inserts are not. Spread 13's "Long Beach" break stays checked.
- Page count: 2 (Inside-Peek) + 2 × numbered spreads + 2 × each end-matter spread present. The current book is 54. Flipbook pages are that count plus front and back, currently 56.

**Fonts and color, from the character style only.** A blind walk of the text key returns Myriad Pro. That default sits above the characters. Read `textStyleRange` → `textStyle` for font, size, leading, and color. Do not fall through to Black. Do not hardcode a swatch. The story color in this PSB is RGB 46, 42, 36, and the BEST-10 and BEST-21 notes both measured that same triple in the PSB and in InDesign. Still read it from the file each build.

| Frame | Font / size / leading | Source |
|---|---|---|
| Story | Andika 17/22 | Standing spec |
| Inside-peek | Caveat 22, plus Andika 14 and Andika 12 | Standing spec |
| Cover byline, front and back, "Written By: Lois Farrell" | Caveat 17/22 | Spec and the 2026-11-04 amendment |
| Edition and design lines | Andika 13/18 | Spec and the amendment |
| Spine title, "Harlow's Accidental Journey" | Andika 9/18, white, bottom to top, title only | Amendment. Apostrophe is U+2019. |

The text-frame baseline in the spec is 49, from BEST-10. BEST-21 reported 93 live frames, including 41 cast names. A changed total is called out. It is not buried and it is not silently "fixed." Red text layers are not in the count.

**PDF export.**

- Interior: preset `Lulu-Interior-Print-PDF`. sRGB, single pages, no crop marks, fonts embedded. Page size 8.75 in (the bleed canvas). TrimBox 8.5 in. BEST-6 and BEST-7 project-log lines record "8.75 media, 8.5 trim."
- Cover: do **not** use the interior preset. The cover page is 17.5 × 8.75 in, bleed 0, because bleed and the temporary spine are already inside the Photoshop canvas. Force RGB. Santa's cover flattened to CMYK when type with a drop shadow met "color unchanged." Confirm by the files on disk. A long script may return a numeric COM code while the PDF is still finishing. Do not start a second create while the first may still be running.
- Cover verification, every build: Andika and Caveat embedded; extracted text has the byline twice, the edition lines, and the spine string character for character; spine glyph margins equal within ±3 px at 300 dpi.

If an output name already exists, move it aside as `*-superseded`. Do not overwrite it quietly. BEST-19's cover folder holds `superseded-spinetypo` and `superseded-offcenter` for that reason.

---

## 4. Covers

**Why live type.** Through gold-v7 the cover shipped as one flattened composite. The BEST-19 build note records that cover PDF at 9,108,682 bytes with the spine baked in as "Harlows's Accidental Journey". pdffonts on those covers was empty. The 2026-11-04 amendment makes the cover follow the interior rule: the plate is art with all type hidden, and the words are InDesign frames. The logo lockup stays baked. The remade cover is about 3.59 MB. gold-v7's flipbook was **not** republished with that remake. gold-v8 is the first published viewer whose cover note says the type is live.

**Spine placement.** Place a rotated frame by its center. A corner-placed rotation swings off the band. Centering the frame box does not center the glyphs: 9 pt type on 18 pt leading sits offset inside the box. Measure the rendered PDF at 300 dpi, blue margin on each side of the glyph column. Pass is equal within ±3 px. The BEST-19 centering note: the frame moved 2.28 pt toward the back cover; the glyph column was x 2613–2638; center 2625.5; margins 25 px back and 24 px front. BEST-21 measured the same margins.

~~The 2026-10-29 size lock said the temporary spine is color only, no spine text, and the softcover addendum repeated that a thin paperback spine cannot carry type.~~ Superseded for this book by the 2026-11-04 amendment and by the published gold-v8 cover, which carries the title as live type. The old sentence stays here so nobody "cleans it up" and loses the reason the rule changed.

**Gradient, barcode, QR.** The spine band is the deep-blue gradient from the PSD. On BEST-21 the barcode group and the QR group were off and stayed out of the composite. The family run carries no barcode. The yellow keep-clear zone on the back stays empty so a later public version can take a barcode. Lulu places a barcode per project when one is wanted. Do not draw one into a family-run file.

**Hardcover vs softcover.**

- Shared: trim 8.5 × 8.5, bleed 0.125, interior PDF uploaded to both projects, face art shared.
- Hardcover case wrap adds board around the trim. Santa's returned template was 19 × 10.25 in with a 0.25 in spine, which is 0.75 in of board past the 8.75 in bleed height. That 0.75 in figure is derived from Santa's file. No desk holds a Lulu sentence that states it. Harlow's own template will state Harlow's height and width. Do not upload 5700×3075 for Harlow. Do not upload the 17.5 × 8.75 working wrap as the hardcover.
- Softcover is one flat sheet. No boards, no hinge. Height 8.75 in. Width is 0.125 + 8.5 + spine + 8.5 + 0.125. The v1 softcover PSD and its InDesign package are the temp-spine twin of the hardcover design, same 5250×2625 canvas, filed under `v1\02-InDesign\Softcover`. The shipped softcover PDF in `03-Deliverables-PDF` is `HAJ-Cover-SOFTCOVER-TEMP-SPINE.pdf`.
- Guide colors on the design desk are Jon's convention, not Lulu's: blue bleed, purple flourish band at 0.625 in inside the trim (stricter than Lulu's 0.5 in safety), yellow barcode zone, teal temporary spine. The purple band is not a Lulu number.

**Temp spine vs the final.** The 0.25 in band in the working files is a placeholder so the canvas stays 5250 px wide. It is Santa's 34-page spine, used as a desk, and it is labeled temporary in the file names. After each Lulu project accepts the interior, only that project's spine band is re-dialed onto the returned template. The two finals replace the TEMP-SPINE PDFs in `03-Deliverables-PDF`. The templates themselves go in `04-Lulu-Templates`.

---

## 5. Lulu

Sources: the two project sheets and the run checklist in `v1\05-Lulu-Project-Info` (filed 2026-11-04; the v1 MANIFEST header still says that folder is empty — the files are there), Santa's `LULU-WEBSITE-ORDER-PLAYBOOK.md` and `LULU-ORDER-CHECKLIST.md` (2026-08-03), `LULU-8.5-SQUARE-CHEATSHEET.md`, the size lock and its softcover addendum.

**Product, both Harlow projects.** Square 8.5 × 8.5 in. Premium Color. 80# white coated. Matte. 54 pages. Hardcover binding is Case Wrap. Softcover binding is Perfect Bound. Goal is Print Your Book, personal printing. No ISBN on the family run. A later public paperback would need its own ISBN, not the hardcover's. License is All Rights Reserved, copyright Lois Farrell 2026. That replaced Santa's CC BY because CC BY would allow republication and because it matches the copyright page. Author Lois Farrell. Contributor Jon Farrell, illustrator. Audience 3–8. Category Children's, Juvenile Fiction / Animals / Cats. The ink-coverage warning on an illustrated book is normal. Stay on Premium Color. Do not switch to Standard.

Pricing on the sheets is a reference, not a lock. Santa hardcover printed at about $18.28 and listed at $22. Santa softcover printed at about $9.46 and listed at $12. Harlow is 54 pages, so both print costs will be higher. Family copies are at print cost. Do not lock a list price until Lulu shows the real number.

**Interior requirements.** Bleed 0.125 in each side, so the full-bleed page is 8.75 in and 2625 × 2625 px at 300 dpi. An opening is 5250 × 2625, fold at the center. Safety is 0.5 in inside the trim. No extra gutter under 60 pages. Lulu adds white endsheets on a hardcover. They are not pages in the PDF and they are not customizable. Upload the interior first. Lulu counts it and returns the cover template. The check after upload is the page count (54) and the trim, not the spinner. The file is `v1\03-Deliverables-PDF\HAJ-Interior-FROM-PHOTOSHOP-BEST-21-LULU.pdf`, 64,428,627 bytes, the S09-patched interior. Never a PSD. Never either TEMP-SPINE cover.

**Template system.** One template per project, generated after that project's interior upload. Santa's numbers are examples from a 34-page book, not Harlow's:

| | Santa, 34 pp, from the 2026-08-03 specs | Harlow |
|---|---|---|
| Hardcover | 19 × 10.25 in, spine 0.25 in, project `v82ejwq` | Waits for Harlow's template. Height follows the case wrap. Width follows Harlow's spine. |
| Softcover | 17.387 × 8.75 in, spine 0.137 in, project `454zdy8` | Waits for Harlow's template. The checklist's scale read, not a measurement, says a 54-page softcover spine should land near 0.2 in. The template wins. |

**Project setup.** Two projects. Titles on the book are both "Harlow's Accidental Journey". "Hardcover" and "Softcover" stay in the internal project name only, which is how Santa kept "The Night I Met Santa" and "The Night I Met Santa Softcover" apart. Language English and category Children are set before Design. On the Santa run, Start sat on "processing" and Review stayed disabled until both were committed.

**Upload lessons from the Santa run.**

- The OS file dialog is not something the embedded browser can finish. On Santa, Jon picked the PDFs. For Harlow, Trinity drives from her own browser so that dialog is on her machine. Jon stays logged out of lulu.com on this PC. One login on two machines can kick a session mid-upload.
- Do not click ahead and do not guess step URLs while Lulu says processing. `lulu.com/account/cart` and `lulu.com/shop/cart` 404'd. The cart that works is `https://www.lulu.com/cart`.
- Quantities stick only after the field is tabbed out.
- Confirm and Publish disables itself while processing. Wait. Do not click it again.
- If a run dies, open My Projects before creating anything. A second project with the same title is the failure.
- A huge raw-embed cover made Santa's softcover preview go blank. A JPEG-compressed re-export around 3–5 MB was accepted. Harlow's live-type cover PDFs are about 3.6 MB, inside that range.
- Cursor's handoff, per project, is the template file itself (into `04-Lulu-Templates`), the project URL and ID, the binding, the spine width and template size printed on that file, the page count Lulu accepted, confirmation the interior was the 64,428,627-byte PDF, and a screenshot of the Design step. Measure the template before building. Santa's inches are not inputs.

---

## 6. Flipbooks

Sources: `BUILD-NEW-BOOK.md`, `LATEST.txt`, the build and patch notes, the v1 manifest.

**Gold versions freeze.** Each publish pushes new files only to `MyDigitalStudioz/Harlows-Accidental-Journey`, the next `flipbook-gold-vN`. Older gold folders stay as they are. Stage with `git add --sparse` or the new images never commit. The header on a gold publish is exactly `Updated HAJ Print-Review v<N>`.

| Gold | Run folder | Viewer pages | Note |
|---|---|---|---|
| v3 | 2026-11-01-best10 | 52 | First BEST-10 publish. Includes Lois's 2026-11-01 call edits, including the S22 comma. |
| v4 | 2026-11-01-best10-r2 | 52 | 49 text frames. Color spot-check RGB 46, 42, 36. |
| v5 | 2026-11-03-best15 | 56 | End matter included. The request named BEST-10; the open file was BEST-15. |
| v6 | 2026-11-03-best17 | 56 | Supersedes the best15 run. |
| v7 | 2026-11-04-best19 | 56 | Published, then the cover was remade live and the flipbook was not republished. S14 peanut-bag patch swapped pages in place. |
| v8 | 2026-11-04-best21 | 56 | Live-type cover. S09 sky patch swapped pages in place. This is the latest published line. |

The flipbook18.html freeze was lifted 2026-11-01. Lois views gold pages. Do not rename, move, or delete flipbook18.html. Book builds never touch the 3D-Flip-BookVizon repo.

**The permanent master.** `flipbook-master.html` always serves the current best book. Later versions replace the files under that same name. Gold links stay as history. The copy in `v1\06-Master-Flipbook` is the v1 snapshot. Its marker is "HAJ Master v1". It was built from the patched gold-v8 pages.

**Patch vs full build.** Patch is one spread: re-export that plate, relink it in the interior indd of record, re-export the PDF, confirm only those pages changed, swap the two 1750 images in place, archive a new folder with a PATCH-NOTE and the `*-before` images. No new gold number. The URL and the header stay. If the change touches more than two spreads, stop. That is a full build, and it is Jon's call. A full build is local until "Publish book Harlow". Publishing the same folder twice is forbidden.

**Verify a publish.** Wait until the Pages status is `built`, not the word "building". Match the live front cover and the S13 files to the local files byte for byte. Confirm the header and the page count. If the new gold page still serves the old build about five minutes after the push, one trivial nudge commit to main, then verify once. A patch verify is the changed spread plus one neighbor left untouched.

~~The standing spec says never upload `pages-data.js`.~~ The gold-v8 build note records that file in the published set (43,894,925 bytes at that publish), and the viewer loads it before the book starts so each turn does not fetch a JPEG. That is the flicker fix, written in the gold-v8 HTML. The spec sentence has not been revised. Shipped practice is: the viewer set includes `pages-data.js`.

**Bookshelf (multi-book viewer) rules — added 2026-11-20, kit v1.2.3, from the Book 2 shelf.** The Book 2 fork shelves several books in one viewer (story book, cast book, spread mockup, prior series books). Three rules govern it:

- **Shelf tile identity:** a book's shelf tile must always show **that book's own cover**. Each catalog entry's `cover` field must name the book's own cover file — audit it whenever a cover page is added or changed (the live defect: a real-cover fix registered the new cover as the entry's first page but never updated `cover`, which still pointed at another book's front page). Cover resolution must **never branch on which book is open** — one resolution path for open and closed books alike. The flipbook probe cycle must include a **return-to-shelf tile-identity assertion for every book** (open → page → return, tile checked before AND after), not just open-and-turn checks; a cached wrong thumbnail self-heals only when its stored source no longer matches the resolved one.
- **Curated shelf order:** the catalog order is the shipped default and is curated (the producer sets which book leads). A per-device saved arrangement (the reader's own rearrange controls) still wins on that device, by design — never mistake a device-local order for the shipped default, and never "fix" the catalog to match one device.
- **Spread-view pattern (`flatPairs`):** a spread book that must also read page-wise in portrait registers as half-pages (each spread split at its center seam) with a flag that pads the pairing at runtime. Runtime blanks belong at the **back only**, as the endpaper. **The front slot is a real cover page, never a blank** — a book opens on its cover, and page 1 is a real page a reader can page back to. (The first build padded the front with a blank and stepped past it on open; paging back landed on a blank "Page 1" — the defect this rule exists to prevent.)


**Book openings (added 2026-11-21, kit v1.2.5, from the Book 2 shelf):**

- **Universal shelf-book flow:** every book on the shelf follows the series' first book — **front cover → blank flyleaf → content → blank flyleaf → back cover.** The flyleaf art is the series' own flyleaf file (a plain page), byte-identical copies in every book that uses it, captioned "Flyleaf". A book with no flyleaves reads as unfinished next to its shelf-mates.
- **The title-page opening:** every book opens **cover → flyleaf → TITLE → content.** The title page is typeset in the book family's serif voice on its cream paper, framed by a double rule, and its small line says what that version IS (each shelf version — story, spread mockup, story & text — carries its own format line). **The © lines sit at the FOOT of the title page — there is no standalone copyright page and no copyright verso;** front-matter parity is kept by pairing the title with the flyleaf in front and balancing flyleafs at the back. A paginated book's content starts on the **left** of the first content spread. Insert front matter in PAIRS in a paginated book, and shift any index-keyed maps (fills, below) with the pages.
- **Parity changes are the owner's call:** when a parity change moves content across a spread seam, check which designed pairs it splits (e.g. a left start can force a facing panel pair apart in landscape) and put the trade to the owner BEFORE building — they may take the split or keep the pair.
- **`flatPairs` front matter:** a flatPairs book takes **NO separate flyleaf spread in front of its title spread** — the title spread's blank left half IS the flyleaf (one blank flip before the title, the same rhythm as the paginated books). Insertions ahead of a flatPairs book's halves must be **spread-width (an even count of slots)** to preserve pairing.
- **The runtime endpaper is a pair-completer, not a page:** pad a flatPairs book only when its own page count is EVEN; a book that ends on a real back cover (odd count) completes its last pair by itself and gets no blank after it. When a book gains a back cover, give it the endpaper's slot, so the counter total and every stored per-page position on readers' devices stay put.

**Text pages and leaf pairing (added 2026-11-21, kit v1.2.5):**

- **The text-page pattern:** a storybook version can carry the story's words as **rendered typeset page images** — one page per passage, the FULL passage auto-fit to one square page (never trimmed), cream paper in the book's palette, the book family's serif voice in warm ink, generous margins, a small paw mark at the foot. A split-panel illustration splits its passage at the panel break — each panel's facing text page carries its half.
- **Leaf-pairing arithmetic:** couples that must FACE each other (art ↔ its text page, portrait ↔ full body) start at an **odd 0-based index** in a viewer that pairs leaves as (odd, even). A book that opens cover → flyleaf → couples therefore **doubles the front flyleaf** rather than breaking the pairing or gluing the back cover into the last spread; the back cover stands alone like every other book's.

**Fill treatments for placeholder art (added 2026-11-21, kit v1.2.5):**

- Placeholder art often sits inside baked-in bands/pillars. A per-book **`fill` map** (`{pageIndex: [scale, originX%, originY%]}`) zooms those pages so the art fills the page frame. **Display-only — never baked into the page files, never carried to print.**
- **Scales are measured, never guessed:** scan each file's actual band extents; scale = frame ÷ art extent with a small uniform overshoot; origin at the art's center. Spread pairs get ONE seam-anchored scale per spread (left halves origin-x 100%, right halves 0%), measured from the halves' pillar boundaries; where a detector catches an interior edge first, verify the boundary by eye against its pair.
- **Scan BOTH axes — all four edges.** A page can be full-bleed on one axis and banded on the other; a one-axis scan classifies it "full-bleed" and ships the bars. The one uniform fill scale must satisfy both axes.
- **Apply the fill at EVERY reader surface:** static bases, the DOM sheet faces, the magazine leaf layers, the canvas leaf (sliced from the same fill window, so the flying leaf shows the filled art), scroll view, and zoom — filled pages get a clipping wrapper in zoom so the zoom shows the filled window, not the whole file scaled. Covers and flyleaves carry no fill.

**Thumbnail-store versioning (added 2026-11-21, kit v1.2.5):**

- Shelf thumbnails generated from cover art and persisted on the device (IndexedDB), validated by the cover's PATH alone, survive an in-place byte swap forever — the reader fetches the new cover fresh while the tile shows the old art indefinitely, and fresh-profile probes will never see it. **Version the thumb store with the cover art: bump the store's version constant in the same change as any in-place cover-art swap,** so every device discards its stored thumbs once and regenerates them. Gate the fix with a **seeded stale-state profile** (the pre-swap world persisted), not a fresh profile — fresh profiles pass while real devices stay stale.

---

## 7. File architecture

**Master-Review.** One folder per build run: `Xtraz\Master-Review\<YYYY-MM-DD>-<psb version>\`. If that name exists, `-r2`, then `-r3`. The highest run number is the newest of that day. A new run folder does not consume a gold number. Each folder gets a BUILD-NOTE: sources and times, page count, PDF sizes, provisional flipbook number, and either NOT PUBLISHED or the published line. `LATEST.txt` has two lines. "Latest build" moves on every build and on every patch. "Latest published" moves only when a gold version is pushed. Patch lines are added under those two. They do not replace them.

**LuLu-Master-Deliverables.** Versions sit side by side. v1 is the current set.

- `01-Source-Photoshop` — copies of the PSB and both cover PSDs.
- `02-InDesign` — packaged Interior, Cover (hardcover), and Softcover. Each package has the indd, Document fonts, Links, and Instructions.
- `03-Deliverables-PDF` — the only upload folder. Interior is FINAL. Both cover PDFs are TEMP-SPINE until Lulu's templates come back.
- `04-Lulu-Templates` — empty until the returned templates land.
- `05-Lulu-Project-Info` — the hardcover sheet, the softcover sheet, and the run checklist.
- `06-Master-Flipbook` — the v1 snapshot of the permanent viewer.
- `MANIFEST.md` — every file, with role, origin, timestamp, size, and FINAL or TEMP-SPINE.

Upload only from the highest version's `03-Deliverables-PDF`. Never from a working folder, never from Master-Review, never from Exports. v1 freezes when the Lulu proofs are ordered. Later changes go in a v2 that starts as a copy of v1. A frozen version is not edited.

**Names stay stable** because publish, patch, and Lulu all find files by pattern. `HAJ-Interior-Spread-BEST-<n>.psb` and `HAJ-Cover-Front-Back-TempSpine-BEST-<n>.psd` are chosen by highest number, then by modified time. The indd and the PDF repeat that version in the name. `TempSpine` in the cover name is the warning that the spine is still the placeholder. Gold HTML names are never reused for a different book. `flipbook-master` is the name that is reused, on purpose, so the link does not change.

---

## 8. Problems → fixes

| Failure | Where it showed | Standing fix |
|---|---|---|
| Spine title shipped baked in, and misspelled "Harlows's" | gold-v7 cover, 9,108,682 bytes, BEST-19 note | Live type. Plate hides type. Spine, bylines, and edition are frames. Logo stays painted. Superseded file kept. |
| Corner rotation put the spine title off the band; the box center was still not the glyph center | BEST-19 centering note, 2.28 pt move, margins 25 and 24 | Place the rotated frame by its center. Measure glyphs at 300 dpi. Pass is ±3 px. |
| Cover type came out Myriad Pro | 2026-11-01, `ISSUES-RESOLVED.md`, `PHOTOSHOP-TEXT-READ.md` | Read `textStyleRange`. The paragraph default above the characters is wrong. |
| Story color fell through to Black | Standing spec | Take color from the same character style. Do not hardcode. Do not use the default Black swatch. |
| Left and right plates placed separately overlapped the gutter by 0.25 in | Print spec pack §2B | One 17.5 × 8.75 image centered on the fold. |
| Alpha channel on an opaque plate flattened the PDF into ~117 dpi tiles | Santa, recorded in the print spec pack | Plain RGB, no alpha. |
| Cover PDF flattened to CMYK | Santa, drop shadow plus "color unchanged" | Force RGB on the cover. Do not use the interior preset for the cover. |
| Softcover preview went blank | Santa 2026-08-03 playbook | Do not upload a huge raw-embed cover. A ~3–5 MB JPEG-compressed PDF was accepted. |
| Start never reached Design | Santa playbook | Set language English and category Children before leaving Start. |
| Cart URLs 404'd; wizard clicks during "processing" failed | Santa playbook | Only `https://www.lulu.com/cart`. Wait. Use Start → Design → Review. |
| Quantity did not stick; Confirm and Publish ignored a second click | Santa playbook and the Harlow run checklist | Tab out of the quantity field. Wait while Confirm is disabled. |
| File dialog could not be driven from the embedded browser | Santa playbook; Harlow checklist | Trinity drives Lulu. Jon is logged out on this PC so the session is not kicked mid-upload. |
| A dead upload followed by "create project" again | Harlow checklist, from the Santa post-mortem | Check My Projects first. Do not make a second project with the same title. |
| 5700×3075 used as Harlow's cover | Size lock, 2026-10-29 | That canvas is Santa's 34-page hardcover. Harlow waits for its own template. |
| Pages served the previous gold build after a push | Standing spec | Wait for status `built`. One nudge commit, then verify once. Match bytes, not a casual reload. |
| `git add` on the gold clone skipped new images | Standing spec | `git add --sparse`. |
| Spec says never upload `pages-data.js`; the published viewers include it | Spec vs gold-v8 build note and the viewer HTML | Shipped practice includes it, loaded before the book starts. The spec line is not yet revised. Do not delete it from a gold or master publish. |
| InDesign `contents` on one character did not yield a usable code when forcing the spine apostrophe | **(from session recall, unverified)** | The file rule that is sourced: set the story, then check `charCodeAt` on the story string. U+2019 is the pass. |
| Photoshop EngineData stored `\'`, so InDesign printed `didn\'t` | `ISSUES-RESOLVED.md`, 2026-08-22 | Unescape before setting contents. |
| Alignment value 2 was read as centered | Same issues file | That value is roman baseline. Justification is the align field. |
| A text frame grew sideways onto the facing page | Same issues file | Grow height only. Clamp to this page. |
| S22 comma flagged against older drafts | Standing spec | The PSB wins. The comma is Lois's, confirmed by Jon 2026-11-01. Never diff the PSB against Rev.19. |
| Visibility saved back, or a hidden spread treated as excluded | Standing spec | Toggle on a duplicate only. Never save the PSD/PSB. Hiding a spread does not exclude it. |

---

## 9. Pre-flight checklists

**Build day**

- Latest PSB and cover PSD by name, then by modified time. State both times. If two files tie, stop.
- Canvas 5250×2625. Any other cover size stops the cover.
- Top-level inventory written down: each spread, the green include, every red exclusion, every utility skip. An unknown group with picture or text stops the build.
- Duplicate only. Original still unsaved by you when you finish.
- Plates 5250×2625, from this PSB, type hidden on the cover plate, logo still in the art.
- New indd, not a copy of the last one.
- Fonts and color from `textStyleRange`. Story spot-check reported as PSB triple and InDesign triple.
- Words and forced breaks match the PSB. Soft wraps do not fail the build.
- Interior page count from the formula. Cover is one page, 17.5 × 8.75, Andika and Caveat embedded, spine margins within ±3 px, apostrophe U+2019.
- Old PDFs moved aside, not overwritten.
- New Master-Review folder. BUILD-NOTE. LATEST "Latest build" updated. Not pushed.

**Publish**

- The folder on "Latest build" is not already "Latest published".
- The staged gold number is still highest-plus-one. If someone published in between, stop.
- New files only. `git add --sparse`. No PSB, no PDF, no Master-Review, unless Jon asked.
- Pages status is `built`. Front cover and S13 match local bytes. Header and page count match.
- One nudge, once, if the new page is stale after about five minutes.
- BUILD-NOTE gains the PUBLISHED line. Only then does "Latest published" move.

**Patch**

- One spread, already in the PSB. More than two spreads means stop.
- Read "Latest published" for the gold version and the indd of record.
- Relink that plate only. Text unchanged unless Jon stated a text change, and then it is made in the PSB first.
- PDF: neighboring pages unchanged. Viewer: two images swapped, header unchanged, `*-before` copies archived.
- No new gold number.

**Lulu run**

- Jon logged out of lulu.com on this PC.
- Upload file is the highest version's `03` interior, byte size checked (v1: 64,428,627).
- Two projects. English and Children set before Design. Premium, 80# coated, Matte. Case wrap or perfect bound. No ISBN.
- After upload: page count 54 and the trim. Then stop and hand Cursor the template file plus the six handoff items.
- Cursor measures the template, builds, returns a cover PDF. Trinity uploads that PDF only to that project.
- Jon does the proof order. Nobody orders family copies from the soft-proof alone.

---

## 10. Boundaries

This document does not cover cast canon, image recipes, style governance, or the render workflow. Those live in Trinity's PICTURE-BOOK PRODUCTION PLAYBOOK on Drive. Point there. Do not copy them here.

It also does not authorize an upload. v1's covers are still TEMP-SPINE. The interior PDF is the one that may be uploaded, and only from `03-Deliverables-PDF`, when Jon says the Lulu run starts.

---

## Dated entries

**2026-11-04.** First filing. Drawn from `BUILD-NEW-BOOK.md` including the cover live-type amendment, Master-Review notes from BEST-10 through BEST-21 and the two same-day patches, `LATEST.txt`, the v1 manifest, the three files in `05-Lulu-Project-Info`, the 2026-10-29 size lock and softcover addendum, the 2026-10-24 print spec pack, `ISSUES-RESOLVED.md`, `PHOTOSHOP-TEXT-READ.md`, and Santa's 2026-08-03 playbook, checklist, and 8.5-inch cheatsheet.
