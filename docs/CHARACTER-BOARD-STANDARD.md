# THE CHARACTER BOARD — our standard (v1, set 2026-11-19 by Jon + Trinity)

Every cast character in *Harlow's Helping Paws* gets ONE board in this exact format, built from their locked cast portrait. The format is harvested from the best reference boards Jon collected (an animated-3D-style Harlow board, a photoreal Chowder board, a Cash cockatiel board — banked in `cast/board-refs/`) and rebuilt as ours. **The layout is the standard; the art is always our §5 finish** (polished dimensional storybook — never the exemplars' 3D gloss or photoreal).

## How it's built (why it stays consistent)

- The **panels are generated** off the character's locked cast portrait (identity + finish authority), one strip per section.
- **All text is typeset** in the compositor (never generated) — names, labels, traits, palette hexes and checklists are always letter-perfect.
- **Palette hexes are sampled from the character's actual portrait pixels**, never invented.
- Board file: `cast/<name>-character-board.png` (2800×2100). Panels banked in `cast/board-panels/`.

## Layout (landscape 4:3, ivory board, warm hairline panel cards)

- **Left column:** character name (display serif) · "CHARACTER SHEET" · finish tag ribbon · the locked cast portrait (hero) · trait list (paw bullets, from the recipe).
- **Head shots** (5): Front · Three Quarter · Left Profile · Right Profile · Happy.
- **Turnaround / model sheet** (4, standing, one scale): Front · Left Side · Back · Right Side.
- **Expressions** (6): Neutral · Curious · Alert · Relaxed · Happy · Content.
- **Actions / poses** (8): Sitting · Standing · Walking · Looking Up · Laying Down · Stretching · Playing · Jumping / Reaching.
- **Details** (8 tiles, right column): Eye · Nose · Chin & Muzzle · Whiskers · Paw · Fur Texture · Ear · Signature feature (Harlow: tail plume).
- **Bottom band:** Color palette (8 swatches, name + hex, sampled) · Size & proportions (side-view mini + measured list from the recipe) · Key traits to maintain (checklist = the recipe's NEVER CHANGE, distilled).
- **Footer:** Style guide line — the §5 finish in one sentence + "keep consistent with this board."

## Rules

1. A board is built **only** from a locked portrait — no board before the lock.
2. Same sections, same order, same labels for every character. Species-specific swaps allowed only inside Actions and the 8th Detail tile.
3. Any panel that drifts (markings, finish, build) fails the board — regenerate that strip, never patch a board together from mismatched takes.
4. The board + the portrait are the two attachments on every future brief for that character.

## Harlow's board (first build, 2026-11-19)

Palette sampled from the canonical portrait: Tail Chocolate `#5A1D06` · Deep Seal `#612A11` · Warm Brown `#893D16` · Caramel Body `#E58944` · Cream Fur `#FDD9A2` · White Fur `#FAE5D4` · Azure Eyes `#3CB5F0` · Pink Nose `#E77C6A`.
Supersedes the six-study sheet (`harlow-character-sheet-v1.png`, kept as a take) as the board format.

## V2 AMENDMENT (Jon, 2026-11-19 late) — single-pass generated board
Jon supplied the "Universal Dimensional Animated Storybook Character Recipe V1" (banked: board-refs/universal-dimensional-storybook-recipe-v1.md) — the master recipe behind the exemplar boards he likes. V2 boards are generated in ONE gpt-image pass (Codex lane) using that recipe's §43 master-board prompt + §44 style lock, with the character's own locked portrait attached as identity authority and the exemplar board as layout guide. Our character details (identity block, measured palette, traits) replace the recipe's placeholders — identity always wins over the generic recipe (§2 conflict rule).
- Sections per §34: script name + ribbon, paw-bullet traits, hero, head shots (5), turnaround (4 — front view may sit, as in the exemplar), expressions (8), actions (8), details (8), painted palette swatches with hexes, size & proportions with dimension arrows, key traits (11), style-guide footer.
- GATE: proof every label at 3x zoom. Palette hexes verified digit-by-digit. A typo may be fixed with a surgical typeset patch (measured geometry, condensed serif, diff confined to the word box) — art is never patched; a drifting panel = regenerate.
- Harlow v2 (2026-11-19): PASSED — all hexes correct, actions clean (no cut/extra tails), one typo ("Mediuen") typeset-fixed. Canonical: cast/harlow-character-board.png (1536×1024). The v1 composited board is retired (kept as harlow-character-board-v1-composited.png).

## TEXT-BLOCK RULE (Jon, 2026-11-19 late — supersedes the typeset-patch allowance above)
If a generated board has a text error, do NOT typeset-patch it: a patched word never matches the generated hand (Jon: the other lines look "tight like a typewriter," a patch looks drawn-on and misaligned). Instead, crop the affected text panel and have the image model regenerate THAT PANEL's text (all lines, exact spellings supplied), then composite the crop back with a feathered mask and gate the seams. Harlow v4 fixed this way: Key Traits panel regenerated — all 11 lines now uniform, "Medium" correct. Canonical updated to the v4 composite.

## FOOTER STYLE LINE (Jon, 2026-11-19)
Every FUTURE character board carries a one-line style note in the footer, beside the motto "Preserve the character first; stylize second":
"Finish: Polished dimensional storybook — rich color, grouped rounded forms, warm dimensional light."
The line goes into the board generation prompt verbatim so the model typesets it with the footer. The full style prose stays in the recipe (§5) — the board gets this one line only. Harlow's board is locked as-is and is NOT regenerated for this; the rule starts with the next character (Lois).

## DRESS LOCK + HUMAN-FACE CONTENT METHOD (Jon, 2026-11-20 — from the Lois board rounds)
- **Presentation dress is LOCKED to the decorated exemplar style** — painted title treatment, floral/watercolor accents, scene-backed panels, watercolor palette dabs (the Harlow v4 / Lois v1 dress). A clean flat typeset layout is NOT an approved presentation: Lois board v3 (2026-11-20) had its content approved but its dress rejected by Jon. Typeset text is acceptable only for small panel labels inside the decorated dress.
- **Human faces are built from governed parts, not one pass.** One-pass generation genericized Lois's face twice (v1, v2). The approved method (Lois v3 content, carried into v4): hero + detail panels are REAL CROPS of the canonical portrait/full body; head shots, expressions, turnaround and actions are generated in small batches, each governed directly by the canonical portrait; the board is assembled programmatically inside the decorated dress. One-pass remains fine for animals (Harlow's identity is fur + markings).
- **Canonical maintenance:** when a canonical portrait or full body changes, the board's hero + detail crops are re-cropped from the current canonicals in the same pass. (2026-11-20: Lois's canonicals were background-warmed to the golden family tone — pale originals banked as `lois-cast-*-PALE-ORIGINAL.png` — and board v4's hero/details were re-cropped from the warmed files.)

## GRID LOCK (Jon, 2026-11-20 — the Harlow grid is THE layout for every board)
Jon's ruling after the Lois v5–v9 rounds: the layout drift between boards ends here. Harlow's approved board (cast/harlow-character-board.png) is the layout authority — every future board, human or animal, is built on this exact grid. Earlier boards composed sections freely per generation; that drift is what made Lois's board differ from Harlow's (traits mid-right, size bottom-right, boxed hero). Content flexes inside the grid (head-shot count, size treatment); POSITIONS NEVER MOVE.
- **Title + identity:** top-left — painted name, book/character-board line, HERO CHARACTER header, identity notes (paw bullets) in the left column.
- **Hero:** FREE-STANDING and large in the left-center on open garden wash — NO window box, NO border (Harlow's treatment). Zone background = plain warm ivory wash so the canonical figure blends in.
- **Head shots:** top-center window, directly right of the title block.
- **Turnaround:** directly under the head-shots window, same width.
- **Details:** right column, 8 tiles stacked, top to ~80% height.
- **Expressions:** bottom-left, two rows.
- **Actions:** center, two rows of 4, right of expressions.
- **Color palette:** bottom-left row, 8 dabs with painted names + hexes.
- **Size & proportions:** bottom-CENTER.
- **Key traits:** bottom-RIGHT.
- **Footer:** motto + finish line across the bottom.
- **Labels:** in reserved parchment bands under each window/row (the Lois fix treatment) — never touching a panel border, never painted inside a window's image area.
- **Gate addition:** every board gate now includes a LAYOUT DIFF against Harlow's board — section positions checked against this grid before content checks. A board that drifts off-grid fails regardless of content quality.

## METHOD CHANGE — ONE-PASS RECIPE IS PRIMARY (Jon, 2026-11-20)
Jon made Lois's adopted board himself in ChatGPT in ONE generation pass: four references, each with an assigned job — (1) canonical close-up = face master, (2) canonical full body = body/wardrobe master, (3) Harlow's approved board = layout template, (4) a prior board of the same character = secondary ideas only — plus a verbatim prompt spelling out every label, the grid percentages, and "full-size readable subjects instead of tiny clustered figures." Result: digit-exact palette, clean lettering, filled cells, zero seams — everything the plate-and-paste pipeline (Lois v3–v12) fought for two days. **One-pass with this recipe is now the PRIMARY board method.** Full recipe banked at cast/board-parts/LOIS-BOARD-RECIPE-JON-CHATGPT-2026-11-20.md. The governed-parts assembly method above remains the FALLBACK when a one-pass face drifts or beautifies (the Mira risk), and its gates still apply to whichever board is adopted. Adopted Lois board: cast/lois-character-board.png (Jon's one-pass, adopted 2026-11-20; the best composite, v12, stays banked as a candidate).

## THREE-PASS REFINEMENT (Jon, 2026-11-20 — from the Mira board)
The one-pass recipe extends to three passes when likeness needs tightening: (1) generate the board one-pass; (2) a LOCALIZED CORRECTION pass — re-attach board + face master, edit ONE cell only, preserve everything else (first use: a right-profile cell drawn facing the same way as the left; GATE ADDITION: always verify the two profiles face OPPOSITE directions); (3) a LIKENESS pass — re-attach board + face master and REPLACE the Front head-shot tile with the actual reference portrait as a scaled crop (crop shoulders/cap to fit; never redraw the face; keep its background), then redraw the surrounding faces toward the portrait (fuller cheeks, rounded chin, brow weight, exact nose width, smile unevenness; tone down exaggerated eyes/grins) and pull the hero's face closer too. Mira's adopted board came from this sequence (Jon in ChatGPT); full recipe: cast/board-parts-mira/MIRA-BOARD-RECIPE-JON-CHATGPT-2026-11-20.md. Known accepted deltas on that board: Cap Pink swatch prints #FDB9CB (Trinity misread it as #FDB9C8 at adoption; corrected 2026-11-20 — the lock stays #F96E6B in the recipe file), 6 short traits, blank badge tile.

**CAST BACKGROUND STANDARD (Jon, locked 2026-11-20):** solo portraits and full bodies sit on the golden warm-ivory watercolor wash ≈ RGB 252,224,184 (background only, faint grounding shadow, no scenery); boards use the same warm ivory family for their open wash and panel grounds, so a character reads identically on their portrait, their board, and any card. Never pale studio white, never a per-character hue.

## PRE-FLIGHT SELF-CHECK (added 2026-11-20, Jon — after the Maria/Jon board miss)
On the live project, two boards shipped built from a reduced brief and gated on text/profiles only; both were missing turnaround, palette hexes, size block, and half the expressions/actions/details. Jon's ruling: check YOURSELF against the exemplar board before generating and before delivering — generating the wrong board wastes credits. Standing rules:
1. Every board brief carries the FULL section inventory with counts (head shots 5 · turnaround 4 · details 8 · expressions 8 · actions 8 · palette 8 with measured hexes · size block · key traits · identity checklist · footer) — pasted into the prompt, never summarized from memory.
2. Before banking or delivering any board, run the LAYOUT DIFF against the exemplar board section by section and state the result. Any missing section = FAIL, regardless of how good the art looks. No delivery without the diff.
3. The palette hexes are sampled from the character's actual art (portrait/full body/detail tiles) BEFORE the brief is written, and verified digit-exact on the finished board at 3x.
4. **Orientation check:** the LEFT PROFILE and RIGHT PROFILE head shots must face the directions their labels claim, and so must the turnaround's side views. (Added 2026-11-20, kit v1.2.3 — a commissioned board's first take mirror-reversed BOTH profile pairs against their labels; only the layout diff caught it. The three-pass gate already checks that the two profiles face opposite directions; this extends the check to *matching the labels*, head shots and turnaround alike.)

## LIKENESS GOVERNANCE — THE PORTRAIT IS THE VERDICT (added 2026-11-20, Jon — the Jon board v3→v4 lesson)
A board can pass every layout and text check and still be wrong: on the live project, a rebuilt board passed the full grid gate, but Jon rejected it on sight — its faces were a plausible cousin of the man, not the man in the approved locked portrait (narrower face, smaller nose, weaker jaw, thinner beard, muted signature silver). Rules:
1. The face verdict belongs to the locked portrait, and the user's eye overrules the gate. Sections passing ≠ board done; the identity verdict is a separate, final check, face by face against the portrait.
2. When a face drifts, do NOT accept the board and do NOT patch it. Regenerate with an explicit LIKENESS CORRECTION block at the top of the brief that (a) names the drift in plain geometry — face width and jaw, nose size, cheek fullness, beard fullness and color, how strongly the signature features read; (b) attaches the rejected board as the prior-board reference for layout/wording/poses ONLY, with its faces marked DO NOT COPY; (c) requires the Front head shot to read as the same face as the portrait at a glance.
3. Describe the portrait's face in the brief from the portrait itself (measured/observed features), never from memory of the character.

## REFERENCE AUTHORITY — REAL PEOPLE (added 2026-11-20, from the Maria redo on Harlow's Helping Paws)
For a character based on a real person, the reference photos have a hierarchy: **candid everyday photos are the identity authority** — real hair as actually worn, the characteristic expression, signature makeup. Styled or studio shots are wardrobe and build reference ONLY; their styling (done-up hair, posed expression) is a trap that produces a polished stranger. The live lesson: a cast set briefed off studio photos "didn't really capture" the person; redone from candid selfies, the character landed immediately. When the two sets conflict on identity features, the candids win and the recipe says so explicitly.

## BANKING CHECK — VERIFY AN UPLOAD'S BYTES (added 2026-11-20)
A file that arrives by upload can carry crossed or wrong bytes (observed: an uploaded portrait whose file bytes were an old page screenshot). Before banking any uploaded image into cast, boards, or builds, verify it is the image it claims to be — view it, and when a known copy exists, pixel-diff against it (a same-image diff reads near zero; a wrong file reads an order of magnitude higher). Never bank on filename alone.

## CAST TIERS — BOARDS ARE FOR MAIN CHARACTERS ONLY (added 2026-11-20, kit v1.2.3 — Jon's scoping call on Harlow's Helping Paws)
Full character boards (the Harlow grid above) are heavy production; they are for **MAIN characters only**. The tiers:
- **Main characters:** recipe + portrait + full body + full board.
- **Supporting characters** (the animals especially): a dialed-in recipe + a headshot + a full-body image each. That suffices — supporting cast needs identity consistency in scenes, not a 40-tile sheet.
- **Groups and families are ONE set, one entry:** a litter, a family, or a bonded group is produced as a single set under a single recipe — one group portrait + one group full body, one showcase card, one cast-census entry — not one set of pieces per member. (Worked examples: the Spice Girls litter set; the Newman Family set — three humans, one portrait, one full body.) A group member who later becomes a main character gets their own pieces then.
- Boards for real-people supporting characters (Maria, Jon on Book 2) were a fun extra, not the standard for the whole cast — don't let the extra become the expectation.

## PAIR DIFFERENTIATION — JUDGED AT READING SIZE (added 2026-11-20, kit v1.2.3)
Members of a cast pair never share a pose or angle: each gets a distinct composition and silhouette so they never read as recolors of each other. A marking split on paper is NOT enough — the first Pixie/Spike split (narrow vs wide blaze, cap vs saddle) failed at reading size: both puppies were tan-dominant faces in the same expression family, and the producer read them as one puppy turned around. Differentiate on the signals that survive at thumbnail size:
1. **Face value mass** — a dark mask vs an open light face (Spike v2's bandit mask vs Pixie's open tan face).
2. **Ear / marking color mass** — near-black ears vs mahogany-tan.
3. **Pose and expression family** — level chin + closed grin + sitting full body vs up-tilted pant + standing step.
Judge the pair check side by side AT READING SIZE on those three signals, never from the recipe text alone. (Origin: Yuki v1 + Raja v1 flagged as "exact copies just different colors"; Yuki was redone near-frontal + reclining.)

## THE FULL-BODY GATE (added 2026-11-20, kit v1.2.3 — the Mira lesson)
A full body is NOT locked until it passes all three checks, whole-frame, against its own portrait:
1. **Style verdict first** — the figure must sit in the portrait's painted hand (same planes, same shadow depth, same finish). A flatter, paler, or glossier figure fails even if the outfit is right.
2. **Measured proportions, stated as a number** — head-to-height units measured on the actual files, compared like-for-like with the portrait's build. The recipe carries the proportion as a NEVER line (e.g. head ≈ 1/7 of height, normal neck length and shoulder width).
3. **Build check** — never slimmed, never elongated versus the portrait. Anti-beautify applies to bodies, not just faces.
An eyeball "finish-match" is not a gate. A later localized-edit pass (brows, markings) verifies its own change map but does NOT re-certify the underlying figure — on the live project a warped full body (6.0 stretched head-units, long neck, narrow shoulders, wrong finish) survived three passes exactly that way, because every pass checked only its own change. When a figure fails the gate, the fix is **regeneration governed directly by the portrait** (portrait attached as face + style authority, the failed figure attached as pose reference only, marked DO NOT COPY for proportions and finish) — never a patch, never a face paste onto a wrong skeleton. First application of the gate as a standalone pass: the cast-wide audit (every adopted full body side-by-side against its portrait: style → proportions → identity/locks) — run it whenever a figure is questioned, and spot-run it before the end-of-cast hi-res batch.

## MARKINGS — TERMINAL SHAPES READ AS SYMBOLS (added 2026-11-20, kit v1.2.3 — the Spike blaze lesson)
A marking that ends in a defined shape — a patch, a block, a cap, a star — reads as an emblem or symbol, not as fur. Stripe and blaze ends **taper, split into hair-fine strands, and fade/feather out into the coat**; recipes state this explicitly in the NEVER CHANGE block (e.g. "tapers, splits into hair-fine strands, and fades into the dark fur — no terminal patch, block, or symbol"). A designed mark must also trace to the author's text or be flagged as a designer invention at presentation (see MASTER-PROCESS §10) — a forehead star the author never wrote survived two versions before anyone asked where it came from.

## CARRYING AN ADOPTED REFINEMENT ONTO THE BOARD (added 2026-11-20, kit v1.2.3 — the Mira brow carry-over)
When a trait refinement is adopted on a canonical pair (brows slimmed, a marking changed), it carries onto the character's board in the same adoption pass:
- **One tight crop per face** through the image lane, composited back under a feathered trait-neighborhood mask, with a per-face change map and a whole-board change map proving zero pixels changed outside the trait neighborhoods (+ any re-typeset text band). A single multi-face STRIP edit fails: the model redraws the whole strip at different dimensions and garbles panel text.
- **Faces too small to carry the trait** (turnaround and size-figure faces where the trait is a 2–4 px dash) are **reported, not forced** — stated plainly in the adoption record.
- **Printed text that quotes the trait is re-typeset in the board's own lettering in the same pass** ("full brows" → "slim, softly arched brows"). A stale printed trait line is a defect on the same footing as stale art.

## THE BACKGROUND / EXTRAS SHEET (added 2026-11-20, kit v1.2.4 — the Book 2 Background Cast)

Every book gets **one** background/extras sheet, designed once: a single group plate of unnamed extras (people + animals) in the book's locked finish, style-governed off an adopted group piece, homed alongside the cast but never counted as cast.

- **The exclusion firewall is the gate that matters.** Every figure is checked — whole-frame, plus native-res crops of anything close — against **every named cast signature**: no cast species, markings, outfits, or accessories may appear on an extra (Book 2's firewall: no seal-point Ragdoll, no tricolor beagle, no Saint Bernard, no orange tabby, no tiger/bunny/pony; no plum cardigan or bow brooch, no pink scrubs, no smartwatch…). No text or logos on extra clothing (name tags render blank — the garble rule).
- **Every figure carries an ID** in the sheet's recipe — `P` + number for people, `A` + number for animals (the reference-code system, REFERENCE-CODES.md) — with a one-line description and the measured palette. **Scene and spread briefs attach the sheet and cite figures by ID** when populating backgrounds, so every scene's crowd is the same crowd.
- **Extras are never** named, foregrounded, given a story beat or dialogue, promoted to characters, or given individual art. If an extra ever needs to become a character, that is a **new commission** under the normal cast rules — not a promotion. (The reverse also holds: a character the manuscript NAMES can never be demoted to the sheet — see the named-character census gate, MASTER-PROCESS §10.)
- **Homing:** the sheet's recipe lives with the character recipes; the plate homes as **ONE showcase card, place-style** (no full-body toggle — the extras are not characters; a wide sheet is **letterboxed on its own wash, never cropped**, so edge figures stay whole). It is **not a cast entry**: no census count, no dashboard character row (an adoption note only), no cast-flipbook page.
