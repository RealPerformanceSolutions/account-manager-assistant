---
description: Produce today's morning briefing — what needs attention across inbox, calendar, quotes, and accounts.
argument-hint: (no arguments)
---

# Morning briefing

Produce a concise, prioritised briefing for the user's day. Work in their workspace.

## Read first
- `CLAUDE.md` and `context/preferences.md` (hours, home base, briefing time, overdue threshold).
- `context/profile.md` and `accounts/` notes (including each account's last-contact date).
- `trackers/quotes.csv`.
- If Microsoft 365 is connected (check `CLAUDE.md` Connections, or try a read): the user's **inbox
  since the last briefing** and **today + this week's calendar**. If it's not connected, say so and
  ask them to paste anything urgent, then continue with what you have.

## Do
1. **Triage new email** into: needs a reply · waiting on the user · a customer waiting for an update ·
   FYI. Keep it tight — only what matters.
2. **Scan the calendar** — where is the user today, and what gaps exist.
3. **Flag overdue quotes and POs** — anything in `quotes.csv` past its `next_chase_date` or the
   overdue threshold: quotes awaiting a decision, and approved quotes still awaiting a PO (follow
   `context/workflows/quote-to-po.md` if present). Show the value and who needs chasing.
4. **Surface quiet accounts** — accounts not contacted in a while (from `accounts/*/notes.md`).
5. **Suggest one travel-efficient visit** if the user is near a client with a stale last-visit —
   phrase it as a suggestion. Offer to prepare a calendar entry (`/prep-calendar`) if they want it.
6. **Pre-draft the top 1–3 urgent replies** in the user's voice (via the `voice-writing` skill) and
   save them to `drafts/` — mention they're waiting there for review. If anything is really a
   service/fault request to pass on, offer to draft a forward (`/draft-forward`).

## Write
- Save the briefing to `briefings/YYYY-MM-DD-briefing.md`.
- Append any relevant follow-ups to the affected `accounts/<client>/notes.md`.
- Show the briefing in chat. Lead with the 3–5 highest-priority actions.

## Rules
- Never send anything. Drafts go to `drafts/` for the user to review and send.
- Don't invent email or calendar content — only use what you actually read (or what the user pasted).
