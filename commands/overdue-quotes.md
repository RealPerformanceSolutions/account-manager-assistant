---
description: Find overdue quotes and draft a chase email for each. Saves drafts for review — never sends.
argument-hint: (no arguments)
---

# Overdue quotes

Chase quotes that have gone quiet. Work in their workspace.

## Read
- `trackers/quotes.csv` and `context/preferences.md` (overdue threshold, default 7 days).
- `context/workflows/quote-to-po.md` if it exists — follow its stages and chase timings.
- `context/voice-profile.md` for tone; the relevant `accounts/<client>/notes.md` for context.

## Do
Handle two stages, based on the mapped workflow (or sensible defaults if none is mapped):

1. **Quotes awaiting a decision** — every quote whose `status` is still open/awaiting and whose
   `date_sent` (or `next_chase_date`) is past due. Draft a short, friendly chase in the user's voice
   asking if they've had a chance to review.
2. **Approved quotes awaiting a PO** — where `status` is approved but `po_status` is still
   outstanding and `next_chase_date` is due. Draft a chase for the **PO**, aimed at whoever the
   workflow says raises it (e.g. the main contractor, not the end customer). Include the quote
   reference and value.

For each: show account, contact, value, and how many days overdue; save the draft to
`drafts/YYYY-MM-DD-chase-<account>.md`; append a line to the account's `notes.md`; and update
`next_chase_date` in `quotes.csv`.

## Rules
- Never send. Drafts are for the user to review and send.
- If `quotes.csv` is empty or missing, tell the user and offer to help them start it.
