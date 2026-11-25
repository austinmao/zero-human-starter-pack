# 14: Add more bots (optional packs)

**Optional.** Do this after the core 8 are set up and working (prompt 00 and your Orchestrator's first run). It adds bots for more of your life and work, one pack at a time:

- **Pack A, Growth (12 bots):** Marketing, Sales, Social, SEO, Analytics, Brand, Writing, PR, Outreach, Presentation, Video, Newsletter.
- **Pack B, Operations (9 bots):** Customer care, Finance prep, Legal admin, HR, Records, Events, Meetings, Note taker, Client prep.
- **Pack C, Life (9 bots):** Friend, Journal, Workout, Learn, Selling, Investment, Health, Home errands, Trip planner.

Add only the packs you will use. The core 8 plus all three packs is 38 bots. Grok Bot may limit how many bots one account can have (a third party reports 50, which xAI has not confirmed). If it refuses, the agent stops and tells you.

**Pack C is private.** Those bots keep what they know in their own memory and in a `private/` folder on the shared computer. It is never saved to GitHub and never in the daily backup. Because every bot shares one computer, this is a rule the bots follow, not a lock. Journal, Health and Investment (and Friend and Workout) also say a plain-language disclaimer the first time they run: they are not therapy, medical advice or financial advice.

Open Grok Bot in a tab and log in yourself. Use a browser agent (Claude in Chrome, ChatGPT agent mode or similar). Paste the prompt below.

```
Add one optional pack of bots to my Grok Bot using my browser. Work from a checklist, not from memory.

First ask me three things, then carry on: which pack (A Growth, B Operations or C Life), my name, and the name of my default bot (the Orchestrator).

Rules:
- I am already logged in. Never ask for or type a password. If a login or code is needed, stop and tell me.
- Do not click Buy, Subscribe, Upgrade, Send, Delete or Share. The one exception is Step 5: you may send one message to my default bot.
- Never overwrite or delete a bot that already exists. If a bot with the same name exists, skip it and say so. The only exception is the Code bot in Step 2, and only after my OK.
- If something looks different from what you expect, stop and describe it.
- Keep your replies short. Never paste a bot's full text into the chat more than once.

Step 1. Open https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/TASKS.md
Under "Optional packs", copy the table for my pack as your checklist. After every change, show me the updated checklist.

Step 2 (Pack C only). The Code bot needs a newer rule before any private bot exists. Fetch bots/code/INSTRUCTIONS.md, replace [YOUR NAME] and [ORCHESTRATOR NAME], and tell me in one line what is new compared with the saved Code bot (it now never backs up private folders). Ask: "OK to update the Code bot?" and wait. After my OK, replace the Code bot's instructions with the new text and save. Touch no other existing bot.

Step 3. Prepare every bot in the pack (do not touch Grok Bot yet).
For each bot, fetch its INSTRUCTIONS.md from the address in TASKS.md and replace [YOUR NAME] and [ORCHESTRATOR NAME]. Change nothing else.
If you can run sub-agents or extra tabs, use one per bot for this step only.
Mark each bot "drafted". Show me a table: bot, first line of its text, and any placeholder left. Ask: "OK to create?" and wait.

Step 4. After my OK, create the bots in Grok Bot one at a time, in the order in the table. Never in parallel.
For each: create the bot, paste its filled text into the instructions, save, mark it "created".
If a bot fails, mark it "failed", say why in one line, and carry on with the next.
If Grok Bot refuses to create more bots, stop, tell me how many were created, and ask me what to do.

Step 5. Show the final checklist. Then open my default bot's chat and send it exactly this one message: "Pack [A, B or C] is in. Run Phase 6." Tell me it was sent. Do nothing more.
```

What a good result looks like: every bot in the pack shows "created", and your Orchestrator answers with the connections it needs (Phase 6 in `bots/SETUP.md`). Run `prompts/09-check-my-bots.md` in a new chat for an independent check.
