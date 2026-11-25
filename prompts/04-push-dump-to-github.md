# 04: Save a knowledge dump to GitHub

You have handoff notes (prompt 07), skills (prompt 08) or dump text (prompt 03). Choose ONE of the two ways below.

Before you save anything:
- Only upload to your **private** `my-agents` repo.
- Never upload raw exports, uploaded client files, or anything with passwords, keys or card numbers.
- Open each file and skim it. If you spot something private, remove it first.

## Way A: ask the Code bot (for text you paste in)

This works for dump text you paste into the chat. It cannot see a folder on your computer. If you have a folder (handoff notes from prompt 07 or skills from prompt 08), use Way B.

Paste this into your Code bot, followed by the dump text.

```
Save the following files into my private repo [YOUR-GITHUB-USERNAME]/my-agents, inside knowledge/[PROJECT-NAME]/.
Each block starts with a line like ===== FILE: name.md =====. Use that name for the file.

Rules:
- Only write into the knowledge/[PROJECT-NAME]/ folder.
- If a file already exists, show me the difference and wait for my OK.
- Never make the repo public.
- If you cannot write to GitHub, say so and do not try workarounds. I will upload by hand.
- Tell me the link to each saved file.

[PASTE THE DUMP HERE]
```

## Way B: upload by hand (always works)

1. Have your files ready on your computer: the `my-agents-upload` folder from prompts 07 and 08, or one file per dump block with the right name.
2. Open your `my-agents` repo on github.com.
3. Click **Add file** > **Upload files**.
4. Drag in the contents of `my-agents-upload` (the `knowledge` and `skills` folders). Check the file list, then click **Commit changes**.

If GitHub refuses a big drag, upload one folder at a time.
