---
description: Build the monthly report for an account from the spec and available data. Never invents figures.
argument-hint: [account and month, e.g. "Acme Ltd, July"]
---

# Monthly report

Assemble a monthly account report. Work in their workspace and use the `report-builder` skill.

## Confirm
- Which account and which month. If not given, ask.

## Gather
- `context/reporting-spec.md` (the sections + KPIs) and `templates/monthly-report.md`.
- `trackers/quotes.csv` (quotes won / open / lost + values for the period).
- `accounts/<client>/notes.md` (issues, callouts, actions, visits).
- Calendar (visits made that month) if Microsoft 365 is connected.

## Build
- Follow the `report-builder` skill: fill every section of the spec.
- **For any KPI you cannot obtain** (e.g. figures from a service platform that isn't connected),
  **list it and ask the user to provide or confirm it — never invent numbers.** Clearly mark any
  figure the user supplied or that is estimated.
- Surface trends and risks explicitly, not just raw numbers.
- Produce the written report **and** a short slide outline for the user's deck.

## Save
- Save to `reports/<account-slug>-<YYYY-MM>.md`.
- Show a summary in chat and note anything you had to ask the user for.
