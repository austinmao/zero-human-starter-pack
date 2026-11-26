# Connectors: who may use which app

This is the target for every bot. Default is **off**. A bot gets an app only if it has a mark here.

**R** read only. **W** read and write: this bot is the single owner of that app's writes. **E** edit the contents of its own named file or folder only (the Drive bot creates, moves, shares and deletes). A dash means off. Other marks are written out.

| Bot | Email | Calendar | Drive | Messaging | Tasks | GitHub | Notes | Web | Other |
|---|---|---|---|---|---|---|---|---|---|
| Orchestrator | R | R | R | - | R | - | - | - | - |
| Code | - | - | - | - | - | W | - | - | - |
| Factory | - | - | - | - | - | - | - | - | - |
| Email | W | - | - | - | - | - | - | - | - |
| Messaging | - | - | - | W | - | - | - | - | - |
| Newsletter | - | - | - | - | - | - | - | - | Email platform R |
| Customer care | R | - | R | - | - | - | - | - | Contact list R |
| Calendar | R | W | - | - | - | - | - | - | - |
| Meetings | - | - | - | - | - | - | - | - | Zoom and Teams W |
| Task | - | - | - | - | W | - | - | - | - |
| Events | - | R | E | - | - | - | - | - | - |
| Note taker | - | R | - | - | - | - | R | - | - |
| Client prep | - | R | - | - | - | - | R | - | - |
| Drive | - | - | W | - | - | - | - | - | - |
| Records | - | - | R, E (inventory sheet) | - | - | - | - | - | - |
| Legal admin | R | - | E | - | - | - | - | R | - |
| HR | - | - | E | - | - | - | - | - | Payroll R |
| Finance prep | - | - | - | - | - | - | - | - | Accounting tool R, bank exports R |
| Brand | - | - | E | - | - | - | - | R | - |
| Writing | - | - | E | - | - | - | - | - | - |
| Presentation | - | - | E | - | - | - | - | - | - |
| Video | - | - | - | - | - | - | - | R | - |
| Social | - | - | E | - | - | - | - | R | Social accounts W (I log in) |
| SEO | - | - | - | - | - | - | - | R | Business listing R (I log in to change) |
| Marketing | - | - | E | - | - | - | - | R | - |
| Sales | - | R | E | - | - | - | R | - | - |
| Analytics | - | - | - | - | - | - | - | - | Web analytics R, booking or payment tool R |
| Outreach | - | - | E | - | - | - | - | R | - |
| PR | - | - | E | - | - | - | - | R | - |
| Friend | - | R | - | - | - | - | - | - | - |
| Journal | - | - | - | - | - | - | - | - | - |
| Workout | - | R | - | - | - | - | - | - | - |
| Learn | - | R | - | - | - | - | - | R | - |
| Health | - | R | - | - | - | - | - | - | - |
| Home errands | - | R | - | - | - | - | - | - | Grocery site (I log in) |
| Trip planner | R | - | - | - | - | - | - | R | - |
| Selling | - | - | - | - | - | - | - | R | Photos I give you R |
| Investment | - | - | - | - | - | - | - | R | - |

## The rules behind the table

1. **Least privilege, enforced in the platform.** Set each bot's connector limits in the platform's settings for that bot: which apps, read only or read and write, and which account. Writing "stay in your lane" in a bot's text is not a security boundary. A bot that is told to behave can still do what its connection allows.
2. **One owner for each app that has side effects.** Email: the Email bot is the only one that drafts or sends email. Calendar: the Calendar bot is the only one that changes events, Calendly or Google Meet links. Drive: the Drive bot owns file changes (create, move, share, delete) in Google Drive, Docs, Sheets and Dropbox. Messaging: the Messaging bot is the only one that sends chats. Code: the Code bot owns GitHub. Task: the Task bot owns the list. Social: the Social bot is the only one that posts. Meetings: the Meetings bot owns Zoom and Teams.
3. **Reads are direct.** Other bots read email, calendars and files themselves, read only, limited to the right accounts. They do not route a plain read through the owner bot. They ask the owner bot only for a write. The one exception is chats, which stay behind the Messaging bot because they are private.
4. **One key or connection can be shared** by several bots when the platform enforces a separate limit for each bot. A bot never sees, prints or stores the key.
5. **Messages, not files.** A bot asks an owner bot to write by sending it a real message with the platform's agent-messaging tool (on GrokBot: SendToAgent). A task is running only after the message was sent. A shared file such as `HANDOFFS.md` may be a log of what happened. It is never the way a job is delivered. Every owner bot can message back.
6. **Changing access needs my yes.** The Factory and the Orchestrator never widen a bot's access on their own. They show the change and wait.
7. **Test both ways.** After you set limits, give each bot one read it is allowed to do and one read it is not allowed to do. The allowed read works. The other one is refused by the platform, not just by the bot saying no.

If your platform cannot set limits per bot, say so plainly in your notes. Keep the table anyway, use one account per area, and treat the prompt rules as a weaker safeguard.
