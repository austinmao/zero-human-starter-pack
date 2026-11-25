# 12: Daily backup to GitHub

Your bots live in Grok Bot. Their instructions, skills, routines and notes are also saved in your private `my-agents` repo, so you can rebuild them if something breaks. This prompt sets up a **daily** backup.

Who does what:
- **Code bot:** does the backup. Only Code writes to GitHub.
- **Orchestrator:** sets up the daily routine, checks each day that the backup ran, and tells you if it did not.

What is saved, as text files: each bot's current instructions, the list of routines, and the list of skills. What is **never** saved: passwords, tokens, API keys, `.env` files, the `wacli` session folder, message or email contents, raw exports.

Paste this to the Orchestrator.

```
Set up a daily backup of my agents to my private GitHub repo [YOUR-GITHUB-USERNAME]/my-agents.

Do this in order and wait for my OK at steps 2 and 4.

1. Ask the Code bot to confirm my-agents is private. If it is public, stop and tell me.
2. Show me what will be saved and what will not (see the rules below). Wait for my OK.
3. Ask each bot to give the Code bot its current instructions, its routines and its skill names as plain text. Never include passwords, tokens, keys, the wacli session folder, or message or email contents.
4. Ask the Code bot to run one backup now. It saves files into the backups/ folder of my-agents, with a clear commit message such as "Daily backup 2026-11-25", and only commits if something changed. Show me the list of files before it commits. Wait for my OK.
5. After my OK, create a routine for the Code bot that runs this backup every day at [TIME, MY TIME ZONE] without asking me, using the same rules. The routine may only write to backups/.
6. Create a routine for yourself that runs each morning: check the latest commit in my-agents/backups, and tell me if the last backup is older than 24 hours or failed.

Rules for the Code bot:
- Only write inside backups/ in my-agents.
- Before saving a file, scan it for anything that looks like a password, token, key or card number. If found, do not save that file and tell me.
- Never make a repo public. Never delete a file. Never overwrite without a commit.
- Never copy ~/.wacli, ~/.local/state/wacli, .env files or raw exports.
- If GitHub cannot be reached, say so. Do not try workarounds. I will upload by hand.

When done, tell me: the link to the first backup, the routine times, and what is not backed up.
```

If the Code bot cannot write to GitHub from your Grok Bot, use prompt 04 (way B) to upload the backup folder by hand, and ask again later. Not confirmed against a real Grok Bot login.
