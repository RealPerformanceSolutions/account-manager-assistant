---
description: Revise part of the assistant's setup — profile, accounts, working style, voice, reporting, or quotes location.
argument-hint: [what to change, e.g. "voice" or "add account"]
---

# Edit context

The user wants to change something about how their assistant is set up, without re-running the whole
`/setup`. Work in the current workspace folder.

1. If they named what to change in the argument, go straight to it. Otherwise ask which area:
   **profile · accounts · working style · voice · reporting · quotes location · connections**.
2. Read the relevant file(s) in `context/`, `accounts/`, or `trackers/` and show the current values.
3. Ask for the change, then update the file(s). For **voice**, re-run the `voice-writing` skill on
   fresh pasted samples and rewrite `context/voice-profile.md` (style only — never store client PII).
   For **accounts**, add/rename a folder under `accounts/` and update `accounts/_index.md`.
4. If the change affects the operating brief (name, role, accounts, overdue threshold, connections),
   update `CLAUDE.md` to match.
5. Confirm what changed. Never overwrite without showing the current content first.
