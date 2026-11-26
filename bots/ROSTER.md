# Roster: who to route to

The Orchestrator reads this file and remembers it. Groups are a routing aid. The Orchestrator still messages the specialist bot directly: there is no extra hop through a group. A group lead routes only when a group does joint multi-bot work, and only if I name one.

Each bot has one **route here when** line and one **not when** line. They do not overlap. If a request fits two bots, the **not when** lines decide. If they still do not decide it, ask me one question.

Effort scaling: a simple ask goes to one bot. Do not fan out to many bots for a simple job.

| Group | Bot | Route here when | Not when |
|---|---|---|---|
| Router | Orchestrator | Anything I send you first, and any job that needs more than one bot. | A job I addressed to one bot directly. That bot does it and tells you in one line. |
| Engineering and factory | Code | Code, scripts, installing tools, anything on GitHub, the daily backup. | Any email, calendar, task, chat or Drive job, even if it needs a small lookup first. |
| Engineering and factory | Factory | Build, change, rename or retire a bot. Add or fix a bot's connector block or roster row. | Doing a bot's job. Connecting my accounts (that is me, guided by the Orchestrator). |
| Communications | Email | Read, sort, summarise, draft or send email. Reply to an email. | Invites and meetings (Calendar). Storing a file (Drive). To-dos (Task). Chat messages (Messaging). Newsletter issues (Newsletter). Questions from customers (Customer care). |
| Communications | Messaging | Read, summarise, draft or send a chat message (WhatsApp, iMessage). | Email (Email). Newsletter (Newsletter). Social posts and comments (Social). |
| Communications | Newsletter | Draft a newsletter issue, subject lines, the pre-send checklist. | One-to-one or group email (Email). Social posts (Social). |
| Communications | Customer care | Questions from customers or past customers. Answers from my help document. The weekly themes. | Sales leads (Sales). Refunds or money moved (Finance prep). Legal complaints (Legal admin). |
| Calendar and ops | Calendar | Add, move, accept, decline or cancel an event. Find free time. Calendly. A Google Meet link. | Zoom or Teams meetings (Meetings). Emailing the invite text (Email). |
| Calendar and ops | Meetings | Create, change or cancel a Zoom or Teams meeting. | Google Meet links and calendar events (Calendar). The invite email (Email). |
| Calendar and ops | Task | Add, change, complete or list tasks and due dates. | Calendar events (Calendar). Saving a note or file (Drive). |
| Calendar and ops | Events | Plan an event: the guest list and RSVP tracking, run of show, budget, the debrief. | A Zoom or Teams link (Meetings). Putting the date on a calendar or sending invites (invites: Calendar for the event, Email for the message). |
| Calendar and ops | Note taker | Find, tag and sort meeting notes. Send action items to whoever owns them. | Preparing for a client call (Client prep). Creating the tasks (Task). |
| Calendar and ops | Client prep | A one-page brief before a call with an existing client. | Prospects who have not bought (Sales). Finding or sorting notes (Note taker). |
| Files, records and admin | Drive | Create, move, rename, share, delete or organise a file or folder. Save a bot's draft into a folder. Apply another bot's edits to a file or sheet. | Drafting the content (the topic bot). Reading a file a bot needs for its own job (that bot reads it directly). |
| Files, records and admin | Records | Where a record lives, who can see it, keep-until dates, the monthly records review. | Finding a file for a task (Drive). Legal deadlines (Legal admin). |
| Files, records and admin | Legal admin | Contract clause flags, the legal intake log, the deadline ledger, a review of health or legal claims in copy. | Paying anything (Finance prep). Staff paperwork (HR). |
| Files, records and admin | HR | The roster, a job brief, interview questions, an offer draft, an onboarding checklist, policy questions. | Changing pay (me only). Contracts (Legal admin). |
| Files, records and admin | Finance prep | Check an invoice, reconcile an export, a cash-flow summary, stage a bill, draft a chaser. | Traffic numbers (Analytics). Contracts (Legal admin). |
| Content and brand | Brand | Create or update a brand kit. The approved voice or facts for a brand. Check a draft against the kit. | Writing the draft itself (Writing, Social, Newsletter). Legal claims (Legal admin). |
| Content and brand | Writing | Articles, pages, scripts, long posts. Edit mode on my own drafts. | Short social posts (Social). Email (Email). Slides (Presentation). Newsletter issues (Newsletter). |
| Content and brand | Presentation | A talk, pitch or class: outline, slide words, speaker notes. | Video scripts (Video). Long articles (Writing). |
| Content and brand | Video | Plan and prepare a video: idea, script, shot list, edit notes. | Slides (Presentation). Social posts (Social). |
| Content and brand | Social | The content calendar, social posts, replies in groups I name. | The newsletter (Newsletter). Chat messages (Messaging). Press pitches (PR). Listings and review replies (SEO). |
| Content and brand | SEO | My business listing, directory entries, review replies, how search and AI describe me. | Social posts (Social). Site traffic (Analytics). Campaign plans (Marketing). |
| Growth and outreach | Marketing | A campaign plan, a competitor brief, the monthly marketing report. | Writing the posts (Social). The newsletter (Newsletter). A long article (Writing). Brand voice (Brand). Traffic numbers (Analytics). |
| Growth and outreach | Sales | A reminder before a booked sales call, a follow-up after it, the pipeline log. | Pitching press or podcasts (PR, Outreach). Someone who already bought and has a question (Customer care). Sending the follow-up (Email). |
| Growth and outreach | Analytics | Visit, sign-up and booking numbers. The morning digest. A report with its sources. | What to change in a campaign (Marketing). Money owed or paid (Finance prep). |
| Growth and outreach | Outreach | Podcasts and speaking slots: find, score, pitch, guest-prep brief. | Press and journalists (PR). |
| Growth and outreach | PR | The press list, press pitches, replies to inbound press, the weekly press report. | Podcasts and speaking slots (Outreach). |
| Personal life (private data) | Friend | Keeping in touch: who is due a hello, birthdays, drafts for friends and family. | Business contacts (Sales, Email). Sending the message (Messaging). |
| Personal life (private data) | Journal | The daily prompt, the nightly reflection, the weekly themes, a friend-safe summary on request. | Health symptoms (Health). To-dos (Task). |
| Personal life (private data) | Workout | Today's session, logging a workout, adjusting the plan. | Pain or injuries to take to a doctor (Health). |
| Personal life (private data) | Learn | Practice coaching for one skill at a time. | Reading about investing (Investment). A talk I must give (Presentation). |
| Personal life (private data) | Health | Appointments, doctor questions, simple logs. No diagnosis. | Workouts (Workout). Mood and reflection (Journal). |
| Personal life (private data) | Home errands | The grocery cart, renewals at 60 and 30 days, chores. | Things to sell (Selling). Trips (Trip planner). |
| Personal life (private data) | Trip planner | Compare and plan a trip. Check a confirmation against what I agreed. Never books. | Putting the dates on a calendar (Calendar). Renewals (Home errands). |
| Personal life (private data) | Selling | Sort, price and draft listings for things I own. Draft buyer replies. | Business sales (Sales). Chores (Home errands). |
| Personal life (private data) | Investment | Learning about investing, with sources and dates. No advice. | Invoices and paperwork (Finance prep). |

Packs: Code and Factory are in the core 8 with Orchestrator, Email, Calendar, Task, Messaging and Drive. Growth, Operations and Life bots only exist if you added their pack. If a bot is not built yet, say so and ask the Factory to build it.

After any change to the roster, re-run `bots/ROUTING-TESTS.md`.
