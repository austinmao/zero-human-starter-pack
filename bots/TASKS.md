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

## Optional packs (prompt 14 only; prompt 00 ignores these)

Three packs sit on top of the core 8. Nobody has to add them. Each is set up with `prompts/14-add-more-bots.md`, one pack at a time, the same way as the core 8. Same address pattern, same four jobs below.

### Pack A: Growth
| # | Bot | Folder | Owns |
|---|---|---|---|
| A1 | Marketing | marketing | Campaign plans, competitor briefs, the monthly report. |
| A2 | Sales | sales | Call reminders, follow-up drafts, a simple pipeline log. |
| A3 | Social | social | The content calendar, post drafts, forum listening. |
| A4 | SEO | seo | Listings, directories, review replies, AI-answer checks. |
| A5 | Analytics | analytics | The morning digest and reports. Read only. |
| A6 | Brand | brand | Creating and keeping each brand: kit, voice, claims. |
| A7 | Writing | writing | Longer drafts and edits. |
| A8 | PR | pr | Media list, pitches, inbound press. |
| A9 | Outreach | outreach | Podcast and speaking pitches. |
| A10 | Presentation | presentation | Talks and decks, in stages. |
| A11 | Video | video | Videos, in stages, with a spend cap. |
| A12 | Newsletter | newsletter | Issue drafts and the pre-send checklist. |

### Pack B: Operations
| # | Bot | Folder | Owns |
|---|---|---|---|
| B1 | Customer care | customer-care | Answers from a help document, check-ins, weekly themes. |
| B2 | Finance prep | finance-prep | Invoice checks, reconciling, cash-flow summary. Never moves money. |
| B3 | Legal admin | legal-admin | Legal intake log, contract flags, deadline ledger. Not legal advice. |
| B4 | HR | hr | Roster, job briefs, offers, onboarding, policies. |
| B5 | Records | records | Where records live, who sees them, how long to keep them. |
| B6 | Events | events | Events from idea to debrief. |
| B7 | Meetings | meetings | Zoom, Meet or Teams meetings. |
| B8 | Note taker | note-taker | Finding, tagging and routing meeting notes. Read only. |
| B9 | Client prep | client-prep | A short brief before each call with an existing client. |

### Pack C: Life (private tier)
Every Life bot keeps its data in its own memory and its own `private/<folder>/` folder. Never GitHub, never the daily backup, never shared with another bot without asking. Each says a plain-language disclaimer the first time it runs.

| # | Bot | Folder | Owns |
|---|---|---|---|
| C1 | Friend | friend | Staying in touch with people I care about. |
| C2 | Journal | journal | A private daily journal. Not therapy. |
| C3 | Workout | workout | A simple workout plan and log. Not medical advice. |
| C4 | Learn | learn | One daily lesson for one skill. |
| C5 | Selling | selling | Selling, donating or clearing out things. |
| C6 | Investment | investment | Learning about investing. No advice, no trades. |
| C7 | Health | health | Appointments, doctor questions, simple logs. No diagnosis. |
| C8 | Home errands | home | Groceries (stops before paying), renewals, chores. |
| C9 | Trip planner | trip | Comparing and planning trips. Never books. |

## Who does what (one owner per area)

- **Code is the only bot that writes code or changes GitHub.** Every other bot hands code and GitHub requests to Code, through the Orchestrator.
- Email, Calendar, Task, Messaging and Drive each own one area. They do not write code and do not touch GitHub.
- The Factory builds bots but saves their files through Code.
- Email and Messaging each keep their own voice cards (one person, many people) and run the humanizer on every draft. Calendar runs the humanizer on invite text. The Factory gives new bots the same rule when they write text for people.
- The Orchestrator hands work out. It does not do other bots' work.
- **Growth (Pack A)** bots plan and draft. The Brand bot owns each brand's approved voice and facts. Analytics supplies the numbers. Nothing goes public, out or into a paid tool without my yes. Sending is Email or Messaging.
- **Operations (Pack B)** bots prepare and check. They never move money, sign, file or delete. Legal admin reviews health, results and legal claims for the other bots.
- **Life (Pack C)** bots keep their own data private (see above). Journal, Health, Investment, Friend and Workout are never saved to GitHub or the daily backup.

## Status values

`todo` > `drafted` (text fetched and filled in) > `created` (saved in Grok Bot) > `verified` (check-back prompt matched it).

## The same four jobs for every bot

1. **Fetch** the bot's `INSTRUCTIONS.md` from the address above.
2. **Fill in** `[YOUR NAME]` and `[ORCHESTRATOR NAME]`. Change nothing else.
3. **Create** the bot in Grok Bot and paste the filled text into its instructions. Save.
4. **Record** the status in your checklist. Do not paste the bot's text into the chat again.

## Order and limits

- Fetch and fill in all of the bots in the set you are doing (the core 8, or one pack) first. This part can run in parallel (one sub-agent or one tab per bot) if your agent supports it.
- Creating bots in Grok Bot happens **one at a time**, in the order above. Never in parallel on the same login.
- Never ask for or type a password. Never click Buy, Subscribe, Upgrade, Send, Delete or Share.
- Connecting accounts (email, calendar and so on) is yours to do after the bots exist. See `prompts/05-connect-more-accounts.md`. WhatsApp is `prompts/10-connect-whatsapp-wacli.md`.
- After connecting, run the **read-only test**: `prompts/11-read-only-connection-test.md`. It sends, creates and deletes nothing.
- Then set up the **daily backup**: `prompts/12-set-up-daily-backup.md`. The Code bot does the backup. The Orchestrator checks it each morning.
