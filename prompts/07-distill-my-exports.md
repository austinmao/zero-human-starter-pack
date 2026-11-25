# 07: Turn your exports into short handoff notes

Your exports are big and private, so they stay on your computer. This prompt turns the tier 1 projects into one short note each. Only those notes go to GitHub.

Use **Claude on your computer** (Claude Cowork or Claude Code), and give it access to ONE folder that holds your unzipped exports. Grok Bot cannot read files on your computer.

Before you start:

1. Unzip your Claude export and your ChatGPT export into separate folders inside one parent folder, for example `exports/claude` and `exports/chatgpt`.
2. Have your filled-in inventory table from prompt 06 ready.

```
I unzipped my Claude and ChatGPT exports into the folder you can see. Turn them into short handoff notes. Do not copy the raw exports anywhere.

Only work on the tier 1 items in my inventory:

[PASTE YOUR INVENTORY TABLE]

For each tier 1 project, write one file called handoff.md with these sections:
1. What this project is for (5 lines at most)
2. The standing instructions I gave it, word for word if they are in the export. If they are not, write "Not in the export: I will paste it."
3. Decisions made, each with its date and the reason
4. Open questions and next steps
5. Names of the files that belonged to the project (names only)

Rules:
- If the export does not show which project a chat belonged to, group chats by title and ask me to confirm the grouping before you write anything.
- Never include passwords, API keys, card or bank numbers, ID numbers, health information, or private details about other people. If you see any, tell me where and leave it out.
- Write "unsure" instead of guessing.
- Save the files in a new folder called my-agents-upload, as my-agents-upload/knowledge/<project-name>/handoff.md. Do not change or delete anything else.
- When you finish, list every file you made with its word count.
```

Then read each note yourself. Fix anything wrong, then save them with `04-push-dump-to-github.md`.
