# Start here

There are three parts. Do Part 1 first. Parts 2 and 3 are optional. You can use the interactive guide (one page, three tabs) or this file. Tick each step off as you go.

## Part 1: Set up your team (about 90 minutes, mostly watching)

You paste one prompt. Your first bot becomes your **Orchestrator**. It builds a **Factory** bot, and the Factory builds the rest. You only log in, scan a QR code and approve. You do not need GitHub until the last step.

### 1. Sign up for Grok (5 min)
Create your account at grok.com.

### 2. Pay for it (5 min)
Grok Bot is included in the Premium, Super and Ultra plans on The X Subscription. The free plan and Plus do not include it. Start on Premium and move to Super when you use it every day. Check the plans page before you pay: https://grok.com/help/grok-bot/plans. Setup uses real usage, so a free trial credit may run out. Check your usage at grok.com/dashboard.

### 3. Install the Grok Bot desktop app and sign in (10 min)
There is no browser version. Download the app from x.ai/bot (Mac, Windows or Linux), choose **Sign in** and finish in your browser. The app opens a chat with your first bot, named "Grok Bot".

### 4. Name your bot and paste the prompt (30 min, mostly watching)
Click your bot's name at the top of its chat and rename it (for example "Chief"). Then open `prompts/00-paste-into-your-first-bot.md` and paste the prompt into that chat. It asks your name, makes your bot the Orchestrator, and has it create the Factory. The Factory builds Code first, then Email, Calendar, Task, Messaging and Drive. It shows you one list and asks "OK to create all six?" once.

### 5. While it works: get the phone app
Install Grok Bot from the App Store (iOS 18 or later) or Google Play (Android 9 or later). Sign in with the same account.

### 6. Answer your Orchestrator (30 min)
From here your Orchestrator runs everything (`bots/SETUP.md`). It checks the team, asks which accounts you use, and tells you where to click to connect each one. **You only log in, scan a QR code and approve.** It tests each connection read only, right after you connect it. Then it shows you which apps each bot may use, read only or read and write (`bots/CONNECTORS.md`), and you set those limits per bot in the platform's connector settings. That step matters: the limit has to be in the platform, not just in the bot's text. For WhatsApp you scan one QR code: WhatsApp > Linked devices > Link a device. The code appears in the bots' computer view.

### 7. Ask it for something real (10 min)
The Orchestrator ends with a read-only check: **What's on my plate this week?** Then it is your turn. Pick any line from `prompts/13-things-to-ask-your-orchestrator.md` and paste it into your Orchestrator's chat.

**Where do I talk?** To your Orchestrator, or to any bot directly (type @ and its name). Both work. Your Orchestrator is the best place to start, because it keeps the whole picture and hands each job to the right bot. Talking to a bot directly is like checking the details yourself: fine when you want them. That bot tells your Orchestrator what you asked.

### 8. Back up to GitHub (10 min, last)
Your Orchestrator offers this last. Create a free account at github.com/signup, connect GitHub in the Code bot's chat, and the Code bot creates a private repo called `my-agents` and sets up a daily backup (`prompts/12-set-up-daily-backup.md`). If GitHub blocks your network, skip it and do it later. Your bots work without it.

## Part 2: Bring your old Claude and ChatGPT knowledge (optional, 2 to 3 hours)
**Start the clock today:** request your Claude and ChatGPT exports before anything else. ChatGPT can take up to 7 days, and OpenAI is retiring custom GPTs on 11 December 2026. Steps and sources are in `knowledge/HOW-TO-EXPORT.md`. This part needs your private GitHub repo from Part 1 step 8.

1. **List what you have.** `prompts/06-inventory-my-projects.md`. Mark the 10 to 15 projects that matter as tier 1. This one needs a browser agent (Claude in Chrome), because it reads your project names in claude.ai and chatgpt.com.
2. **Copy your skills.** `prompts/08-copy-my-skills.md`.
3. **Make handoff notes.** `prompts/07-distill-my-exports.md`, run in Claude on your computer. Raw exports stay on your computer.
4. **Fill the gaps for tier 1 projects.** Run `prompts/03-knowledge-dump-chatgpt.md` or `prompts/03-knowledge-dump-claude.md` inside the project.
5. **Save it.** `prompts/04-push-dump-to-github.md`. Only handoff notes and skills go to GitHub, never the raw exports.

## Part 3: Add more bots (optional, 20 minutes per pack)
When the core 8 work, add more, one pack at a time: Growth (marketing, sales, social and more), Operations (customer care, finance prep, legal admin and more) and Life (friend, journal, workout, health and more). Paste `prompts/14-add-more-bots.md` into your Orchestrator and pick a pack. The Factory shows you the list and asks "OK to create all of them?" once. Life bots keep their data private and never back it up to GitHub.

## Already have a team from an older version?
Paste the block in `GROKBOT-UPDATE.md` into your Orchestrator. It audits what each bot can use, shows you a table, sets per-bot limits with you, fixes the wiring and runs a routing test and an access test. It asks you before it changes any access.

## If something goes wrong
Paste the error message into Claude or ChatGPT together with the step you were on. Nothing in this pack is permanent, so you can always start a step again.
