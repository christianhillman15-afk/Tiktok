# Faceless AI Production System

> You're running the **faceless, pure-AI** variant of this playbook: no camera, no face — every video is generated. This doc is the production engine. It overrides the "show your face / raw founder-to-camera" guidance in docs 01, 02, and 08 — everything else (strategy, funnel, offers, hooks, scripts) stays exactly the same.

## The one tradeoff, and how we beat it

Faceless + fully-AI content converts a little **colder** on a trust purchase like websites, because there's no human to bond with. We counter it with three trust layers baked into every video:

1. **Real screen-recordings** of actual (blurred) or example websites — the "evidence" is real even if the voice isn't.
2. **One consistent, authoritative AI voice** across every video — the voice becomes your brand the way a face would.
3. **Hard numbers on screen** — "76% call within 24 hours," "$0 down," "live in 7 days," real before/after results.

Lean into the formats that don't need a face anyway: **teardowns, before/afters, "what it should cost," myth-busts.** These were already your highest-volume pillars.

---

## The three production lanes

Pick the lane per video. Most of your content is Lane A.

### Lane A — Screen-record teardown + AI voiceover  *(highest trust, cheapest)*
The core format. You record a screen (a real blurred site, an example site, or a site you mock up), and an AI voice narrates the teardown over it.
- **Visual:** screen-record on your phone/computer (free) — scroll the site, point out flaws with the cursor.
- **Voice:** one fixed AI voice (see below).
- **Assemble:** drop screen-record + VO into CapCut, add burned-in captions, export 9:16.
- **Use for:** Films 1, 2, 4, 5, 7 (teardowns, word-of-mouth, build-process, nephew site).

### Lane B — Animated explainer  *(fully AI, no screen needed)*
For education/price/myth-bust videos where there's nothing real to show. Uses the Higgsfield **`video-explainer`** workflow: one AI narrator over stylized 10-second animated blocks, one locked visual style.
- **Fully generated** — script in, finished short out.
- **Use for:** Films 6 ("what it should cost"), 8 (the offer), plus any "3 mistakes" style explainer.

### Lane C — AI image slides / carousel  *(cheapest, no video)*
AI-generated still graphics posted as a photo carousel or turned into a slideshow with VO. TikTok pushes photo posts too, and they're save-magnets.
- **Use for:** before/after reveals (Film 3), "$X vs $XXXX," stat cards, "5 signs your website is costing you jobs."
- *(The "$500 vs $5,000" graphic I generated for you is exactly this lane.)*

---

## Your AI toolchain (Higgsfield)

| Need | Tool | Notes |
|---|---|---|
| The narrator voice | `create_voice` (once) → reuse forever | Make ONE brand voice and use it on every video. Consistency = your "face." |
| Voiceover audio | `generate_audio` (text-to-speech with your voice) | Paste the VO script; export the track. |
| Slides / thumbnails / b-roll stills | `generate_image` (`nano_banana_pro` for text/graphics) | ~2 credits each at 1K. Great for before/after, stat cards, title frames. |
| Animated explainer shorts | `video-explainer` workflow | Fully AI narrated short; Lane B. |
| Short b-roll clips | `generate_video` | For motion backgrounds; heavier on credits. |
| Aspect / cleanup | `reframe` (to 9:16), `upscale_image` | Make anything vertical + crisp. |

**Fixed brand voice:** pick one confident, trustworthy, mid-pitch voice (auditioned via `list_voices`) OR clone one with `create_voice`. Use it on 100% of videos. Never switch — the voice is the brand anchor that replaces your face.

**Credit reality:** images ≈ 2 credits each; narrated video costs meaningfully more. Your current balance is near empty — **top up before batch-producing video.** Budget guidance: a week of 4 posts done mostly as Lane A (screen-record + one VO track + 1–2 images) is cheap; leaning on Lane B animated shorts every day is not.

---

## The repeatable weekly pipeline

1. **Script** — pull the VO text straight from `10-weekend-1-shoot-pack.md` (already written).
2. **Voice** — `generate_audio` each script with your one fixed brand voice → get 4 VO tracks.
3. **Visuals** —
   - Lane A: screen-record the site(s) on your phone.
   - Lane B: run the `video-explainer` workflow.
   - Lane C: `generate_image` the slides (prompts below).
4. **Assemble** — CapCut: visual + VO + **burned-in captions** (non-negotiable — retention + SEO). Export 9:16.
5. **Post** — schedule Tue/Wed/Thu/Sat per `03-content-calendar-30-days.md`. Say/show the trade + "website" for search.
6. **Route leads** — keyword comments → DM flow in `06-lead-funnel-and-dm-templates.md`.

Batch it: write all scripts Monday, generate all VO + images Tuesday, assemble + schedule Wednesday. A week of content in one sitting.

---

## Worked example — Film 3 fully AI, end to end

**"$500 Website vs $5,000 Website"** (Lane C + VO):
1. **Image** (done — 2 credits): the before/after split graphic. Use it as the whole video background or the cover.
2. **VO script** (paste into `generate_audio` with your brand voice):
   > "This is a five-hundred-dollar plumber website versus a five-thousand-dollar one. Same business. The cheap one has a tiny logo, no phone number up top, and a contact form nobody fills out — it exists, it doesn't work. The real one? Giant tap-to-call button, real reviews, book-online right there. Same plumber. Five times the calls. I build the one on the right for zero down — comment WEBSITE."
3. **Assemble:** graphic on screen, VO over it, a slow zoom, burned-in captions. 30 seconds. Done.
4. **Caption:** `$500 website vs $5,000 website — same plumber, 5x the calls 👀` + `#websitedesign #plumbertok #trades #smallbusinessmarketing`

---

## Ready-to-paste image prompts (Lane C)

Feed these to `generate_image` (`nano_banana_pro`, 9:16). Swap "plumber" for any trade.

- **Before/After split** *(generated):* "Vertical 9:16 split-screen, top caption '$500 WEBSITE vs $5,000 WEBSITE'. Left 'BEFORE' in red: dated ugly plumber site on a phone, tiny logo, no phone number, cluttered. Right 'AFTER' in green: clean modern plumber site, big TAP TO CALL button, 5-star reviews, crew photo, Book Online. High contrast, legible."
- **Teardown title card:** "Vertical 9:16 bold TikTok title card, dark background, big text '3 THINGS KILLING YOUR PLUMBING WEBSITE', small subtitle 'and how to fix them', red warning accent, high contrast, thumb-stopping."
- **The 9pm Google test:** "Vertical 9:16, a hand holding a phone at night showing a Google search for a plumber with NO results / a broken page, worried mood, bold caption 'THE 9PM GOOGLE TEST', cinematic, high contrast."
- **Nephew website:** "Vertical 9:16 meme-style graphic, caption 'THE NEPHEW WEBSITE 💀', a comically bad amateur plumber website on an old computer, one page, broken links, stock wrench photo, humorous, bold text."
- **Stat card:** "Vertical 9:16 bold stat card, huge text '76%', subtitle 'of people who search plumber near me call within 24 hours', clean modern design, orange and dark navy, legible."

---

## What this changes in the rest of the playbook

- **Docs 01 / 02 / 08 "show your face / raw founder-to-camera":** replaced by this doc. Your brand anchor is the **consistent AI voice + visual style**, not a face.
- **Doc 04 scripts & Doc 10 shoot pack:** the *scripts* are your VO scripts now; the "shot notes" become "screen-record / generate" notes. Everything else (hook, on-screen text, CTA, caption) is unchanged.
- **Everything else** — positioning, ICP, funnel, DM templates, offers, algorithm/SEO, tracking — is identical. Faceless-AI only changes *how the pixels get made*, not the strategy.

*Make one voice. Lock one style. Generate, don't film.*
