# FYI — Lulu run knowledge: the goal law + the full Harlow HC run

From: Trinity — for Cursor (and Ravyn). Filed 2026-11-05 ~00:05 PT, while the goal-switch session was live.
Re: Lulu project `rmq8eyw` — "Harlow's Accidental Journey — Hardcover"

Everything below was learned live on the 2026-11-04/05 Harlow hardcover run. Most of it cost real time; all of it is now the standing process. If a future run contradicts any of it, flag it — do not silently improvise.

## THE GOAL LAW (the single biggest lesson)

A Lulu print project's **goal**, chosen at creation, determines what the project can EVER do:

- **"Print Copies for Your Own Use" (Personal Printing)** — author copies at print cost, nothing else. The wizard shows ONLY Start / Design / Review. There are **no metadata forms, no pricing step, and no access controls anywhere in the project** — not hidden, not locked, *absent*. Direct URLs (`/account/wizard/<id>/details`, `/copyright`, `/pricing`) redirect to Start. The step list may show those steps with check marks; they are inert. Publishing under this goal = COMPLETE + **Private Access**, list price defaults to print cost ($0 revenue), **no buy link exists**.
- **"Publish Your Book" (Retail Sales)** — unlocks Details / Copyright metadata, **Pricing & Payees**, and Retail Options. Checking **Lulu Bookstore only** = **no ISBN required**, no tax forms, 80% of the markup (after print cost) to the author, paid via the account's existing payee (Jon's = PayPal, set up on the Santa book).
- **Global Distribution** (Amazon / Ingram / B&N) — a different lane: ISBN required (free Lulu ISBN or your own), tax forms, print channels cannot be opted out individually. NOT part of the family/direct-link model.

**Rule: decide the sales model BEFORE creating the project, and create it under the matching goal.** Harlow's HC was created under Personal Printing (family-run thinking) and therefore could not take a price or a link until the goal was switched.

## THE GOAL SWITCH (changing a live project to sellable)

Documented by Lulu's help ("Selling on Lulu.com") and executed on rmq8eyw on Jon's go:

1. Project → Revise / Continue Editing → wizard **Start** step.
2. Scroll to **"Select a Goal"** → select **Publish Your Book** → check **Lulu Bookstore only**.
3. The Details / Copyright forms wake up under this goal — fill from the locked project sheet (title, author, contributor/illustrator, © holder + year, All Rights Reserved, edition line, description, keywords, category, explicit = No).
4. **Pricing & Payees** → set the USD list price; accept auto-converted equivalents for other currencies; keep the existing payee (do not re-enter payment details).
5. **Retail Options** → **Select Access** (buyable ONLY via the direct URL — the Santa/Facebook model; not searchable) or General Access (searchable in the bookstore). Private Access = author only.
6. **"Publish to the Lulu Bookstore"** → the product page + shareable URL are created immediately.

Harlow HC locked values: list **$26.00**, print cost $22.58 → $3.42 markup → ≈ **$2.74/copy** to Jon at the 80% rate.
_(Outcome of the 2026-11-05 switch run: appended to this note when the session reports.)_

## WHAT WORKED (keep doing)

- **Uploads via the Design step**: interior replace = "Replace your PDF file"; cover = "Upload Your Cover". A 64 MB interior and a 5 MB cover both uploaded natively through Trinity's browser. (Santa-run history said Cursor's browser can't drive the OS file dialog — Trinity's browser CAN and remains the upload lane.)
- **Never click ahead while Lulu says "processing."** Wait for the success line ("Your Book file was successfully uploaded!" / "You successfully uploaded a cover file!").
- **Review page = ground truth** for specs + page count + print cost. Confirm there before publishing.
- **Cover geometry verified from Lulu's own read-back**: 1 page, 19 × 10.25 in, spine 0.25 in, fonts embedded, layers flattened — matches the returned template exactly.
- **Revisability**: a published project can be Revised at any time (files swapped, re-confirmed). Only copies already ordered are frozen to the files at order time. Publish is not a point of no return.

## WHAT DIDN'T WORK / GOTCHAS

- **Specs can silently unregister.** After the first interior acceptance, the Design UI held NO ink/paper/binding/finish selections and print cost showed "–". Fix: re-affirm — never change — the locked specs in order (Premium Color → 80# White — Coated → Hardcover Case Wrap → Matte) until the Review page shows all four + the cost. Verify specs on Review, not on Design.
- **The ink-coverage warning is NORMAL** for a fully illustrated book ("high levels of ink coverage… may result in less readable print quality"). Do not downgrade Premium Color or any spec because of it.
- **Hunting for metadata forms under Personal Printing burns ~35 minutes.** If the wizard shows only Start/Design/Review, the forms do not exist for that project — check the GOAL first (see the law above). Trinity's earlier working theory ("Details unlocks once Design completes") was WRONG — it is goal-gated, not sequence-gated.
- **No pricing in the Personal-Printing publish flow.** "Confirm and Publish" there just finalizes the private project; the version history will show List Price = Print Cost. A price can only be set after the goal switch.
- **Wizard sign-in (api.lulu.com, client_id=project-wizard) hits Cloudflare repeatedly.** The check stalls at "Verifying…"; the working recovery is a fresh browser environment + fresh sign-in with the saved vault login (jonbeatz@gmail.com). Expect to do this more than once in a long session. **One session at a time** — Jon stays logged out of Lulu everywhere else during a run.
- **The Review page shows a generic "Success! Congratulations! Your Book was successfully published!" heading as page furniture.** It is NOT evidence a publish action happened. Judge state by My Projects (status, version, access), never by that banner.

## THE HARLOW HC RUN, END TO END (for the record)

1. Project created 2026-11-04 (Personal Printing goal — see the law), Square 8.5×8.5, Premium Color, 80# coated, Case Wrap, Matte. Template returned: 19 × 10.25 in, spine 0.25 in.
2. Interior BEST-21 uploaded + accepted (54 pp, $22.58) as a placeholder while the final build finished.
3. Final files (LuLu-Master-Deliverables **v2**, from `03-Deliverables-PDF` only): interior = BEST-22 build, quote-swept clean by Trinity (144 marks, 0 anomalies) — replaced in via "Replace your PDF file", accepted 54 pp; cover = `HAJ-Cover-HARDCOVER-FINAL-JON-v2.pdf` (5,031,055 B, SHA-256 verified against the inbox copy) — uploaded, accepted.
4. Published (Jon's go) → COMPLETE, Version 1, Private Access.
5. Goal switch (Jon's go, 2026-11-05) → Publish Your Book + Lulu Bookstore, $26.00, Select Access. _(Outcome appended on report.)_
6. Remaining: **Jon orders the physical proof himself** (payment + soft-proof look). SC project starts only after the HC proof is ORDERED, and is created under the correct goal from day one.

## FOR FUTURE PROJECTS (checklist delta)

- Create under the FINAL goal. For a Santa-style direct-link seller: **Publish Your Book + Lulu Bookstore, Select Access** from the start — metadata + pricing then exist in the first pass and no switch is needed.
- Keep the locked metadata on the project sheet regardless — under the right goal it all gets typed in.
- Trinity runs Lulu uploads/publish steps; Jon alone orders (payment). Cursor builds files; Cursor never drives Lulu.

— Trinity

## OUTCOME — goal switch completed (2026-11-05, Trinity-verified on the live shop page)

- rmq8eyw is now **Version 3, COMPLETE, SELECT ACCESS** on My Projects (with the SELECT ACCESS link shown, like Jon's older books). List **$26.00**; print $22.58; gross $3.42; Lulu share $0.68; **author revenue $2.74/copy** (Payee: Jon Farrell, PayPal, 100% — untouched).
- **Buy link:** https://www.lulu.com/shop/lois-farrell-and-jon-farrell/harlows-accidental-journey/hardcover/product-rmq8eyw.html — live, InStock at $26.00, showing the locked description, All Rights Reserved, "By (author): Lois Farrell, Illustrated by: Jon Farrell".
- Under the Publish goal, the metadata forms EXIST and were filled from the sheet: copyright (Lois Farrell, 2026, All Rights Reserved), edition "First illustrated edition", BISAC **JUVENILE FICTION / Animals / Cats**, all 10 keywords, audience Children/Juvenile, explicit No, **"Proceed without ISBN"** — no ISBN added. Distribution: Lulu Bookstore ONLY.
- Traps caught in the flow (verify on Review before publishing): (1) **Global Distribution was checked BY DEFAULT after the goal switch** — uncheck it explicitly. (2) Copyright year + illustrator's last name did not persist on the first pass — fields need a Tab/commit; re-check the Review summary. (3) The USD price did not persist across navigation until all five currency prices were filled (Lulu auto-conversion supplied them; USD then re-set to exactly 26.00).
- Files/specs untouched by the switch. Remaining: Jon orders the proof; SC starts after.

## FINAL OUTCOME — softcover published (2026-11-05 ~01:58, via YOUR browser on Vader — thank you)

- v854g55 "Harlow's Accidental Journey — Softcover": **Version 2, COMPLETE, SELECT ACCESS**, Lulu Bookstore. List **$16.00**; print **$13.76**; **author revenue $1.79/copy** (payee Jon Farrell, PayPal, 100%). Access verified on a fresh Retail Options reload: Select selected ("Unlisted… available only by a direct URL"), General/Private unselected. SC project sheet in v2\05 closed out by you 2026-11-05 02:02 (status PUBLISHED + buy link; manifest row refreshed).
- **Both buy links (keep on file — if Jon asks for help with either listing, start here):**
  - HC $26.00 (rmq8eyw, v3): https://www.lulu.com/shop/lois-farrell-and-jon-farrell/harlows-accidental-journey/hardcover/product-rmq8eyw.html
  - SC $16.00 (v854g55, v2): https://www.lulu.com/shop/lois-farrell-and-jon-farrell/harlows-accidental-journey/paperback/product-v854g55.html
- **Why your browser ran it:** Trinity's Lulu sign-in was Cloudflare-walled twice (01:20 + 01:38 attempts; the verification loop binds the VM's datacenter IP + browser fingerprint, and even Jon's own takeover clicks looped). Your Vader browser on Jon's home connection passed instantly. STANDING FALLBACK: if Trinity's Lulu sign-in walls again, the publish lane is Cursor's browser on Vader with Jon present for the credential step.
- **Findings from your publish pass (new since the HC switch):** (1) USD alone did not persist and Lulu did NOT auto-convert this time — all five currency prices were hand-filled from Lulu's printed minimums (EUR 15.41 / AUD 24.16 / GBP 12.47 / CAD 24.47), USD exact at 16.00. (On the HC switch, auto-conversion supplied them — behavior differs per pass; always fill all five and re-set USD.) (2) **The payee does not carry into a new project** — v854g55 had NO payee attached, which blocked Review; you attached the existing Jon Farrell PayPal payee at 100%. Future projects: attach the payee explicitly. (3) **Access is chosen in the post-publish retail dialog** (General/Select/Private) — the wizard Complete screen's access radio is a pre-selection display, not the final state; verify access on a fresh Retail Options reload after publishing. (4) No ink-coverage warning on the SC cover upload (the HC interior warned; illustrated covers may not). (5) Lulu stated the book is not eligible for Global Distribution (no ISBN) — consistent with the plan; it stays off.
- Remaining: Jon orders the physical proofs for BOTH formats (his step). When both proofs are ordered, the dated BOOK-BUILD-BIBLE entry is owed (both project IDs, template sizes, print costs, goal law, Cloudflare rough spot + Vader fallback) and LuLu-Master-Deliverables v2 freezes. Nothing else open on the Lulu run.
— Trinity

## TRINITY RECONCILIATION (2026-11-05 ~02:30) — Cursor's read-back, resolved

Cursor read this note, the Playbook, and the Ravyn/Folio note, and flagged conflicts instead of harmonizing (per protocol). Resolutions:

- **Access radios:** the FINAL OUTCOME wording ("pre-selection display") is corrected per Cursor's live observation: the wizard Complete-screen radios sit UN-SET until the choice is made in the post-publish retail dialog. Final state verified twice on fresh Retail Options reloads (his + the closeout check): SELECT ACCESS. Playbook §35 addendum corrected in place the same night.
- **Santa softcover ID — SETTLED: 454zdy8.** Cursor read the partly-visible card as 454zdv8 (twice); Trinity re-read Jon's own My Projects screenshot (2026-11-05 02:08) at 5× enlargement: the ID prints "454zdy8" — the 5th character carries a descender (a 'y', not a 'v'). The checklist and Trinity's 2026-11-04 account verification (which matched Cursor's own Santa-era records) agree. Cursor's FOR-TRINITY note gets the one-character fix (hygiene prompt item 1).
- **Bible trigger:** this note's FINAL OUTCOME deferred the BOOK-BUILD-BIBLE entry until proofs are ordered; the Bible's own rule (update after every Lulu run) governs — the entry is due on the run itself. Hygiene prompt item 2 directs it now; the deferral wording here is superseded.
- **Sheet closeout addendum:** after this note's FINAL OUTCOME was written, the SC sheet got one more edit — the geometry line (02:19:21), taking it to 2,787 bytes; its manifest row reads 2026-11-05 02:19:21 | 2787. The closeout record above (stopping at 02:02) is complete with this line added.
- **Historical layers stand as the plan of record:** the checklist's step 1 goal wording, its v1/BEST-21 upload block, and its "Jon logged out on Vader" line, and this note's early sections, describe the pre-run plan; the OUTCOME sections and the Playbook §35 addendum record what actually happened (SC published from Vader under Publish Your Book, no proof ordered, BEST-22 from v2). Playbook §35.6's two superseded standing rules (lane split, SC-after-proof sequencing) were stamped SUPERSEDED in place 2026-11-05. The v2 checklist's plan-layer lines get the same in-place stamps via the hygiene addendum.
- **Still open (one item):** payee ID spelling — Cursor read yjpmry9 off the live page; Trinity's HC record says yjpmy9. Unresolved by design until a payee screen is read again (hygiene prompt item 4). No impact on payments.
— Trinity
- **Payee ID — SETTLED (2026-11-05 ~02:51): yjpmy9.** Read off the "Payees for Your Book" panel in Jon's own screenshot (Jon Farrell · ID yjpmy9 · jonbeatz@gmail.com · PayPal · USD). Trinity's HC record was correct; Cursor's yjpmry9 carried an extra 'r'. Cursor's FOR-TRINITY note gets the same one-character fix. With this, every item in this reconciliation is closed.

---

## REVISION RUN — 2026-11-05 (BEST-23: HC v3→v4, SC v2→v3) — combined desk findings

Cursor published the revision from the Vader browser and documented the flow in `.cursor/docs/LULU-BOOKSTORE-SELECT-PLAYBOOK.md` ("Revising a book that is already published"); the same section is folded into the Playbook as **§35 ADDENDUM 2**. The traps that will bite the next upload if forgotten:

- **Revise = navy button; Retire = cyan button directly under it.** A miss opens "Retire this Book" — Cancel is safe.
- **A new interior upload clears the spec radios and returns the cover to pending**, even if the cover file is unchanged. Re-select the published spec (Premium Color → 80# Coated → binding → Matte). Ink warning normal; never Standard.
- **Green "uploaded" banner + 54 pages ≠ normalized.** SC Design stayed incomplete on a validated-only interior; a reload didn't fix it. Uploading the SAME interior a second time + re-selecting spec + confirming the unchanged list price is what published SC v3. Never upload a third time before reading file status and publish errors.
- **Print cost must read back at $22.58 / $13.76 before leaving Design.** Pricing may claim the list price changed when it hasn't — read, then Confirm.
- **Proof of publish = the My Projects card** (new version + COMPLETE + Select Access), never the success banner. No Order Copies clicks; no access-radio changes.

Trinity's verification layer (also in §35 Addendum 2): Project Details pages show NO file names/sizes — verify via the **Source Files** / **Print-Ready Files** download buttons. On this run: source files byte-exact with original names (interior 65,008,627 in both projects; covers 5,027,947 / 4,091,305); the two source interiors SHA-256 identical (d6a8807a…); print-ready interiors differ from the published BEST-22 text by exactly the two approved strings ("By:"→"By", "sites"→"sights"); all cover PDFs read the colon-free byline ×2; render spot-checks must be **trim-aligned** (bleed false-alarms). Buy links are project-bound — revisions never change them; strip `?page=&pageSize=` review-pagination suffixes when sharing. Trinity's browser also read both project pages directly this run (fresh environment + saved login beat the morning's Cloudflare wall), so read-only verification no longer depends solely on the Vader lane.
— Trinity

## PLATFORM FACTS — author pages + finding buy links (checked live 2026-11-05 evening)

- **Finding a project's buy link inside Lulu:** there is NO "View in Bookstore" button, share button, or printed URL anywhere on the Project Details page or in Version History. The link is the **"SELECT ACCESS" text itself** — Project Details → "Retail and Publishing" → "Lulu Bookstore Settings" (also in the header summary) — clicking it opens the public buy page in a new tab. The line above it reads "Unlisted on the Lulu Bookstore and available only by a direct URL."
- **Contributor name links** (clicking "Lois Farrell" / "Jon Farrell" on a product page) run a Bookstore contributor SEARCH. For Select Access projects it returns "No search results" — no books, no bio area — because Select Access is unlisted and not indexed. Verified live 2026-11-05. Not a defect; it's the access setting working as designed.
- **Author Spotlight** (Lulu's author page: bio, photo, website link, book list, lulu.com/spotlight/<name>/): **requires General Access.** Lulu help article 64000261190: with only Private/Select Access projects "you will not be able to create an Author Spotlight," and "Only projects with General Access will be displayed." Jon's Promote page (lulu.com/account/promote) shows only Promotional Pricing — no Spotlight option appears. Creating one = flipping a project to General Access first (which also makes it searchable and populates the contributor pages). DECISION (Jon, 2026-11-05 evening): both Harlow projects STAY Select Access — he weighed the empty contributor pages + no Spotlight against going public and kept the family-run posture; Spotlight is revisited only as a by-product of a future public/Amazon phase, not as a standalone fix.
- Spotted, not investigated: Santa softcover (454zdy8) shows an "Unpublished Draft" notice on My Projects (2026-11-05).

## SANTA WHITES + PAGINATION FINDINGS (2026-11-05 evening — Jon's catch)

- **The white leaves in the printed Santa HC are BINDERY ENDPAPERS, not file pages.** Santa print-ready interiors (BOTH formats) = 34 pages, ZERO blank-white pages; the interior PDF is byte-identical in size across SC/HC (29,278,936 B — shared interior). Structure: p1 solid burgundy → designed spreads → p32 Happy Holidays | p33 solid burgundy → p34 solid burgundy. The physical HC adds white flyleaves at both ends in case binding. Harlow HC will have them too, by construction; Harlow SC (perfect bound) prints the file exactly. No spacer page in any file creates or removes them.
- **PAGINATION LAW (the big one): designed spreads face each other in print ONLY when the interior starts on an even-page offset — i.e., ONE page precedes the first designed spread.** Santa has it (solid p1; plates land on facing pairs (2,3),(4,5)…). **Harlow BEST-23 does NOT**: p1 = peek-L, so every designed spread sits back-to-back on a leaf (peek split; cast grid split across the last two openings — verified by rendering facing pairs from the print-ready PDF). Fix = insert ONE page before the first spread + ONE after the last (54 → 56 pp); plates/art unchanged, positions shift by one. Flipbooks/decks/PSB show plates whole, so this fault is invisible on every review surface — only the printed object shows it. CHECK PAGINATION ON FACING PAIRS (render (2,3),(4,5)…) for every future book build.
- Lulu Source-Files downloads for the Santa projects repeatedly served ~900-byte stub ZIPs (ExpiredToken XML inside) on 2026-11-05 — 7 attempts, both projects; Print-Ready zips stubbed once then succeeded on retry. If a Source zip lands suspiciously small, check its contents before trusting it.
- Status: COLOR DECIDED (Jon, 2026-11-05 evening) — the bookend is Jon's warm ivory watercolor-wash page (banked: goal files/HAJ-BOOKEND-PAGE-WASH-2625.png, exactly 2625x2625). Jon is dialing in the FINAL front and back wash pages in Photoshop at home (back = a very similar wash, his variant/flip) and will show Trinity before calling them ready. Then: Cursor revision build (56 pp) + Lulu revision (HC v5 / SC v4) BEFORE Lois orders proofs; 2D flipbook unchanged. PLUS Jon's standing requirement: rebuild the 3D flipbook to mimic the physical book — white inside-cover leaf after the front cover (and, by symmetry, before the back cover), wash bookends as real leaves — so the pagination lesson can't be forgotten.
- DOCUMENTATION REQUIREMENT (Jon, 2026-11-05): when the bookend revision is built, the LuLu-Master-Deliverables set and ALL documentation update WITH it — a new build in the documents, the front/back wash pages recorded as design decisions with the why (pagination law), so no future run can forget them. The 3D flipbook also mimics the physical opening: a fake left side of the opening (the back of the front cover, plain white) facing page 1 — mirrored at the back. Pagination law filed permanently in Playbook §36.

## SANTA SOURCE FILES — RESOLVED (2026-11-05, 20:25–20:38 retry)
The morning/evening ExpiredToken stubs were TRANSIENT serve failures, not a dead end. Retry the same night landed both real zips: HC source 32,349,537 B, SC source 64,281,395 B. Trick when the Source Files generation spins and silently returns to the button: reload the project details page and click again — the file then serves immediately (HC came first try; SC took three stalls + one reload). Contents verified by Trinity: original filenames inside (TNIMS-Interior-FINAL.pdf, TNIMS-Cover-FINAL.pdf, TNIMS-Cover-SOFTCOVER-FINAL.pdf); interiors byte-size-identical across formats (29,283,260 B, 34 pp, 630x630 pt); source interior = print-ready interior pixel-for-pixel (max mean abs diff 0.01 over 34 pp); ZERO blank pages in the source; p1 + p34 solid burgundy (73,13,22) in the uploaded originals. Santa record now closed at every level: source = print-ready = printed copy.
