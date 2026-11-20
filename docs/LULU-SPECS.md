# Lulu Specs — verified on Books 1–2 (Nov 2026)

The print facts every book project in this system starts from. Verified against Lulu production files and the printed Book 1 hardcover.

## Interior
- **Trim:** Square 8.5 × 8.5 in (both books; confirm per book at project start)
- **Bleed:** 0.125 in on all sides
- **Safety:** 0.5 in — keep text and faces inside it
- **File margin lesson (from the printed Book 1 hardcover):** keep at least 3/8 in of file margin at the fore-edge; tight art reads cramped in print.
- **Color:** Premium Color
- **ISBN:** none (Books 1–2 pattern; revisit only if distribution changes)

## Cover — COVER-START RULE (locked)
Design on Lulu's real geometry from day one; never rescale art later.
- **Casewrap (hardcover):** face window 8.75 × 9 in + 0.625 in wrap; canvas 19 × 10.25 in at a 0.25 in spine. The spine is ESTIMATED at design time and stamped as an estimate on the file. When the real template returns, only the spine band moves (faces shift Δ/2); art is never rescaled or extended.
- **Paperback:** trim + 0.125 in bleed on all sides.
- **Finish:** Matte — locked for both formats. It does not change the cover PDFs and can change any time before ordering.

## The viewer's print guides (same numbers, on screen)
The flipbook's Page Settings draw from `PAGE_SPEC = { trimIn: 8.5, bleedIn: 0.125, safetyIn: 0.5, basis: "trim" }`:
- TRIM frame (red) at the page edge
- SAFE frame (purple dashed) at a 5.88% inset (0.5 / 8.5)
- The spread review pages draw the same frames, plus a seam guide (amber band 44–56% of spread width + dashed center line) that exists only in the review pages.

## Reference prices (Book 1, Nov 2026 — guide only, recheck per book)
- Hardcover $26.00 · Paperback $16.00 (Lulu list, Matte, Premium Color, no ISBN)
