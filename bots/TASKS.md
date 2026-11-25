# Bootstrap task list: the 8 bots

A browser agent (Claude in Chrome, ChatGPT agent mode or similar) walks down this list. The same list is used again by the check-back prompt (`prompts/09-check-my-bots.md`).

Raw file address for each bot: `https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/<folder>/INSTRUCTIONS.md`

| # | Bot | Folder | Owns |
|---|---|---|---|
| 1 | Orchestrator | orchestrator | The default bot. Takes requests and hands them to the right bot. |
| 2 | Factory | factory | Builds and updates the other bots. |
| 3 | Code | code | Files, scripts, installing tools, GitHub, the daily backup. |
| 4 | Email | email | Reading, sorting and drafting email. |
| 5 | Calendar | calendar | Reading calendars, finding time, drafting invites. |
| 6 | Task | task | The one task list. |
| 7 | Messaging | messaging | WhatsApp (wacli) and iMessage. Other chat apps are drafts only. |
| 8 | Drive | drive | Files in Google Drive, Dropbox and similar. |

## Who does what (one owner per area)

- **Code is the only bot that writes code or changes GitHub.** Every other bot hands code and GitHub requests to Code, through the Orchestrator.
- Email, Calendar, Task, Messaging and Drive each own one area. They do not write code and do not touch GitHub.
- The Factory builds bots but saves their files through Code.
- The Orchestrator hands work out. It does not do other bots' work.

## Status values

`todo` > `drafted` (text fetched and filled in) > `created` (saved in Grok Bot) > `verified` (check-back prompt matched it).

## The same four jobs for every bot

1. **Fetch** the bot's `INSTRUCTIONS.md` from the address above.
2. **Fill in** `[YOUR NAME]` and `[ORCHESTRATOR NAME]`. Change nothing else.
3. **Create** the bot in Grok Bot and paste the filled text into its instructions. Save.
4. **Record** the status in your checklist. Do not paste the bot's text into the chat again.

## Order and limits

- Fetch and fill in all 8 first. This part can run in parallel (one sub-agent or one tab per bot) if your agent supports it.
- Creating bots in Grok Bot happens **one at a time**, in the order above. Never in parallel on the same login.
- Never ask for or type a password. Never click Buy, Subscribe, Upgrade, Send, Delete or Share.
- Connecting accounts (email, calendar and so on) is yours to do after the bots exist. See `prompts/05-connect-more-accounts.md`. WhatsApp is `prompts/10-connect-whatsapp-wacli.md`.
- After connecting, run the **read-only test**: `prompts/11-read-only-connection-test.md`. It sends, creates and deletes nothing.
- Then set up the **daily backup**: `prompts/12-set-up-daily-backup.md`. The Code bot does the backup. The Orchestrator checks it each morning.
