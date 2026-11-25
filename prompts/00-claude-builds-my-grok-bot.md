# 00: Let a browser agent set up all 8 bots

Use this with a browser agent: Claude in Chrome, ChatGPT agent mode, or another agent that can drive your browser. Open Grok Bot in a tab and log in yourself. Then paste the prompt below into the agent.

The prompt is short on purpose. The agent works from a task list (`bots/TASKS.md`) instead of from one long message.

```
Set up my 8 Grok Bot bots using my browser. Work from a checklist, not from memory.

My name: [TYPE YOUR NAME]
Name for the default bot: [TYPE A NAME, OR LEAVE AS "Orchestrator"]

Rules:
- I am already logged in. Never ask for or type a password. If a login or code is needed, stop and tell me.
- Do not click Buy, Subscribe, Upgrade, Send, Delete or Share.
- If something looks different from what you expect, stop and describe it.
- Keep your replies short. Never paste a bot's full text into the chat more than once.

Step 1. Open https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/TASKS.md
Copy its table into your reply as your checklist. After every change, show me the updated checklist.

Step 2. Prepare all 8 (do not touch Grok Bot yet).
For each bot, fetch its INSTRUCTIONS.md from the address in TASKS.md and replace [YOUR NAME] and [ORCHESTRATOR NAME]. Change nothing else.
If you can run sub-agents or extra tabs, use one per bot for this step only.
Mark each bot "drafted". Then show me a table: bot, first line of its text, and any placeholder left. Ask: "OK to create all 8?" and wait.

Step 3. After my OK, create the bots in Grok Bot one at a time, in the order in TASKS.md. Never in parallel.
For each: create the bot, paste its filled text into the instructions, save, mark it "created".
If a bot fails, mark it "failed", say why in one line, and carry on with the next.
If Grok Bot gives you no way to create bots from the browser, stop and tell me. I will use the Factory path instead.

Step 4. Show the final checklist. Then tell me the next three things, in order: (1) open a NEW chat and run prompts/09-check-my-bots.md, (2) connect my accounts myself, then run prompts/11-read-only-connection-test.md, (3) set up the daily backup with prompts/12-set-up-daily-backup.md.
```

If the agent cannot do this, open `bots/orchestrator/INSTRUCTIONS.md`, copy the text below the line and paste it into your bot's instructions by hand. Then use prompts 01 and 02 and let the Factory build the rest.
