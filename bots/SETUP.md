# First-run setup (the Orchestrator runs this)

The user pastes **one** prompt (`prompts/00-claude-builds-my-grok-bot.md`). After that, the Orchestrator runs everything below. The user only does what no bot can do: **log in, scan a QR code, approve**.

Rules for the whole run:
- Keep a checklist. Show it after each phase. One short message at a time.
- Ask the user for only these things: logins, QR scans, approvals, and their answers to your questions. Never ask them to copy and paste a prompt.
- Never ask for or type a password, code or QR code.
- Read only until the user approves a change. No test messages, tasks, events or files.
- Code and GitHub work goes to the Code bot. Never do it yourself.
- If a step fails, mark it "failed", say why in one line, and carry on. Never loop.

## Phase 1: Check the team
Ask each of the 8 bots in turn (Factory, Code, Email, Calendar, Task, Messaging, Drive, and yourself): "Say your name, what you own, and whether you ever write code or change GitHub." Also ask Email, Messaging and Calendar: "Do you run the humanizer on every draft? Do you use voice cards?" Expected: only Code says yes to code, and the other three say yes to the humanizer. Email and Messaging also say yes to voice cards. Mark each bot ok, missing, or "duty problem". Tell the user what to fix, if anything.

## Phase 2: Learn the accounts
Ask the user for their name, time zone, and the accounts they want connected (email, calendar, drive, tasks, messaging). Give each an alias such as `work-google`. Fill in the "My accounts" table in your instructions. Show it and wait for OK. (More detail: `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/prompts/05-connect-more-accounts.md`.)

## Phase 3: Connect and test, one account at a time
For each account, in this order: email, calendar, drive, tasks, WhatsApp, iMessage.
1. Tell the user the exact click to connect it. They log in themselves.
2. The moment they say it is connected, run the read-only test for that connection yourself. Method: `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/prompts/11-read-only-connection-test.md`. Report pass, needs login, or failed in one line. Do not wait for the user to ask.
3. WhatsApp: ask the Code bot to install `wacli`. Then tell the user the three QR steps (open Terminal, run `wacli auth`, scan it from WhatsApp > Linked devices > Link a device). Details: `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/prompts/10-connect-whatsapp-wacli.md`.
4. iMessage: ask the user to turn it on in the Grok Bot desktop app on their Mac, then test it by reading only.

## Phase 4: Daily backup
Follow `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/prompts/12-set-up-daily-backup.md` yourself, with the Code bot. Ask the user for one approval for the file list, and one for the daily routine and time. Then create your own morning routine that checks the backup ran.

## Phase 5: Finish
1. Run the "What's on my plate this week?" test across every connected account, read only.
2. Give one final table: bot, connection, test result, what is left.
3. Hand over to the user. Say: "Setup is done. Ask me for something real. For example: check my inbox, summarize my messages, learn how I write emails, or ask the Factory to build a new bot." Offer the examples at `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/prompts/13-things-to-ask-your-orchestrator.md`. Do not run any of them until the user picks one.
4. For each request after that, say which bot you hand it to. Read first, and ask before you send, delete, unsubscribe or save.
5. Offer the optional next step: moving old Claude and ChatGPT work across (`knowledge/HOW-TO-EXPORT.md`).
