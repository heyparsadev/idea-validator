---
description: Red-team a startup idea or hypothesis — build the strongest case that it's wrong
argument-hint: [the hypothesis, or a venture slug]
---

Red-team this idea: **$ARGUMENTS**

Launch the `idea-red-team` agent with the hypothesis as its brief. If `$ARGUMENTS` names a venture in `ventures/`, read `00-idea-stage/01-hypothesis.md` first and pass the current hypothesis version verbatim.

When the agent returns:
1. Write the result to `ventures/<slug>/00-idea-stage/02-redteam.md` if a workspace exists.
2. Append every finding to `EVIDENCE.md` with its grade and source, marked as **challenging**.
3. Present the ranked findings to the founder and ask them to concede or rebut each one — record which, with reasoning.

The gate: at least one finding the founder concedes is genuinely worrying. If nothing lands, the red team was too soft — run it again with a harder brief.

Respond in the founder's language.
