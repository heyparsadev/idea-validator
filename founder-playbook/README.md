# founder-playbook

Idea-stage validation copilot, built on **The Founder's Playbook: Building an AI-Native Startup** (Anthropic, 2026).

The book's thesis: agentic coding collapsed the distance between "I have an idea" and "I have a product," and AI research gave confirmation bias an engine. 42% of startups failed by building something nobody wanted — *before* building became nearly free. This plugin implements Chapter 3's answer: don't build until the evidence justifies it.

## Skills

| Skill | What it does |
|---|---|
| **`idea-stage`** | The full Chapter 3 pipeline — hypothesis → red team → competition → market → trends → discovery design → interviews → solution concept → prototype brief → exit gate. Coach, auto, or hybrid mode. |
| **`stage-map`** | Whole-book lifecycle router. Diagnoses which of the four stages (Idea / MVP / Launch / Scale) you're *actually* in from evidence, names that stage's goal, exit criteria and failure modes, and routes to the next action. |

## Commands

```bash
/founder-playbook:idea <your idea>          # run or resume the pipeline
/founder-playbook:idea-redteam <hypothesis> # adversarial pass only
/founder-playbook:idea-gate <venture-slug>  # score the exit gate
```

## Agent

`idea-red-team` — prompted to **refute**, not assess. Builds the strongest case the idea is wrong, hunts disconfirming evidence, and finds the graveyard of prior attempts with causes of death.

## The two modes

**Coach** — one sharp question at a time; the founder does the thinking; Claude challenges and writes up. Slower, and the founder ends up understanding their own market.

**Auto** — Claude runs steps 1–6 and 8–10 end to end from desk research and hands over a full dossier with every assumption flagged.

**Hybrid** (recommended) — auto for the research-heavy steps, coach for the judgment ones.

### The wall

**Auto mode cannot produce problem–solution fit**, and the skill says so up front rather than at the end. It produces a sharpened, well-attacked hypothesis and a ready-to-run discovery plan — all desk work, grade C and D evidence. Step 7 (real conversations) is the only source of grade-A evidence and no mode crosses it. What auto mode *can* do at the wall is the logistics: prospect list, outreach drafts, scheduling, follow-up cadence, tracking sheet.

## What makes the gate mean something

Every claim entering the workspace is graded:

| Grade | Source |
|---|---|
| **A** | A named target-profile person said it, in a conversation the founder had |
| **B** | A real user said it in public — a review, a forum, an app-store complaint |
| **C** | Third-party research: analyst report, survey, filing, credible journalism |
| **D** | Model reasoning, estimate, or `[SIMULATED]` output |

**No exit criterion passes on grade-D evidence alone.** "Is the problem real and specific?" requires an A. This is the mechanism that stops the stage becoming an elaborate, well-researched-looking case for a bad idea — the exact failure the book warns about.

Also enforced: kill criteria written *before* research starts · the case against written before the case for · a bias audit after every synthesis · and the rule that a prototype is a conversation prop, never evidence.

## Workspace

Interoperates with the [venture](https://github.com/heyparsadev/claude-venture-plugin) plugin. If `ventures/<slug>/VENTURE.md` exists it's reused; otherwise a minimal one is created.

```
ventures/<slug>/00-idea-stage/
├── STATE.md · EVIDENCE.md · DECISION.md
├── 00-brief.md … 10-prototype.md
└── 07-interviews/
```

`STATE.md` makes the pipeline resumable across sessions — it never restarts from scratch.

## Install

```bash
/plugin marketplace add https://github.com/heyparsadev/idea-validator.git
/plugin install founder-playbook@idea-validator
```

## Coverage

Chapter 3 (Idea Stage) is implemented in depth. Chapters 4–6 (MVP, Launch, Scale) are covered at map level by `stage-map` — goals, exit criteria, failure modes, and the book's exercises in `stage-map/references/lifecycle.md` — and are structured so each can become its own deep skill later.
