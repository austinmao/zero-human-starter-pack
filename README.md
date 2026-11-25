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

## Quick start

1. Click **Use this template** at the top of this page and create a **private** repo called `my-agents`. Everything you build is backed up there.
2. Open `START-HERE.md` and follow the steps in order.
3. Paste `prompts/01-orchestrator-bootstrap.md` into your assistant first.

## What is in this pack

- `bots/<name>/INSTRUCTIONS.md`: the text you paste into each bot.
- `bots/<name>/SKILLS.md`: skills worth adding to each bot, with links.
- `prompts/`: step-by-step prompts, from setup to moving your old ChatGPT and Claude knowledge across.
- `knowledge/`: where your own notes go, in your private copy only. `knowledge/HOW-TO-EXPORT.md` explains how to get your work out of Claude and ChatGPT.

## Safety rules built into every bot

- A bot never asks for or stores a password. You log in yourself.
- A bot asks before it sends, pays for, deletes or shares anything.
- A bot says which account it is using every time.
- A bot never moves data from one account to another without asking.

## Licence

MIT. See `LICENSE`. Zero Human by Austin Mao.
