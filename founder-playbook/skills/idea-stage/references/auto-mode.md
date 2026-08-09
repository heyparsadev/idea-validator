# Auto mode

Auto mode runs the pipeline end to end and hands the founder a finished dossier to react to. It is genuinely useful and it has one hard limit that must never be blurred.

## The hard limit — state it before starting

**Auto mode cannot produce problem–solution fit.**

It produces a sharpened hypothesis, a serious red team, a researched competitive landscape, an attacked market model, a trend read, a ready-to-run discovery plan, a stress-tested solution concept, and a prototype brief. Every one of those is desk work — grade C and D evidence.

Problem–solution fit requires grade A: real conversations with real people. Step 7 is a wall no mode crosses. Say this at the start, not at the end, and never let the volume of generated output imply otherwise.

The failure mode this guards against is precisely the one the book names: *"a founder who isn't asking hard questions can now construct an elaborate, well-researched-looking case for a bad idea faster than ever before, while feeling fully confident they are performing due diligence."* A thirty-page auto-mode dossier is exactly what that failure looks like if the grading is dropped.

## Run order

Auto mode may run without stopping through:

| Step | Runs | Notes |
|---|---|---|
| 0 Brief | **Partial** | Founder must supply the raw idea, context, and kill criteria. Draft candidate kill criteria for approval — never assume them. |
| 1 Hypothesis | Yes | Produce 2–3 variants at different specificity; every filled number marked `ASSUMED`. Founder picks. |
| 2 Red team | Yes | Delegate to the `idea-red-team` agent. Run it before any supportive research so the framing isn't already anchored. |
| 3 Competition | Yes | Real search. `no data found` where nothing is found. |
| 4 Market | Yes | Assumption table mandatory. Totals never reported alone. |
| 5 Trends | Yes | Three, each with explicit verdict. |
| 6 Discovery plan | Yes | Full profile, reach map, per-persona scripts, probes. |
| 7 Interviews | **STOP** | See below. |
| 8 Solution concept | Yes, **provisional** | Marked `PRE-DISCOVERY` — it addresses the assumed problem, not a revealed one. Must be revisited after step 7. |
| 9 Prototype brief | Yes, **provisional** | Same caveat. Do not encourage building it before step 7. |
| 10 Exit gate | **Partial** | Score honestly. With no interviews, question 1 fails on grade. The verdict is `BLOCKED — awaiting discovery`, never PROCEED. |

## At the wall (step 7)

Stop and say clearly: the desk work is complete, the hypothesis survived it, and problem–solution fit is not established.

Then offer what genuinely helps:

- **Interview logistics.** Build the prospect list from the target profile, draft personalized outreach, design the follow-up cadence (e.g. a day-seven nudge for non-responders), and set up a tracking sheet with outreach status, follow-up cadence, and completion columns. With Gmail/Calendar MCP connected, run the scheduling thread too. This is the book's Cowork workflow and it removes real friction.
- **Script rehearsal.** Role-play an interview against a `[SIMULATED]` persona so the founder can practice. This tests the *script*, never the hypothesis. Every output is graded D and cannot enter the gate.
- **Debrief-on-demand.** As soon as real interviews start, process notes into debriefs and synthesis immediately, while detail is fresh.

## Labelling rules

Non-negotiable in auto mode:

- Any model-generated user voice is prefixed `[SIMULATED]` in every file it appears in — not just where it's introduced.
- Every unverified number carries `ASSUMED` inline, at the point of use, not only in a footnote.
- Every claim in the dossier is graded in `EVIDENCE.md` as it's produced.
- Section headers for provisional work carry the `PRE-DISCOVERY` marker.
- Where research found nothing, write `no data found` and say which of these it likely means: a small market, a mis-framed query, or a genuinely unserved niche.

## The auto-mode dossier summary

Every auto run closes with this block, at the top of `DECISION.md`:

```markdown
## Auto-mode summary — <date>

**What this dossier is:** desk research and structured adversarial analysis.
**What it is not:** evidence of problem–solution fit.

| Evidence grade | Count |
|---|---|
| A — real conversations | 0 |
| B — real users, public | _ |
| C — third-party research | _ |
| D — model reasoning | _ |

**Verdict:** BLOCKED — awaiting customer discovery.

**Strongest reason to proceed:** <one line, with grade>
**Strongest reason to stop:** <one line, with grade>
**The single riskiest assumption:** <one line> — test it in interviews 1–5.
**Closest kill criterion:** <which, and how close>

**Next action:** run <n> interviews against `06-discovery-plan.md`.
```

The founder should be able to read that block alone and know exactly what they do and do not yet know.

## Hybrid mode

The recommended default. Auto for the research-heavy steps (3, 4, 5) where breadth and speed are the value; coach for the judgment steps (1, 2, 8, 10) where the founder's own thinking is the product.

Step 7 is always the founder's, in every mode.
