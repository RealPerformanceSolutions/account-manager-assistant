---
description: Draft a reply to an email in the user's voice. Saves the draft for review — never sends.
argument-hint: [which email, e.g. "reply to Tom about the Q3 quote"]
---

# Draft a reply

Draft a reply to a specific email in the user's own voice. Work in their workspace.

## Find the email
- If the user described it (sender / subject / topic), locate it via the Microsoft 365 connector.
- If M365 isn't connected, ask them to paste the email they want to reply to.

## Read for context
- `context/voice-profile.md` — match this style closely (use the `voice-writing` skill).
- The relevant `accounts/<client>/notes.md` — history, open items, tone for that client.
- `templates/email-reply.md` — the reply structure.

## Draft
- Write the reply in the user's voice: acknowledge, give the answer or action, keep it brief, and
  **commit to a clear next step with a timeframe**.
- Offer 2–3 quick variants on request (shorter / firmer / warmer).

## Save & record
- Save to `drafts/YYYY-MM-DD-reply-<who>-<topic>.md`.
- Append a one-line note to the relevant `accounts/<client>/notes.md` (what was replied to / the
  next step).
- Show the draft in chat and remind the user: **review and send it from Outlook — I can't send.**
