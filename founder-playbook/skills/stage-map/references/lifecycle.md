# Exercises by stage

The concrete exercises from *The Founder's Playbook*, stage by stage. Use these when a founder asks "what do I actually do next?" — each is a self-contained session.

---

## Idea stage

1. **Sharpen the hypothesis.** Work until the problem statement is testable. "Contract review takes too long" isn't. "In-house legal teams at mid-market companies spend 3+ days per contract review cycle because redlines are managed across email threads rather than a single version-controlled document" is.
2. **Argue against your own idea.** Ask for disconfirming evidence that refutes the hypothesis: negative market signals, failed competitors, contradicting customer behavior, structural obstacles. Arrive at customer discovery having already stress-tested against the strongest counterarguments, so interviews are genuinely open-ended rather than a search for confirmation.
3. **Map competitors by tier** — direct, indirect, potential acquirers, adjacent players who could move in — then argue why *each tier* poses a genuine threat, not the easily dismissed version of it.
4. **Mine competitor reviews** across key sources for the top complaints existing solutions haven't resolved. If the hypothesis addresses one, that's strong evidence of problem–solution fit. If it doesn't, that's worth knowing too.
5. **Build TAM/SAM/SOM** from public data and pressure-test the assumptions. Classify the market as expanding, consolidating, or mature. Map the buyer landscape: who holds budget, who influences, and whether they're the same person.
6. **Three external trends** — regulatory, technological, demographic — that could significantly affect the market in two years, each assessed as a tailwind or headwind for *this specific hypothesis*.
7. **Audit your interview questions.** Draft them by hand first, then have every question flagged if it's leading, future-facing, too broad, or likely to produce a socially desirable answer. Add follow-up probes for the two or three moments most likely to generate deflection.
8. **Synthesize every five interviews** into two lists: evidence supporting the hypothesis, and evidence challenging it. If the first is significantly longer, ask whether that asymmetry reflects the data or what you hoped to find.
9. **Automate discovery logistics.** From the validated target profile: build a prospect list, draft a personalized outreach sequence, set up a tracking sheet with outreach status, follow-up cadence, and interview completion. Let it run while you prepare for the conversations.
10. **Stress-test the solution concept.** Identify the three assumptions the design depends on most heavily, what would have to be true for each to hold, and the consequences if any doesn't.
11. **Build the one interaction.** Define the single core interaction the solution depends on and build only that. Put it in front of five people from the validated target profile. What you learn determines whether you keep building or go back to the drawing board.

---

## MVP stage

1. **Architecture before code.** Before opening Claude Code, describe what you're building — the core problem, the users, the scale realistically expected in six months — and define the architectural principles that should govern the build, the dependencies to avoid, and the tradeoffs you're consciously accepting. Save it as `CLAUDE.md`: the first artifact of the build, and the one every subsequent session depends on.
2. **Scope document.** What the MVP does, what it deliberately does *not* do, and the feature amendment criteria — what specific evidence from real users would justify adding something. This moves the decision from "should we build this?" to "have a critical mass of users told us they can't get value without it?"
3. **Session template.** Each Claude Code session opens with the architectural context and the specific task; each session ends with a log entry recording what was built, what was decided, and what assumptions were introduced. Five minutes of documentation per session is cheap insurance against architectural drift.
4. **Security review before any user touches it.** Review for authentication and session handling, data exposure in API responses, input validation and injection risks, and dependencies with known vulnerabilities. AI review is a first pass — not a substitute for security tooling or, at higher stakes, a human reviewer.
5. **Measurement framework before launch.** Retention benchmarks, activation criteria, Day-7 and Day-30 targets — set *before* release. Then define what a false positive looks like for this specific product (signups without activation, revenue without retention, enthusiasm without repeat usage). When data arrives, ask for the adversarial case against your own traction.
6. **Feedback loop operations.** Outreach to the early user list, scheduled feedback sessions, structured intake for bugs and feature requests, weekly synthesis. Review the synthesis yourself first, then ask for what you overlooked. Keep a human in the loop for nuance — "this is great but I wish it could also…" needs interpretation no tool can supply.
7. **The pivot diagnostic.** After three or more iteration cycles without movement toward PMF benchmarks, feed in retention data, user feedback, and the original hypothesis, and ask three questions: Is there a segment responding differently than the rest? Is the gap between designed and experienced value a positioning problem or a product problem? What would have to be true for the current product to find genuine PMF, and is that realistic given what you're seeing?

---

## Launch stage

1. **Architectural audit → sequenced remediation.** Audit the MVP codebase for structural weaknesses, test coverage gaps, and refactoring candidates. Then sequence the work: what must be fixed before the next release, what can run parallel to feature work, what can wait. Document the MVP-era architectural decisions that lived only in your head into `CLAUDE.md`.
2. **Founder-attention audit.** Document every recurring task, every decision landing on your desk, every workflow that happens only because you remember it. Categorize: automate entirely / needs a human but not you / genuinely requires founder judgment. Then design the workflow logic for the automation candidates — triggers, decision rules, outputs, destinations.
3. **Security and compliance as a workstream.** A code-level review oriented to the frameworks your target market requires (SOC 2, GDPR, HIPAA). Produce two things: a prioritized remediation sequence, and the documentation and controls an enterprise buyer's compliance review will ask for. Build it into the development cycle rather than running it as a one-time project. AI scans aid but don't substitute for qualified compliance review.
4. **A lightweight PM operating system.** A defined sprint cadence, a minimum spec template, a bug triage decision tree, and a weekly metrics brief pulling from real data sources — then automate the recurring parts (scheduling, routing, report compilation) so they happen without you.

---

## Scale stage

1. **Bottleneck map.** Every workflow, decision, and approval currently routed through you — then extrapolate what happens to each when you're unavailable for a week. The ones that stall are where handoff criteria, escalation paths, or exception handling still need tightening.
2. **Enterprise gap analysis.** Pick three ideal or most-demanding prospects. What documentation, SLAs, and support infrastructure would their procurement team expect before signing a multi-year contract, and where do you fall short? Use it to sequence the technical and documentation work.
3. **Encode the moat as tests.** Identify one edge case a generic competitor would definitely get wrong in your vertical, and build a dedicated test case for it based on a scenario you've actually seen. Add one every time a similar case surfaces. The test suite becomes a map of your moat.
4. **Data flywheel + moat narrative.** From your interaction data, identify the three highest-signal behavioral patterns and design a feedback loop that turns each into systematic product improvement. Then draft a one-page moat narrative: how the flywheel works, how long it's been spinning, and why a well-resourced competitor starting today couldn't replicate it in under two years.
5. **Workflow integration audit.** For the top ten customers: the automations they've built, the integrations they depend on, the team workflows running through the product, and an estimate of their switching cost. Then find the patterns — what type of integration creates the deepest lock-in, and what would deepen it for customers currently at the surface.

---

## The through-line

The founder's job hasn't changed: find a real problem, build something that solves it, scale it into a company that matters. What changed is the path. Validation cycles that took months take afternoons; a prototype no longer needs a co-founder with the right stack; launch readiness compresses from a scramble into a continuous workstream.

**The bottleneck is no longer what you can build, but what you choose to build.**
