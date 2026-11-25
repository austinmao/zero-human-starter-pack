# Start here

Do the steps in order. Tick each one off as you go. Total time: about 90 minutes the first time.

## 1. Get Grok Bot (10 min)
Grok Bot comes with an X Premium or Super subscription. Start on Premium. Move to Super once you use it every day. You pay for this yourself.

## 2. Set up GitHub (10 min)
1. Create a free account at github.com.
2. Open this repo and click **Use this template** > **Create a new repository**.
3. Name it `my-agents` and choose **Private**.

This private repo is the backup of everything you build.

## 3. Let Claude set up the Orchestrator for you (15 min)
Install Claude in Chrome. Open `prompts/00-claude-builds-my-grok-bot.md`, paste it into Claude, and watch it fill in the Orchestrator for you. If that does not work, paste `bots/orchestrator/INSTRUCTIONS.md` into Grok Bot by hand.

## 4. Bootstrap the Orchestrator (10 min)
Paste `prompts/01-orchestrator-bootstrap.md` into your Orchestrator.

## 5. Let the Factory build the other bots (15 min)
Paste `prompts/02-factory-builds-the-other-bots.md`. The Factory creates Code, Email, Calendar, Task, Messaging and Drive.

## 6. Connect your accounts (20 min)
Connect email, calendar, drive, tasks and messaging. You log in yourself every time. To add a second or third account, use `prompts/05-connect-more-accounts.md`.

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
