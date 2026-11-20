# Publish Gate — four-part diff, one source of truth

Locked after the Book 1-era regressions (Oct 2026). Applies to every design publish in the system — pages, boards, covers, flipbook visuals.

## The rules
1. **One source of truth:** nothing ships unless it is in the design source (the artifact / design file) first. Any change ever made directly to a published file gets ported back into the source in the SAME round.
2. **Four-part pre-publish diff** of the new export against the currently LIVE build — any unexplained difference BLOCKS the push:
   - (a) **Palette tokens** — every color variable/value compared
   - (b) **Copy markers** — the strings that prove the intended copy is present and the old copy is gone
   - (c) **Image inventory** — hash every embedded image and compare the sets; add a warm/cool pixel signature when tone matters
   - (d) **File size** — a size jump is a finding, not a footnote
3. **Share assets ride along:** og-image + screenshots are re-captured from the new build and pushed in the same pass as any visual change — never left stale.

## Companion gates
- **Flipbook changes** additionally pass the port gate (RUNBOOK Step 3): AST/scope census + cold-boot behavior probes in Chromium and WebKit, before and after shipping.
- **Selective/masked image edits** additionally produce a change map: verify the target moved as intended AND the off-target is ~untouched. A target-only check is not verification.
