# 03: Knowledge dump from a Claude project

Run this inside ONE Claude project at a time. It produces files you can save to your private `my-agents` repo.

Note: Claude's GitHub connector can only read from GitHub. It cannot write to it, so you save the result using `04-push-dump-to-github.md`.

```
I am moving this project's knowledge to a new system. Please produce a "knowledge dump" for this project only.

Create these four sections, each as its own clearly labelled block, in plain Markdown:

FILE 1: summary.md
- What this project is for, in one page.
- Who it is for, the main goals, and the current state.

FILE 2: instructions.md
- The project's custom instructions, copied word for word. If there are none, say "none".

FILE 3: decisions.md
- Every important decision made in this project's chats, each with a date if you know it, the reason, and anything still undecided.

FILE 4: files.md
- A list of every file in the project knowledge, with a one-line description of each. Do not paste the files themselves.

Rules:
- Use only what is in this project. If you are unsure, write "unsure" instead of guessing.
- Leave out passwords, API keys, bank details and anything private about other people.
- Start each block with a line like: ===== FILE: summary.md =====
```

Then copy each block into a file with that name, inside `knowledge/<project-name>/`.
