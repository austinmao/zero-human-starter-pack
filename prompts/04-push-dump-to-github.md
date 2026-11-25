# 04: Save a knowledge dump to GitHub

You have the dump text from prompt 03. Choose ONE of the two ways below.

## Way A: ask the Code bot (try this first)

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

1. Save each block as a file on your computer with the right name.
2. Open your `my-agents` repo on github.com.
3. Go to `knowledge/`, click **Add file** > **Upload files**.
4. Drag your files in, and click **Commit changes**.
