# 09: Check that all your bots are done

**Optional.** The Orchestrator already does a quick check of its team during setup. Use this for a second, independent check. Run it in a **new chat** with a browser agent (Claude in Chrome or ChatGPT agent mode), after setup. If you do not use a browser agent, skip this: your Orchestrator already checked the team in Phase 1. It only looks. It changes nothing. A fresh chat matters: the agent that built the bots tends to say "done" about its own work.

Open Grok Bot in a tab and log in yourself first.

```
Check my Grok Bot bots: the core 8, and any optional pack bots that exist. You are only looking. Do not create, edit, save, send or delete anything.

Rules:
- I am already logged in. Never ask for or type a password.
- Keep your replies short.

Step 1. Open https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/TASKS.md
Copy the first table (the core 8) as your checklist. Then, under "Optional packs", add every row whose bot already exists in Grok Bot. Skip the packs I have not added.

Step 2. For each bot on the checklist, in order:
1. Open it in Grok Bot. Does it exist? If not, mark "missing".
2. Read its saved instructions.
3. Fetch its INSTRUCTIONS.md from the address in TASKS.md.
4. Compare. The only allowed differences are my name and the default bot's name. Mark "matches", "differs" (say where, in one line) or "placeholder left" (still shows [YOUR NAME] or [ORCHESTRATOR NAME]).
5. Note which accounts, if any, the bot shows as connected.
6. Duties: only the Code bot may write code or change GitHub. Mark "duty problem" if any other bot's instructions say it writes code or changes GitHub, or if it has a GitHub account connected. Orchestrator and Factory must hand that work to Code. Also check the Messaging bot mentions both WhatsApp (wacli) and iMessage, and that Email, Messaging and Calendar each have a humanizer rule (Email and Messaging also voice cards). Mark "voice problem" if missing. For every bot that writes text for other people (all Growth and Operations bots except Analytics, Records, Note taker and Client prep, and the Life bots Friend, Journal, Learn, Selling, Investment, Health and Trip planner), check it has the humanizer rule. Where TASKS.md says it has voice cards, check it has them too. For each Life bot, check its instructions say its data stays in its own memory and a `private/<folder>/` folder, never GitHub, never the daily backup, never shared without asking. Mark "privacy problem" if not. Check Journal, Health, Investment and Workout each say a plain-language disclaimer. Check the Code bot's instructions say it never saves `private/` folders.
If you can run sub-agents or extra tabs, use one per bot for steps 1 to 6. Otherwise go in order.

Step 3. Give me one table: bot, exists, instructions (matches, differs, placeholder left), accounts connected, duties (ok, duty problem, voice problem or privacy problem).

Step 4. Under the table, list in order what is still to do, with the one prompt or click for each. Say "all done" only if every bot on the checklist exists and matches. If you could not see something, say "could not check" instead of guessing.
```

What a good result looks like: one row per bot, every bot "matches", and a to-do list that is only about connecting accounts. Anything marked "missing", "differs", "placeholder left", "duty problem", "voice problem" or "privacy problem": paste the same bot's name back into prompt 00 (core 8) or prompt 14 (a pack) and ask the agent to redo only that bot.
