# How to get your old work out of Claude and ChatGPT

Checked against the vendors' own help pages on 25 Nov 2026. Rules change, so if a screen looks different, trust the screen.

## Do this first: request both exports today

| | Claude | ChatGPT |
|---|---|---|
| Where | Settings > Privacy > **Export data** (web or desktop app, not the phone app) | Settings > Data controls > **Export data** > Confirm |
| Wait | A download link arrives by email | Up to **7 days** |
| Link lasts | 24 hours, and may work only once | 24 hours after you receive it |
| You get | Your conversation data and account data, including memory | A zip with a viewer (`index.html`), your conversations as JSON, and other data files |
| Not included | The original files you uploaded | Not stated in the help page. Check the zip before you rely on it. |
| Not available on | Phone app | Business, Enterprise and Healthcare workspaces (ask your workspace owner). Edu depends on your admin. |

Sources: support.claude.com article 9450526, help.openai.com article 7260999.

Download each zip the day the email arrives and keep it **on your computer**. Do not put raw exports on GitHub.

## What an export does NOT give you

| Thing | How to get it |
|---|---|
| Files you uploaded to a Claude project | No documented bulk download. Keep your own originals, or re-save them from the source. Test one project first. |
| Files in a ChatGPT project | Open the project's file list. Each file can be previewed and downloaded one at a time. |
| Project instructions | Copy the text from the project's settings page by hand. |
| Claude skills | Settings > Customize > Skills, open a skill, click **...** then **Download**. Or let Claude Code copy them (prompt 08). |
| Custom GPTs | Copy the Instructions text from the GPT editor. Knowledge files are not documented as downloadable, so find your originals. |
| Memory | Ask the assistant to list it (the prompt is in Claude's own help article), or open the memory settings and copy it. |

## Custom GPTs are being retired

OpenAI says custom GPTs are being replaced by plugins. The standard retirement date is **11 December 2026**. After a GPT is migrated, the original becomes read-only. Copy the instructions of every GPT you care about before then, and check the notice for your own account.

Source: help.openai.com article 8554397.

## Skills sync to Claude Code

If you sign in to Claude Code with your Claude account, it downloads your account's skills into `~/.claude/skills/synced/` on your computer. This is one way only (it never uploads). It does not work if Claude Code is signed in with an API key. Anthropic's own skills such as pdf and xlsx are in there too, so skip those.

Source: code.claude.com/docs/en/skills.

## Chat search inside a project

On paid plans, both Claude and ChatGPT can look up other chats **inside the same project**. So the per-project dump prompts (03) can see more than the one chat you run them in. Search is not a complete read, so treat the answer as a draft and check it against the export.

Sources: support.claude.com article 11817273, help.openai.com article 10169521.

## Not confirmed yet

Test each of these once on a single project before you rely on it:

- Whether the Claude export contains project instructions.
- Whether the ChatGPT export marks which project each chat belongs to.
- Whether Claude project knowledge files can be downloaded from the project page.
- Whether your Grok Code bot can save files to GitHub (the upload-by-hand route always works).
