# Update an existing GrokBot team to the least-privilege design

For people who already built their team from an earlier version of this pack. It takes your Orchestrator (and your Factory) through the update, one step at a time. You log in, click the connector settings and approve. The bots do the rest.

Your bots keep their jobs. What changes:

1. **Each bot gets only the apps it needs**, read only or read and write, on named accounts. Set in the platform, not just in the bot's text.
2. **One owner for each app with side effects**, listed in `bots/CONNECTORS.md` (the one canonical list). Other bots read directly, read only, and ask the owner only for a write.
3. **The Orchestrator delegates with real messages** (on GrokBot: `SendToAgent`), with a four-part brief, and checks the result. No file-only hand-offs.
4. **A roster with route-when and not-when lines**, and a routing test set.
5. **The Factory writes a connector block and roster row for every new or changed bot.**

Time: about 60 to 90 minutes, mostly watching. Nothing is deleted. Nothing is sent. Your voice cards, account tables and private data are kept.

## Check on your platform first
Before Part 1, confirm these three things. If any one is missing, the related rule becomes **prompt-only** (written in the bot's text, not enforced). Your Orchestrator will say so in the Step 9 report.
- [ ] **Agent messaging.** The tool is called `SendToAgent` (or what your platform calls it), a bot can send a message to another bot, and the other bot can reply.
- [ ] **Per-bot connector limits.** The platform lets you set, for each bot, which apps it may use, **read only versus read and write**, and **which account**. Not just one setting for the whole team.
- [ ] **A refused read is blocked by the platform.** When a bot tries to read an app that is off for it, the platform refuses, not only the bot declining in its reply.

## Fetching the files before and after merge
The addresses in Part 1 use `main`. Until this change is merged into `main`, fetch from the branch instead: replace `main` with `feat/least-privilege-orchestrator-patterns` in every address. After the merge, use `main`.

## Before you start
- Your Orchestrator and Factory exist and answer.
- Read the safety rules in the paste block below. They apply to every step.
- If your platform cannot limit a connection per bot, the update still helps (clear owners, real messages, a roster), but the access limits are only prompt rules. Your Orchestrator will say so in Step 4.

## Part 1. Paste into your Orchestrator

```
Update my team to the least-privilege design. Work from the checklist below, one step at a time. Show the checklist after every step.

Safety rules for the whole job:
- Read only until I approve a change. Do not send, post, pay, delete, share or move anything. No test emails, events, files or messages to real people.
- Never ask for, type, print or store a password or key. Show account aliases, never secrets, and never message bodies or file contents. Show names, dates and counts only.
- You never widen a bot's access on your own. Every change to access waits for my yes at a STOP.
- A prompt rule is not a security boundary. Real limits are set per bot in the platform's connector settings. I click those myself. You tell me where.
- If a step fails, mark it failed, say why in one line, and carry on. Never loop. Never retry more than 3 times.
- Keep replies short.

Step 1. Get the new files. Use `main` in these addresses, unless I tell you a branch name.
Read these and remember them:
https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/orchestrator/INSTRUCTIONS.md
https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/factory/INSTRUCTIONS.md
https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/CONNECTORS.md
https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/ROSTER.md
https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/ROUTING-TESTS.md
For every other bot I have, the file is https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/bots/<folder>/INSTRUCTIONS.md. List which bots I have and which of them have no file in the pack. Mark any bot I built myself as "custom".

Step 2. Check messaging, then inventory what each bot can use today.
First a ping test. It has no side effects. Ask each bot, with SendToAgent, to reply "ping from <bot name>". Mark each bot ok or "cannot reply". If a bot cannot receive or reply, stop and fix messaging for that bot first (Steps 1, 2 and 4 depend on it). Do not go on with that bot until it replies.
Then ask each bot, with SendToAgent, one at a time: "List every app connected to you, the account alias for each, and whether you can read only or read and write. Do not use any of them. Reply to me with SendToAgent." If a bot cannot tell, say "unknown" and I will read it from the platform settings.
Mark a bot "did not reply" if it does not answer. Do not guess.

Step 3. Build the table.
Make one table: bot, app, access (read only, read and write, unknown), account alias. One row per app per bot.
Next to it, fill the target from CONNECTORS.md. Then list three things:
  (a) Extra: access a bot has now that the target does not allow.
  (b) Missing: access a bot needs for its job and does not have.
  (c) Two owners: any app where two bots can write.
Also list every place the team passes work through a file instead of a message (for example a shared HANDOFFS file used as a queue).
STOP 1. Show me the table and the three lists. Ask: "OK with this target?" Wait. I may change the target for any bot.

Step 4. Set per-bot connector limits in the platform.
For each bot, in this order (tighten before you remove): 1) change write to read only where the target says read only, 2) restrict each app to the right account, 3) turn off every app the target does not list. Agent messaging is not an app: it stays on for every bot.
For each bot, tell me exactly where to click in the platform: that bot's connector or "Connect apps" settings, then the app, then read only or read and write, then the account. If the platform has no per-bot limit, tell me plainly, say which rules will be prompt-only, and suggest the safest fallback (one account per area).
STOP 2, once per bot. Show: bot, app, from, to. Wait for my yes. I make the change myself and tell you "done". Then you re-ask that bot (SendToAgent) to list what it can use now, and confirm it matches. Write the previous setting in your notes (aliases only) so I can undo it.
Never turn on an app I have not connected. Never connect an account for me.

Step 5. Rewrite each bot's connector block.
First send the Factory its new standing rules: the text in Part 2 of https://raw.githubusercontent.com/austinmao/zero-human-starter-pack/main/GROKBOT-UPDATE.md. Ask it to confirm.
Then ask the Factory, with SendToAgent, to update each bot from the new INSTRUCTIONS.md in the pack. Rules for the Factory:
- Keep everything personal: my name, account tables, voice cards, aliases, notes.
- Replace only: the "What you connect to" section with the "Route to me when" and "Connector access (least privilege)" sections, and the line that sent code and GitHub work "through the Orchestrator" with the agent-messaging wording.
- For a custom bot, write its connector block and roster row from its job, using CONNECTORS.md as the example.
- Never overwrite or delete a bot without my yes. Never touch the Life bots' private data.
STOP 3. The Factory shows one table first: bot, what changes, any personal text it would touch (should be none). I answer once: "OK to update all of them?" After my yes it updates the bots one at a time, then asks each bot to say its name, what it owns, and its connector table, to prove it took.

Step 6. Fix the orchestration wiring.
1. Replace your own instructions with the new Orchestrator text. Keep my name, your name, and my accounts table. Add the last column ("Bots that may read it") from CONNECTORS.md.
2. Make sure every bot can message back to you and to the owner bots it needs (you proved they can receive in Step 2). Agent messaging stays on for every bot.
3. Stop using any file as the way a job is delivered. A shared HANDOFFS file may stay as a log. A job exists only when you sent a message.
4. From now on every delegation has four parts: goal, scope and limits, expected output, done means. You verify the result against done means. You never accept "done" without proof.
5. Simple asks go to one bot. Do not fan out for a simple job.

Step 7. Routing test.
Run every test in ROUTING-TESTS.md as a dry run: name the bot you would choose, send nothing. Give me the score and a table of failures: request, expected, what you chose. For each failure, propose a fix to that bot's route-here or not-when line. STOP 4. Wait for my yes before the Factory edits any line. Then run the tests again until all pass.

Step 8. Access test, one allowed read and one refused read per bot.
For every bot, ask it with SendToAgent:
  (a) Allowed: do one read in an app on its list. Show only names, dates or counts. Expect success.
  (b) Refused: try one read in an app that is off for it. Never test with a write. Expect the platform to refuse. A bot that only says "I should not" without being blocked is a FAIL, because the limit is not in the platform.
Give me one table: bot, allowed read, refused read, result (pass, fail, could not test). For every fail, go back to Step 4 for that bot. Never run a write as a test.

Step 9. Report.
Give me one report: what changed per bot, the final bot x app x access x account table, routing score, access test results, anything prompt-only, anything custom, and what needs my decision. Say "done" only if every bot passed Steps 6 to 8. Otherwise say what is left.
Then ask me if I want the report and the final table saved in `my-agents` (through the Code bot). No keys, no private data.
```

## Part 2. What your Factory does from now on (the Orchestrator sends this in Step 5)

The Orchestrator sends the Factory this message in Step 5. You do not paste it. It is here so you can see what the Factory is told.

```
New standing rules for you from now on.
1. Every bot you create or change gets a connector block (a table: app, read only or read and write, account; default off; the owner bot for every write it does not own) and a roster row (one "route here when" and one "not when" line that do not overlap another bot). Show both to me before you build.
2. Each app with side effects has one owner, as in the owner list in bots/CONNECTORS.md. If two bots would write to the same app, stop and ask me.
3. Other bots read apps directly, read only, on the right accounts. They ask an owner bot only for a write, with SendToAgent.
4. Tell me exactly which per-bot connector limits to set in the platform. I click them. You never widen access yourself. If the platform cannot limit a bot, say so.
5. Tell the Orchestrator about every new or changed bot, with its roster row, so it re-runs the routing tests.
6. Use bots/CONNECTORS.md and bots/ROSTER.md in the pack as the reference. Keep my edits.
Confirm you have taken this, and say it back to me in three lines.
```

## If something goes wrong
- **A bot will not reply to SendToAgent.** Open its chat and ask it to remember that it can message the Orchestrator. If it still cannot, rebuild only that bot with the Factory, after my yes.
- **The platform cannot limit one bot's apps.** Keep the table, use one account per area, and treat the bot text as the weaker safeguard. Say so in the Step 9 report.
- **A refused read succeeded.** The limit is not set. Go back to Step 4 for that bot.
- **A bot lost a connection when you tightened it.** Use the previous setting your Orchestrator wrote down in Step 4. Reconnect it yourself.
- **Not sure about a custom bot.** Leave its access as it is, mark it "custom, review later", and carry on.
