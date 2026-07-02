---
description: Draft a quote request to the estimating team from a few quick answers. Saves the draft for review.
argument-hint: [customer / site, if known]
---

# Quote request

Turn a quick brief into a clear quote request to the estimating team. Work in their workspace.

## Gather (ask what's missing, briefly)
- Customer / account and site + address.
- Items required — quantity and specification for each.
- Required-by date, and any special requirements (access, timing, existing system, etc.).
- The opportunity value / context, if known.

Pull anything you can from the relevant `accounts/<client>/notes.md` so you don't re-ask.

## Draft
- Fill `templates/quote-request.md` with the gathered details, addressed to estimating.
- Keep it complete and unambiguous — estimating should not have to come back with questions.

## Save & record
- Save to `drafts/YYYY-MM-DD-quote-request-<account>.md`.
- Add the pending quote to `trackers/quotes.csv` (status = requested; set `next_chase_date` from the
  overdue threshold or the mapped quote-to-PO workflow) and note it in the account's `notes.md`.
- Show the draft and remind the user to review and send it.
