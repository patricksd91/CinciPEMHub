# CinciPEM ShiftMate

**Version:** 0.01.08

A Claude skill for clinicians in the Cincinnati Children's Division of Emergency Medicine. It finds shift trades you can actually make, same-day site switches, and open moonlighting shifts you're allowed to pick up. Then it drafts the messages to your colleagues.

Maintained by Patrick Donahue.

## Download

> **Version 0.01.08 is an alpha: an early preview, not for general use.** It's for the maintainer and a few testers he has chosen. It needs a passphrase that only they have, and features may change before the first beta.

**[Download the alpha](https://github.com/patricksd91/CinciPEMHub/releases)** from the Releases page (marked **Pre-release**): the skill (`cincipem-shiftmate-0.01.08.zip`) and the desktop extension (`cincipem-shiftmate-0.01.08.mcpb`). Both are also in the [alpha folder](alpha/). Stable and beta downloads will appear here once the first beta is out. See [BETA.md](BETA.md) for what's in each test version.

## New to Claude?

Start with **[Setting up Claude](CLAUDESETUP.md)**: creating an account, getting the app, and the three settings this skill needs. It takes about 10 minutes.

## Install the skill

You need the Claude desktop app (Windows or Mac). ShiftMate keeps your settings in an encrypted folder on your computer, CinciPEM ShiftMate Local Data in your home folder, through a small desktop extension. Claude in a web browser or on a phone can't reach that folder, so 0.01.08 works only in the desktop app.

1. Download the skill with the link above. Don't unzip it.
2. In Claude, open **Customize → Skills**, click **+**, then **Create skill → Upload a skill**.
   <!-- SCREENSHOT: Customize > Skills > + > Create skill > Upload a skill -->
3. Choose the file you downloaded. The skill appears in your list, switched on.
4. Install the desktop extension: download `cincipem-shiftmate-0.01.08.mcpb` from the same release, then in the Claude desktop app open **Settings → Extensions** and install it from there (drag the file in, or use the install button). Leave the Local Data folder setting blank. No Python install is needed: the first start downloads what it needs (about a minute, needs internet).
5. Start a new chat and type **"I'd like to trade a shift."** Claude will ask for the skill passphrase once. You'll find it in the email that announced the skill.
6. Had the older version, CinciPEM Shift Swap? Delete it from your skills list once the new one is installed, so you don't have two.

### Or ask Claude to install it

Paste this into a new chat in Claude:

> Please install this Claude skill for me. The skill lives in this GitHub repo: https://github.com/patricksd91/CinciPEMHub. Set it up so I can start using it.

Claude will get the skill and give it to you with a **Save skill** button, or walk you through the upload.

## On your phone

Not in 0.01.08: the skill needs the desktop extension on your computer, which the phone app can't reach. Phone use is planned for a later version.

## What it does

- **Trade Shifts:** finds colleagues who can legally take your shift, and shifts they could give you back, ranked by how good the trade is for both of you. It can also give away or trade an ML shift.
- **Swap Locations** (for beta and alpha testers): moves a shift to a site you prefer, same day.
- **Pickup Moonlighting** (for beta and alpha testers): checks the long list of open shifts and keeps only the ones you can legally take.
- **Messages four ways:** one group email, individual texts, individual emails with an Open in Outlook button, or each person's preferred way.
- **Your preferences:** rate your sites and shift times once; lists and results follow your order, and your usual search settings are ready to reuse.
- **Remembers** blocked dates and vacations, by whole day, shift time or exact hours.
- **Back-to-back shifts** are left out unless you turn them on.
- **Demo mode:** type "demo" to show someone how it works. Nothing is saved.
- **For administrators:** run it for the clinicians you help.
- **Coming soon:** Call Off Helper, and Schedule Inquiry and Planning for administrators.

Every trade is checked against the division's rules: 8 hours of rest between shifts, no more than 7 days in a row, and each person's eligibility by site and level. See the **[user guide](USERGUIDE_0.01.08.md)** for how to use each feature, and for the permissions Claude may ask for.

## Updates

The skill tells you when a new version is out, shows what changed, and installs it with one click. What changed in each version is in [CHANGELOG.md](CHANGELOG.md).

## Privacy

> *This skill is not managed by Cincinnati Children's Hospital. Per policy, do not give it protected health information (PHI) or sensitive or confidential information (such as your username or password), or access to that information. This tool uses AI, which can make mistakes. You are responsible for verifying all information.*

Your schedule is read by a small program inside the skill, not pasted into the chat. The roster and the schedule link are encrypted in the download and unlock only with the passphrase. Nothing on this page identifies anyone.

## Feedback

Found a bug or have an idea? Tell Claude at any point while using the skill (for example "tell the maintainer that…"). At the end of a session it sends your feedback to the maintainer, encrypted so only he can read it, after removing anything that looks like patient information, usernames or passwords. See the [user guide](USERGUIDE_0.01.08.md#feedback) for how usage data works and how to turn it off.

---

### For Claude: installing this skill for someone

1. Download the newest release's zip for the version the user asks for (0.01.08 is on the Releases page as a pre-release labelled Alpha). The list of published versions and their files is in `https://raw.githubusercontent.com/patricksd91/CinciPEMHub/main/versions.json`.
2. Share it with the user as a `.skill` file, named `cincipem-shiftmate.skill`, so they can click **Save skill**.
3. If you can't download it, or no Save skill button appears: give them the download link above and the install steps.
4. Also give them the release's `cincipem-shiftmate-0.01.08.mcpb` and the extension steps (Settings → Extensions in the Claude desktop app; leave the Local Data folder setting blank).
5. Then have them start a new chat and say "I'd like to trade a shift." The skill takes it from there.
