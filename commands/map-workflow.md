---
description: Map one of the user's recurring work processes step by step, then save it so the other commands follow how they actually work.
argument-hint: [process name, e.g. "quote to PO" or "service request"]
---

# Map a workflow

Interview the user about **one** recurring process, then write it down so the assistant works the way
they actually work instead of a guessed default. Work in their workspace.

## Pick the process
- If they named one in the argument, use it. Otherwise ask which process they want to map. Common
  ones for an account manager: quote-to-PO, service/fault requests, new enquiry handling, meeting
  follow-up.

## Interview (one question at a time)
Draw out the real shape of the process:
1. **Trigger** — what starts it? (an email arrives, a quote is accepted, a call comes in…)
2. **Steps** — walk through what happens, in order, in their words.
3. **People / parties** — who's involved at each step (customer, main contractor, estimating,
   service, a specific person like "raise a PO to the main contractor").
4. **Decision points** — where does it branch? (approved / not, urgent / routine…)
5. **Timings** — how long before each chase or next step? (e.g. chase a PO after 5 working days)
6. **Done** — what does "finished" look like?

For each step, note whether the assistant can help (**read / draft / track**) or whether it's
something the user does themselves (**send / act / decide**). Be honest: in this version the
assistant prepares and tracks, the user sends and acts.

## Save it
Write `context/workflows/<slug>.md` (create the `context/workflows/` folder if needed) with:

```
# <Process name>
Trigger: …
Steps:
  1. <step> — [assistant: read/draft/track | user: send/act]
  2. …
Parties: …
Decision points: …
Timings / chases: …
Done when: …
Commands that use this: …
```

## Wire it up
- Tell the user which commands will now follow this workflow (e.g. `/overdue-quotes` reads
  `quote-to-po.md` for the stages and chase timing).
- Offer to map another process, or to stop here. They can re-run `/map-workflow` any time a process
  changes.
