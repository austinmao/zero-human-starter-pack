# Connectors: who may use which app

This is the target for every bot. Default is **off**. A bot gets an app only if it has a mark here.

**R** read only. **W** read and write: this bot is the owner of that app's writes. A dash means off. **On** means the bot may use agent messaging (on GrokBot: SendToAgent), which is not an app and is never turned off by the limits below. "Prompt-only" means the platform cannot enforce the limit (for example a browser session I log in to, or a thread-level limit inside a connected account), so it is only a rule in the bot's text.

| Bot | Agent messaging | Email | Calendar | Drive | Chats | Tasks | GitHub | Shared files | Notes | Web | Other |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Orchestrator | On | R | R | R | - | R | - | - | - | - | - |
| Code | On | - | - | - | - | - | W | W (shared work folder, never private/) | - | - | - |
| Factory | On | - | - | - | - | - | - | - | - | - | - |
| Email | On | W | - | - | - | - | - | - | - | - | - |
| Messaging | On | - | - | - | W | - | - | - | - | - | - |
| Newsletter | On | - | - | - | - | - | - | - | - | - | Email platform R |
| Customer care | On | R | - | R | - | - | - | - | - | - | Contact list R |
| Calendar | On | R | W | - | - | - | - | - | - | - | - |
| Meetings | On | - | - | - | - | - | - | - | - | - | Zoom and Teams W |
| Task | On | - | - | - | - | W | - | - | - | - | - |
| Events | On | - | R | R | - | - | - | - | - | - | - |
| Note taker | On | - | R | - | - | - | - | - | R | - | - |
| Client prep | On | - | R | - | - | - | - | - | R | - | - |
| Drive | On | - | - | W | - | - | - | - | - | - | - |
| Records | On | - | - | R | - | - | - | - | - | - | - |
| Legal admin | On | R | - | R | - | - | - | - | - | R | - |
| HR | On | - | - | R | - | - | - | - | - | - | Payroll R |
| Finance prep | On | - | - | - | - | - | - | - | - | - | Accounting tool R, bank exports R |
| Brand | On | - | - | R | - | - | - | - | - | R | - |
| Writing | On | - | - | R | - | - | - | - | - | - | - |
| Presentation | On | - | - | R | - | - | - | - | - | - | - |
| Video | On | - | - | - | - | - | - | - | - | R | - |
| Social | On | - | - | R | - | - | - | - | - | R | Social accounts W, prompt-only (owner: Social) |
| SEO | On | - | - | - | - | - | - | - | - | R | Business listing W, prompt-only (owner: SEO) |
| Marketing | On | - | - | R | - | - | - | - | - | R | - |
| Sales | On | - | R | R | - | - | - | - | R | - | - |
| Analytics | On | - | - | - | - | - | - | - | - | - | Web analytics R, booking or payment tool R |
| Outreach | On | - | - | R | - | - | - | - | - | R | - |
| PR | On | - | - | R | - | - | - | - | - | R | - |
| Friend | On | - | R | - | - | - | - | W (own private/friend/ only) | - | - | - |
| Journal | On | - | - | - | - | - | - | W (own private/journal/ only) | - | - | - |
| Workout | On | - | R | - | - | - | - | W (own private/workout/ only) | - | - | - |
| Learn | On | - | R | - | - | - | - | W (own private/learn/ only) | - | R | - |
| Health | On | - | R | - | - | - | - | W (own private/health/ only) | - | - | - |
| Home errands | On | - | R | - | - | - | - | W (own private/home/ only) | - | - | Grocery site W, prompt-only (owner: Home errands) |
| Trip planner | On | R | - | - | - | - | - | W (own private/trip/ only) | - | R | - |
| Selling | On | - | - | - | - | - | - | W (own private/selling/ only) | - | R | Photos I give you R |
| Investment | On | - | - | - | - | - | - | W (own private/investment/ only) | - | R | - |

## Owners (the one canonical list)

Every other file in this pack links here. None of them restates this list.

- **Email:** the Email bot is the only one that drafts or sends email.
- **Calendar:** the Calendar bot is the only one that changes events, Calendly or Google Meet links.
- **Drive:** the Drive bot owns every file change (create, edit, move, share, delete) in Google Drive, Docs, Sheets and Dropbox.
- **Chats:** the Messaging bot is the only one that sends a chat (WhatsApp, iMessage).
- **GitHub:** the Code bot.
- **Task list:** the Task bot.
- **Social accounts:** the Social bot is the only one that posts.
- **Zoom and Teams:** the Meetings bot.
- **Business listing:** the SEO bot (prompt-only: a browser session I log in to).
- **Grocery site:** the Home errands bot (prompt-only: a browser session I log in to).

## The rules behind the table

1. **Least privilege, enforced in the platform.** Set each bot's connector limits in the platform's settings for that bot: which apps, read only or read and write, and which account. Writing "stay in your lane" in a bot's text is not a security boundary. A bot that is told to behave can still do what its connection allows.
2. **One owner for each app that has side effects**, as in the list above. A Drive or Dropbox connection grants edit, create and share together, so any edit to a file is a real Drive write. Bots with a working folder or tracker sheet read it directly and send their edits to the Drive bot. If your platform can limit a bot to one folder, you may give that bot write on that folder only.
3. **Reads are direct.** Other bots read email, calendars and files themselves, read only, limited to the right accounts. They do not route a plain read through the owner bot. They ask the owner bot only for a write. The one exception is chats, which stay behind the Messaging bot because they are private: it gives a short summary only, never message bodies, and logs which bot asked and what for.
4. **One key or connection can be shared** by several bots when the platform enforces a separate limit for each bot. A bot never sees, prints or stores the key.
5. **Messages, not files.** A bot asks an owner bot to write by sending it a real message with the platform's agent-messaging tool (on GrokBot: SendToAgent). Agent messaging is not an app and is on for every bot. A task is running only after the message was sent. A shared file such as `HANDOFFS.md` may be a log of what happened. It is never the way a job is delivered. Every owner bot can message back.
6. **Changing access needs my yes.** The Factory and the Orchestrator never widen a bot's access on their own. They show the change and wait.
7. **Test both ways.** After you set limits, give each bot one read it is allowed to do and one read in an app that is off for it. The allowed read works. The other one is refused by the platform, not just by the bot saying no.
8. **Prompt-only limits.** Some limits cannot be enforced by a connector: a thread-level limit inside a connected mailbox or calendar (the connector gives the whole account), and browser sessions I log in to (business listing, social accounts, grocery site). Those rows are marked prompt-only. Treat them as the weaker safeguard.

If your platform cannot set limits per bot, say so plainly in your notes. Keep the table anyway, use one account per area, and treat the prompt rules as a weaker safeguard.
