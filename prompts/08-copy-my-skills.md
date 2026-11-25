# 08: Copy your Claude skills

Your Claude skills are folders of instructions. Keep a copy in your private repo.

## Easiest way (no tools)

1. Go to claude.ai > Customize > Skills.
2. Open one of your own skills, click **...** next to the switch, then **Download**.
3. Repeat for each skill you want to keep.

## Faster way (Claude Code)

If you use Claude Code signed in with your Claude account, it already keeps a copy of your skills on your computer. Paste this into Claude Code.

```
Copy my own Claude skills into a folder I can upload to my private GitHub repo.

1. Look in ~/.claude/skills/synced/ and ~/.claude/skills/. Each skill is a folder that has a file called SKILL.md.
2. Skip Anthropic's built-in skills (pdf, xlsx, docx, pptx and similar). Copy only skills I made.
3. Copy each one, with everything inside it, to my-agents-upload/skills/<skill-name>/.
4. Search every copied file for anything that looks like a secret: API keys, tokens, passwords, private URLs with keys in them, card or bank numbers, phone numbers, email addresses.
5. Show me the matches with the file name. Do not edit or upload anything flagged. I will decide.

Do not change the originals. When you finish, list the skills you copied and the files you flagged.
```

Then save the folder with `04-push-dump-to-github.md`.

## Good to know

- The copy in `~/.claude/skills/synced/` is read-only in practice. If you edit it, a later sync can overwrite your change. Edit skills on claude.ai.
- This does not work if Claude Code is signed in with an API key. Use the easiest way above.
