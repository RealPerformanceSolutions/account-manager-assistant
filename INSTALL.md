# Getting started

This assistant helps with the day-to-day of account management: it reads your Outlook, drafts
replies in your voice, chases quotes and POs, files your documents, keeps notes on each account, and
builds your monthly reports.

One thing to know up front: it writes drafts, it doesn't send. You always read what it's written and
click send yourself. Think of it as a fast, organised assistant sitting next to you, not someone
acting on your behalf.

Setting up takes about 15 minutes, and you don't need to be technical.

## 1. Get the Claude app

- Go to **claude.ai/download** and install the app, like any other.
- Open it and sign in. A **Pro or Max plan** is recommended so you have enough capacity for a full
  working day. Your usage sits on your own subscription.

## 2. Add the assistant

1. Click the **+** button near the message box and choose **Plugins**.
2. Choose **Add plugin**, then add the marketplace named:
   ```
   RealPerformanceSolutions/account-manager-assistant
   ```
3. Install **account-manager-assistant** from it.

## 3. Make a folder for it to work in

- Create a new, empty folder somewhere easy to find. Call it something like `My Assistant`.
- Open that folder in the Claude app when it asks which folder you want to work in. This is where the
  assistant keeps your notes, drafts, and reports, all on your own computer.

## 4. Let it set you up

- Type **`/setup`** and press enter. (Or just say "set me up" and it will offer.)
- It asks about your role, your accounts and roughly where they are, how you like to work, and your
  email style.
- Have a couple of things ready to paste or upload: **3 to 5 emails you've recently sent** (so it
  learns your voice) and **a recent monthly report** (so it copies your format).
- Want to change something later? Run **`/edit-context`**.

## 5. Connect your email (Outlook)

- Type **`/connect-outlook`** and follow the steps.
- Your company's IT may need to approve this once before it works. If so, there's a ready-made email
  in `docs/IT-Approval-Email.md` you can forward to them.
- The assistant can **read your email and write drafts**, but it **cannot send** — you always review
  and click send.

## 6. Use it

- Each morning, type **`/morning-briefing`** to see what needs your attention.
- Other commands: `/draft-reply`, `/draft-forward`, `/overdue-quotes`, `/quote-request`,
  `/file-quote`, `/prep-calendar`, `/meeting-actions`, `/monthly-report`.
- Got a process with lots of steps? Run **`/map-workflow`** and it'll learn to work your way.

## Getting updates

When there's an improvement, open **Plugins**, refresh the marketplace, and choose **Update**. Your
own files and data stay exactly as they are.
