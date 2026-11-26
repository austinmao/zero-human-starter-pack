# 11: Read-only test of every connection

**Normally you do not paste this.** The Orchestrator runs it for you during first-run setup (`bots/SETUP.md`). It is here so you can re-run it by hand.

Run this after you connect accounts (step 5 of the guide), and again any time you add one. It only reads. It sends, creates, edits and deletes **nothing**, so it is safe to run on live accounts.

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
8. Only if the Sales or Customer care bot exists, contact list or CRM: the number of contacts, and the names of the 3 newest. No notes or messages.
9. Only if the Analytics bot exists, web analytics: yesterday's visit count. Nothing else.
10. Only if the Social bot exists, each social account: the first line and date of my 3 newest posts.
11. Only if the Finance prep bot exists, accounting tool: the number of open invoices and the number of open bills. No amounts, no names.
12. Only if the Meetings bot exists, video meeting account: the title and time of the next 3 meetings.
13. Only if the Note taker, Sales or Client prep bot exists, notes tool: the titles and dates of the 3 newest notes. No note text.
14. Only if the Newsletter bot exists, email platform: the names of my lists and how many people are on each. No addresses.

After the connection tests, for each bot that exists, also do one allowed read and one read it should be refused (an app that is not in its table in `bots/CONNECTORS.md`). The refusal must come from the platform. Never do a write as a test.

Then give me one table: connection, alias, result (pass, needs login, failed, not connected), and one line on what you saw.
For anything that is not "pass", tell me the one thing I should do next. If you could not check something, say "could not check". Do not guess.
```

What a good result looks like: every connection you made shows **pass**, and you can see the account alias on each line. Connections you have not made yet show **not connected**. That is fine.
