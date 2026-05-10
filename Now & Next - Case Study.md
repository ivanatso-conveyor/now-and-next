# Now & Next: A Trust Center Built by Listening

**Ivana Tso · Senior Product Designer · Conveyor**
**Case Study · 13 slides · 9 interviews · 135 ratings**

Squad: PM · Designer · Eng
Tools: Figma, FigJam, Lovable, Claude Code
Timeline: Q1 2026 (6 weeks) → Q2 Vision Sprint (3 days)

---

## Slide 01 · Cover

# Now & Next
## *A Trust Center Built by Listening*

A research-led redesign of the Conveyor Trust Center — the touchless surface every B2B security review starts with. Nine voices. 135 sentiment ratings. One bet held in tension with a north star.

**Trust Center (definition):** Conveyor's customer-facing portal where Trust Center Visitors (the third-party risk managers reviewing a company's security posture) can self-serve documentation, get cited AI answers, and run questionnaires without ever emailing the security team.

**TPRM:** Third-Party Risk Management — the function inside customer organizations that audits the security of vendors they're considering or already using.

---

## Slide 02 · The Brief

# "Make the Trust Center better."

The Trust Center is where every B2B security review starts. It's the surface the third-party risk manager hits before they ever talk to our customer's security team. Get this right, and the rest of the review can be touchless.

But "better" is not a brief. It's a starting line.

What we had: a static document portal that customers were bypassing — emailing the security team instead of self-serving. What we needed: a research-led decision about what to ship now versus what to swing for later.

---

## Slide 03 · The Arc

# Where this case study *fits*.

A four-stage product arc — Brief → Research → Decide → Ship → Reflect — with a parallel vision sprint thread.

This case study covers two panels:
- **Panel 3 (now):** The interim ship — the bet we placed in market in Q1 2026 based on 9 customer voices and 135 sentiment ratings.
- **Panel 4 (next):** The north-star vision — a 3-day Q2 sprint where six designers built six prototypes in parallel.

The first two panels (the legacy Trust Center, the redesign brief) sit in the accordion as context but aren't the focus.

---

## Slide 04 · Orient · What are we testing?

# What are we *testing*?

As we gathered our feedback, two prototypes were built in parallel: **Card Layout** and **Open Layout**. Each tested 15 features the team had been debating. The prototypes weren't precious — they were probes.

**Built in:** Lovable AI prototyping. Two production-shaped prototypes in two days. That cost-of-testing collapse let us avoid a coin flip and instead test both directions side by side.

**Constraint:** No staging environment. Lovable carried us from idea → testable artifact in two days, where the engineering team needed weeks to spin up traditional staging.

**Prototype A — Card Layout:** Pinned announcements, compact header, segmented Your Documents card.
**Prototype B — Open Layout:** Wide layout, search-led top bar, surfaced product line selector.

---

## Slide 05 · The Cast

## Nine voices across three lenses: **Admins** who run the Trust Center, **Visitors** who review it, and **Internal stakeholders** who ship and sell against it.

### Participants

**Admins (TC Admins)**
- **J.N.** — Lead Analyst, Security Risk & Compliance · Cvent — *"Do it in a week, if you can, seriously. I would welcome that."*
- **N.E.** — Program Manager, Cybersecurity Compliance · Workday
- **P.L.** — Lead Customer Security Assurance Analyst · DocuSign — *(Re: Automatic Changelog) "I think [The Automatic Changelog] is probably going to create me more problems than anything else… scared."*
- **A.H.** — Manager of Customer Security · Symplr
- **R.T.** — Third-Party Risk Management · Notion — *"Where is this table of contents? What table of contents, no?… I did not see that at all."*
- **B.C.** — Director, Security GRC & AI Governance · [Undisclosed] — *"Where were you 10 years ago? — on ConveyorAI."*
- **R.B.** — Senior Program Manager, Cybersecurity (Colorblind) · Workday

**Internal (greys)**
- **D.B.** — Head of Sales · Conveyor — *"This is a step in the right direction. It does feel like a step versus tearing this thing down to the studs."*
- **M.A.** — VP of Marketing · Conveyor — *"I want it to look different. Distinctively visual where if I see a Conveyor trust center, I know it's a Conveyor trust center."*

### Field notes

- P.L. was interviewed in-person at DocuSign.
- R.B. is colorblind and surfaced accessibility issues with the new header.
- R.T. is the only participant with both Admin & Visitor experience — his feedback held both lenses at once.

---

## Slide 06 · Decide · What did the research say?

# What did the research say?

Across **9 external participants × 15 features**, we collected **135 sentiment ratings**. The pattern was clear before the analysis was finished.

### Overall sentiment by participant

| Participant | Tally |
|---|---|
| P1 | 11 Excited · 4 Neutral |
| P2 | 11 Excited · 2 Neutral · 2 Mixed |
| P3 | 7 Excited · 8 Neutral |
| P4 | 7 Excited · 7 Neutral · 1 Mixed |
| P5 | 6 Excited · 4 Neutral · 4 Mixed · 1 Scared |
| P6 | 5 Excited · 10 Neutral |
| P7 | 3 Excited · 12 Neutral |
| P8 (G.D. · Instructure) | 12 Excited · 3 Neutral |
| P9 (R.A. · PRGX) | 12 Excited · 3 Neutral |

**Aggregate:** 74 Excited · 53 Neutral · 7 Mixed · 1 Scared

### Per-feature distribution (n=9)

| Feature | Result |
|---|---|
| Global Search | 9E |
| Updated Header | 8E · 1N |
| Preview TC Updates | 8E · 1N |
| New Look / Layout | 7E · 2N |
| Auto Rollout New UI | 6E · 3N |
| Your Documents (relocated) | 5E · 1M · 3N |
| Product Line Selector | 5E · 1M · 3N |
| Pinned Announcements | 4E · 5N |
| New Company Links | 4E · 5N |
| Logo / Profile Image Removal | 4E · 4N · 1M |
| Onboarding Modal | 3E · 5N · 1M |
| Table of Contents | 3E · 1M · 5N |
| Rollback to Current Design | 3E · 2M · 4N |
| Changelog / Recently Updated | 3E · 5N · 1S *(only Scared)* |
| Doc Count + Updated Date | 2E · 7N |

> *"Even if Conveyor were to just roll them out tomorrow and not tell us, it'd be okay… it's definitely an improvement."* — P2, Trust Center Admin

---

## Slide 07 · Findings & Decisions

# Four findings. *One bet.*

When we synthesized 135 ratings across nine voices, four patterns emerged. Three pointed at what to ship — one pointed at what to let go.

### Finding 01 · The Layout Finding
**No one preferred all of *one* layout.**
Across nine external participants, every single one cherry-picked across the two prototypes. The shipping spec became a hybrid — each pick traceable to a specific majority.

*Accordion: Per-feature winning matrix (Card vs Open across 7 components).*

### Finding 02 · The AI Finding
**Same product. *Opposite reactions.***
When senior admins saw ConveyorAI, they braced. When visitors saw it, they exhaled. The design pattern wasn't whether the AI was good. It was making prominence a **dial**, not a default.

> Admin: *"Enterprise customers are very leery when they see the word AI. As soon as they see AI, they're going to go: well, what are you doing with my data?"* — J.N. · Lead Analyst, Cvent
> Visitor: *"Where were you 10 years ago?"* — B.C. · Director, Security GRC & AI Governance

### Finding 03 · The Timeline Finding
**Two truths, *both right*.**
Visitors wanted us to ship the small fixes now. Sales wanted us to swing for an AI-native rebuild. We chose to hold both — shipping the midway feature this quarter, sprinting the vision next. Neither voice got everything. Both got moved closer.

> Admin: *"Do it in a week, if you can, seriously. I would welcome that."* — J.N. · Cvent
> Sales: *"This is a step in the right direction. It does feel like a step versus tearing this thing down to the studs."* — D.B. · Head of Sales, Conveyor

*Accordion: How we held both voices in scope — two parallel tracks (immediate ship + Q2 vision sprint).*

### Finding 04 · The Deprioritization Finding
**The feature I was sure about *didn't matter*.**
I was sure customers would lean on a Table of Contents — long pages, dense docs, a lot to scan. Then we tested. Nine walkthroughs, zero unprompted mentions. Two of our most engaged participants had already built their own pattern: **Ctrl+F**. The rest didn't see it at all. The decision wasn't to redesign it — it was to deprioritize.

> Visitor: *"Where is this table of contents? What table of contents, no?… I did not see that at all."* — R.T. · TPRM, Notion
> Where the time went: Engineering capacity reinvested in an accessibility fix R.B. flagged on active-tab contrast — a separate issue surfaced by the same finding.

**The bet wasn't one decision. It was four of them — three held in tension, one deliberately let go — all shaped by the customers who told us where the tension lived in the first place.**

---

## Slide 08 · Act · The bet, and how to ship it.

# The bet, and how to ship it.

A defensible recommendation isn't "ship everything." I sorted the 15 changes into four tiers, then paired them with a rollout sequence customers told us they wanted.

| Tier | Features | Signal |
|---|---|---|
| **Ship** | Global Search · Updated Header · Pinned Announcements · Your Documents | 7/7 align |
| **Configure** | Onboarding Modal · Product Line Selector · Table of Contents | Mixed signal |
| **Reconsider** | Changelog (admin opt-in only, audit timing risk surfaced) | 1 Scared rating |
| **Future** | Mobile optimization · Layout style standardization | Out of scope |

---

## Slide 09 · Live · One direction, built from research.

# One direction, built from research.

The shipped spec is a hybrid — each pick traceable to a specific majority on a specific feature.

- Card layout for: Updated Header, Pinned Announcements, Your Documents
- Open layout for: Search bar + Product Line filter
- Preserved: Ctrl+F as the dominant scanning pattern
- Surfaced: an accessibility fix R.B. flagged on active-tab contrast

---

## Slide 10 · Live · In market

# The bet shipped without surprise.

The midway ship rolled out behind a feature flag with a 2-week preview window. Every Trust Center editor saw an in-app tour announcing the change. The numbers below are real, captured in production.

| | |
|---|---|
| **173** | active Trust Centers receiving the rollout |
| **0** | emails back with concerns from 3.2K editors who saw the announcement |

### Announcement tour — real-world engagement

| Step | Count | % |
|---|---|---|
| Editors started the tour | 3.2K | — |
| Clicked "Remind Me" | 296 | 9.3% |
| Previewed their Trust Center | 207 | 6.5% |
| Dismissed (acknowledged) | 2.3K | 72% |

**503 editors (16%)** engaged with preview or remind. The other 72% acknowledged and moved on. Zero objections in either group — and zero from the top strike-zone customers we proactively checked in with before launch.

**Powering trust for customers including:** Cvent · Workday · DocuSign · Symplr · Notion · Atlassian · Alteryx · Arctic Wolf · PRGX · +164 more

*Accordion: Read more about the rollout mechanics — advance notice, preview window, Remind Me, no opt-out, feature flag.*

---

## Slide 11 · What's Next · Vision Sprint

# Three days that pointed at *2027*.

The interim move shipped. The next loop turned the north star into a focused Q2 bet — six people, six prototypes built in parallel, three days of structured convergence.

### From ambiguous to aligned
- **100% of external participants comfortable with a near-term rollout.** Not a single objection raised about the rollout itself.
- **6 weeks** from a vague brief to a tiered shipping recommendation, a rollout plan, and a research artifact teams kept revisiting.
- 135 sentiment ratings turned into one defensible decision matrix.
- Per-feature heatmap surfaced the one risky change (Changelog) before it shipped.
- Sales lead and Marketing lead reached consensus despite different lenses.
- Engineering received a tier-prioritized scope, not a wish list.

### The vision statement
> *"Trust Center Visitors can confidently and efficiently complete their security review without support when using a Conveyor hosted Trust Center."*

### 3-day sprint timeline
| Day | Date | Focus |
|---|---|---|
| **Day 1** | Mar 31 | **Diverge & Build** — Heads-down. Each person builds independently. AI prototypes, sketches, code, whatever moves fastest. Showable, not perfect. |
| **Day 2** | Apr 1 | **Show & Debate** — 10-minute show & tells. Find the convergence. Surface the tension. Sleep on it overnight. |
| **Day 3** | Apr 2 | **Converge & Decide** — Force-rank by impact x feasibility. Lock the bets. Walk away with a Q2 scope and a list of what we're not building. |

**My contribution:** a comprehensive vision called *Coco* — three pillars: an AI agent, a Trust Scorecard, and comparison tools. *(Detailed on the next slide →)*

### Where we converged
- **AI as interface, not feature.** Not a chatbot bolted on — the way people interact with the Trust Center.
- **Constrained flexibility wins.** Templates and pre-built blocks beat free-form editing every time.
- **Transparency is the differentiator.** Genuinely useful security info is the real moat.

### Q2 priorities locked
- **Trust Center Agent (reimagined).** Primary differentiator. Unify with search.
- **Visual / design themes.** Templates with constraints. Brand alignment without ugly outputs.
- **Staging environments.** Foundational. Lightweight scope. Builds confidence for future rollouts.

*Accordion: Sprint structure, the six prototypes (Ivana, Chris, Sydney, H.T., Anner, Nadim), and what we cut from Q2 scope.*

---

## Slide 12 · The Vision Prototype

# What I brought to the *vision sprint*.

Three pillars, one thesis: a Trust Center that *genuinely helps* third-party risk managers assess security — not one that performs compliance theater.

### Carousel · 8 prototype screenshots
1. **Entry** — pick your Coco companion
2. **Trust Center home** — overview at a glance
3. **Coco** — conversational review with thought process and todo list
4. **Coco** — start a review or upload a questionnaire
5. **Documents and Knowledge** — search, browse, and ask
6. **Trust Scorecard** — coverage, freshness, depth, comparisons
7. **Viewport view** — a focused review surface
8. **Viewport overview** — full Trust Center

[Live prototype: ivanatso-conveyor.github.io/trust-center](https://ivanatso-conveyor.github.io/trust-center) (built in Claude Code)

### The three pillars

**Pillar 01 — *Coco*, the AI agent**
Conversational and voice-enabled. Handles search, questionnaires, and review checklists in one interface. Pick your Coco character on entry; it stays with you across the visit.

**Pillar 02 — *Trust Scorecard***
Quantifies coverage, freshness, and framework alignment. Category scores and content gaps surface at a glance. Exportable for boardrooms and QBRs.

**Pillar 03 — *Comparison* tools**
Visitors stack a vendor against peers — response time, doc freshness, certification breadth — so "which vendor passes our bar?" becomes a one-screen answer.

*Accordion: The wider vision — dark mode, session history, MCP server integration, badge gamification for admins. Full Scorecard / reputation system scoped as Phase 2.*

---

## Slide 13 · Reflection · What I'm taking forward.

# What I'm taking forward.

Six lessons from the loop. The ones I'll carry into the next bet, and the one after that.

**01 · Quantitative meets qualitative.**
Numbers alone don't earn buy-in. Quotes alone don't earn rigor. The case lands when both arrive together: 135 ratings backed by the words behind them.

**02 · Build the graph, not the deck.**
A heatmap, a dot grid, a tiered scope. Every visualization was a tool for alignment. Something Sales, Marketing, Engineering, and customers could read in 30 seconds and agree on. Graphs traveled where slides couldn't.

**03 · Interim moves clarify the vision.**
Placing a smaller bet today is how I learned what to bet bigger on later. Ship something credible now. The north star stays sharper because of it, not in spite of it.

**04 · AI prototyping changed the math.**
A working base prototype in two days. Two parallel directions in five. The cost of testing a "maybe" dropped to almost zero, so we tested both. Research picked the survivor.

**05 · Risk has a denominator.**
135 ratings turned "this feels risky" into "this is 1-in-135." That single Scared rating on the Changelog was the signal worth slowing down for. Everything else, we shipped with confidence.

**06 · Alignment is the deliverable.**
The research report became the asset Sales referenced, Marketing quoted, and Engineering scoped against. Customers saw their words land in the bet. The alignment was the work.

---

**Thanks for reading.**
Ivana Tso · Senior Product Designer · Conveyor

→ Next case study: *The Trust Center, 2026*
