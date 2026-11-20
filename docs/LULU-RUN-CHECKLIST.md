# Lulu run checklist — Harlow HC + SC (Trinity drives, Cursor builds covers)

Filed 2026-11-04, incorporating Cursor's Santa-run post-mortem (2026-08-03 run) and its handoff spec (consult report, 2026-11-04). Decision inputs: Trinity recommended A; Cursor recommended A ("the Santa run already required Jon at the file dialog, and a 64 MB upload is that same step"). Jon decides.

## Before the run
- Jon is logged OUT of lulu.com on Vader (one login on two machines can kick the session mid-upload). — SUPERSEDED by the 2026-11-05 run (see Playbook §35 + addendum)
- Jon drops Trinity's two LULU-PROJECT-SHEET files into `LuLu-Master-Deliverables\v1\05-Lulu-Project-Info\`.
- Files to upload live in `v1\03-Deliverables-PDF` only. Interior: `HAJ-Interior-FROM-PHOTOSHOP-BEST-21-LULU.pdf` = 64,428,627 B, 54 pages. NEVER upload a PSD, never upload either TEMP-SPINE cover. — SUPERSEDED by the 2026-11-05 run (see Playbook §35 + addendum)

## Per project (HC first, then SC — two separate projects)
1. Create project: Print Book → goal "Print Your Book" (personal printing; NOT bookstore distribution, NO ISBN purchase). — SUPERSEDED by the 2026-11-05 run (see Playbook §35 + addendum)
2. Set Book language = English and Book category = Children EARLY — on the Santa run, Start sat on "processing" and Review stayed disabled until both were committed.
3. Design step: Square 8.5 × 8.5, Premium Color, 80# White — Coated, Matte; binding = Case Wrap (HC) / Perfect Bound (SC). The ink-coverage warning is NORMAL on an illustrated book — the correct choice stays Premium Color, never Standard.
4. Metadata per the project sheet (identical for both): title, author Lois Farrell, contributor Jon Farrell — Illustrator, All Rights Reserved license, copyright Lois Farrell 2026, FINAL SHORT description, keywords, audience 3–8, explicit No, payee Jon Farrell 100%.
5. Upload the interior PDF. Patience rule: never click ahead while Lulu says "processing" (guessed URLs and early clicks 404'd on Santa; the working cart is https://www.lulu.com/cart).
6. After acceptance, the check is PAGE COUNT (must be 54) and trim — not the spinner.
7. If anything dies mid-run: check My Projects BEFORE creating anything again (no duplicate same-title projects).

## Handoff to Cursor (per project — its six-item spec)
Mechanics (Cursor, 2026-11-04): the handoff lands in the BRIDGE INBOX Drive folder (`1IuiukWnQcxFeINl7t-_DguikBLZwESwa`) — ONE note carrying items 2–6, plus the template PDF and the Design screenshot as FILES (never pasted into a Doc). A note without the template file is not a handoff. Cursor needs no lead time; it returns the finished cover the same way — a …-FINAL PDF dropped in the inbox for Trinity to upload (a Windows path is not uploadable by Trinity). Agreed final names: `HAJ-Cover-HARDCOVER-FINAL.pdf` / `HAJ-Cover-SOFTCOVER-FINAL.pdf`. Cursor's SC spine operating rule is TIGHTER than Trinity's thresholds: ≥ ~0.17 in keeps 9 pt; ANY result under ~0.17 in is a STOP for Jon before shrinking or dropping (the 2026-11-04 checklist update governs over the October addendum's "no spine text"). Sequencing: the SC project starts after the HC proof is ORDERED (not after the physical book arrives); family copies of either format still wait for the physical HC proof. HC build watch-out (Cursor): the real casewrap canvas is 10.25 in tall vs 8.75 in art — Cursor places faces in the template windows, never scales the wrap up, and STOPS to show Jon the placement if the turn-in bands have no art.
1. Lulu's returned cover template FILE itself (filed into `v1\04-Lulu-Templates\` on Vader).
2. Project URL + project ID + which binding.
3. The spine width and full template size printed on the template.
4. The page count Lulu accepted (54).
5. Confirmation the uploaded interior was the v1 PDF at 64,428,627 B.
6. A screenshot of the Design step showing the specs (Square 8.5×8.5, Premium Color, 80# coated, Matte, binding, no ISBN).
Cursor measures the template before building. Santa's template numbers (34 pp: HC 19 × 10.25 in, spine 0.25 in; SC 17.387 × 8.75 in, spine 0.137 in) are NOT Harlow's — scale read only: at 54 pp Harlow's SC spine should land ~0.2 in, which keeps the spine title viable (final call off the real template).

## After Cursor returns the final cover PDF
- Upload it to the project; quantities stick only after tabbing out of the field (Santa lesson); Confirm/Publish disables while processing — wait, don't re-click.
- Cover PDFs ~3.6 MB are in the range Lulu's preview accepts (Santa's blank preview came from a huge raw-embed file needing a 3–5 MB JPEG-compressed re-export).
- STOP at the proof order: payment, the soft-proof look, and addresses are Jon's. One proof per format; family copies only after Jon has the physical proof in hand.

## Update — 2026-11-04 evening (post-v1 closure, appended by Trinity background prep)

Decisions Jon made after the checklist above was filed; they govern the run equally:

1. **Softcover spine text — KEEP it (Jon, 2026-11-04 ~14:22 PT).** Jon prefers the spine title stay on the softcover so HC and SC match; dropping it is acceptable only if the real spine is too thin. Thresholds from Trinity's measurement in chat (title ink column ~0.083 in at 9pt), AS AMENDED by Cursor's locked terms in its 2026-11-04 ack:
   - Returned SC spine ≥ ~0.17 in → spine text stays exactly as-is (9 pt).
   - ANY returned spine under ~0.17 in → FULL STOP for Jon. Cursor does not shrink or drop on its own anywhere in the ~0.13–0.17 in band or below it. (Trinity's recommendation if Jon wants the title kept in the band: shrink to ~8 pt; under ~0.13 in, dropping is the expected outcome — both on Jon's word, at the stop.)
   - Scale read: Santa's 34-page SC spine was 0.137 in; Harlow's 54 pages should land ~0.2 in, so keep-as-is is the expected outcome. The real Lulu template number decides.
2. **Final-cover naming rule (Jon/Trinity, 2026-11-04 ~14:53 PT).** The template-built final covers get NEW names (e.g. `...-FINAL`) — never overwrite the TEMP-SPINE files in v1. No renaming of any existing v1 file: Lulu reads contents, not names, and the MANIFEST, packaged InDesign Links, project sheets, and this checklist all cite the current names.
3. **v1 is now complete and self-contained (2026-11-04 ~14:52 PT).** The softcover cover's InDesign package was saved into `v1\02-InDesign\Softcover\` (HAJ-Cover-Front-Back-TempSpine-SOFTCOVER-BEST-1.indd, the exact document that wrote the shipped softcover PDF at 1:58:32 PM; that PDF untouched at 3,587,068 B). All three source docs (interior, HC cover, SC cover) are now in v1. Jon also confirmed the interior PSB's 1:22:57 PM save was incidental — no content change; v1's PSB and FINAL interior PDF are in sync.
4. **Run-readiness (updated 2026-11-04 ~15:20 PT, supersedes the first filing of this item):** the two project sheets + this checklist ARE now filed in `v1\05-Lulu-Project-Info\` (3 files, 9,687 B total, listed in the MANIFEST). Trinity's Lulu login was verified live 2026-11-04 — account Jon Farrell / jonbeatz@gmail.com, both Santa projects present (SC ID 454zdy8, HC ID v82ejwq, matching Cursor's Santa records), nothing changed in the account. Option A (Trinity drives the site, Cursor builds the template covers, Jon orders the proofs) is the standing plan — recommended by both Trinity and Cursor (Cursor's consult report, 2026-11-04). Still pending: Jon's go to start the run itself.

**Reconciliation (2026-11-04 ~15:27 PT):** Cursor's ack flagged that the copy of this checklist in `v1\05` still carried the pre-ack spine band (shrink in the band) and lacked the proof-order gate and the hardcover turn-in stop. The spine rule in item 1 above now states the locked terms (stop-for-Jon under ~0.17 in), and the proof-order gate + turn-in stop are in the Handoff section of this file. THIS version supersedes the copy previously in `v1\05` — Jon to drop it over that copy so the folder record matches the locked terms Cursor confirmed.


---

## Addendum 2026-11-04 (evening) — standing cover-start rule (Jon locked)
Future covers START on Lulu's real geometry (casewrap canvas incl. boards + 0.625 wrap; spine estimated, stamped ESTIMATE) — the trim+bleed canvas is retired as a starting shape. Only the spine band may move when a template returns; art is never rescaled. Full spec: files/COVER-START-SPEC-2026-11-04.md. Cursor prompt for the two blank starter PSDs (HC 5700×3075 / SC 5250×2625) filed as files/CURSOR-PROMPT-STARTER-COVER-PSDS-2026-11-04.md.

---

## ADDENDUM 2026-11-05 — THE GOAL LAW (supersedes the Details sequencing note above)

The 2026-11-04 assumption "Details unlocks once Design completes" was WRONG. A Lulu project's **creation goal** gates everything: "Print Copies for Your Own Use" has NO metadata forms, NO pricing step, and Private Access only — the forms are absent, not locked. To sell Santa-style (shareable link, ~80% of markup, no ISBN), the project must be under **"Publish Your Book" + Lulu Bookstore** — set at creation, or switched later via Revise → Start → "Select a Goal" → Pricing & Payees (list price) → Retail Options → **Select Access** → "Publish to the Lulu Bookstore." Full record: LULU-RUN-KNOWLEDGE-2026-11-05.md (bridge inbox) + Playbook §35. Harlow HC: created under Personal Printing (2026-11-04), published COMPLETE v1 Private, goal switch run 2026-11-05 on Jon's go (list $26.00, Select Access). Future projects: create under the FINAL goal from day one.

## BEST-23 revision — 2026-11-05

Uploaded 2026-11-05 after Trinity's verification. My Projects confirms hardcover rmq8eyw at Version 4 and softcover v854g55 at Version 3. Both are COMPLETE and SELECT ACCESS. Hardcover list $26.00, print $22.58. Softcover list $16.00, print $13.76. Payee Jon Farrell (yjpmy9) 100% on both. Metadata, pricing, payee, and access were not changed.

The revision procedure, including the Retire misclick, the spec radios clearing after an interior upload, and the interior that stayed VALIDATED until a second upload, is in `.cursor/docs/LULU-BOOKSTORE-SELECT-PLAYBOOK.md` under "Revising a book that is already published." Trinity's download-back check and the verified BEST-23 results are in that same section.

Trinity's download-back on 2026-11-05: the source interior is 65,008,627 bytes in both projects, SHA-256 `d6a8807af1dcb8277b1fc3abc8823090d873db91b79f25255ab3700ed8ccfea6`. Hardcover cover 5,027,947 bytes. Softcover cover 4,091,305 bytes. Print-ready text differs from published BEST-22 by exactly two tokens: peek `By:` to `By`, and spread 22 left `sites` to `sights`. Cover byline twice, colon byline zero, on source and print-ready. Files built, uploaded, held, and printed from match. Physical proof copies are still unproven.

What changed from BEST-22:
- The byline is "Written By Lois Farrell" (the colon is gone) on the interior peek and on both cover faces.
- Spread 22 left reads "familiar sights".
- The peek-left art sits lower. That move is in the plate.
- Spread 09 is Jon's new plate. The Photoshop smart object is 5250x2625 at 300 ppi and is placed 1:1.

Staged upload files, in `v3\03-Deliverables-PDF` only:
- Interior: `HAJ-Interior-FROM-PHOTOSHOP-BEST-23-LULU.pdf` — 65,008,627 bytes, 54 pages.
- Hardcover cover: `HAJ-Cover-HARDCOVER-FINAL-JON-v3.pdf` — 5,027,947 bytes.
- Softcover cover: `HAJ-Cover-SOFTCOVER-FINAL-v2.pdf` — 4,091,305 bytes.
