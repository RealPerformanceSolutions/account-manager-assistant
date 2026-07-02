---
description: Turn a meeting transcript into a summary, action points, and draft follow-up emails. Saves drafts for review — never sends.
argument-hint: [which meeting / account, if known]
---

# Meeting actions

Take a meeting transcript and pull out what matters: the decisions, the action points, and the
follow-ups. Then draft what needs sending. Work in their workspace.

## Get the transcript
Take it from whichever source the user has:
- A meeting recorder they use (e.g. Fathom, Zoom, Descript) if that connector is available — offer
  to pull the most recent meeting.
- A file they've dropped in `to-file/`, or a transcript they paste in.

If none is available, ask them to paste or drop the transcript.

## Work out the context
- Which account/project is this meeting about? Read the relevant `accounts/<client>/notes.md` for
  background. If it's unclear, ask.
- If the user has mapped a meeting follow-up process (`context/workflows/meeting-followup.md`),
  follow it.

## Pull out
1. **Decisions** — what was agreed.
2. **Action points** — each with an owner and a due date where the transcript gives one. Separate
   the user's own actions from other people's.
3. **Follow-ups** — anything the user committed to send or do.
4. **Quote/PO items** — if a quote, PO, or chase came up, note it for the tracker.

Only use what's actually in the transcript. Don't invent actions or attribute things that weren't
said.

## Save and draft
- Write a meeting note to `accounts/<client>/meetings/YYYY-MM-DD-<topic>.md`: attendees, decisions,
  actions (with owners/dates), and follow-ups.
- Add the user's own actions to the top of the relevant account's `notes.md` so they surface in the
  next `/morning-briefing`.
- If anything is chaseable (a PO to raise, a quote to send), add it to `trackers/quotes.csv` with a
  `next_chase_date`.
- Draft the follow-up emails in the user's voice (via `voice-writing`) and save them to `drafts/`.

## Confirm
- Show the summary and the list of actions.
- Point to the drafts waiting in `drafts/` and remind the user to review and send them. Never send.
