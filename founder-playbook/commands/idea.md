---
description: Validate a startup idea — Idea-stage pipeline from The Founder's Playbook (coach / auto / hybrid)
argument-hint: [the idea, or a venture slug to resume]
---

Run the Idea-stage validation pipeline from *The Founder's Playbook* on: **$ARGUMENTS**

Invoke the `founder-playbook:idea-stage` skill and follow it.

- If `$ARGUMENTS` names an existing venture in `ventures/`, read its `00-idea-stage/STATE.md` and `EVIDENCE.md` first and **resume from the recorded step** — do not restart the pipeline.
- If `$ARGUMENTS` is a new idea (or empty), start at step 0: capture the brief verbatim, get the kill criteria written down before any research, then pick the mode.
- If the founder hasn't specified a mode, ask once with `AskUserQuestion` — coach / auto / hybrid, with hybrid recommended.

Respond in the founder's language.
