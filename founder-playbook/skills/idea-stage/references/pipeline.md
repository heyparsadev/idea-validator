# The ten-step Idea-stage protocol

Run in order. Each step lists: what it produces, how to run it in **coach** mode vs **auto** mode, and the gate that must pass before advancing. Coach mode = one question at a time, founder answers, you sharpen. Auto mode = you produce a draft and mark every assumption.

---

## Step 0 — Brief & kill criteria

**Produces:** `00-brief.md`

Extract everything already said before asking anything. Then ask only the gaps, batched.

Capture:
- **The raw idea**, in the founder's own words, unedited. Preserve it verbatim — it's the baseline you'll compare against after discovery reshapes things.
- **Origin story.** Where did this come from? First-hand experience beats observation beats reading about it. Note which.
- **The founder's unfair advantage.** Domain expertise, access to the buyer, distribution, a technical edge. "None yet" is a legitimate and useful answer.
- **Constraints.** Runway in months, hours per week, capital, geography, regulatory exposure.
- **Kill criteria — write these before any research.** Ask directly: *"What would you have to learn in the next six weeks for you to walk away from this?"* Push until there are 2–4 concrete, checkable statements. Vague ones ("if nobody wants it") get sharpened to checkable ones ("if fewer than 3 of 12 target-profile interviewees describe this as a top-3 workflow problem").

If the founder cannot name anything that would change their mind, say so plainly: an unfalsifiable idea cannot be validated, only believed. Get at least one real kill criterion before proceeding.

**Gate:** kill criteria written and specific enough to be checked.

---

## Step 1 — Forge the hypothesis

**Produces:** `01-hypothesis.md`

Turn an observation into a testable hypothesis. The book's distinction:

> "People struggle with expense reporting" is an observation.
> "Finance managers at mid-market companies spend four-plus hours a week reconciling submissions because their current tools don't integrate with their accounting software" is a testable hypothesis.

**The form:**

> **[WHO — specific role, seniority, company type/size, geography]** loses **[MAGNITUDE — hours, money, error rate, deals]** every **[FREQUENCY]** because **[ROOT CAUSE — mechanism, not symptom]**. Today they cope by **[CURRENT WORKAROUND — a named tool, a person, a spreadsheet, or suffering]**.

**The four-question testability rubric.** A hypothesis is not ready until all four have precise answers:

| Question | Not ready | Ready |
|---|---|---|
| **Who exactly?** | "small businesses" | "office managers at 5–20 chair dental clinics in Tehran" |
| **How often?** | "regularly" | "every appointment cycle, ~40×/week" |
| **How severely?** | "it's frustrating" | "~6 no-shows/week × ~2M IRR per slot" |
| **What do they do today?** | "nothing good" | "a WhatsApp broadcast the receptionist sends manually each evening" |

The fourth is the most diagnostic: **if there is no current workaround, there may be no real problem.** People who genuinely hurt find *some* way to cope. Absence of a workaround is a red flag, not a green field — record it as such.

**Then extract the assumption stack.** List every assumption the hypothesis rests on, and rank by (risk if wrong) × (uncertainty). The top three become the interview agenda in step 6.

- Coach: ask the four questions one at a time; reflect back a sharpened draft after each; don't accept a vague answer by paraphrasing it into a precise-sounding one.
- Auto: draft 2–3 candidate hypothesis variants at different specificity levels, mark every filled-in number as an assumption to verify, and hand the founder the choice.

**Gate:** all four rubric questions answered precisely; assumption stack ranked.

---

## Step 2 — Red team

**Produces:** `02-redteam.md`

Point the same research engine in the opposite direction. This is the antidote the book prescribes for "confirmation bias with a research engine."

Required sections, written in this order (against first):

1. **The strongest case this is a bad idea.** Not a strawman — the argument a smart skeptic who *wants* the founder to succeed would actually make.
2. **Disconfirming evidence.** Search specifically for: negative market signals, companies that tried this and died (and *why* they died — the mechanism matters more than the fact), customer behavior patterns that contradict the hypothesis, structural obstacles (procurement cycles, regulation, switching costs, budget ownership).
3. **The graveyard.** Named dead or pivoted attempts at this problem, with cause of death. "No one has tried this" is almost never true and is usually a research failure; if it holds up after real search, treat it as a warning about the market, not a moat.
4. **Why the problem might be real but unmonetizable.** Real pain that nobody pays to fix is the most common trap for domain-expert founders.
5. **What would have to be true** for the idea to work anyway — the counter-case, written last, and only after 1–4 are complete.

Delegate to the `idea-red-team` agent when available; it is prompted to refute rather than assess.

**Gate:** at least one finding the founder concedes is genuinely worrying. If nothing lands, the red team was too soft — run it again with a harder brief. A red team that produces no discomfort has failed.

---

## Step 3 — Competitive landscape

**Produces:** `03-competition.md` — see `research-kit.md` for the full method.

Four tiers, all four filled:

| Tier | Definition | Why it matters |
|---|---|---|
| **Direct** | Solving the same problem for the same buyer | Obvious; usually the only tier founders map |
| **Indirect** | Different approach, same job-to-be-done — including spreadsheets, agencies, and hiring a person | The real incumbent is usually Excel or a human |
| **Potential acquirers** | Larger players who'd buy rather than build | Shapes exit path and pricing ceiling |
| **Adjacent** | One product decision away from entering | The tier that kills you 18 months in |

Then the **competitor-neglect antidote**, verbatim from the book: for the strongest player in each tier, make *the most compelling argument for why they succeed and you do not.* Why their approach is actually better, why customers would choose them, why the founder's differentiators may not be as defensible as they think. Write it to persuade, not to be dismissed.

**Gate:** four tiers populated; the "why they win" case is one the founder cannot immediately wave away.

---

## Step 4 — Market & complaint mining

**Produces:** `04-market.md` — full method in `research-kit.md`.

Three parts:

1. **Complaint mining.** Synthesize publicly available customer feedback on competitors — reviews, forums, subreddits, app-store ratings, support communities — and extract the top recurring complaints existing solutions haven't resolved. This is free qualitative research on competitors' customers. Then the decisive check: **does the hypothesis address one of them?** If yes, that's real evidence of problem–solution fit (grade B). If no, that is equally worth knowing and must be recorded as such, not quietly dropped.
2. **TAM / SAM / SOM**, built from publicly available data, with every assumption listed separately and pressure-tested. Report the assumptions more prominently than the totals — a TAM is only as good as its weakest multiplier. Also classify: is the market **expanding, consolidating, or mature**? This drives timing and differentiation strategy.
3. **Buyer map.** Who holds budget, who influences the decision, who uses the product, who can veto — and whether any of those are the same person. In B2B, "user ≠ buyer" is where most first-time founders' go-to-market assumptions break.

**Gate:** sizing assumptions listed and attacked individually; buyer map distinguishes user, buyer, and veto.

---

## Step 5 — Trend read

**Produces:** `05-trends.md`

Identify exactly **three** external trends — regulatory, technological, or demographic — that could significantly affect this market in the next two years. For each: state the trend, cite the evidence, then judge it explicitly a **tailwind** or a **headwind for this specific hypothesis** — not for the industry in general. A trend with no verdict is trivia.

Also:
- **Language mining.** The exact words target users reach for when describing the problem, harvested from the communities where they already discuss it. This vocabulary goes straight into the interview script and later into positioning.
- **Analogous markets.** Where was a structurally similar problem solved before? Extract what worked and what didn't. Analogy is the cheapest form of experience available at this stage.
- **Why now?** If the answer is only "AI makes it possible," ask what stops fifty other founders from having the same thought this quarter.

**Gate:** three trends, each with an explicit tailwind/headwind verdict and reasoning.

---

## Step 6 — Design customer discovery

**Produces:** `06-discovery-plan.md` — full method in `interview-kit.md`.

Three parts: **who to talk to**, **where to reach them**, **what to ask**.

The quality of what the founder learns is determined by the quality of the questions and whether they're being asked of the right people. A precise target profile is worth infinitely more than a long contact list.

Non-negotiables:
- Questions probe **the relevant past**, never the hypothetical future. "Tell me about the last time you dealt with this" — never "would you use something like this?"
- Every question passes the **four-flag audit**: leading · future-facing · too broad · invites a socially desirable answer. See `interview-kit.md`.
- **Separate scripts per persona.** A finance manager and a CFO have different relationships to the same problem; one flat script erases the distinction.
- Pre-written **follow-up probes** for the two or three moments most likely to produce deflection or vagueness.

Best practice when the founder is willing: have them draft the questions by hand first, then audit them. Founder-drafted-then-audited scripts consistently beat generated ones, because the founder's questions reveal what they actually believe.

**Gate:** every question survives the four-flag audit; per-persona scripts exist; probes written.

---

## Step 7 — Run interviews (the wall)

**Produces:** `07-interviews/*.md`, `08-synthesis.md`

**This is the only source of grade-A evidence, and no mode can run it for the founder.** Auto mode stops here and says so.

- **Volume:** 8–12 conversations minimum for a single persona; 8–12 *per persona* if the hypothesis spans several.
- **Per interview:** raw notes captured first, verbatim where possible, then a debrief answering three questions — what **confirmed** the hypothesis, what **challenged** it, what was **genuinely surprising**. The surprises are usually the most valuable line in the file, because they're the part nobody's bias could have generated.
- **Every five interviews:** produce two lists — supporting evidence and challenging evidence — then run the asymmetry check: *if the supporting list is significantly longer, does that reflect what's in the data, or what the founder was hoping to find?* Record the answer, not just the question.
- **Pattern-matching check:** after synthesizing, take the synthesis back and ask where the founder's own read might be pattern-matching to what they want to hear.

What can be offered instead of real interviews, clearly labelled: rehearsal against a simulated persona (to test the *script*, never the hypothesis), and Cowork-style logistics — prospect list, outreach drafts, scheduling, follow-up cadence, tracking sheet. Logistics support is genuinely useful. It is not evidence.

**Gate:** ≥8 real conversations logged; synthesis current; asymmetry check answered.

---

## Step 8 — Solution concept

**Produces:** `09-solution.md`

The reality checkpoint: **does this design address the problem discovery revealed, or the problem originally assumed?** Say explicitly which, and if they differ, rewrite the hypothesis in `01-hypothesis.md` and mark steps 3–5 stale.

For the concept, produce:
- What it does, for whom, and the specific workflow moment it replaces.
- **The three assumptions the design depends on most heavily.** For each: what would have to be true for it to hold, how it could be cheaply tested, and what the consequence is if it doesn't hold. If a single assumption failing kills the product, name it as such.
- Gaps and alternatives — including the alternative of not building software at all (a service, a template, a spreadsheet, a person).
- What would have to be true for this to work **at scale**, not just for the first ten users.

**Gate:** three load-bearing assumptions named, each with test and consequence.

---

## Step 9 — Lightweight prototype brief

**Produces:** `10-prototype.md`

Now, and only now, building is allowed — and only this:

**Define the single core interaction the solution depends on. Build only that.** The minimum surface area needed to put the idea in front of a real human and get a genuine reaction. Not a product; a functional sample for customer and investor conversations.

The brief contains:
- The one interaction, in one sentence.
- Explicitly out of scope: auth, onboarding, settings, billing, admin, empty states, mobile, and every second feature. Write the exclusion list — it's what makes the brief hold.
- Fake-it-first list: what can be hardcoded, mocked, or done by hand behind the screen.
- **The test plan:** five people from the *validated* target profile, what to watch for (where they hesitate, what they try that doesn't exist, what they ignore), and the decision rule written before the tests — what result means keep building, and what result means back to the drawing board.

Reiterate the prime directive: the prototype's existence is not evidence. The five reactions are.

**Gate:** exactly one interaction; exclusion list written; decision rule written *before* testing.

---

## Step 10 — Exit gate

**Produces:** `DECISION.md`

Score the three exit questions from `SKILL.md`, each with cited evidence and grade. Then check the step-0 kill criteria: were any met? If yes, that outweighs a favorable-looking scorecard — that is what writing them in advance was for.

Verdict: **PROCEED** · **ITERATE** · **PIVOT** · **KILL**. Write the reasoning, append to VENTURE.md's decision log, and deliver it to the founder plainly. A KILL verdict is not softened, and it is not a failure — the stage is designed to surface that before the money and the year are spent.

On PROCEED, close with what the next stage changes: the guiding question shifts from *"is this worth building?"* to *"what exactly should we build first?"*, and AI's role shifts from research partner to construction crew.
