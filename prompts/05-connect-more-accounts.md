# 05: Connect more than one account

Most people have several accounts: two or three Google calendars, a work and a personal drive, a Dropbox. Each one gets a short alias so your bots always say which one they mean.

## Step 1: choose aliases
Write one line per account.

| Alias | Service | Used for |
|---|---|---|
| work-google | Google | Work email, calendar, drive |
| personal-google | Google | Personal email and calendar |
| dropbox-main | Dropbox | Shared files |

## Step 2: connect each account yourself
Your platform has a connections or integrations area. Connect one account at a time and log in yourself. Never type a password into a chat.

Some platforms connect only one Google account directly. If yours does, ask it how to add more (for example, through a connector service that supports account names). If it cannot, connect the extra accounts in a second profile or browser and tell the bot which is which.

## Step 2b: give each bot only what it needs
Connecting an account is not the same as giving every bot access to it. In your platform's per-bot connector settings, give each bot only the apps it needs, read only or read and write, on the right account. The table is `bots/CONNECTORS.md`. Email, Calendar and Drive are the only bots that write to mail, calendars and files. Other bots read, read only. Your Orchestrator will walk you through it.

## Step 3: tell the Orchestrator

```
I have connected these accounts. Update the "My accounts" table and pass the right ones to each bot.

[PASTE YOUR ALIAS TABLE]

Rules from now on:
- Always say which alias you used.
- Search every account for the area unless I name one.
- Never copy anything from one account into another without asking me.
- Never give a bot access to an app or account that is not in its table in `bots/CONNECTORS.md`, and never widen access without my yes.
- If an account stops working, tell me and do not try to log in.

Then run the read-only test in prompts/11-read-only-connection-test.md. It checks every connection without sending or changing anything.
```
