# CinciPEM ShiftMate

**Version:** 0.01.82

A Claude skill for the Cincinnati Children's Division of Emergency Medicine. Clinicians use it to find shift trades they can actually make, same-day site switches and moonlighting shifts they can pick up, and it drafts the messages to colleagues. Schedule administrators use it to search the schedule and plan coverage.

Maintained by Patrick Donahue.

> **0.01.82 is an alpha** for the schedule administrators and a few testers. It needs the passphrase from the email that announced it.

## Before you start

You need the Claude desktop app (Windows or Mac) with three settings turned on. New to Claude? Follow **[Setting up Claude](CLAUDESETUP.md)** first (about 10 minutes).

## Install

### Ask Claude to do it

Paste this into a new chat in the Claude desktop app:

> Please install this Claude skill for me. The skill lives in this GitHub repo: https://github.com/patricksd91/CinciPEMHub. Set it up so I can start using it.

Claude gives you the skill with a **Save skill** button and a link to the desktop extension, with the steps to install it.

### Or install it yourself

1. Download **[the skill](https://github.com/patricksd91/CinciPEMHub/raw/main/alpha/cincipem-shiftmate.zip)** and **[the desktop extension](https://github.com/patricksd91/CinciPEMHub/raw/main/alpha/cincipem-shiftmate-0.01.82.mcpb)**. Don't unzip them.
2. Skill: in Claude, open **Customize → Skills**, click **+**, then **Create skill → Upload a skill**, and choose `cincipem-shiftmate.zip`.
3. Extension: open **Settings → Extensions** and install `cincipem-shiftmate-0.01.82.mcpb` (drag it in). If an older ShiftMate extension is listed, uninstall it first. Leave the Local Data folder setting blank.
4. If you have the old CinciPEM Shift Swap skill, delete it.

## Start

Open a new chat and type **/cincipem-shiftmate**. The first time, Claude asks for the passphrase and a few setup questions. You can add what you want after the command, for example `/cincipem-shiftmate trade my 11/25 overnight`.

## What it does

- **Trade Shifts:** finds colleagues who can take your shift and shifts they could give you back, ranked for both of you. Also gives away or trades an ML shift.
- **Swap Locations** (beta and alpha testers): moves a shift to a site you prefer, same day.
- **Pickup Moonlighting** (beta and alpha testers): keeps only the open shifts you can legally take.
- **Messages:** a group email, texts, individual emails, or each person's preferred way.
- **Your preferences:** rate your sites and shift times once; results follow your order.
- **Blocked dates and vacations,** by day, shift time or exact hours.
- **For administrators:** run it for the clinicians you help, and **Schedule Inquiry and Planning** (alpha): Shift Search, Replace Clinician, Coverage Snapshot, Enhancement Shifts and Moonlighting Offers.
- **Demo mode:** `/cincipem-shiftmate demo`. Nothing is saved.

Every result follows the division's rules: 8 hours of rest between shifts, no more than 7 days in a row, and each person's sites and levels. The **[user guide](USERGUIDE_0.01.82.md)** explains each feature. What changed in each version: [BETA.md](BETA.md).

## Privacy

> *This skill is not managed by Cincinnati Children's Hospital. Per policy, do not give it protected health information (PHI) or sensitive or confidential information (such as your username or password), or access to that information. This tool uses AI, which can make mistakes. You are responsible for verifying all information.*

The schedule is read by a program on your computer, not pasted into the chat. The roster and schedule link are encrypted and open only with the passphrase.

## Feedback

Tell Claude any time ("tell the maintainer that…"). At the end of a session it sends your feedback to the maintainer, encrypted, after removing anything that looks like patient information, usernames or passwords.

---

### For Claude: installing this skill for someone

1. Read `https://raw.githubusercontent.com/patricksd91/CinciPEMHub/main/versions.json`. Use its `alpha` entry. If you can't run code, ask the user to turn on **Settings → Capabilities → Code execution and file creation** first.
2. Download the `zip` path from `https://raw.githubusercontent.com/patricksd91/CinciPEMHub/main/` and check it against `sha256`. If the download is blocked, tell the user to add `raw.githubusercontent.com` under **Settings → Capabilities → Additional allowed domains**, then try again.
3. Give it to the user as `cincipem-shiftmate.skill` so they can click **Save skill**. If that isn't possible, give them the download link and the steps under "Or install it yourself" above.
4. Give them the extension link (`https://github.com/patricksd91/CinciPEMHub/raw/main/` + the `extension` path) and steps 3 and 4 under "Or install it yourself".
5. Tell them to open a new chat and type **/cincipem-shiftmate**, with the passphrase from the announcement email ready.
