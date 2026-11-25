# 11: Read-only test of every connection

**Normally you do not paste this.** The Orchestrator runs it for you during first-run setup (`bots/SETUP.md`). It is here so you can re-run it by hand.

Run this after you connect accounts (step 6), and again any time you add one. It only reads. It sends, creates, edits and deletes **nothing**, so it is safe to run on live accounts.

Paste it to the Orchestrator.

```
Run a read-only test of every connection I have made. You are only looking.

Hard rules for this test:
- Do not send, create, edit, move, delete, share or save anything. No test messages, no test tasks, no test events, no test files, no GitHub commits.
- Never ask for or type a password, code or QR code. If a login is needed, say "needs login" and move on.
- Keep each result to one line. Do not show message bodies, file contents or email text. Show only names, subjects, dates and counts.

Ask each bot to run its own check and report back:
1. Email: list the sender and subject of the 3 newest messages in each account.
2. Calendar: list the next 3 events in each calendar, with the alias.
3. Task: list up to 3 open tasks.
4. Drive: list the names of 5 recently changed files in each drive.
5. Messaging, WhatsApp: run `wacli doctor` and `wacli --read-only --json messages list --limit 3`. Show only the chat names and times.
6. Messaging, iMessage: list the names and times of the 3 newest conversations. If the Mac is asleep or iMessage is not turned on in the desktop app, say so.
7. Code: read the list of files in my private my-agents repo. Do not write anything.

Then give me one table: connection, alias, result (pass, needs login, failed, not connected), and one line on what you saw.
For anything that is not "pass", tell me the one thing I should do next. If you could not check something, say "could not check". Do not guess.
```

What a good result looks like: every connection you made shows **pass**, and you can see the account alias on each line. Connections you have not made yet show **not connected**. That is fine.
