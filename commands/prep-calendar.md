---
description: Prepare a calendar entry (a file the user double-clicks to add to Outlook). Never writes to their calendar directly.
argument-hint: [what the event is]
---

# Prepare a calendar entry

The Outlook connector can read the user's calendar but can't add to it. So instead of booking
anything, prepare an event file they open with one click to add it themselves. Work in their
workspace.

## Gather the details
- From the email/request or by asking: title, date, start and end time, location, who's invited, and
  a line of notes.
- If it's a suggested client visit from a briefing, carry over the travel context (e.g. "near
  your Tuesday visit, the next site is 35 mins away").

## Create the file
- Write a standard `.ics` calendar file to `calendar/<YYYY-MM-DD>-<slug>.ics` with those details.
- Also show a plain summary in chat (date, time, where, who).

## Hand over
- Tell the user: open that file and it'll pop into Outlook, then they just hit save. Make clear you
  haven't put anything in their calendar yourself, it's ready for them to accept.
- If there's a scheduling clash you can see in their calendar, flag it before they add it.
