# Physical Mockup — the bound-book viewer spec

A flipbook variant that mimics holding the REAL bound book, so the physical reading experience — what faces what, where the turns fall — can be proofed before (and alongside) a printed proof. Built for Book 1 from the BEST-24 page set (Nov 2026); the pattern is book-agnostic.

## Leaf order (the whole point)
1. Front cover (single)
2. **Plain WHITE inside-front-cover leaf** — a viewer-only asset generated flat white at page dimensions. It is the back of the front cover. It exists ONLY in this mockup, never in any print file.
3. The front bookend/wash page
4. The interior pages in print order, paired as printed — every designed spread appears as ONE opening; no designed spread may straddle a page turn
5. The back bookend/wash page (left page of the final opening)
6. **Plain WHITE inside-back-cover leaf** (right page of the final opening, facing the wash)
7. Back cover (single)

For a 56-page interior this yields exactly 60 leaves. Page turns are single at the two ends (cover, flyleaves, bookends) and facing spreads through the body.

## Source discipline
- Pages come from the book's CURRENT final page set (the same images as the print build). If that set isn't built yet, STOP — never substitute an older revision's pages.
- The viewer is rebuilt from the page folder, so swapping in a newer page set is a re-run, not a rebuild.

## Verify + report
- Leaf count matches the formula (interior pages + 4) and the order above
- Spot renders: leaf 2 pure white; leaf 3 the wash/bookend; first opening pairs as printed; any grid/cast page appears as ONE opening; final opening is wash (left) + white (right)
- Turn behavior checked at the ends and mid-body
