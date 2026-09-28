# Setting up Claude

**Version:** 0.01.82

About 10 minutes. Then go back to the [README](README.md#install) to install the skill.

## 1. Create a Claude account

1. Go to **[claude.ai](https://claude.ai)** and sign up with your email or a Google account.
2. If you used email, click the confirmation link Claude sends you.
3. Answer the short welcome questions.

## 2. Get the desktop app

**[Download the Claude desktop app](https://claude.com/download)** (Windows or Mac), install it and sign in. ShiftMate works only in the desktop app, not in a web browser or on a phone.

## 3. Turn on three settings

Open **Settings** (your name or initials, bottom left):

1. **Capabilities → Code execution and file creation:** on.
2. **Capabilities → Additional allowed domains:** add these three:
   - `www.shiftadmin.com` (the schedule)
   - `raw.githubusercontent.com` (installing and updating the skill)
   - `api.github.com` (sending feedback)
3. **Memory → Generate memory from chat history:** on. Claude then remembers your passphrase, so you enter it only once.

Claude may ask for other permissions while you use the skill; the [user guide](USERGUIDE_0.01.82.md#claude-may-ask-for-permission) explains each one. Claude never asks for your ShiftAdmin username or password.
