# 10: Connect WhatsApp with wacli (QR code)

**The Orchestrator walks you through this during setup.** Read on only if you want to do it by hand.

`wacli` is a command-line tool that links to your WhatsApp as a **linked device**, the same way WhatsApp Web does. You pair it once by scanning a QR code with your phone. After that the Messaging bot can read and search your chats, and send with your approval.

Source: https://github.com/openclaw/wacli (docs: https://wacli.sh). Third-party tool, not made by WhatsApp or Meta. WhatsApp can ban accounts that behave like spam, so keep the Messaging bot's limits.

## Choose where wacli runs

| | A. On your Mac | B. On the Bot's computer |
|---|---|---|
| Good for | Most people. You can see the terminal and the QR code. | When you want it running while your Mac is off. |
| Needs | Terminal on your Mac. Grok Bot desktop app with **Execution on this computer** set to ask each time. | The Code bot installs it. You watch the QR code in the computer view. |
| Not confirmed yet | Whether the Messaging bot can drive it from the desktop app. | Whether the QR code is readable in the computer view. |

Start with **A**.

## Route A: on your Mac

1. Open Terminal on your Mac.
2. Install: `brew install openclaw/tap/wacli`. (No Homebrew? Download the release for your Mac from https://github.com/openclaw/wacli/releases/latest. It needs macOS 15 or newer.)
3. Run: `wacli auth`
4. A **QR code** appears in the Terminal window.
5. On your phone, open WhatsApp:
   - iPhone: **Settings > Linked devices > Link a device**.
   - Android: the three dots **> Linked devices > Link a device**.
6. Point the phone camera at the QR code. Wait. `wacli` does a first sync after pairing.
7. If the QR code is hard to scan, run `wacli auth` again for a fresh one, make the Terminal window bigger, or use the phone-number pairing option in https://github.com/openclaw/wacli/blob/main/docs/quickstart.md.

## Route B: on the Bot's computer

1. Ask the Orchestrator: "Ask the Code bot to install wacli on your computer from https://github.com/openclaw/wacli/releases/latest and tell me when it is tested." Code installs it. You do not.
2. In Grok Bot, open the Messaging chat and ask it to run `wacli auth`. Open the **computer** from the conversation to watch the screen.
3. When the QR code appears, scan it from your phone as in step 5 above. If you are asked for anything else, use **take over** in the computer view. Do not type secrets into the chat.

## Check it works (read only)

Run these. None of them sends anything.

```
wacli doctor
wacli --read-only --json messages list --limit 5
```

`doctor` should report no problems. The second command should show your five newest messages. If both work, tell the Messaging bot the alias you want (for example `whatsapp-main`).

Then run `prompts/11-read-only-connection-test.md`.

## Keep it safe
- The folder `~/.wacli` (on Linux, `~/.local/state/wacli`) holds your WhatsApp session. Treat it like a password. Never paste it, print it or back it up to GitHub.
- To disconnect any time: on your phone, **Linked devices**, choose the device, **Log out**.
- Never send test messages. Test by reading.
- If WhatsApp ever shows a warning, a login prompt you did not start, or `wacli` reports logged_out or a ban, stop and tell the Messaging bot.
