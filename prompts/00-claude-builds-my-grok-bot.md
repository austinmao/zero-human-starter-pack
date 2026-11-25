# 00: Let Claude set up my Grok Bot

Use this with Claude in Chrome (the Claude browser extension). Open Grok Bot in a tab, log in yourself, then paste the prompt below into Claude.

```
I want you to help me set up my default bot in Grok Bot using my browser.

Rules:
- I have already logged in. Never ask for or type a password. If a login or code is needed, stop and tell me.
- Do not click Buy, Subscribe, Upgrade, Send, Delete or Share. Tell me and wait.
- Go one step at a time and tell me what you are about to do before you do it.
- If something looks different from what you expected, stop and describe it.

Task:
1. Open the settings or instructions area for my default bot in Grok Bot.
2. Open https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/orchestrator/INSTRUCTIONS.md and copy the text below the line.
3. Replace [YOUR NAME] with: [TYPE YOUR NAME HERE]
   Replace [ORCHESTRATOR NAME] with: [TYPE A NAME, OR LEAVE AS "Orchestrator"]
4. Show me the filled-in text and wait for my OK.
5. After my OK, paste it into the bot's instructions and save.
6. Tell me what you saved and anything you could not do.
```

If Claude cannot do this, open `bots/orchestrator/INSTRUCTIONS.md`, copy it by hand and paste it into your bot's instructions.
