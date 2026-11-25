# Start here

Do the steps in order. Tick each one off as you go. Total time: about 90 minutes the first time.

## 1. Get Grok Bot (10 min)
Grok Bot comes with an X Premium or Super subscription. Start on Premium. Move to Super once you use it every day. You pay for this yourself.

Then install the apps and sign in to both with the same account:
1. **Desktop app** (Mac, Windows or Linux): download it from the Grok Bot page at cursor.com/dashboard/bot.
2. **iPhone app** (iOS 18 or later): search "Grok Bot" in the App Store.
3. **On a Mac, turn on iMessage** in the desktop app (look for iMessage under **Connect apps** in the sidebar). iMessage works only on a Mac, and only while the Mac is on. Not confirmed against a real account: if you cannot find it, ask your bot where it is.

## 2. Set up GitHub (10 min)
1. Create a free account at github.com.
2. Open this repo and click **Use this template** > **Create a new repository**.
3. Name it `my-agents` and choose **Private**.

This private repo is the backup of everything you build.

## 3. Let a browser agent build all 8 bots (30 min)
Open Grok Bot in a tab and log in yourself. Use Claude in Chrome, ChatGPT agent mode or a similar browser agent. Paste `prompts/00-claude-builds-my-grok-bot.md`. It works from a task list (`bots/TASKS.md`), prepares all 8 bots, asks for one OK, then creates them one at a time.

Then open a **new chat** and paste `prompts/09-check-my-bots.md`. It only looks, and gives you a table: does each bot exist, does it match, and is each bot doing only its own job. Only the Code bot writes code or changes GitHub.

## 4. If the agent cannot create bots: bootstrap from inside Grok Bot (10 min)
Paste the text from `bots/orchestrator/INSTRUCTIONS.md` into your default bot by hand. Then paste `prompts/01-orchestrator-bootstrap.md` into it.

## 5. If the agent cannot create bots: let the Factory do it (15 min)
Create a bot called Factory with `bots/factory/INSTRUCTIONS.md`, then paste `prompts/02-factory-builds-the-other-bots.md`. Finish with `prompts/09-check-my-bots.md`.

## 6. Connect your accounts (20 min)
Connect email, calendar, drive, tasks and messaging. You log in yourself every time. To add a second or third account, use `prompts/05-connect-more-accounts.md`.

**WhatsApp:** follow `prompts/10-connect-whatsapp-wacli.md`. You scan a QR code from WhatsApp's Linked devices screen. The Messaging bot reads WhatsApp with `wacli` and iMessage with the desktop app.

**Test it, read only:** run `prompts/11-read-only-connection-test.md`. It sends, creates and deletes nothing.

**Back it up daily:** run `prompts/12-set-up-daily-backup.md`. The Code bot saves your agents to GitHub every day, and the Orchestrator checks each morning that it happened.

## 7. Move your old knowledge across (optional, 2 to 3 hours in total)
**Start the clock today:** request your Claude and ChatGPT exports before anything else. ChatGPT can take up to 7 days, and OpenAI is retiring custom GPTs on 11 December 2026. Steps and sources are in `knowledge/HOW-TO-EXPORT.md`.

Then, once the exports arrive:
1. **List what you have.** `prompts/06-inventory-my-projects.md`. Mark the 10 to 15 projects that matter as tier 1.
2. **Copy your skills.** `prompts/08-copy-my-skills.md`.
3. **Make handoff notes.** `prompts/07-distill-my-exports.md`, run in Claude on your computer. Raw exports stay on your computer.
4. **Fill the gaps for tier 1 projects.** Run `prompts/03-knowledge-dump-chatgpt.md` or `prompts/03-knowledge-dump-claude.md` inside the project, and copy its instructions by hand.
5. **Save it.** `prompts/04-push-dump-to-github.md`. Only handoff notes and skills go to GitHub, never the raw exports.

## 8. First test (2 min)
Ask the Orchestrator: **What's on my plate this week?** It should check every connected calendar, inbox and task list and tell you which account each item came from.

## If something goes wrong
Paste the error message into Claude or ChatGPT together with the step you were on. Nothing in this pack is permanent, so you can always start a step again.
