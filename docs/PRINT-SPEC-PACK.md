# PRINT SPEC PACK — Harlow's Accidental Journey
**Issued:** 2026-10-24 · **For:** Cursor (print-shop build, Vader) · **From:** Trinity
**Story source of truth:** Rev.17 storyline DOCX (Drive `1tAsDS-Mzb6HQ2AaZXKQa_hqRfwkFKYyW`, md5 `7342ca2af84de7bccf11564760837987` — verified on download 2026-10-24). Text in §4 is verbatim Rev.17 (wording + punctuation; multi-space runs in the DOCX are normalized to single spaces).

## ⚠ OPEN ITEMS — read before building
1. **S05 — RESOLVED (2026-10-24).** The S05 gold is **S05-Y** — Jon's own finished version of the in-pond scene (the differentiated ducklings, incl. the restored natural middle-duckling head), ruled 2026-10-24; it superseded S05-V, which Jon had crowned earlier the same day. S05-V, S05-W and S05-X were removed from Final Pass V6 and remain board records on Spread Options / Final Pass V2 only. **Build S05 from the delivered s05.png** in the Drive print-masters folder (**re-run from the S05-Y master on the evening of 2026-10-24**; see the folder MANIFEST for its notes).
2. **S24 — RESOLVED (2026-10-24).** The S24 gold is **S24-AM** — Jon's own revised fireside version (back-view frame derived from AD, carrying the cleaned lamp table), ruled 2026-10-24; it superseded S24-AD, which had taken the gold in the final rulings earlier the same day. S24-Q, S24-AG, S24-AH, S24-AD and S24-AN were removed from Final Pass V6 and remain board records on Spread Options / Final Pass V2 only. **Build S24 from the delivered s24.png** (**re-run from Jon's S24-AM master on the evening of 2026-10-24**; see the folder MANIFEST for its notes).
3. **Dedication wording — PLACEHOLDER.** The dedication is Lois's words; she has not supplied them yet. Set the placeholder line on the dedication page (p. 3, §2) exactly as marked; final wording comes from Lois via Jon.
4. **Page count — RESOLVED: 52** (Jon's ruling 2026-10-24 — the page-parity fix, §2). Request the cover template from Lulu only AFTER the interior PDF is uploaded and counted; Lulu returns the template with the true spine. The saved 0.25-in spine (19 × 10.25 in) belongs to *The Night I Met Santa* (34 pp) — it is **NOT** this book's spine.
5. **S19 — RESOLVED (2026-10-24).** The S19 gold is **S19-R**, Jon's corrected Photoshop version (his final hand adjustment to Harlow's coat on the Q frame, which was itself his coat softening on the S19-O frame). The polish run it grew out of (M → O → P → Q) is closed: M, O, P and Q are off Final Pass V6 and remain board records on Spread Options / Final Pass V2 only. **The s19.png in the Drive print-masters folder was re-run from the R master — build S19 from the delivered s19.png.** (Earlier updates on this item, same day: the polish pass posted as S19-O beside gold M, then a softened grade as S19-P; Jon settled it with Q, then corrected Q to R the same afternoon.)
6. **Rev.18 items are NOT in this build.** Set Rev.17 text exactly as written — including S18's word "shore" (the "boardwalk" change is a pending Rev.18 item) and S16's boy named "Jon" in the text (the character is JJ Boy; the Rev.17 wording stands).

## 1. BOOK SPEC
- Trim: **8.5 × 8.5 in** square. Bleed: **0.125 in** all sides.
- Page canvas: **2625 × 2625 px @ 300 dpi**. Spread canvas: **5250 × 2625 px**, fold at **x = 2625**.
- Full-bleed art on every spread page; front/back cover art is single-page 2625 × 2625.

## 2. INTERIOR STRUCTURE (mirrors *The Night I Met Santa*)
| Interior pages | Content |
|---|---|
| p. 1 | **Title page** — "Harlow's Accidental Journey" (title treatment per the locked title; no story text) |
| p. 2 | **Copyright page** |
| p. 3 | **Dedication page** — dedication line: **[DEDICATION — PLACEHOLDER: Lois's wording to come]** |
| pp. 4–51 | The 24 spreads as FACING OPENINGS, 2 pages each: S01 = pp. 4–5, S02 = pp. 6–7, … S24 = pp. 50–51 (each spread's pages are also given in its §4 header) |
| p. 52 | **Closing page** — content TBD (an author note for Lois is the standing suggestion; Jon/Lois call) |

**Page-count math:** 1 (title) + 1 (copyright) + 1 (dedication) + 24 spreads × 2 pages + 1 (closing) = **52 interior pages** (Open Item 4, resolved).
**⚠ PARITY CORRECTION (2026-10-24, Jon's ruling — supersedes the original 50-page map):** in a bound book the facing pairs are (2,3), (4,5), (6,7)… — a spread split across pp. 3–4 sits on two sides of one sheet and never appears as an opening. The original map came from 2 + 48 arithmetic without the parity check (Cursor caught it; Trinity verified). Under this structure every spread starts on an EVEN page and reads as one opening.

## 2B. PRODUCTION METHOD — THE SANTA PATTERN (adopted 2026-10-24, from *The Night I Met Santa*'s locked runbook)
- **Photoshop is the design desk, not the print file.** Duplicate the blank spread template (5250 × 2625; page 2625 × 2625; cover 2625 × 2625 — blanks in `Xtraz\Adobe-Photoshop\`; guides: cyan = trim, magenta = 0.5-in safety, orange = fold; hide guides before export). Paint the art; story type sits as layers named `type/body-01`, etc. **Never place a Photoshop file into InDesign.**
- **Type handoff = `type-inventory.json`** exported from the Photoshop layers: exact words, font, size, leading, and the box in pixels. InDesign builds one LIVE frame per inventory entry; a faded copy of the Photoshop type sits underneath at ~35% until the live type matches, then is hidden. (On Santa, matching type by eye was the biggest time sink — the inventory is the fix.)
- **InDesign: FACING PAGES ON.** Place ONE 17.5 × 8.75 in image across the whole opening, center on the fold. **Never place left/right halves separately with full bleed on each half — that overlaps the gutter by 0.25 in** (the Harlow TEST doc used halves as a mechanics proof only; it is NOT the build method). The print file is 17.5 in wide vs the 17.25-in bleed box — with whole-image placement the extra 0.125 in per side is the outer bleed, exactly as designed.
- **Plates: plain RGB, NO alpha channel.** A fully opaque PNG that still carries an alpha channel makes InDesign flatten the PDF into ~117-dpi tiles (Santa's trap). **Trinity checked 2026-10-24: all 26 Harlow print masters are plain RGB with no alpha — clean, nothing to resave.**
- **Live type:** Rev.17 verbatim, Andika 17 pt / 1.3 — the way Santa set Cormorant. Do not bake story text into art. Typographer's quotes OFF before setting (verbatim apostrophes).
- **Lulu exports (both PDFs):** sRGB, single pages, **no crop marks**, fonts embedded; interior page size 8.75 in, TrimBox 8.5 in; presets `Lulu-Interior-Print-PDF.joboptions` / `Lulu-Cover-Print-PDF.joboptions`. **Upload the interior FIRST** — Lulu counts it and returns the cover template with the real spine; the cover waits for that template. Lulu adds white endsheets itself (not pages in the PDF). Books under 60 pages get no extra gutter. Text stays 0.5 in inside trim. Cover PDF must be FORCED to RGB (cover type with a drop shadow + "color unchanged" flattened Santa's to CMYK). Measure a small cover element's dpi from its own frame, not the whole wrap.
- **Photoshop control on Vader = the UXP bridge** (Photoshop open + Creative Cloud signed in + Jon reloads Adobe Python Bridge in UXP Developer Tools; broker port 8766). The standard Windows connection fails. The currently loaded plugin can see Photoshop but cannot open documents — Santa's bridge is the one that edited files; the Photoshop step waits for a doc-capable bridge.
- **Type-handoff gotchas (vault, 2026-08-22):** Photoshop alignment value 2 = roman baseline, NOT centered — centering comes from paragraph justification. Apostrophes are stored escaped in the export — clean them or InDesign prints `didn\'t`. An overflowing frame grows in HEIGHT only. On a facing spread the page bounds run ~17 in wide — a frame that grows sideways runs onto the other page.
- The July 15 vault path (Pillow → Typst → Lulu) is STALE — superseded by this pattern. (Its sRGB / 2625 / 5250 facts stand.)

## 3. ART
- **Print art = Trinity's Topaz upscales, delivered via Drive folder: "Harlow Print Masters — V6 Golds (5250)" — https://drive.google.com/drive/folders/1zWydBlPfavGrrhad2-ysHOcmHLIeDjBz.** Spreads at 5250 × 2625; covers (FRONT E, BACK C) at 2625 × 2625.
- Upscales are run off the **banked 1774 × 887 masters** in Trinity's art kits (×2.96) — **NEVER off the repo JPGs.** The repo files are review-board encodes; 7 golds sit in the repo at 1400 × 700 and would force a ×3.75 upscale. Full audit: `~/workspace/harlow-art-kit/gold-res-audit-2026-10-24/REPORT.md` (Trinity's side).
- **Do not upscale locally.** Do not substitute repo JPGs for a missing upscale — flag it to Jon instead.
- **Bake-off confirmed 2026-10-24 (S01):** Topaz HF V2 stands as the lane; ×4 twins NOT banked (Jon's lock); Clarity/AuraSR/Standard rejected — see Playbook §19.
- **The 24 V6 golds (final, 2026-10-24):** S01-AY · S02-AF · S03-T · S04-M · S05-Y · S06-AB · S07-AQ · S08-AG · S09-AO · S10-T · S11-L · S12-AK · S13-Q · S14-M · S15-X · S16-O · S17-U · S18-V · S19-R · S20-J · S21-X · S22-AQ · S23-AJ · S24-AM. **All 24 settled — no art holds remain.** The only open items left are the dedication wording (Item 3) and Jon's go (the page count is settled at 52 — Item 4).
- **S01 gold update (2026-10-24):** Jon's AY Photoshop touchup replaced AX as the S01 gold the same day AX was crowned; s01.png in the Drive folder was re-run from the AY master (see the folder MANIFEST). AX remains a board record on Spread Options / Final Pass V2 only — it is NOT the S01 build art.
- **S19 gold update (2026-10-24):** Jon's Q Photoshop version replaced M as the S19 gold; s19.png in the Drive folder was re-run from the Q master (see the folder MANIFEST). M, O and P remain board records on Spread Options / Final Pass V2 only — they are NOT the S19 build art.
- **S19 correction (2026-10-24, same afternoon):** Jon corrected his own Q — **S19-R** (his final coat adjustment on the Q frame) is the S19 gold; s19.png in the Drive folder was re-run from the R master (see the folder MANIFEST). Q joins M, O and P as board records on Spread Options / Final Pass V2 only — Q is NOT the S19 build art; R is.
- **Final gold rulings (2026-10-24, late afternoon):** **S05-V** took the S05 gold from S05-S, **S09-AO** took the S09 gold from S09-AQ, and **S24-AD** took the S24 gold from S24-Q (S24-AG and S24-AH also came off V6). s05.png and s24.png were built new and s09.png was re-run from the AO master — all three are delivered in the Drive folder (see the folder MANIFEST). S05-S, S09-AQ, S24-Q, S24-AG and S24-AH are board records on Spread Options / Final Pass V2 only — they are NOT build art. Notes on the new runs: S05-V's master is Jon's Photoshop file at 1773 × 887 (the fal output's 1-px rounding was corrected deterministically to exactly 5250 × 2625 — MANIFEST has the detail); S24-AD's banked master is a 1400 × 700 PNG — its creation resolution from the 2026-10-23 room-variation pass — and was upscaled ×3.75 from that banked kit PNG (never from a repo JPG).
- **Gold changes after the final rulings (2026-10-24, evening):** Jon replaced two golds with his own finished versions — **S05-Y** (over S05-V) and **S24-AM** (over S24-AD). **s05.png and s24.png were both re-run from Jon's banked masters the same evening and are delivered in the Drive folder (see the folder MANIFEST).** S05-V, S05-W, S05-X, S24-AD and S24-AN are board records on Spread Options / Final Pass V2 only — they are NOT build art.
- **Covers:** FRONT E (front), BACK C (back). Master resolutions: FRONT E is 1400 × 1400 native (Jon's Photoshop master — that is the most that exists); BACK C's true master is 1254 × 1254 (the repo's 1400 × 1400 is an upscale encode — Trinity's print upscale is figured from the 1254 master, ×2.09).
- Audited masters for the 7 flagged spreads (all 1774 × 887 PNG, in Trinity's kits): S04-M `6c8422c1…`, S11-L `1833048a…`, S14-M `6cc1dd7c…`, S17-U `dee0de84…` (Jon's Photoshop), S20-J `24d07db3…`, S22-AQ `89194508…`, S24-Q `40e581c0…`. The other 17 golds' repo JPGs are already 1774 × 887 encodes of banked masters.

## 4. TEXT
**Global rules — every spread:**
- Typeface: **Andika, 17 pt, 1.3 leading.** Rev.17 story text contains **no italic runs** (verified against the DOCX) — set regular throughout; if a future rev adds italics, use true italics, never faux/oblique.
- Text lives **only** inside the Lulu safe rects (percent of the 5250 × 2625 spread): **left page x 3.6% → 46.4%, right page x 53.5% → 96.3%, both y 7.4% → 92.5%.**
- **Fold rule:** no main character's face center (Harlow or Lois) inside **x 44–56%**; text never crosses the fold. Where a spread's text splits across pages, split **at a sentence boundary** — the split point is marked in each entry (L = left page block, R = right page block).
- Default text band: top of the spread, to **y32%**, unless the entry says otherwise (S01 and S23 left zone: to **y40%**; S15: to **~y36%** on Harlow's page).
- **Show-text proof rule:** a spread's text fit is proven ONLY by a rendered proof with the text visible (Show-text toggle capture) — per spread, no exceptions. An art-only proof proves nothing about fit.

### S01 — Harlow at Home · interior pp. 4–5 · BOTH pages — split 4 lines L / 2 lines R (lock); left text zone extends to y40%
**L:**
> Hey there! I'm Harlow, a laid-back Ragdoll cat living the good life in sunny Long Beach, California with my best human friend, Lois. My favorite pastimes boil down to eating, sleeping, and eating some more. I want to share a wild, unexpected journey I had recently — not a story about cat curiosity, but one about the kindness and generosity of strangers.
**R:**
> I think you're going to love it.

### S02 — The Silver Blue Mustang · interior pp. 6–7 · LEFT page only
> A few days ago, Lois asked, “Hey Harlow, how would you like to drive out to Farrelli Farms for some fresh fruits and veggies and enjoy the country scenery?” That sounded awesome to me, so we hopped into her classic ’65 Mustang for a nice day trip to the country.

### S03 — The Farmers Market · interior pp. 8–9 · RIGHT page only (lock)
> “Ah, we finally made it,” I sighed, taking in the rolling green fields as we pulled into Farrelli Farms. Lois was practically shaking with excitement, her eyes locked on a vibrant display of heirloom tomatoes and fresh berries. Seeing her completely mesmerized and in her element, I smiled and decided to wander off to stretch my legs.

### S04 — Sweet Pea's Muddy Puddle · interior pp. 10–11 · BOTH pages
**L:**
> “Phew, it's toasty today!” grunted Sweet Pea the pig, splashing in a big muddy puddle. “Come on in! The mud is where it's at to beat the heat.” I crept to the edge, then jumped back, wrinkling my nose. “I appreciate the tip, but have you seen my coat? This fur does not do mud.”
**R:**
> “Are you sure? It feels amazing!” Sweet Pea snorted, wiggling happily. “I'll find another way to cool off,” I said. “Lovely meeting you — catch you later!”

### S05 — Mama Fiona's Pond · interior pp. 12–13 · BOTH pages · art settled — S05-Y (Open Item 1, resolved 2026-10-24) · keep the top area clear for text
**L:**
> I soon spotted a pond, where Mama Fiona and her ducklings — Missi, Sammi, and Lili — swam over to greet me. “Oh honey, you look miserable!” Fiona said, seeing how hot and dusty I was from riding in the convertible. “Come take a dip — you'll feel so refreshed!” Normally a cat avoids water at all costs, but desperate times call for desperate measures.
**R:**
> I took a breath and hopped in — it felt amazing! I scrambled out, shook my fur dry, thanked Fiona and her girls, and set off again.

### S06 — Molly, Albie & Dallas · interior pp. 14–15 · BOTH pages
**L:**
> After a while, I realized I'd wandered far from Lois. Molly the donkey and her baby, Albie, trotted over, sensing I was lost. “Feeling turned around, little guy?” Molly chuckled. “Take a look at our big ears — let them remind you to listen to your surroundings in tight spots.”
**R:**
> I swiveled my ears like radar dishes and caught the sound of people talking. “That's brilliant! Thank you, Molly!” I called, nodding to her and Albie as I hurried toward the voices.

### S07 — Chester's Chuckle · interior pp. 16–17 · BOTH pages
**L:**
> As I zipped along, I heard giggling that was coming straight from Chester, a retired racehorse! “What's so funny?” I asked, baffled. “Well,” Chester chuckled, “I was a bit startled by you and started chuckling. You see, life on the racetrack could get pretty tough — but I always found something to laugh about to get me through.
**R:**
> Always keep your sense of humor, no matter what life hands you!” “I'll remember that!” I smiled, heading toward the voices with a grin on my face.

### S08 — The Red Farm Truck · interior pp. 18–19 · BOTH pages · text at the TOP of the scene
**L:**
> Hearing voices ahead, I got so excited that I stopped paying attention. I completely missed a bright red pickup truck being loaded with fruit and vegetable crates for a city delivery. In the rush, farm hands accidentally scooped me up and loaded me into the back.
**R:**
> Before I knew it, the engine roared to life, and we were speeding off toward the big city. Yikes!

### S09 — Lost in the City · interior pp. 20–21 · BOTH pages
**L:**
> With the truck flying down the highway, I hunkered down until we finally rolled into the bustling city hours later. The second the engine stopped, I bolted.
**R:**
> I was free—but looking up at the towering buildings in this unfamiliar city with roaring traffic, my stomach dropped. I was completely lost and had no idea how to get home.

### S10 — Philly's Pizza Lesson · interior pp. 22–23 · BOTH pages · split set by hand at the marked boundary
**L:**
> As I wandered the city sidewalks, my stomach started to rumble. I darted down an alley and spotted Philly the rat, eating a slice of pizza. As hunger beat out fear — I timidly asked for a bite, and Philly grinned, pushing the box over. “Sure thing! Help yourself, man.”
**R:**
> As we munched, he puffed out his chest. “I'm a big deal — I've been in the papers for my pizza heists.” “No way! You're a pro,” I said. “Would you please teach me your ways?” Philly's sly smile said yes — masterclass time.

### S11 — Penelope in Midtown Park · interior pp. 24–25 · BOTH pages
**L:**
> Stuffed and grateful for Philly's help, I wandered into Midtown Park to find a quiet spot and figure out a way back home to Long Beach. I spotted an elegant dog with her owner and piped up, “Hey there! I'm Harlow. Could you help me find my way back to Long Beach?”
**R:**
> Penelope the Afghan Hound snobbishly tossed her head and replied, “I'm much too busy to talk to you.”—though she wasn't doing anything at all. A nearby stray calico couldn't be bothered to help either.

### S12 — Otis the Coyote · interior pp. 26–27 · BOTH pages
**L:**
> My faith was taking a hit after Penelope. In a rougher part of town, I spotted Otis the coyote who was scruffy but friendly. “Hey there, my friend, can I help you out?” he asked.
**R:**
> I sighed with relief. “Yes, thank you! Do you know how to get to Long Beach?” Otis shook his head. “I wish I could help, but I've lived on these streets for so long I don't know anywhere else. Good luck — and never let your guard down around here.” I thanked him and headed off.

### S13 — Gideon Points the Way · interior pp. 28–29 · BOTH pages · split set by hand at the marked boundary
**L:**
> Feeling braver with Otis' tip, I started asking for help. Gideon the pigeon swooped down from a high ledge. “You look lost, buddy. Where are you headed?” he chirped.
**R:**
> “I'm trying to get back to Long Beach — can you help?” I asked. “It's a long shot, but the baseball park a few blocks over might have someone who can,” he said, pointing towards the ballpark. “That's the best I can do — I'm a city bird, and I never leave town. Best of luck!” Grateful, I set off at once.

### S14 — Chippy and the Popcorn · interior pp. 30–31 · BOTH pages
**L:**
> Finding the ballpark was a breeze, and I slipped in unnoticed. I heard frantic chittering over the crowd — a nervous squirrel was scrambling up a tall pole. “Hey, I'm Harlow!” I called. “What's the emergency?” “I'm Chippy, and I'm racing up this pole for peanuts!” he squeaked.
**R:**
> “Peanuts sound amazing! Teach me to pole-climb?” Chippy squinted down. “Sure — but you'd do better on the ground, where fans drop buttery popcorn everywhere.” The floor was a giant treasure hunt! “Fair point!” I thanked him and scampered off.

### S15 — The Hibernator · interior pp. 32–33 · BOTH pages · text band may extend to ~y36% on Harlow's page
**L:**
> I'd never seen a baseball game — guys in matching pajamas just tossed a ball around. Suddenly the ground shook. Boom, boom, boom! Out charged a colossal fuzzy bear-like character, waving giant paws. “HELLO EVERYBODY! I'm The Hibernator, your team mascot! Who's ready for fun?!” he roared.
**R:**
> “I AM!” I yelled, waving my paws. Even doubting I'd ever get back to Lois, I remembered Chester's golden rule: always keep a sense of humor, no matter what — even if life hands you a giant fuzzy bear!

### S16 — Edward's Big Hug · interior pp. 34–35 · BOTH pages · the text names the boy "Jon" — set verbatim (Open Item 6)
**L:**
> After the show, fear and loneliness crept back in. In the stands, a friendly face caught my eye. “Howdy,” he said. “I'm Edward the Emotional Support Dog, and this is my friend, Jon. You look a little down in the dumps.”
**R:**
> “I'm totally lost,” I confessed. “I'm so sorry,” Edward said. “With patience and persistence, you'll find help. Come give me a hug if you want.” I didn't hesitate — I gave Edward the biggest hug ever and instantly felt better.

### S17 — Jasmine at the Water Bowl · interior pp. 36–37 · BOTH pages · keep text room at the top
**L:**
> Feeling better but parched, I wandered to the snack shack, where workers left water bowls out for pets.
**R:**
> As I lapped it up, I heard buzzing overhead. “What's a cat like you doing at a ballpark?” asked Jasmine the bumblebee. “Trying to get back to Long Beach,” I answered. Jasmine lit up. “No way! I know Long Beach — just follow my buzz!” One last sip, and off we went.

### S18 — Babs the Crab · interior pp. 38–39 · BOTH pages · Rev.17 reads "shore" — set verbatim (Open Item 6)
**L:**
> Jasmine led me to the sand and buzzed off, leaving me gazing at the gorgeous ocean. A crab was walking sideways along the shore. “Are you alright?” I asked. “You're moving strangely.” “I'm fine — that's just how we roll. I'm Babs,” she shot back.
**R:**
> “I'm Harlow, trying to get back home,” I said. Babs sighed. “Sorry, I can't help — we crabs only walk sideways and can't see straight ahead. But here's a tip: always look in every direction before crossing streets.” I thanked her and continued on down the beach.

### S19 — Finnegan the Shark · interior pp. 40–41 · BOTH pages · art settled — S19-R (Open Item 5, resolved)
**L:**
> I'd never seen the ocean, so I crept to the water's edge. Suddenly a giant shark surged out! Finnegan the shark was just as spooked by me. Once we caught our breath, I shared my tale of woe.
**R:**
> “I wish I could help, but I can't leave the water,” Finnegan said. “Remember: the ocean is dangerous if you don't know it. If you don't know — don't go!” “Thanks, Finnegan, I'll remember that,” I said, heading back to dry land.

### S20 — Pebbles the Lost Penguin · interior pp. 42–43 · BOTH pages
**L:**
> As I was walking, I suddenly tripped over something round and lumpy — a penguin napping on the sunny beach! “SQUAWK!” Pebbles the penguin bolted upright, feathers ruffled. “Can't you see I was napping?!” “I'm so sorry!” I blurted.
**R:**
> “Aren't you a million miles from home?” Pebbles slumped. “Yeah. I took a wrong turn at a glacier, and now I'm totally lost.” “I'm in the same boat — though your trip home is longer than mine,” I sighed. “Good luck, buddy. I hope you find your way home soon!”

### S21 — Helga's Pouch Ride · interior pp. 44–45 · TWO text blocks (lock) — one block per page
**Block 1 (L):**
> Feeling a massive shadow sweep over me, I spotted a pelican circling down. “Hey little fella, you look exhausted and lost. Can I help?” she called. “Yes, please!” I squeaked. “I live in Long Beach, but I'm lost.” “Say no more!” she smiled.
**Block 2 (R):**
> “I'm Helga — I'll scoop you into my throat pouch, and you can watch for familiar places. I'll drop you at the start of your road. That's as close as I can get without leaving the ocean.” Breathing easier, I replied, “That's beyond perfect. I can't thank you enough!”

### S22 — Mittens and Teddy · interior pp. 46–47 · BOTH pages
**L:**
> Helga gently lowered me down and I started to recognize some familiar sites around me. But even better, I felt a strong sensation that I wasn't walking alone.
**R:**
> Could it be that Guardian Angels have been with me this whole time? I wondered, feeling a wave of peace. I nodded toward the sky in silent thanks to my invisible caretakers—and right on cue, my house finally came into view!

### S23 — Home Again · interior pp. 48–49 · BOTH pages · left text zone extends to y40% (lock, shared with S01)
**L:**
> There it was, right in plain sight—MY HOME! “Hooray! I'm finally home!” I shrieked, quivering with excitement.
**R:**
> Lois must have heard my paws on the porch, because she whipped the door open and scooped me up into the biggest, tightest hug. “Oh, my darling Harlow, where have you been?!” she gasped, eyes shining. “I was out of my mind with worry, but I'm so happy you're back. Come inside—I've got a delicious tuna dinner waiting for you!”

### S24 — Fireside with Little Mouse · interior pp. 50–51 · BOTH pages · art settled — S24-AM (Open Item 2, resolved 2026-10-24)
*Punctuation note: Rev.17 itself uses straight quotes/apostrophe on this page (unlike the rest of the book) — reproduced exactly as written; do not normalize.*
**L:**
> Settled warmly in front of my cozy fireplace, I looked back on everything that happened. I was completely blown away by how kind and helpful total strangers had been. Since I couldn't repay them, I decided to pay it forward at the very first chance I got.
**R:**
> Looking toward the corner near the fireplace, I spotted my first lucky recipient. "I see you over there, my little chum," I whispered with a smile. "How would you like some cheese?"

## 5. PRODUCTION RULES
1. **Build NEW.** The August InDesign file is a stub from old locks — not a source, do not build on it. Build the interior fresh in the print-shop folder **`D:\Hermes\projects\Harlows-Big-Adventure`**, reading print art from the Drive print-masters folder (§3) — not from the repo.
2. **Art handling:** place Trinity's delivered upscales as-is. No local upscaling, no recompression passes, no color "correction." If a file is missing or short of 5250 × 2625 (spreads) / 2625 × 2625 (covers), stop and flag it to Jon.
3. **S24-AM's finish is final art** — no polish or style passes on it. (Supersedes the earlier protection on S24-Q's painterly finish: Q was ruled out as gold on 2026-10-24; AM is the build art.)
4. **Edward's vest lettering ("Emotional Support Dog", S16-O) is APPROVED** — Jon ruled 2026-10-24; edward-recipe.md amended the same day. Do not flag or alter it.
5. **Text is set in layout, never in the art.** The art files carry no lettering; all type comes from §4.
6. **Proofs:** every spread gets a Show-text proof (text visible) checked against §4's side/split and the safe rects before the interior is called done. (The S05/S24 proof hold is lifted — Open Items 1–2 resolved 2026-10-24.)
7. **Cover template** is requested from Lulu only after the final interior page count is confirmed (Open Item 4). Do not reuse Santa's spine dimensions.

## Sources
- Final-pass briefs + text geometry: `files/FINAL-PASS-NOTES-2026-10-20.md` (incl. standing geometry: S01 split 4L/2R, S03 right-only, splits at sentence boundaries) + spread-plan layout locks (S01/S23 left zone to y40%, S21 two blocks, S03 right page).
- Art resolutions/masters: `~/workspace/harlow-art-kit/gold-res-audit-2026-10-24/REPORT.md`.
- Story text: Rev.17 DOCX, md5-verified (see header). Downloaded copy + extraction: `~/workspace/harlow-art-kit/print-spec-pack-2026-10-24/`.
