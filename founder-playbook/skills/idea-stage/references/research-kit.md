# Research kit — competition, market, trends

For steps 3, 4 and 5. Everything here obeys one rule: **the case against is written before the case for.**

---

## Step 3 — Four-tier competitive landscape

There's a startup-specific phenomenon the book calls **competitor neglect**: focusing so intensely on your own vision and execution that you systematically underweight what others are doing. The tiering exists to force attention outward.

### The tiers

**Tier 1 — Direct.** Same problem, same buyer, similar approach. Easy to find and the only tier most founders map.

**Tier 2 — Indirect.** Same job-to-be-done, different approach. **Always include the non-software options:** a spreadsheet, an agency, a contractor, a junior hire, a WhatsApp group, or simply tolerating the problem. In early-stage B2B the true incumbent is usually Excel or a person — and both are free-at-the-margin, already trusted, and infinitely flexible. A landscape that omits them is fiction.

**Tier 3 — Potential acquirers.** Larger players who would buy rather than build. Shapes exit paths, pricing ceilings, and how much of the market can be taken before someone notices.

**Tier 4 — Adjacent.** One product decision away from entering the space: they have the users, the data, or the distribution and lack only the feature. This is the tier that kills companies eighteen months in. For each, name the specific trigger that would bring them in.

### Per-competitor profile

```markdown
### <Name> — Tier <n>
- **What they do / for whom:** 
- **Approach:** 
- **Pricing & model:** 
- **Traction signals:** funding, headcount trend, review volume, hiring, release cadence
- **What customers praise:** <from real reviews — grade B>
- **What customers complain about:** <from real reviews — grade B; this is the opening, if there is one>
- **Why a target user would choose them over us:** 
- **Their trigger to move into our space:** (tiers 3–4)
```

### The competitor-neglect antidote — mandatory

For the strongest player in each tier, write **the most compelling argument for why they succeed and this venture does not.** Cover:
- Why their approach is actually better than the founder's, on the merits.
- Why customers would rationally choose them.
- Why the founder's claimed differentiators are not as defensible as they think — distribution, data, brand, switching costs, integrations, capital.

Write it to persuade. A version written to be dismissed has no value. Then, separately and afterwards, the founder's honest answer.

### Differentiation reality check

For each claimed differentiator, answer: **how long would it take a funded incumbent to copy this?** Under six months means it is a feature, not a moat. Say so.

---

## Step 4 — Market research

### 4a. Complaint mining — the highest-yield research in the stage

Synthesize publicly available customer feedback about competitors: review sites, subreddits, forums, app-store reviews, support communities, Twitter/X threads, YouTube comments on demos. This is essentially free qualitative research on competitors' customers, and it's grade **B** evidence — real users, unprompted.

Produce:
1. The **top recurring complaints** existing solutions haven't resolved, ranked by frequency and intensity, each with a real quote and link.
2. The decisive check: **does the hypothesis address one or more of them?**
   - **Yes** → strong evidence of problem–solution fit. Log to `EVIDENCE.md` as grade B with the source.
   - **No** → record it just as prominently. That the idea solves a problem no existing customer complains about is a finding, not a gap in the research, and it must not be quietly dropped.
3. The **exact language** users employ. Harvest it for the interview script and later for positioning — users' own words outperform invented category terms.

### 4b. TAM / SAM / SOM

Build from publicly available data, bottom-up wherever possible. Report the **assumptions more prominently than the totals**.

```markdown
### SAM — <segment>
Formula: <units> × <price> × <adoption>
| Input | Value | Source | Grade | Confidence | If wrong by 2×, SAM becomes |
|---|---|---|---|---|---|
| Clinics in Tehran, 3–20 chairs | 4,200 | <source> | C | med | ±2× |
| Annual willingness to pay | ? | none — inferred from adjacent SaaS | D | low | ±2× |
| Realistic 5-yr adoption | 8% | analogy: <market> | D | low | ±2× |
```

Then attack it:
- Which single input, if wrong, moves the answer most? That one deserves an interview question.
- What does the model look like at the pessimistic end of every input simultaneously? Is the business still interesting there?
- Is any input a grade-D number that has quietly become load-bearing?

Never present a total without the assumption table beside it. A TAM is only as strong as its weakest multiplier, and a fundable-looking number produced from three D-grade guesses is exactly what the book warns about.

**Market state.** Classify as **expanding**, **consolidating**, or **mature**, with evidence — funding flow, entrant and exit counts, M&A activity, pricing pressure. This drives timing and differentiation strategy: a mature market rewards a wedge, an expanding one rewards speed, a consolidating one rewards being acquirable or being the consolidator.

### 4c. Buyer map

| Role | Who | What they care about | What kills the deal for them |
|---|---|---|---|
| User | | | |
| Buyer (budget) | | | |
| Influencer | | | |
| Veto (security / legal / IT) | | | |

State explicitly whether user and buyer are the same person. In B2B they usually are not, and that gap is where most first-time go-to-market assumptions break. Also record the **procurement reality**: typical cycle length, whether a security review is involved, and who has ever been fired for a bad purchase in this category.

---

## Step 5 — Trend read

Exactly **three** trends — regulatory, technological, or demographic — that could significantly affect this market in the next two years.

```markdown
### Trend <n>: <name>  —  ⬆ TAILWIND / ⬇ HEADWIND
- **What's happening:** <specific, with evidence and date>
- **Source:** <link, grade>
- **Why it's a tailwind/headwind for THIS hypothesis:** <not for the industry — for this specific bet>
- **Time horizon:** <when it bites>
- **What it would change about the plan:** 
```

A trend without an explicit verdict for *this hypothesis* is trivia. Force the call.

**Analogous markets.** Where has a structurally similar problem been solved before — another vertical, another country, another decade? Extract what worked, what failed, and what the timing depended on. Analogy is the cheapest experience available at this stage.

**The "why now?" test.** Why is this possible or necessary *now* and not three years ago? If the only answer is "AI makes it possible," ask what prevents fifty other founders from having the same thought this quarter — and write down the answer. "No good answer" is itself a finding worth recording.

---

## Sourcing discipline

- Cite source and date for every external claim. Prefer primary sources over summaries.
- Grade everything into `EVIDENCE.md` as it's found — not in a batch at the end, when provenance is already blurred.
- **Never fabricate a number.** `no data found` is a legitimate and useful result; an invented figure is a liability that compounds through every downstream model.
- When search returns nothing on a competitor or market, say so — silence in the data may mean a small market, a mis-framed query, or a genuinely unserved niche, and those are very different situations. Note which you think it is and why.
- Re-run this whole kit whenever the hypothesis changes. The book is explicit that market and competitive work is not a one-time exercise.
