---
description: Guide the user to connect Microsoft 365 (Outlook/Calendar) in Claude Desktop, then verify it with a test read.
argument-hint: (no arguments)
---

# Connect Outlook (Microsoft 365)

Help the user connect the **Microsoft 365 connector** so the assistant can read their Outlook email
and calendar. Be patient and non-technical.

## 1. Detect
First check whether it's already connected: try a **minimal read** (e.g. list the single most recent
email or today's calendar). 
- If it succeeds → tell them it's already connected, show the concrete proof ("I can see your most
  recent email, from …"), update the Connections note in `CLAUDE.md`, and stop here.
- If it fails or the tool isn't available → it's not connected; continue.

## 2. Guide
Walk them through it, one step at a time:
1. Open **Settings → Connectors** in the Claude desktop app.
2. Find **Microsoft 365** and click **Connect**.
3. Sign in with their **work** Microsoft account and accept the requested permissions.
4. Come back and say **"done"**.

Make the boundary explicit: *"I can't click through the sign-in for you — that's your login. Once
you've connected, tell me and I'll verify it."*

## 3. Handle the company-IT case
If sign-in is blocked, or they see a message about needing an administrator, explain plainly:
Microsoft 365 is managed by their company, so an IT administrator (a "Microsoft Entra Global Admin")
has to approve Claude's connector **once** for the whole organisation. Give them a short message they
can forward to IT, e.g.:

> "I'd like to use Anthropic's Claude Microsoft 365 connector to help me read and draft email. It
> needs a one-time admin consent in Microsoft Entra. Setup guide:
> https://support.claude.com/en/articles/12542951-set-up-the-microsoft-365-connector
> It's read-only (no sending/changing). Could you approve it, or let me know the process?"

Tell them that until IT approves, the assistant still works — they can paste emails in manually, and
everything else (drafting, reports, quote tracking) runs as normal.

## 4. Verify
Once they say it's connected, run the minimal read again. Only confirm success **after** a real
read works, and show concrete proof. Then remind them of the key limit:

> "Connected. I can now read your email and calendar and draft for you — but I can't send or book.
> You'll always review and click send yourself."

## 5. Record
Update the **Connections** section of `CLAUDE.md` to reflect the status (connected / awaiting IT /
not connected) so the other commands know whether to read live or ask the user to paste.
