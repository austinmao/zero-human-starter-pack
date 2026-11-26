# Routing tests

A test set for the Orchestrator. Each line is a real-style request and the bot it should go to. Run it as a **dry run**: for each request, name the bot you would choose and send nothing. Score it. Fix the route lines for anything that failed. Run it again.

**Re-run it every time the roster changes**: a bot added, renamed or retired, or any bot's route-here or not-when line edited.

Only bots that exist can be chosen. If a test names a bot you have not built yet, the right answer is "that bot is not built yet, ask the Factory", and that counts as a pass.

## How to score
- **Pass:** the Orchestrator names the expected bot (and only that bot for a simple ask).
- **Pass (ambiguous):** it asks me one short question, then routes to the expected bot after my answer.
- **Pass (out of scope):** it says the request is outside the team, names the closest bot or "none", and does not invent one.
- **Fail:** wrong bot, several bots for a simple ask, or doing the work itself.
Target: every test passes. Report as "N of N passed" and list each failure with the line that needs a fix.

## Simple asks (one bot)
| # | Request | Expected |
|---|---|---|
| 1 | What emails do I need to reply to today? | Email |
| 2 | Draft a reply to the supplier who wrote yesterday. | Email |
| 3 | Move my Thursday call to 3pm. | Calendar |
| 4 | Find me an hour next week for a call with someone in another time zone. | Calendar |
| 5 | Add "renew the domain" to my list, due Friday. | Task |
| 6 | What did I say to my sister on WhatsApp about Sunday? | Messaging |
| 7 | Reply to the group chat: I'll be ten minutes late. | Messaging |
| 8 | Rename the folder "Old" to "Archive 2025" and share it with my accountant. | Drive |
| 9 | Write a small script that renames my photos by date. | Code |
| 10 | Create a Zoom meeting for Tuesday at 10, 45 minutes. | Meetings |
| 11 | Draft this week's newsletter and three subject lines. | Newsletter |
| 12 | A customer asks where their order is. Draft an answer from my help document. | Customer care |
| 13 | Write a 1,200-word article from these notes. | Writing |
| 14 | Plan the talk I give next month. Start with the outline. | Presentation |
| 15 | Check this invoice against what we agreed. | Finance prep |
| 16 | Flag anything odd in this contract. | Legal admin |
| 17 | Give me today's visits and bookings. | Analytics |
| 18 | Find podcasts that fit my topic. | Outreach |
| 19 | Pitch this story to local journalists. | PR |
| 20 | Draft three posts for next week from this idea. | Social |
| 21 | Prepare me for my call with an existing client at 2pm. | Client prep |
| 22 | Sort the notes from this morning's meeting and send the action items on. | Note taker |
| 23 | Plan the guest list and run of show for my party. | Events |
| 24 | Today's workout? | Workout |
| 25 | Who is due a hello this week? | Friend |

## Reads versus writes (reads are direct)
| # | Request | Expected |
|---|---|---|
| 26 | Does this client have a call booked this week? (Sales needs to know.) | Sales reads the calendar itself. No Calendar hand-off. |
| 27 | Sales wants a follow-up email sent to a prospect after my yes. | Sales drafts, then Email sends. |
| 28 | Save the new campaign plan into the Marketing folder. | Marketing sends the file to Drive. Drive does the save. |

## Ambiguous (ask me one question)
| # | Request | Expected |
|---|---|---|
| 29 | Send the invite for the retreat. | Ask: calendar invite (Calendar) or email to guests (Email)? |
| 30 | Tell Sam I'm running late. | Ask: by WhatsApp or iMessage (Messaging) or by email (Email)? |
| 31 | Put the quarterly numbers in a file and send them to my partner. | Ask which is wanted first. Analytics gets the numbers, Drive saves the file, Email sends it. Not one bot for all three. |
| 32 | Follow up with the people from last week. | Ask: prospects (Sales), existing clients (Client prep or Email), or press (PR)? |

## Joint work (send each part to its owner, in one reply)
| # | Request | Expected |
|---|---|---|
| 33 | Book a Zoom with a client and send them the invite. | Meetings creates the meeting. Calendar adds the time. Email sends the invite text. |
| 34 | Launch a webinar: plan it, write the emails, and post about it. | Events plans. Newsletter or Email writes. Social posts. Orchestrator sends each part to its owner and brings the answers back as one reply. |

## Out of scope (say so, do not invent)
| # | Request | Expected |
|---|---|---|
| 35 | Book me a flight and pay for it. | Trip planner compares options only. It never books or pays. Tell me. |
| 36 | Buy 50 shares of a company. | Out of scope. Investment only teaches. No bot trades. |
| 37 | Diagnose this rash. | Out of scope. Health keeps appointments and logs, and gives no diagnosis. |
| 38 | Turn the lights off at home. | Out of scope. No bot controls devices. |
| 39 | Delete everything in my inbox. | Email asks first. Nothing is deleted without my yes. |
| 40 | Post this on a platform I have not connected. | Out of scope until I connect it. Tell me where to click. |
