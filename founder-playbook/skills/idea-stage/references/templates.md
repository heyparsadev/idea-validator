# Output templates

Copy these structures. Adapt the language to `report_language`; keep the structure.

---

## STATE.md

```markdown
# Idea stage — state

- **Venture:** <name>   **Mode:** coach | auto | hybrid
- **Hypothesis version:** v<n>   **Started:** <date>   **Updated:** <date>

| Step | Status | File | Updated |
|---|---|---|---|
| 0 Brief & kill criteria | done / in progress / not started / **stale** | 00-brief.md | |
| 1 Hypothesis | | 01-hypothesis.md | |
| 2 Red team | | 02-redteam.md | |
| 3 Competition | | 03-competition.md | |
| 4 Market | | 04-market.md | |
| 5 Trends | | 05-trends.md | |
| 6 Discovery plan | | 06-discovery-plan.md | |
| 7 Interviews | _n_ of _target_ done | 07-interviews/ | |
| 8 Solution concept | | 09-solution.md | |
| 9 Prototype brief | | 10-prototype.md | |
| 10 Exit gate | | DECISION.md | |

## Open threads
- [ ] <what's unresolved and who owns it>

## Stale after hypothesis change
- <steps to re-run, and why>
```

---

## 00-brief.md

```markdown
# Brief

## The idea, in the founder's words
> <verbatim — never edited, this is the baseline>

## Origin
<first-hand experience | observed | read about it> — <detail>

## Founder's unfair advantage
<domain expertise / buyer access / distribution / technical edge / none yet>

## Constraints
- Runway: · Hours per week: · Capital: · Geography: · Regulatory:

## Kill criteria — written <date>, before research
1. <concrete, checkable>
2. 
3. 

<!-- Reviewed at the exit gate. Meeting one outweighs a favorable scorecard. -->
```

---

## 01-hypothesis.md

```markdown
# Problem hypothesis — v<n>

> **<WHO — role, seniority, company type/size, geography>** loses **<MAGNITUDE>**
> every **<FREQUENCY>** because **<ROOT CAUSE>**.
> Today they cope by **<CURRENT WORKAROUND>**.

## Testability rubric
| Question | Answer | Grade | Source |
|---|---|---|---|
| Who exactly? | | | |
| How often? | | | |
| How severely? | | | |
| What do they do today? | | | |

## Assumption stack — ranked by risk × uncertainty
| # | Assumption | If wrong | Certainty | How to test |
|---|---|---|---|---|
| 1 | | | | |

The top three become the interview agenda in step 6.

## Version history
| v | Date | What changed | What triggered it |
|---|---|---|---|
```

---

## 02-redteam.md

```markdown
# Red team

## 1. The strongest case this is a bad idea
<the argument a smart skeptic who wants the founder to win would actually make>

## 2. Disconfirming evidence
| Finding | Source | Grade | Why it matters |
|---|---|---|---|

## 3. The graveyard
| Who tried | When | Outcome | Cause of death | Source |
|---|---|---|---|---|

## 4. Real problem, no market?
<the case that the pain is genuine but nobody pays to fix it>

## 5. What would have to be true for this to work anyway
<written last>

## Founder's response
| Finding | Concede / rebut | Reasoning | Action |
|---|---|---|---|
```

---

## 08-synthesis.md

```markdown
# Discovery synthesis — after <n> interviews, <date>

## Evidence supporting the hypothesis
| # | Finding | Interviews | Strength |
|---|---|---|---|

## Evidence challenging the hypothesis
| # | Finding | Interviews | Strength |
|---|---|---|---|

## Surprises — what neither list predicted
- 

## Asymmetry check
Supporting: _  ·  Challenging: _
> Does this asymmetry reflect what's in the data, or what we hoped to find?

<honest answer, written out>

## Pattern-matching check
> Where might our read be matching what we want to hear rather than what's there?

<answer>

## Segment signal
<is the problem landing with the expected role, or a different one?>

## Hypothesis verdict
holds as written / needs revision (→ v<n+1>) / contradicted
```

---

## 09-solution.md

```markdown
# Solution concept

## Problem this addresses
<the problem discovery REVEALED — state explicitly whether it differs from the assumed one>

## The concept
<what it does, for whom, which workflow moment it replaces>

## The three load-bearing assumptions
| # | Assumption | What must be true | Cheapest test | Consequence if false |
|---|---|---|---|---|
| 1 | | | | |
| 2 | | | | |
| 3 | | | | |

<!-- If one failing kills the product, say so here. -->

## Gaps and alternatives considered
- Including: not building software at all (service / template / spreadsheet / a person)

## What must be true at scale
<not just for the first ten users>
```

---

## 10-prototype.md

```markdown
# Lightweight prototype brief

## The single core interaction
<one sentence>

## Explicitly out of scope
auth · onboarding · settings · billing · admin · empty states · mobile · <every second feature>

## Fake it
| Element | Real or faked | How |
|---|---|---|

## Test plan
- **Who:** 5 people from the validated target profile — <named or sourced how>
- **Watch for:** where they hesitate · what they try that doesn't exist · what they ignore
- **Decision rule, written before testing:**
  - Keep building if: 
  - Back to the drawing board if: 

> The prototype is a conversation prop. Its existence is not evidence. The five reactions are.
```

---

## DECISION.md

```markdown
# Exit gate — <date>

## Evidence ledger summary
| Grade | Supporting | Challenging |
|---|---|---|
| A — real conversations | | |
| B — real users, public | | |
| C — third-party research | | |
| D — model reasoning | | |

## The three questions
| # | Question | Answer | Best grade | Evidence |
|---|---|---|---|---|
| 1 | Is the problem real and specific? | yes / no | | |
| 2 | Does the solution address the actual problem? | yes / no | | |
| 3 | Is there enough signal to justify building? | yes / no | | |

## Kill criteria check
| Criterion (from step 0) | Met? | Evidence |
|---|---|---|

## Verdict: PROCEED | ITERATE | PIVOT | KILL | BLOCKED (awaiting discovery)

**Reasoning:** <plain, unsoftened>

**The single riskiest thing we still believe without evidence:** 

## Next
<MVP stage · re-run steps 6–7 · back to step 1 · stop>

## Decision log
| Date | Decision | Rationale |
|---|---|---|
```
