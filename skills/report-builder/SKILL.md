---
name: report-builder
description: Assemble a monthly account report from the reporting spec and available data, without inventing figures. Use from /monthly-report or whenever the user asks for their monthly/account report.
---

# Report builder

Build a factual, well-structured monthly account report.

## Inputs
- `context/reporting-spec.md` — the required sections and KPIs.
- `templates/monthly-report.md` — the layout.
- `trackers/quotes.csv` — quotes won / open / lost and values for the period.
- `accounts/<client>/notes.md` — issues, callouts, actions, visits.
- Calendar / inbox via the Microsoft 365 connector, if connected.

## Method
1. Confirm the account and month.
2. Gather data from each source above.
3. **Never invent numbers.** For any KPI you can't obtain (e.g. callout counts from a service
   platform that isn't connected), **list it and ask the user to provide or confirm it.** Mark every
   user-supplied or estimated figure clearly (e.g. "(provided by the user)", "(estimated)").
4. Fill **every** section of the spec. If a section has no data, say so rather than padding.
5. Surface trends and risks explicitly — compare to the previous month where you can, and call out
   what needs attention.
6. Produce two things: the **written report** (markdown) and a short **slide outline** for the deck.

## Output
- Save to `reports/<account-slug>-<YYYY-MM>.md`.
- Summarise in chat, and clearly note anything you had to ask the user to supply.
