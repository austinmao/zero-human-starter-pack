# Start here

Do the steps in order. Tick each one off as you go. Total time: about 90 minutes the first time. You paste one prompt. The bots do the rest.

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

## 3. Paste one prompt (30 min, mostly watching)
Open Grok Bot in a tab and log in yourself. Use Claude in Chrome, ChatGPT agent mode or a similar browser agent. Paste `prompts/00-claude-builds-my-grok-bot.md`.

The agent asks your name and what to call your default bot. It builds all 8 bots, then sends your default bot the message "Start setup".

## 4. Answer your Orchestrator (30 min)
From here your Orchestrator runs everything (`bots/SETUP.md`). It checks the team, asks which accounts you use, and tells you where to click to connect each one. **You only log in, scan a QR code and approve.** It tests each connection read only, right after you connect it, sets up WhatsApp, and sets up the daily GitHub backup with the Code bot.

For WhatsApp you scan one QR code: WhatsApp > Linked devices > Link a device. The Orchestrator tells you when.

## 5. If the agent cannot create bots in Grok Bot
Paste the text from `bots/orchestrator/INSTRUCTIONS.md` into your default bot by hand, then tell it "Start setup". Or paste `prompts/02-factory-builds-the-other-bots.md` into a Factory bot.

## 6. Ask it for something real (10 min)
The Orchestrator ends setup with a read-only check: **What's on my plate this week?** Then it is your turn. Pick any line from `prompts/13-things-to-ask-your-orchestrator.md` and paste it into your Orchestrator's chat. Examples: check my inbox, find the junk to unsubscribe from, summarize my messages, learn how I write emails and texts, or ask the Factory to build a new bot.

Watch which bot it hands each job to. It should read first and ask before it sends, deletes or saves anything.

## 7. Move your old knowledge across (optional, 2 to 3 hours in total)
**Start the clock today:** request your Claude and ChatGPT exports before anything else. ChatGPT can take up to 7 days, and OpenAI is retiring custom GPTs on 11 December 2026. Steps and sources are in `knowledge/HOW-TO-EXPORT.md`.

Then, once the exports arrive:
1. **List what you have.** `prompts/06-inventory-my-projects.md`. Mark the 10 to 15 projects that matter as tier 1.
2. **Copy your skills.** `prompts/08-copy-my-skills.md`.
3. **Make handoff notes.** `prompts/07-distill-my-exports.md`, run in Claude on your computer. Raw exports stay on your computer.
4. **Fill the gaps for tier 1 projects.** Run `prompts/03-knowledge-dump-chatgpt.md` or `prompts/03-knowledge-dump-claude.md` inside the project, and copy its instructions by hand.
5. **Save it.** `prompts/04-push-dump-to-github.md`. Only handoff notes and skills go to GitHub, never the raw exports.

## 8. Add more bots (optional, 20 minutes per pack)
When the core 8 work, you can add more, one pack at a time: Growth (marketing, sales, social and more), Operations (customer care, finance prep, legal admin and more) and Life (friend, journal, workout, health and more). Paste `prompts/14-add-more-bots.md` into a browser agent and pick a pack. The agent shows you the list and stops at "OK to create?". Life bots keep their data private and never back it up to GitHub.

## If something goes wrong
Paste the error message into Claude or ChatGPT together with the step you were on. Nothing in this pack is permanent, so you can always start a step again.
