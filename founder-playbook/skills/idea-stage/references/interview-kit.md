# Customer discovery kit

For step 6 (design) and step 7 (run and synthesize).

Two things determine what the founder learns: the quality of the questions, and whether they're being asked of the right people. Both are designed here.

---

## Part 1 — Who to talk to

A precise target profile beats a long contact list every time.

**Profile fields — all of them, specifically:**

| Field | Bad | Good |
|---|---|---|
| Job title(s) | "decision makers" | "office manager", "clinic owner-dentist" |
| Seniority | "senior" | "owner or direct report to owner" |
| Company type & size | "SMBs" | "private dental clinics, 3–20 chairs" |
| Team structure | — | "1–2 reception staff, no IT person" |
| Geography | "Middle East" | "Tehran, Districts 1–6" |
| Proximity to the problem | — | "personally does the task being replaced" |
| Disqualifiers | — | "chains with in-house software — different buying process" |

**Reach map.** For each profile: where do these people actually congregate? Professional associations, trade events, LinkedIn groups, Slack/Discord workspaces, subreddits, Telegram channels, supplier networks, WhatsApp groups, conferences. Warm paths first — a single warm introduction outperforms fifty cold emails.

**Prioritization.** Rank prospects by *proximity to the problem*, not by ease of access. The founder's friendly contacts are the easiest to book and the least informative — they are motivated to be encouraging. Book the closest-to-the-problem people first, while the script is still sharp and curiosity is highest.

**Persona split.** If the hypothesis spans multiple roles, each gets its own profile, its own script, and its own interview count. A finance manager and a CFO have different relationships to the same problem, and a single framework flattens that distinction.

---

## Part 2 — What to ask

### The one rule

**Ask about the relevant past, never the hypothetical future.**

> ✗ "Would you use something like this?"
> ✓ "Tell me about the last time you dealt with this."

Future-facing questions measure politeness. Past-behavior questions measure reality. People are excellent reporters of what they did and terrible predictors of what they will do.

### The four-flag audit

Every question, before it ships:

| Flag | Symptom | Fix |
|---|---|---|
| **Leading** | Contains the answer or the founder's assumption. "How frustrating is the manual reminder process?" | Strip the assumption: "Walk me through how reminders get sent." |
| **Future-facing** | "Would you…", "Do you think you'd…", "If there were a tool that…" | Convert to past: "When did you last…", "What did you do the last time…" |
| **Too broad** | "How do you manage your operations?" | Anchor to one incident or one time window. |
| **Socially desirable** | Invites the flattering or agreeable answer. "Do you care about patient experience?" | Ask what they did and what it cost, not what they value. |

A question that trips a flag is rewritten, not softened.

### Script structure

1. **Warm-up (2 min).** Their role, their day, their team. No product talk. Builds the context you'll interpret everything else against.
2. **The incident (10 min).** The last time the problem occurred. Walk through it minute by minute: what happened, who was involved, what they did, how long it took, what it cost, what went wrong. This section carries most of the value in the interview.
3. **Frequency & severity (5 min).** How often does that happen? Was that time typical or unusual? What's the worst version?
4. **Current solution (8 min).** What they use today, what they've tried before and abandoned, and *why* they abandoned it. Have they ever paid for anything in this category? What happened to it? Abandonment stories are the highest-signal part of any discovery interview.
5. **Budget & authority (5 min).** Who would decide? Who holds budget? What's the last tool of this kind they bought, and what did that process look like? Never "would you pay X?" — instead "what do you currently spend on this problem, in money or in someone's hours?"
6. **Open close (5 min).** "What haven't I asked about that matters here?" and "Who else should I be talking to?" The second question is how the pipeline sustains itself.

**Do not demo in the first interviews.** Once the founder shows a solution, the conversation stops being about the problem and the interviewee starts being polite about the product. Save any prototype for step 9 sessions.

### Deflection probes

Pre-write probes for the two or three moments most likely to produce vagueness. Deflection is usually the interviewee being polite about something that doesn't matter to them — which is itself information.

| They say | Probe |
|---|---|
| "It's fine, we manage." | "What does managing it look like in practice? Who does that part?" |
| "It's annoying but not a big deal." | "When was the last time it actually cost you something?" |
| "Yeah, that'd be useful." | "What are you using for it now? What would have to stop working for you to change that?" |
| "We've thought about fixing it." | "What stopped you? What did you look at?" |
| A vague number | "How did you arrive at that? Is there somewhere it's recorded?" |
| Enthusiasm for the concept | "What would you have to stop doing to make room for this?" |

---

## Part 3 — Running and synthesizing

### Per interview

Capture raw notes first, verbatim where possible — quotes are the asset, summaries are lossy. Then a debrief, in this order:

```markdown
## Interview #N — <role>, <company type>, <date>

**Profile fit:** on-profile / partial / off-profile (say why)

**Raw notes**
<verbatim, especially direct quotes about the incident, the workaround, and money>

**Debrief**
- **Confirmed:** <what supported the hypothesis — with the quote>
- **Challenged:** <what contradicted it — with the quote>
- **Surprised:** <what neither side predicted>
- **Their actual current workaround:** <named tool / person / process>
- **Evidence of cost:** <hours, money, errors — or "none given">
- **New evidence rows:** #_, #_ → EVIDENCE.md
```

The **surprised** line is the most valuable in the file: it's the part no one's prior bias could have produced. If several interviews produce no surprises, the script is probably leading.

### Every five interviews

Produce exactly two lists — **supporting** and **challenging** — then the asymmetry check:

> If the supporting list is significantly longer than the challenging list, does that asymmetry reflect what's actually in the data, or what the founder was hoping to find?

Answer it in writing. Then re-read the synthesis and ask where the founder's read might be pattern-matching to what they want to hear rather than what's there. Both answers go into `08-synthesis.md`.

### What good and bad look like at n≈10

| Signal | Reading |
|---|---|
| Most interviewees describe the same incident unprompted | Strong — the problem is real and shared |
| They already pay someone or something to cope | Strong — budget exists, which is most of the battle |
| They tried a solution and abandoned it | Strong, and diagnostic — find out exactly why |
| Polite interest, no incident recalled | Weak — likely not a real problem for them |
| The problem is real but sits with a different role than expected | **Pivot signal on segment, not on problem** — often the most valuable finding in the whole stage |
| Everyone agrees it's a problem, nobody has ever spent anything on it | Real pain, no market — the domain-expert founder's classic trap |

Record the reading, not just the tally.
