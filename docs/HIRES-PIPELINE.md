# Hi-Res Pipeline — print masters discipline

How print masters are made, moved, and verified. Proven on Book 1's Gold-24 set (Oct–Nov 2026).

## What a master is
- Spread masters for the square book: **PNG, 5250 × 2625 px** (17.5 × 8.75 in at 300 dpi — trim + bleed). Singles: 2625 × 2625.
- Masters are **print files**, not working files: once a master is verified, it is copied byte-exact and never re-encoded, resized, recompressed, or re-saved through an editor.

## How masters are made
- "Hi-res" means a real **AI upscale** — fal Topaz **High Fidelity V2, face enhancement OFF**, 4× (the Gold route) — or Gigapixel Pro. A Lanczos/plain resize of a render is a PREVIEW, never a deliverable.
- Generation renders land at working size; the upscale pass is a separate, deliberate step whose output is checked against the source for finish drift before it becomes a master.

## When masters are made — locked work only, one batch (Jon, 2026-11-20)
- **No hi-res masters for un-locked work.** Pieces still iterating — supporting-tier art, anything awaiting a formal lock or the author's review — stay at working resolution. Masters are for finals, not for review rounds that will change anyway; upscaling art that is still moving wastes credit and money. Review copies for the author are working-res by design.
- **The hi-res pass runs ONCE, as a single end-of-cast batch,** after all characters are caught up, adopted, and locked — not piecemeal per character as each one lands. A piece superseded after a master exists (a refinement adopted later) is re-run **in that batch, from the adopted art** — never as a one-off in between.

## The manifest rule (every master set ships one)
Each set carries a `MANIFEST.md`: file list, exact dimensions per file, and the **md5 of every file**. Any transfer (Drive → disk, disk → layout) verifies against it:
1. All files present
2. Every file measures exactly spec
3. Every md5 matches — name any mismatch; one re-download retry, then stop and report

## Storage
- The verified set lives in Drive **Cast Finals** (for cast art) or the project's print-masters folder (for spreads), and nowhere else as "the" set. Working copies are labeled as copies.
