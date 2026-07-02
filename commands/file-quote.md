---
description: File dropped PDFs (quotes, drawings, POs) into the right account/project folder and log them.
argument-hint: [account or project, if you know it]
---

# File quote documents

Sort loose documents into the right place under `accounts/<account>/projects/<project>/` and note
them. Work in their workspace.

> Why drop-and-file: the Outlook connector can read email text but **does not hand over
> attachments** — it drops them. So the user saves the attachment (or drags it into the workspace)
> and this command files it. Getting the file into the folder is their one manual step; the rest is
> automatic.

## Find the files
- Look in the `to-file/` folder for anything new. If it's empty, ask the user to drop the PDFs there
  (or point you at a file) and to include the customer/project in the filename or tell you.

## Work out where each belongs
For each file:
1. Read it (and, if Outlook is connected, search for the related quote email by customer/keywords)
   to identify the **account** and the **project** (e.g. "Acme Ltd — South London CCTV upgrade").
2. If you can't tell confidently, ask the user rather than guessing.

## File and log
- Create `accounts/<account-slug>/projects/<project-slug>/` if it doesn't exist.
- Move the file there (keep the original name; tidy it only if it's meaningless).
- Add a line to that project (a short `notes.md` in the project folder, and a pointer in the
  account's main `notes.md`): what the document is, its date, and the quote/PO it relates to.

## Confirm
- Show the user exactly what you filed and where. Never delete anything you can't confidently place —
  leave it in `to-file/` and say so.
