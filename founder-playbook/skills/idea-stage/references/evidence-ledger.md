# The evidence ledger

The mechanism that stops this stage becoming an elaborate, well-researched-looking case for a bad idea.

The book's warning: *"Ask AI to validate your startup idea and it will find supporting evidence; ask it to size your potential market and it will find the number that makes your TAM look fundable."* A founder who isn't asking hard questions can now build that case faster than ever while feeling fully confident they're doing due diligence.

The ledger makes the *provenance* of every claim visible, so the exit gate is scored on what was actually learned rather than on how much was written.

## Grades

| Grade | Source | Example |
|---|---|---|
| **A** | A real, named person in the target profile said it, in a conversation the founder had | "Maryam, office manager, Sana Clinic, 2026-08-04: 'I re-send the reminders by hand every night, it takes 40 minutes.'" |
| **B** | A real user said it in public, unprompted | A G2 review, a subreddit thread, an app-store complaint, a support-forum post |
| **C** | Third-party research or reporting | Analyst report, industry survey, regulatory filing, credible journalism, competitor's public metrics |
| **D** | Model reasoning, inference, estimate, or simulation | Anything you concluded rather than found — including every `[SIMULATED]` persona response |

**Grade honestly, and grade down when unsure.** A plausible inference dressed as a finding is the exact failure mode this system exists to prevent. If a number came from a chain of reasoning, it is D, however sound the reasoning.

## Gate arithmetic

| Exit question | Minimum grade |
|---|---|
| Is the problem real and specific? | **A** — requires real conversations. No exceptions. |
| Does the solution address the actual problem? | **A or B** |
| Is there enough signal to justify building? | Judgment call, but every supporting claim must be graded and shown |

**No exit criterion can be satisfied by grade-D evidence alone.** When the ledger contains nothing above C, the honest report is: *"the desk research is done and the hypothesis survived it; problem–solution fit is not established and cannot be until interviews happen."* Say exactly that rather than implying more.

## Ledger format

`EVIDENCE.md`, appended continuously — never rewritten:

```markdown
# Evidence ledger — <venture>

Grades: A = named target-profile person, in conversation · B = real user, public
        C = third-party research · D = model reasoning / estimate / simulation

| # | Claim | Grade | Source | Date | Supports / Challenges | Step |
|---|-------|-------|--------|------|----------------------|------|
| 1 | Receptionists re-send reminders manually each evening | A | Interview #3 — Maryam, Sana Clinic | 2026-08-04 | supports | 7 |
| 2 | No-show rate in Tehran private clinics ≈ 18% | C | <source + link> | 2026-08-02 | supports | 4 |
| 3 | Two prior local booking apps shut down in 2024 | B | Founder post-mortem thread | 2026-08-02 | challenges | 2 |
| 4 | Clinics would pay ~3M IRR/month | D | Estimate from adjacent SaaS pricing — UNVERIFIED | 2026-08-02 | supports | 4 |

## Balance
- Supporting: A: _  B: _  C: _  D: _
- Challenging: A: _  B: _  C: _  D: _

## Unverified claims blocking the gate
- [ ] #4 — willingness to pay: no evidence above D. Test in interviews 9–12.
```

Keep the balance counts current. They are the fastest way to see confirmation bias forming: a ledger with fifteen supporting rows and two challenging rows is describing the researcher, not the market.

## Bias audit

Run after every synthesis and before the exit gate. Six questions, answered in writing:

1. Is the supporting list materially longer than the challenging list? Does that asymmetry reflect the data, or what the founder hoped to find?
2. Which supporting claims are grade D wearing the costume of grade A? Re-grade them now.
3. What is the single strongest piece of disconfirming evidence found so far, and what happened to it? If it was explained away, write down the explanation and check whether it would convince a stranger.
4. Which of the step-0 kill criteria is closest to being met?
5. Where did the search go looking for confirmation? Re-run the weakest search with an inverted query.
6. If a competitor's founder read this dossier, what would they say was missing?

Write the answers into the current step's file. An audit that produces no changes was not an audit.

## Staleness

When the hypothesis changes, evidence gathered against the old hypothesis may no longer apply. Mark affected rows `[STALE — hypothesis v1]` rather than deleting them; the trail of what was believed and when is itself useful at the gate, and prevents quietly re-importing a conclusion whose basis has been revised away.
