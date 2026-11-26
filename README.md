# Zero Human Starter Pack

A set of ready-to-paste instructions that turn an agentic assistant (Grok Bot, or any similar system) into a small team of bots that run your email, calendar, tasks, messages and files.

You do not need to be technical. If you have used ChatGPT or Claude, you can do this.

## What you end up with

| Bot | Job |
|---|---|
| Orchestrator | The default bot. Takes your request and hands it to the right bot. |
| Factory | Builds and updates the other bots from the files in this pack. |
| Code | Writes and fixes files and small scripts. Saves your work to GitHub. |
| Email | Reads, sorts and drafts email. Never sends without your OK. |
| Calendar | Reads your calendars, finds time, drafts invites. |
| Task | Keeps one clear list of what needs doing. |
| Messaging | Reads and drafts messages in your chat apps. |
| Drive | Finds and organises files in Google Drive, Dropbox and similar. |

Every bot can be connected to **more than one account** (for example, two Google calendars).

**Optional packs (Part 3).** When the core 8 work, add more bots one pack at a time with `prompts/14-add-more-bots.md`: Growth (12 bots), Operations (9) and Life (9). Life bots keep their data private and out of the GitHub backup.

## Quick start

1. Sign up for Grok, pay for a plan that includes Grok Bot, and install the desktop app (x.ai/bot).
2. Open `START-HERE.md` (or the interactive guide) and follow Part 1.
3. Paste `prompts/00-paste-into-your-first-bot.md` into your first bot. It becomes your Orchestrator and builds the rest.
4. At the end, connect GitHub for a daily backup. Optional Part 2 moves your old Claude and ChatGPT work across. Optional Part 3 adds more bots.

## What is in this pack

- `bots/<name>/INSTRUCTIONS.md`: the text you paste into each bot.
- `bots/<name>/SKILLS.md`: skills worth adding to each bot, with links.
- `bots/CONNECTORS.md`, `bots/ROSTER.md`, `bots/ROUTING-TESTS.md`: who may use which app, who to route to, and the routing test set.
- `GROKBOT-UPDATE.md`: updates an existing team to this design.
- `prompts/`: step-by-step prompts, from setup to moving your old ChatGPT and Claude knowledge across.
- `knowledge/`: where your own notes go, in your private copy only (Part 2). `knowledge/HOW-TO-EXPORT.md` explains how to get your work out of Claude and ChatGPT.

## How the team is wired

- **Least privilege.** Each bot lists the apps it may use, read only or read and write, and which account. Default is off. These limits are set per bot in the platform's connector settings, not just written in the bot's text. A line saying "stay in your lane" is not a security boundary. See `bots/CONNECTORS.md`.
- **One owner per app with side effects.** The owner list is in `bots/CONNECTORS.md`. Other bots read directly, read only, and ask the owner only for a write.
- **Real messages.** The Orchestrator delegates with the platform's agent-messaging tool (on OpenMausBot: `coordinate_bots`; on GrokBot: SendToAgent), with a brief that has a goal, limits, expected output and a "done means". It checks the result. Files are never the way a job is handed over.
- **A roster and a test set.** `bots/ROSTER.md` groups the bots and gives each a "route here when" and a "not when" line. `bots/ROUTING-TESTS.md` is the test set to run after any change.

Already built your team from an older version? Follow `GROKBOT-UPDATE.md`.

## Safety rules built into every bot

- A bot never asks for or stores a password. You log in yourself.
- A bot asks before it sends, pays for, deletes or shares anything.
- A bot says which account it is using every time.
- A bot never moves data from one account to another without asking.
- A bot uses only the apps and accounts in its own table. Anything else is off.

## Licence

MIT. See `LICENSE`. Zero Human by Austin Mao.
