# COVER-START SPEC — design on real Lulu geometry from day one
**Locked 2026-11-04 (Jon's call, after the Harlow HC template rounds). Standing for every future book (Harlow SC included, and future BookVizion titles at this trim).**

## Why this exists
The Harlow covers started on a trim+bleed canvas (5250×2625) because a cover was needed before any Lulu project existed. Lulu's real hardcover template is 19 × 10.25 in — the difference forced a rescue round (extension rejected, design PSD, Jon recomposing). The geometry that caused it is FIXED for casewrap at a given trim; only the spine width varies. So: start on the real geometry with an estimated spine; when the template returns, only the spine band can move.

## Hardcover (case wrap) — 8.5 × 8.5 trim, VERIFIED from the rmq8eyw template (2026-11-04)
- Per-face window (the board): **8.75 wide × 9.0 tall** — bigger than the 8.5 × 8.5 page.
- Wrap (turn-in): **0.625 in** past every board edge.
- Canvas: W = 2 × (0.625 + 8.75) + spine · H = 0.625 + 9.0 + 0.625 = **10.25 in**. At spine 0.25: **19 × 10.25 in = 5700 × 3075 px @300dpi**.
- Guides (inches from top-left, spine 0.25, verified): V 0 · 0.625 · 1.25 · 5.125 · 8.75 · 9.375 · 9.625 · 10.25 · 17.75 · 18.375 · 19 — H 0 · 0.625 · 1.25 · 7.745 · 9.0 · 9.625 · 10.25. Barcode print area 3.622 × 1.26 in (keep empty of important art; family runs carry no barcode).
- Safety: 0.625 in inside each face window — logo, text, faces, and anything that matters stay inside it.

## Softcover (paperback, perfect bound) — 8.5 × 8.5 trim
- No boards, no wrap. Canvas: W = 0.125 bleed + 8.5 + spine + 8.5 + 0.125 bleed · H = 8.5 + 2 × 0.125 = **8.75 in**. At spine 0.25: 17.5 × 8.75 in = 5250 × 2625 px @300dpi.
- Safety: 0.5 in inside each face's trim lines. Barcode keep-clear box on the back face is a CONVENTION in the starter PSD until a returned SC template verifies it.

## Spine width — the only true unknown
- Set by Lulu from page count + paper AFTER the interior uploads. Verified data points we own: **54 pp Premium Color → 0.25 in** (Harlow HC); Santa SC 34 pp → 0.137 in.
- At design start, estimate from Lulu's page-count/paper guidance and stamp the starter file "ESTIMATE — spine <X> in placeholder." The returned template is the truth.

## Composition rules (both formats)
- Design each face as its FULL zone (window + wrap on HC; trim + bleed on SC) — real painting fills the zone; principals inside safety; no edge-stretching, no smearing, ever (locked 2026-11-04).
- Logo = baked graphic (canonical PNG only). ALL other cover text (bylines, edition lines, spine title) = LIVE TYPE at the PDF build, never baked into the plate.
- Spine: deep-blue gradient + white Andika 9/18 title, bottom-to-top (Harlow lock; other titles follow their own design).

## When the real template returns
1. Compare spine width to the estimate. If different: shift each face by Δ/2 — NEVER rescale art.
2. Re-verify the guide set against the returned template file before building any PDF.
3. Nothing else moves. If turn-in/wrap bands would be bare, STOP and show Jon the placement (standing gate).

## Starter PSDs (Cursor-built, 2026-11-04 — filed with the Harlow Photoshop sources)
`Cover-Start-HARDCOVER-8.5x8.5.psd` (5700×3075, guides + zones + spine 0.25 centered) · `Cover-Start-SOFTCOVER-8.5x8.5.psd` (5250×2625 at est. spine 0.25). Both: TEMPLATE LINES + ZONES + LABELS locked layers, empty FRONT/BACK/SPINE art layers, RGB @300dpi. Other trim sizes need their own geometry — recompute from the formulas above.
