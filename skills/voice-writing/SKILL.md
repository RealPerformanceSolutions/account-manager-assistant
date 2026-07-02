---
name: voice-writing
description: Write emails and messages in the user's own voice, and distil a reusable style guide from their sample emails. Use whenever drafting on the user's behalf (replies, chases, quote requests) or during /setup and /edit-context when they paste writing samples.
---

# Voice writing

This skill has two modes.

## Mode A — Distil a style guide (during setup / edit-context)

Given 3–5 emails the user has **sent**:

1. Analyse: tone and formality; greeting and sign-off; typical length; sentence structure; how they
   open and close; recurring phrasings; vocabulary; punctuation habits; British vs US spelling.
2. Capture clear **do's** and **avoid's** (e.g. "avoids exclamation marks", "no long preambles").

**Privacy (important):** summarise **style only**. Do **not** copy third-party personal data —
strip names, customer details, addresses, and figures. Use `<first name>` style placeholders in any
example phrasings. Never store the raw sample emails.

Write the result to `context/voice-profile.md` with these sections:
`Tone · Greeting · Sign-off · Length · Structure · Does · Avoids · Phrasings`.
Keep it short enough to load as context on every draft.

## Mode B — Draft in the user's voice (day to day)

When drafting a reply, chase, or message:

1. Read `context/voice-profile.md` and follow it closely.
2. Lead with the answer or action; keep it brief; commit to a clear next step with a timeframe.
3. Match their greeting, sign-off, sentence length, and phrasings.
4. Never send — drafts are always saved for the user to review and send.
