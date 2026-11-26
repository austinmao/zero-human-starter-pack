# 02: Factory builds the other bots (fallback)

**Normally you do not paste this.** Prompt 00 already asks your Orchestrator to create the Factory and send it this job. Use this only if the Factory exists but the other bots do not: paste it into the Factory.

```
You are the Factory. Follow the instructions you were given.

Build these bots, in this order, one at a time: Code, Email, Calendar, Task, Messaging, Drive. The text for each is at https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/<folder>/INSTRUCTIONS.md (and SKILLS.md), where <folder> is code, email, calendar, task, messaging or drive.

First, for each bot, fill in my name and the Orchestrator's name and change nothing else. Show me one table: bot, first line of its text, any placeholder left. Ask once: "OK to create all six?" and wait.

After my OK, build them one at a time with no more questions:
1. Create the bot and name it.
2. Send it its filled-in text as its first message and ask it to remember it as its lasting job and rules.
3. Add the skills in SKILLS.md that your platform supports. List the ones you could not add.
4. Ask the new bot to say its name and what it owns. Tell the Orchestrator it exists.
If one fails, say why in one line and carry on.

Each bot keeps to its own job. Only the Code bot writes code or changes GitHub. Do not save anything to GitHub yet: I connect it at the end of setup.
Do not ask for passwords. If a bot needs an account connected, tell me where to click and I will do it myself.
If I ask for one of the optional packs (Growth, Operations or Life, listed in bots/TASKS.md), build those bots the same way and use prompts/14-add-more-bots.md for the order. For the Life pack, update the Code bot first.
After all six, give me a table: bot, what it owns, accounts, what is left to do.
Then tell the Orchestrator: "All six exist."
```
