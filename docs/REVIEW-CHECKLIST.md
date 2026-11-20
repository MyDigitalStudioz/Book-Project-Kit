# Book Desk — Pass 2 Review Checklist (Trinity's acceptance pass)

Prepared 2026-10-28, after Jon pasted the master continuation prompt to Cursor
(source file: `2026-10-28-book-desk-MASTER-prompt-v2.md`, same folder).
Use when Cursor's DONE note lands on the bridge (01_INBOX). Nothing here
authorizes touching HAJ-Interior-FINAL-v3-2.indd or any Lulu upload.

## Gate 0 — Did the report actually arrive?
- [ ] DONE note is on the bridge (01_INBOX), not only on Vader disk.
- [ ] BookDesk-Report-*.txt/.md and the proof PNGs are in 01_INBOX with it.
- [ ] Report header present: panel version + profile version, source .indd
      name AND its saved date, run date/time.
- [ ] If the run document was NOT HAJ-Interior-FINAL-v3-2.indd, the report
      opens with the loud banner naming the document that WAS run.

## A. Report plumbing
- [ ] Proof strips chunked one spread per bridge call; a failed spread was
      retried once.
- [ ] If any spread is missing, first line says PARTIAL and names which
      spreads finished. A partial run must not read as complete.
- [ ] sha256 + byte size listed for every PDF and PNG the run produced.
- [ ] Every report line labeled with spread AND InDesign pages
      ("S09 / pp.20-21"; S_n = pp.(2n+2)–(2n+3)).
- [ ] Dry-run mode exists and was the first run on any new document.

## B. Portable flipbook
- [ ] flipbook-local/<version>/ folder written; version = source name +
      export date; no earlier version overwritten.
- [ ] Page list/manifest is INLINED in a script file — not fetched JSON
      (a fetched manifest silently breaks when opened from disk).
- [ ] Viewer shows the version label and NOT FOR PRINT on screen.
- [ ] StPageFlip-class library bundled self-hosted WITH its license text.
- [ ] Proof claimed: folder opened locally in a browser and flips.

## C. Placement proof on real geometry
- [ ] Scratch doc exists, clearly named (e.g. BookDesk-Scratch-52):
      52 pages, 8.5 × 8.5 in, 0.125 in bleed, facing spreads.
- [ ] Proved on the scratch doc: seamless place (17.5 × 8.75 in centered on
      fold), text-and-image place mode, bleed meter on a placed frame,
      View p.3, View p.52, fold proof strip, S23 (pp.48–49) fade-edge crop.
- [ ] harlow.json now carries Lulu numbers: safetyMarginIn 0.5,
      gutterMinIn 0.2, gutterAddedIn 0 (52 pp is under Lulu's 60-page
      no-added-gutter line).
- [ ] Preflight strip has the Lulu clearance line (text inside safe rects,
      yes/no per spread).

## D. Rev.19 text compare
- [ ] REV19-SPREAD-TEXT-SOURCE.md is on the PC inside the project and
      harlow.json textSourcePath points at it.
- [ ] Rev.19 DOCX (md5 00a7ed603e099acf88a712de8c6d6ad9) pulled as the
      typography authority; source md5 pinned in every compare report.
- [ ] Diff is per SPREAD in reading order, left+right frames joined.
- [ ] Eight classes reported SEPARATELY: (1) word/substance, (2) quote/
      apostrophe style, (3) dash spacing/type, (4) double spaces,
      (5) double periods, (6) italics/bold runs vs the docx, (7) all-caps
      shouts, (8) soft returns / paragraph breaks / trailing spaces.
- [ ] Two views offered: normalized (substance) and strict (everything).
- [ ] Known source quirks print as KNOWN SOURCE QUIRK, not errors:
      S12 "kind.." double period; S14 quote slip. (Jon's rulings on both
      are still open — see REV19-TYPESET-CALLS.md.)
- [ ] Also caught: missing/extra text frames, text on hidden or MOCK
      layers, story-thread order problems.
- [ ] A sample of the compare output is included in the DONE note.
- [ ] Expected substance landings on the real file later: S09, S12, S14,
      S16, S18, plus the comma on S22. Diffs on the scratch/proof doc are
      expected and do not count as failures.

## E. Fade measurement + proof strips
- [ ] Fade measured per text LINE: pixels behind each line's box,
      5th-percentile luminance, against ink #2E2A24, at print size.
- [ ] Flag under 7:1; HARD mark under 4.5:1 — marks only, never a block
      (Jon's standing rule).
- [ ] Fade-edge strip runs on EVERY spread, not only S23.
- [ ] 100% strip of the top bleed edge with trim line included.
- [ ] Fold strip notes nearest face pixel vs the x44–56% fold zone.
- [ ] Nothing baked by the panel.

## F. Export read-back + covers
- [ ] Every print-set export read back: page count, page size,
      TrimBox/BleedBox, fonts embedded (yes/no + list), color space,
      minimum effective ppi across placed images.
- [ ] Status lines now three: p.2 copyright line (ISBN placeholder),
      "p.3: TEMP placeholder still in place",
      "p.52: closing content not set".
- [ ] Cover art paths set in the profile (FRONT E / BACK C masters,
      2625 × 2625) and cover-wrap export proved — marked PROVISIONAL
      (true spine width only comes from Lulu after interior upload).
      NOTE: Jon's new cover variants (see COVER-LINEUP-2026-10-28.md) are
      NOT in the profile until he picks a pair — if Cursor swapped cover
      paths to a new variant without Jon naming it, flag it.
- [ ] Flipbook export proved with cover singles as first/last pages;
      page count + page size reported.

## G. Tidy
- [ ] Preset names normalized to InDesign's loaded names (no .joboptions
      suffix mismatch in reports); change noted in DONE.

## Refusal classes
- [ ] Every refusal in the pass is classed: geometry (correct) or
      measurement (not permitted). Any measurement-based refusal or
      blocked export = fail against Jon's "flags report, never block" rule.

## Verdict line (fill in on review)
- Result: PASS / PASS WITH NOTES / FAIL — items:
- Date reviewed:  ·  Report file(s) reviewed:
