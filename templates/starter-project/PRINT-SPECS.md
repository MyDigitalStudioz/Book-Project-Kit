# Print Specs — the locked Lulu numbers for this book

Carried in every starter project so the numbers are never re-derived. Full detail: the kit's `docs/LULU-SPECS.md` + `docs/PRINT-SPEC-PACK.md` + `docs/COVER-START-SPEC.md`.

## Interior
- Trim: **Square 8.5 × 8.5 in** · Premium Color · paperback + hardcover
- Bleed: **0.125 in** all sides → spread master **17.5 × 8.75 in @ 300 dpi = 5250 × 2625 px** (singles 2625 × 2625)
- Safety: keep text/faces **0.5 in** inside trim; fore-edge margin **≥ 3/8 in** in the file (Book 1 proof lesson)
- Flipbook/review guides use the same numbers: TRIM at the page edge, SAFE dashed at **5.88% inset**

## Covers (design on this geometry from day one — spine estimated, stamped as such)
- Hardcover casewrap: face window **8.75 × 9 in**, **0.625 in** wrap, canvas **19 × 10.25 in** at spine 0.25 in
- Paperback: trim + 0.125 in bleed
- When the real Lulu template returns, only the spine band moves (faces shift Δ/2) — art is never rescaled or extended
- Finish: **Matte — LOCKED** for both formats

## Book 1 reference points (Harlow's Accidental Journey, published)
- Hardcover $26.00 (print cost $22.58) · Paperback $16.00 (print cost $13.76) · no ISBN · © author
- Hi-res masters: AI upscale only (fal Topaz High Fidelity V2, face enhancement OFF) — never a plain stretch; every master set ships an md5 MANIFEST (see `docs/HIRES-PIPELINE.md`)
