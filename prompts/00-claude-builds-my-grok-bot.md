# 00: The one prompt. A browser agent sets up everything

Use this with a browser agent: Claude in Chrome, ChatGPT agent mode, or another agent that can drive your browser. Open Grok Bot in a tab and log in yourself. Then paste the prompt below into the agent.

This is the only prompt you paste. It builds the 8 bots, then hands over to your Orchestrator, which runs the rest. You only log in, scan a QR code and approve.

The prompt is short on purpose. The agent works from a task list (`bots/TASKS.md`) instead of from one long message.

```
Set up my 8 Grok Bot bots using my browser. Work from a checklist, not from memory.

First ask me two things, then carry on: my name, and what I want to call my default bot (the Orchestrator).

Rules:
- I am already logged in. Never ask for or type a password. If a login or code is needed, stop and tell me.
- Do not click Buy, Subscribe, Upgrade, Send, Delete or Share. The one exception is Step 4: you may send one message to my default bot.
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

Step 4. Show the final checklist. Then open my default bot's chat and send it exactly this one message: "Start setup." Tell me the setup has started in that chat. From there my default bot runs the connection tests, the WhatsApp pairing help and the daily backup. I only log in, scan and approve. Do nothing more.
```

If the agent cannot do this, open `bots/orchestrator/INSTRUCTIONS.md`, copy the text below the line and paste it into your bot's instructions by hand. Then use prompts 01 and 02 and let the Factory build the rest.
