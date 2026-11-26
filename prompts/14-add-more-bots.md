# 14: Add more bots (optional packs)

**Optional.** Do this after the core 8 are set up and working (prompt 00 and your Orchestrator's first run). It adds bots for more of your life and work, one pack at a time:

- **Pack A, Growth (12 bots):** Marketing, Sales, Social, SEO, Analytics, Brand, Writing, PR, Outreach, Presentation, Video, Newsletter.
- **Pack B, Operations (9 bots):** Customer care, Finance prep, Legal admin, HR, Records, Events, Meetings, Note taker, Client prep.
- **Pack C, Life (9 bots):** Friend, Journal, Workout, Learn, Selling, Investment, Health, Home errands, Trip planner.

Add only the packs you will use. The core 8 plus all three packs is 38 bots. Grok Bot may limit how many bots one account can have (a third party reports 50, which xAI has not confirmed). If it refuses, the Factory stops and tells you.

**Pack C is private.** Those bots keep what they know in their own memory and in a `private/` folder on the shared computer. It is never saved to GitHub and never in the daily backup. Because every bot shares one computer, this is a rule the bots follow, not a lock. Journal, Health and Investment (and Friend and Workout) also say a plain-language disclaimer the first time they run: they are not therapy, medical advice or financial advice.

Open your Orchestrator's chat in Grok Bot and paste the prompt below. There is no browser agent. Your Orchestrator hands the building to the Factory.

```
Add one optional pack of bots to my team. Work from a checklist, not from memory. You hand the building to the Factory. Do not build bots yourself.

First ask me which pack: A Growth, B Operations or C Life.

Rules:
- Never ask for or type a password. If a login or code is needed, tell me to do it myself.
- Do not send, pay, delete or share anything.
- Never overwrite or delete a bot that already exists. If a bot with the same name exists, skip it and say so. The one exception is the Code bot in Step 2, and only after my OK.
- If something looks different from what you expect, stop and describe it.
- Keep replies short. Show the checklist after every change.

Step 1. Read https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/TASKS.md
Under "Optional packs", copy the table for my pack as your checklist.

Step 2 (Pack C only). The Code bot needs a newer rule before any private bot exists. Ask the Factory to read https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/code/INSTRUCTIONS.md, fill in my name and your name, and tell me in one line what is new compared with the Code bot's current rules (it now never backs up private folders). Ask me: "OK to update the Code bot?" and wait. After my OK, the Factory sends the Code bot the new text and asks it to remember it as its lasting rules, replacing the old. Touch no other existing bot.

Step 3. Ask the Factory to prepare every bot in the pack: for each, fetch its INSTRUCTIONS.md from the address pattern in TASKS.md, fill in my name and your name, and change nothing else. The Factory shows me one table: bot, first line of its text, any placeholder left. Then ask me: "OK to create all of them?" and wait.

Step 4. After my OK, the Factory creates the bots one at a time, in the order in the table, never in parallel. For each: create it, send it its filled-in text as its first message, ask it to remember it as its lasting job and rules, mark it "created". If one fails, mark it "failed", say why in one line, and carry on. If Grok Bot refuses to create more bots, stop, tell me how many exist, and ask me what to do.

Step 5. Show me the final checklist. Then run Phase 6 of https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/SETUP.md for this pack.
```

What a good result looks like: every bot in the pack shows "created", and your Orchestrator asks which connections you want (Phase 6 in `bots/SETUP.md`). For an independent check, run `prompts/09-check-my-bots.md` in a new chat. It needs a browser agent, so skip it if you do not use one.
