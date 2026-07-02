# AI Account Manager Assistant (Claude plugin)

A personal AI assistant for account managers. It runs inside the **Claude desktop app** (no
terminal) and helps with the recurring work of the role: triaging Outlook, drafting replies in your
own voice, chasing quotes and purchase orders, filing documents, keeping per-account notes, and
building your monthly report.

One rule shapes everything: **it prepares, you approve.** It drafts, files, tracks, and tees things
up. You send, book, and decide. Nothing is sent or written to your systems automatically.

> This repo is the **engine** (a Claude plugin: commands, skills, templates).
> Your own data lives in a **workspace** the plugin generates locally when you run `/setup`. That
> workspace is git-ignored and never committed here.

## Install

See **[INSTALL.md](INSTALL.md)** — install the Claude desktop app, add this marketplace, install the
plugin, run `/setup`.

## What's in the box

```
commands/   setup · edit-context · connect-outlook · map-workflow ·
            morning-briefing · draft-reply · draft-forward · overdue-quotes ·
            quote-request · file-quote · prep-calendar · meeting-actions · monthly-report
skills/     voice-writing · report-builder
templates/  email-reply · quote-request · monthly-report · account-notes
docs/       IT-Approval-Email · Scope-Note
```

## How it works

1. **`/setup`** interviews you and scaffolds your workspace (`CLAUDE.md`, `context/`, `accounts/`,
   `trackers/`, `drafts/`, `reports/`, `briefings/`).
2. **`/connect-outlook`** guides you to add the Microsoft 365 connector and verifies it.
3. Day-to-day commands read your workspace plus the connector and **write drafts, reports, and files
   you review**. Nothing is ever sent for you.

## Known limits

- The Microsoft 365 connector is **read-only** and doesn't read attachments — the assistant drafts;
  you send and book, and you drop documents in for filing.
- Connecting corporate Microsoft 365 needs your employer's IT to grant consent once.
- No live meeting note-taking from a call, no auto-send, no deep CRM in this version.
