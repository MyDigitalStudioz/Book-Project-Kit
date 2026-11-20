# STANDING COMMAND — "Flipbook: <name>" (Jon, locked 2026-11-02)

Jon's one-off review-flipbook process for Lois. When Jon says **"Flipbook: <name>"** and gives a source folder, Trinity generates the paste-ready Cursor prompt (Harlows-Big-Adventure project) with everything below filled in — Jon supplies only the name and the folder.

## Jon's input
- **Name** — e.g. "Cast v2", "End v1". Drives the title, filename slug, and review folder.
- **Source folder** — a Vader folder of Jon's own exported images: numbered files are SPREAD-width exports (5250×2625); `Front.jpg` / `Back.jpg` are single-page covers in the same folder.

## Auto-derived defaults
- **Title:** `HAJ <Name>-Test-Review v<N>` — name split into words + version (e.g. "Cast v2" → "HAJ Cast-Test-Review v2").
- **Publish filename:** `flipbook-<slug>-v<N>.html` (slug = lowercase name words, e.g. flipbook-cast-v2.html) → live at `https://mydigitalstudioz.github.io/Harlows-Accidental-Journey/<filename>`.
- **Local review copy:** `D:\Hermes\projects\Harlows-Big-Adventure\Xtraz\Master-Review\<YYYY-MM-DD>-review\<slug>`.
- **Template:** `D:\Hermes\projects\Harlows-Big-Adventure\Images\Flipbook-Template` — cloned as-is; its current title string ("Updated HAJ Print-Review v4") replaced by the new title everywhere it appears. Template itself never modified.

## The build (what the Cursor prompt specifies)
1. Copy the template; swap title + page set only. No redesign, no viewer changes.
2. **Split pass:** every numbered spread → two page files at the exact pixel center (left half, then right half — the gold builds' L/R convention, cf. 02-peek-L / 03-peek-R). Front.jpg / Back.jpg are NOT split; if either is spread-width, Cursor stops and reports.
3. **Page order:** Front → for each spread in NUMERIC order: L, R → Back.
4. **Publish pages at 1750×1750** (LANCZOS downscale from the 2625 masters, which stay untouched in Master-Review) **with an embedded pages-data.js** — all pages as image data, loaded before the book starts, web and disk alike. This is the FLICKER FIX (proven 2026-11-02): without the embedded file, the viewer fetched each JPEG mid-turn and the 1.2s turn timeout painted whatever had arrived — the flicker Jon saw, at any resolution. Never ship a flipbook without its pages-data.js.
5. **Source folder is READ-ONLY** (corrected 2026-11-02 after the first run): the build writes splits only into the flipbook destination folder and never duplicates anything in the source — so originals are never moved, renamed, or deleted. (The original spec's archive-original-spreads step was retired the same day: it solved a duplication problem that didn't exist and only shuffled Jon's exports.)
5. **Publish:** commit to `MyDigitalStudioz/Harlows-Accidental-Journey`, branch Harlows-v2 → sync main (Pages serves main); nudge commit if Pages stalls. Never touch flipbook18.html or flipbook-gold-v4.html.
6. **Verify:** local flip-through; page count = 1 + 2×spreads + 1; one split seam-checked; live URL fetched, correct title confirmed. Report: spread count, page count, local path, live URL.

## Provenance
First run under this name's pattern: flipbook-cast-v1 / flipbook-end-v1 (2026-11-02, prompt filed as CURSOR-PROMPT-FLIPBOOKS-CAST-END-2026-11-02.md). The pattern itself is the third use (gold review books, print-review v4 before it).
