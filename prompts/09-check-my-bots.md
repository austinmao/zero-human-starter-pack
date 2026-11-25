# 09: Check that all 8 bots are done

Run this in a **new chat** with a browser agent, after prompt 00 (or after the Factory step). It only looks. It changes nothing. A fresh chat matters: the agent that built the bots tends to say "done" about its own work.

Open Grok Bot in a tab and log in yourself first.

```
Check my 8 Grok Bot bots. You are only looking. Do not create, edit, save, send or delete anything.

Rules:
- I am already logged in. Never ask for or type a password.
- Keep your replies short.

Step 1. Open https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/TASKS.md
Copy its table as your checklist.

Step 2. For each of the 8 bots, in order:
1. Open it in Grok Bot. Does it exist? If not, mark "missing".
2. Read its saved instructions.
3. Fetch its INSTRUCTIONS.md from the address in TASKS.md.
4. Compare. The only allowed differences are my name and the default bot's name. Mark "matches", "differs" (say where, in one line) or "placeholder left" (still shows [YOUR NAME] or [ORCHESTRATOR NAME]).
5. Note which accounts, if any, the bot shows as connected.
6. Duties: only the Code bot may write code or change GitHub. Mark "duty problem" if any other bot's instructions say it writes code or changes GitHub, or if it has a GitHub account connected. Orchestrator and Factory must hand that work to Code. Also check the Messaging bot mentions both WhatsApp (wacli) and iMessage.
If you can run sub-agents or extra tabs, use one per bot for steps 1 to 6. Otherwise go in order.

Step 3. Give me one table: bot, exists, instructions (matches, differs, placeholder left), accounts connected, duties (ok or duty problem).

Step 4. Under the table, list in order what is still to do, with the one prompt or click for each. Say "all 8 done" only if every bot exists and matches. If you could not see something, say "could not check" instead of guessing.
```

What a good result looks like: 8 rows, every bot "matches", and a to-do list that is only about connecting accounts. Anything marked "missing", "differs", "placeholder left" or "duty problem": paste the same bot's name back into prompt 00 and ask the agent to redo only that bot.
