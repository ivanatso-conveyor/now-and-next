# Product Design Case Study — Structural Blueprint

> Paste this whole file into a new AI chat as context. It captures the structure, narrative arc, visual system, and voice rules used in the "Now & Next" Trust Center case study so another instance can scaffold a similar deck for a different project.

---

## 1. What this blueprint produces

A **single-file HTML case study** that:
- Reads as a 13-slide pitch deck a recruiter or design leader can scan in ~5 minutes.
- Is rendered as a long scrolling page with CSS scroll-snap, so each slide fills the viewport but the reader can scroll continuously.
- Supports accordions (`<details>` / `<summary>`) for "click in deeper" content without bloating the visible slide.
- Embeds all imagery as base64 inline so the file is portable as a single `.html`.
- Lives at portfolio scale (~2.5 MB single file is fine).

The deliverable is **content + structure**, not pixel-perfect Figma frames. The case study demonstrates *thinking*, not just craft.

---

## 2. Audience and tone rules

- **Audience:** product design leaders, hiring managers, recruiters at top-tier tech companies.
- **Voice:** confident but not arrogant. Strategic but grounded. Empathetic and learning-focused. Uses "we" more than "I" when describing team work; uses "I" when describing personal craft and decisions.
- **AI framing:** treat AI as a *design material*, not a buzzword. Show how AI changed the math (faster prototyping, cheaper alternatives, etc.) — don't lead with the AI angle.
- **Show the thinking:** lots of user-interview data, framing of tensions and tradeoffs. Pixels are evidence, not the point.
- **Avoid em-dashes (—).** Use a regular hyphen with spaces (` - `). The previous deck got flagged repeatedly for em-dashes that rendered as visible "M" shapes; they read as typos in browser. Hyphens with surrounding spaces look cleaner.
- **Avoid `&nbsp;`** in titles — non-breaking spaces render as visibly wider gaps. Use plain spaces and let lines break naturally.
- **Empathetic, learning-focused phrasing:** lead with the customer/user, not the designer. Say "What our customers taught us," not "What I learned." Say "as we gathered feedback," not "before we built anything."
- **No emojis** unless the user requests them.

---

## 3. The seven-act narrative arc

This is the spine. Adapt the slide count up or down by 1–2, but keep this arc:

1. **Hook (Cover)** — title, subtitle, meta (squad size, timeline, deliverable count).
2. **The Brief** — what we were asked to do, why it was a starting line not an answer.
3. **The Arc** — where this case study fits in a longer product journey. Helps recruiters scan in seconds whether the work is research, design, ship, or vision.
4. **Orient** — what were we actually testing? Surface the constraints (no staging environment, two prototypes in two days, etc.) and the artifacts.
5. **The Cast** — who we talked to. Show the human beings behind the data. 9–12 cards with role, company, lens, and a key quote.
6. **Decide** — the research findings, with quantitative evidence (a dot grid, a heatmap, a tier matrix). The slide with the most "thinking made visible."
7. **Findings & The Bet** — synthesize the decisions made from the research. 3–4 distinct findings, each with framing + evidence + tradeoff.
8. **Act** — the recommendation, tiered. Ship / Configure / Reconsider / Future.
9. **Live (the spec)** — what shipped. Trace each design decision back to a majority on a specific feature.
10. **Live (impact)** — real-world results: rollout numbers, customer engagement, zero objections, named customers.
11. **What's Next (vision)** — the larger swing. Sprint structure, north star, convergence priorities.
12. **The Prototype** — your personal contribution to the vision. Pillars + carousel of screenshots + live prototype link.
13. **Reflection** — 5–7 transferable lessons. The takeaways that travel to the next role.

---

## 4. Slide-by-slide template

Each slide follows this skeleton. Use it as a fill-in-the-blank.

```
SLIDE [N] · [SECTION NAME]
─────────────────────────
Theme:        [cover/sand/white/cream/mint/midnight/darker]
Eyebrow:      [section number · category] (small mono uppercase, green accent)
H2 hero:      [headline with one italicized emphasis word in <em>]
Lede (1–2 lines): [the one-sentence-then-one-more pattern, NEVER three paragraphs]
Body content: [tables, cards, lists, pull quotes — see component menu below]
Accordion:    [What we'd do differently / Deeper detail / Read more]
Continue arrow: "Continue ↓" at bottom, snaps to next slide
```

### Component menu (pick 2–3 per slide max)

- **Dot grid** — for showing N participants × M features with sentiment colors. Cells are E (Excited, green), N (Neutral, gray), M (Mixed E/N or N/S), S (Scared, red).
- **Heatmap table** — features in rows, participants in columns. Same color encoding as dot grid.
- **Aggregate distribution bars** — horizontal stacked bars showing per-feature E/N/M/S percentages, sorted by E descending.
- **Cast cards** (3-col grid) — 64×64 thumbnail · name initials · role · company · key quote · tag pill. Internal stakeholders get a different background tint.
- **Pull quote** — large italic serif, left-aligned, with a forest-green left border and an attribution line in mono uppercase.
- **Finding card** — numbered 01–04, with an eyebrow ("The Layout Finding"), an H3 with italicized emphasis, body text, and two side-by-side quote cells (one neutral, one dark-cell variant for contrast).
- **Tier list** — Ship / Configure / Reconsider / Future, each a horizontal pill with a tag, a title (feature names), and a count.
- **Stat block** — `.big-num` huge serif numeral + small body text underneath. Two-up grid usually.
- **Launch funnel** — vertical or horizontal step diagram with start step → branches → counts and percentages, ending in a takeaway line.
- **Customer strip** — horizontal pills with customer names, bookended by a `+N more` pill in the brand mint.
- **Sprint timeline** — 3-day cards in a row with arrows between them, each card showing a `sd-tag` mono label, an H3 title, and a body line.
- **Coco pillar cards** (3-col) — pillar number eyebrow, pillar name in italic serif, body description. Used for showing 3 thesis pillars of a vision prototype.
- **Vision carousel** — fixed-aspect-ratio frame with prev/next, dots, counter, and a "Try the live prototype" CTA. Each slide has a `data-cap` attribute and an image.
- **Reflection cards** (3-col grid) — numbered, small H4 title, 3-line body. 5–7 cards total.
- **Field notes panel** — a card in the cast grid for asterisked notes that didn't fit elsewhere.
- **Accordion** — `<details><summary>Read more…</summary>…</details>`. Use for context, deep dive matrices, what-we-cut, what-we'd-do-differently. Never hide the punchline in an accordion.

---

## 5. Visual system

### Color palette (CSS variables)

```css
--green-100: #D0EBDC;   /* mint accent (NOT used as slide bg in this deck) */
--green-200: #1DEAB4;   /* neon highlight, dark-bg only */
--green-400: #008661;   /* primary forest accent */
--green-700: #006B4A;   /* darker forest, used on light bg for accents */
--green-900: #002118;   /* darkest, dark-mode body */
--sand-100:  #F8F3ED;   /* warm beige bg */
--white:     #FFFFFF;
--ink:       #001510;   /* primary text on light */
--ink-2:     dark gray (body text)
--ink-3:     lighter gray (captions, eyebrows-on-light)
--hairline:  rgba(0,33,24,0.08)
```

### Slide background themes

- `.slide.cover` — dark (#001510 base + radial green gradients)
- `.slide.sand`, `.slide.cream` — warm beige (`--sand-100`), visually identical
- `.slide.white` — pure white
- `.slide.mint` — pale cool stone `#F5F8FB` (NOT the saturated `--green-100` — the saturated mint clashes with green accents and chart cells)
- `.slide.midnight`, `.slide.darker` — dark variants for moody/cinematic slides (only use 1 dark slide besides cover)

### Adjacency rule

**No two adjacent slides may share the same visible background.** `sand` and `cream` are the same color visually — treat them as one bucket for adjacency checks. Use the three light variants (white, sand-tone, mint stone) in alternating rhythm.

### Typography

- **Serif (Newsreader):** hero H2s and italic `<em>` emphasis only. Used for emotional weight.
- **Sans (display + body):** all H3s, body copy, lists, pull-quote text.
- **Mono:** eyebrows, slide numbers, author tags, captions, attributions, small labels. Always uppercase with 1.4–1.5px letter-spacing.

Three typefaces total. Resist adding a fourth.

### Light-theme override rule

Components originally styled for dark backgrounds (carousel internals, `.next-card`, accordion summaries, north-star cards) need explicit `[data-theme="light"]` overrides:
- `var(--green-200)` (neon teal) → `var(--green-700)` (forest)
- `color: white` → `var(--ink)`
- `rgba(255,255,255, 0.XX)` → `var(--ink-2)` or `var(--ink-3)`
- Bright green bg → soft mint card: `background: rgba(0, 134, 97, 0.08); border: 1px solid rgba(0, 134, 97, 0.22);`

---

## 6. Quantitative framing patterns

This deck leans heavily on numbers paired with quotes. Recipes that worked:

- **N voices × M features = K ratings.** "9 external participants × 15 features = 135 sentiment ratings." Use this as the hook in the Decide slide.
- **The one risky signal.** Find the single outlier (the one Scared rating) and name it explicitly. "1-in-135 risk" reads concretely.
- **Cherry-pick framing.** "Every participant cherry-picked across both prototypes" → ship a hybrid spec, each pick traceable to a majority.
- **Tier-counted alignment.** "7/7 align" / "Mixed signal" / "1 Scared rating" as tier-count microcopy.
- **Funnel with engagement %.** "3.2K saw → 503 engaged (16%) → 0 objections." A funnel reads better than a single big number.
- **Customer name strip.** Logos/names as pills. Anchors abstract numbers in real accounts.

---

## 7. Voice patterns and turns of phrase

These phrases landed well in the deck. Reuse the *pattern*, not the literal wording:

- *"X. But Y is not a brief. It's a starting line."* (Slide 2 framing)
- *"The decision wasn't to X — it was to Y."* (Slide 7 finding 4)
- *"Three findings. One bet."* (Decisive H2 numerology)
- *"Two truths, both right."* (When holding a tension)
- *"The bet shipped without surprise."* (Impact slide hero)
- *"What I'm taking forward."* (Reflection hero)
- *"From ambiguous to aligned."* (Mono eyebrow for impact stats)
- *"AI as interface, not feature."* (Vision principle)
- *"Constrained flexibility wins."* (Vision principle)
- *"Risk has a denominator."* (Reflection takeaway)
- *"Build the graph, not the deck."* (Reflection takeaway)

---

## 8. Interaction & UX rules

- **Scroll-snap navigation.** Each slide fills the viewport. Snap on `y mandatory`.
- **Accordion auto-collapse.** When the reader scrolls past a slide, any open accordions on it should smoothly close to preserve visual position on the next slide. Animate the collapse and compensate scrollTop with a cubic ease-out over ~380ms.
- **Click-to-zoom lightbox** for any thumbnail image.
- **Live prototype embeds.** Use a transparent iframe layered over a screenshot fallback (for hosts that block iframe embedding via X-Frame-Options). If the iframe loads, it covers the screenshot; if it's blocked, the screenshot reads.
- **Continue arrow** at the bottom of each slide with `data-next="sN"` to enable jump-scroll.

---

## 9. Constraints & guardrails

- **Length:** 13–18 slides max. Cut anything redundant.
- **Slide density:** never more than 2 visual components per slide (a chart + an accordion is fine; a chart + a chart + a quote + a card grid is too much).
- **One pull quote per slide** at most.
- **One italic emphasis per H2.** Don't double up on `<em>` in the same headline.
- **No back-to-back identical backgrounds.** See adjacency rule.
- **Accordions are for depth, not for hiding the lead.** The punchline lives in the visible body.

---

## 10. Process recipe (how to actually build it)

If you're scaffolding a new case study from scratch, follow this order:

1. **Outline the seven-act arc** in plain prose first. Don't think about visuals.
2. **Mine the research artifacts.** Quotes, ratings, FigJam syntheses, customer feedback themes. Pull the strongest single quote per participant. Anonymize to initials (e.g., `R.T. · Notion`).
3. **Build the data viz first.** The dot grid + heatmap + tiered scope are the deck's spine. If those don't read in 30 seconds, the slides built around them won't either.
4. **Draft each slide as Markdown** (use the slide template above). Get the words right before touching CSS.
5. **Apply visual system.** Theme each slide. Run the adjacency check.
6. **Add accordions last.** Anything that doesn't fit the body but you don't want to cut goes here.
7. **Final passes:** strip em-dashes; strip `&nbsp;` from titles; verify no white text remains on light slides; verify the lede counts (e.g., "Six lessons" matches 6 cards).
8. **Voice pass:** read every slide aloud. If a sentence sounds like a job description ("I led a cross-functional initiative…"), rewrite as "we" + concrete verb.

---

## 11. Anti-patterns to avoid

- ❌ Three-paragraph ledes that the eye glazes over. Use one sentence then a punch.
- ❌ Pure-italic body text. Italic = emphasis, not paragraph style.
- ❌ Anonymizing customers as "Customer A / B / C." Use initials + company.
- ❌ Pixel-perfect screenshots without context. Always pair a screenshot with the *decision* it represents.
- ❌ "I" everywhere. The work is a squad's work; the framing is yours. Use "we" for the work, "I" for the judgment calls.
- ❌ Dark theme everywhere. One dark slide (cover) + one optional dark moment (vision sprint) is the maximum.
- ❌ Em-dashes (—). Always use ` - ` instead.
- ❌ Lavish adjectives. "Massive impact," "industry-leading," "best-in-class." Cut.

---

## 12. How to feed this to a fresh chat

When starting a new case study with a different AI session, paste this entire blueprint plus a project brief like:

```
I'm building a portfolio case study. Use the attached blueprint to scaffold it.

Project: [your project name + 2-sentence summary]
Role: [your title + your specific contribution]
Audience: [who the case study is for]
Tools used: [Figma, FigJam, Lovable, etc.]
Research artifacts: [interview transcripts, surveys, analytics]
Key participants: [list of N participants with initials, role, company]
Headline numbers: [N interviews, K ratings, M features tested]
The bet that shipped: [what you ended up recommending]
The north-star vision: [the larger swing, if any]
The reflections: [3–6 transferable lessons]

Generate a 13-slide HTML case study following the blueprint exactly.
Output as a single self-contained file. Use placeholder text where I haven't
filled in details so I can fill them in afterward.
```

The blueprint above carries the structural DNA. The brief above carries your specific project. Together they should produce a case study with the same narrative shape, voice, and visual system as Now & Next.
