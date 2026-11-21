# Page Polish — share, cache, and screenshot discipline for project pages

Harvested from Jon's wider site work (The Starting Blocks, Yolando's sites, the Hub) and applied to every book-project page — showcase, spread review, and any page that gets shared by link.

## Link previews must stay lean
- A page that will be shared (iMessage, Facebook, chat) keeps its HTML small with **images as separate files**. A single-file page with embedded images can pass 13 MB and link previews silently fail — no thumbnail, no card. (Learned on The Starting Blocks: splitting images took the page to 145 KB with byte-identical visuals.)
- og-image: 1200 × 630, and its URL is **versioned** (`?v=` stamp) so crawlers refetch instead of serving a cached card. Facebook caches aggressively — force a re-scrape via their debugger when a preview goes stale instead of changing the page again.
- Fold page weight + image splitting into the pre-publish check for every page.

## Cache-busting
- After any push, browsers and crawlers may serve stale assets. The standard fix: stamp `?v=YYYYMMDDHHMM` on the page's CSS/JS/image URLs inside the HTML before pushing, and hand out preview links with a fresh `?v=N` **only after** live byte-verification passes.
- GitHub's README image cache ignores same-path updates: after refreshing any repo image, bump the `?v=` stamp on its README URL.

## Screenshots stay current
- Whenever a build's visuals change, retake the screenshots in the same pass: README hero (dark mode), gallery views, og-image, and the repo social preview source. No stale screenshots, ever.
- Chat previews of images: downscaled JPEG (~1600 px, q88) with a FRESH filename — same-name re-sends render cached on iOS, and previews must preserve aspect (resize by width only).

## Publish verification
- Byte-verify live files against local after every push (md5). A Pages build can lag or stall behind rapid pushes — if verification fails 5+ minutes after a merge, push a nudge commit rather than polling.

## Showcase presentation (added 2026-11-20, kit v1.2.3 — the Book 2 showcase rules)
- **Cast cards lead with the portrait.** Every cast card (lead and supporting) shows the portrait first and carries a per-card **"Show full body" toggle** that reveals the full body below it, hidden by default — the full cast reads at one weight, and full bodies are one tap away, not absent. (Supersedes an earlier portrait-only round: full bodies live on the showcase behind the toggle, and in the cast files and cast book regardless.)
- **Place cards:** adopted environment plates get cards in the cast grid, after the cast (same card pattern — image, name, blurb — but **no full-body toggle**; they are places, not characters). Web media lives under `media/scenes/`, **square-cropped on each scene's signature elements** — choose the crop window per scene so the defining features survive (the Fireside plate's crop is taken from the side that keeps the lit fireplace, sofa, and rug); never blind-center-crop a wide plate.
- **Link rule: same-site = same tab, external = new tab.** Navigation among the project's own pages (showcase, bookshelf, spread review, dashboard) stays in the same tab; only genuinely external destinations (Drive, GitHub, Lulu, other sites) open new tabs. Probe invariant: the flipbook's static-anchor `target="_blank"` count is 0 (JS-set links to external stores are the sanctioned exception).
- **Menu:** the shared ☰ drawer's entry for the page you're on is marked in **gold** — gold = current page, on every surface.
- **Manuscript button:** the showcase footer carries a button — "Read the current manuscript — <Draft N>" — pointing at the author's current draft in Drive (external, so it opens a new tab). The label carries the draft version on purpose. **When a new draft is banked, re-point this button (target + version label) AND the dashboard's manuscript link in the same pass — never one without the other.**
