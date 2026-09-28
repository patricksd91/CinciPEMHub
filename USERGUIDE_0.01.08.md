# CinciPEM ShiftMate: user guide

**Version:** 0.01.08

> *This skill is not managed by Cincinnati Children's Hospital. Per policy, do not give it protected health information (PHI) or sensitive or confidential information (such as your username or password), or access to that information. This tool uses AI, which can make mistakes. You are responsible for verifying all information.*

This guide explains what the skill does and how to use it. To install it, see the [README](README.md). If you're new to Claude, start with [Setting up Claude](CLAUDESETUP.md).

**Version 0.01.08 is an alpha:** an early preview for a small group of testers, not for general use. Some features may change before the first beta.

## The basics

You talk to Claude in plain language, and Claude asks one question at a time, usually with buttons to press. You never have to use the buttons: you can always type your answer in your own words, like *"any weekday in October except the 14th."* Where it makes sense, the last button is **Something else (type it below)**.

Behind the scenes, a small program inside the skill reads the ShiftAdmin schedule and checks every option against the division's rules. Your schedule never gets pasted into the chat.

Use the Claude desktop app. The skill keeps your settings, preferences and unsent feedback in a Local Data folder on your computer (a folder named CinciPEM ShiftMate Local Data in your home folder, made by the ShiftMate desktop extension), so it needs the desktop app; Claude in a web browser (claude.ai) can't reach that folder.

To start, open a new chat and say something like **"I'd like to trade a shift"**, **"switch my Thursday shift to Liberty"** or **"find moonlighting shifts I can pick up."** If you say more up front ("trade my 11/25 overnight, I'll work anywhere"), Claude remembers it and won't ask again.

The skill has three workflows (a workflow is one kind of task, from start to finish):

| Workflow | What it does | Who can use it |
|---|---|---|
| **Trade Shifts** | Finds colleagues who can take your shift and shifts they could give you back. Also gives away or trades an ML shift | Everyone |
| **Swap Locations** | Moves a shift to a site you prefer, same day | Beta and alpha testers |
| **Pickup Moonlighting** | Finds the open moonlighting shifts you're allowed to pick up | Beta and alpha testers |

Each workflow's steps have a name and a number, like "Availability (Trade Shifts 3)". The name always stays the same; the numbers may change between versions.

Every trade it suggests follows these rules for both people:
- at least 8 hours off between shifts (Jeopardy and moonlighting count)
- no more than 7 days in a row
- each person's eligibility by site and level (faculty, clinical staff, APP, fellow year)
- nobody is offered a shift on a vacation day or a date they've blocked
- no back-to-back shifts, unless that person has turned them on (see Back-to-back shifts below)

**Ask me why.** You can ask Claude why anything happened, like *"why wasn't Dr. Example offered?"* or *"why can't I pick up that shift?"*, and it will explain, listing every reason the program found. If you notice a mistake, say so; Claude will try to fix it and note it as feedback.

## When you start the skill

The skill always starts the same way, even if your first message already says what you need. Claude keeps your request and gets to it as soon as the start is done, without asking again.

1. **Title, known issues and privacy notice:** the skill's name, the version (for example "v0.01.08 alpha") and when you installed it, any known issues in this version in one line (you can ask about any of them), then the privacy notice above. All of this comes before the passphrase.
2. **Passphrase:** the first time, and after a new version with a new passphrase.
3. **Welcome:** a welcome line with your name and role, and a short introduction.
4. **Other chats:** if you have the skill open in another chat, Claude tells you when that chat started and what it was doing, so you can find it. You don't have to close it, but using one chat at a time avoids mix-ups.
5. **Updates and news:** whether a newer version is out, and what's new if you've just updated.
6. **Demo or test mode**, if you asked for one (see below).
7. **Your role**, only for people who are both clinicians and administrators: "Which role are you working in today?" **Clinician** / **Administrator**.
8. **Questions that are due:** for example checking your role once a quarter, or preferences you asked to be asked about again.
9. **Which workflow** you'd like, unless you've already said.

## First time: setup (about 5 minutes)

Claude tells you how many questions setup has and about how long it takes. You only do it once.

1. **Name check (Setup 1):** your first and last name, checked against the division roster. If Claude finds a close match, it asks "Did you mean …?". After three names that aren't on the roster, setup pauses for 24 hours (Claude warns you before the last try). New to the division, or changed your name recently? Ask the maintainer to add you. The skill is only for staff employed by the Division of Emergency Medicine right now.
2. **Help level (Setup 2):** *Walk me through everything*, *Standard*, or *I'm an advanced user*. You can change this any time.
3. **About You and Role Check (Setup 3):** the name people call you, your credentials (MD, DO, NP, PA-C …), your cell, email, how you'd like colleagues to reach you about trades, and your role and permissions (for example "Faculty, Standard Clinical Staff permissions"). This opens as a page beside the chat. Check it, press **Save** (which copies one line), then paste that line into the chat and send it. If the page doesn't open, Claude asks the same things in the chat. If your role isn't right, you can correct it (the schedulers still have the final say). Your answers are used right away and sent to the maintainer so the roster can be corrected.
4. **Usage data and plan (Setup 4):** Claude mentions that usage data is on, which also means your feedback is sent automatically (see Feedback below), and asks which Claude plan you're on (Free, Pro and so on), so we can see how the skill works on each.
5. **Allowed websites and the beta (Setup 5):** Claude may ask whether you'd like to try new features early (the beta program). Then it quickly checks that it can reach the three websites the skill needs. If they all work, one line says so. If not, Claude offers to walk you through adding them and checks again after each fix, or you can go on without them (Claude tells you once what that limits). See [Claude may ask for permission](#claude-may-ask-for-permission).
6. **Location and Shift Time Preferences (Setup 6):** a page beside the chat where you rate each site and each of the 11 shift times from 1 to 9 (1 strongly prefer not, 3 prefer not, 5 neutral, 7 prefer, 9 strongly prefer), no two the same. An 8 counts twice as much as a 4, so keep ratings close together if you don't mind much, and spread them out if you do. The 11 shift times are weekday day, Mon–Thu evening, Friday evening, weekend day, weekend evening, Mon–Thu overnight, Friday overnight, weekend overnight, holiday day, holiday evening and holiday overnight. As with the page before, press **Save** and paste the line into the chat. The starting ratings are only a guess, so check them. You can also choose "no preference" or "ask me again next time." Your shift-time order ranks trades, and every list of sites follows your location order.
7. **Back-to-back shifts (Setup 7):** "Should I include back-to-back shifts for you (up to 12 h 15 min in a row, the most the division allows)?" **No** (the default), **Yes, but only if I ask for it**, or **Yes, and let others ask me to work back-to-back shifts**. **Yes, but only if I ask for it** means back-to-back options are included in your own searches, but colleagues' searches never offer them a trade that would give you a back-to-back. **Yes, and let others ask me** means both. **No** means neither (you can still ask for back-to-back shifts in one search).
8. **Dates you can't work (Setup 8):** vacations not yet in ShiftAdmin, one-time conflicts, and recurring ones ("every Wednesday day shift"). Each can be a whole day, one shift time, or exact hours. You can also tell Claude about a ShiftAdmin vacation day when you're actually free. If you give one shift time ("12/9 evening"), only that shift time counts; Claude tells you this and checks that's what you meant.
9. **Save and check (Setup 9):** Claude saves everything, checks nothing is missing, and says setup is done.

## When there's a new version

The first time you start a new version, Claude shows your saved settings: **Looks right**, **Change something** or **Start fresh**. Standard and advanced users see them all at once; with *Walk me through everything*, Claude goes through them one at a time. Your location and shift-time ratings always come back on the ratings page to confirm. **Start fresh** runs setup again from the beginning; Claude first says what will be cleared and asks you to confirm.

In 0.01.08, holiday is now three shift times (day, evening and overnight). Your old Holiday rating now applies to all three (moved by 0.01 where needed so no two are the same). Please check them on the ratings page.

## Trade Shifts

1. **Who it's for (Trade Shifts 1):** usually you. See [Run it for a colleague](#run-it-for-a-colleague).
2. **The shift (Trade Shifts 2):** give the date. Claude shows your shift that day, or tells you if you're not working. It asks extra questions only when they apply:
   - **Jeopardy:** Jeopardy only, or would you take a scheduled shift?
   - **Holiday or pre-scheduled peri-holiday:** which kinds of shifts you'd take in return (including regular shifts only)
   - **Moonlighting (ML):** give it away (Claude shows everyone who could take it, grouped by level, and you pick who to ask), or trade it for another ML shift
3. **Availability (Trade Shifts 3):** when you could work instead: a few dates, a few ranges, or "any time." Claude checks your schedule and blocked dates and shows the **days you're available and there are shifts you could trade into**, counting only shifts you're allowed to work. It tells you which days or times it left out and why.
4. **Settings (Trade Shifts 4):** sites, shift times, whether you'd take a longer shift, whether a colleague may, and which kinds of trades to show:

   | Category | What it means |
   |---|---|
   | A. Win-win | Better for both of you |
   | B. Even (1:1) | Same shift time both ways |
   | C. Colleague gains | Better for your colleague |
   | D. Colleague even | About the same for your colleague |
   | E. Colleague loses | Worse for your colleague |
   | F. Lose-lose | Worse for both |

   - **Your usual and your most recent:** after your first search, Claude asks whether to make those settings **your usual**. The settings of your last search are kept as **your most recent**. When you come back, you can start from either.
   - **Summary mode:** once you have a usual, Claude can show all your saved settings at once instead of one question at a time. Claude offers it from time to time; you can always choose **Let's go through these one-by-one instead**.
   - **Show me everything:** if you have a usual saved, you can say "show me everything" for a wide search, then narrow it by site, shift time (any mix, like "weekend days and weekday evenings"), category, length or date. Say "make this my usual" if you'd like the narrowed settings to become your usual.
   - Anything added only because your shift is a holiday (holiday shift times, or category E) is used for that search only and never saved as part of your usual.
5. **Search (Trade Shifts 5):** Claude searches. A slow step comes with a short "one moment" line.
6. **The list (Trade Shifts 6):** first a table with your shift times as rows (in your order) and sites as columns (in your order). Each box shows the total, then how many are good for both or even (A+B), good for your colleague (C+D), and worse for your colleague (E+F); a dash means a shift time you didn't choose or narrowed out. With 12 options or fewer, the list follows, grouped by category, like `10/21 Wed B 9aE 0900-1700 (Example, A.)`. With more, you can **Display all** or **Narrow it** (by site, shift time or category).
   - Claude always checks every site you're allowed to work, and tells you how many more options there are at sites you left out.
   - Options on the same day you're giving up are marked "(same day)": they'd change your site or time, not give you the day off.
   - With fewer than 10 options, Claude shows how many you'd get by loosening one setting at a time (only changes that actually add options; allowing back-to-back shifts is always the last suggestion). You choose what, if anything, to change. If nothing would help, Claude says "No search setting I can loosen would add more options." If no one fits at all, it says "No one fits these dates and settings." and asks what you'd like to do next.
   - Changes you make for one search stay with that search.
7. **Recipients (Trade Shifts 7):** pick the colleagues to contact. If you've asked someone about the same shift before, Claude mentions it.
8. **Delivery (Trade Shifts 8)** and **Draft (Trade Shifts 9):** how to send, then the messages (see Messages below).
9. **Sent or not (Trade Shifts 10)** and **Your usual (Trade Shifts 11):** Claude asks whether you sent the requests, and, if this search used different settings from your usual, shows both side by side and asks whether to update your usual (**Update my usual**, **Keep my old usual** or **Keep some of them**).

Giving away an ML shift skips Availability, Settings and Your usual, and goes straight to who can take it.

## Swap Locations

*For beta and alpha testers.* Tell Claude which sites you'd like to leave. Claude suggests the sites you rated higher than all of those, with your ratings, and asks "Are these still right?" **Use these** / **Change them**. Then give the dates (or "all future dates"), and Claude tells you how many of your shifts that covers. Then it finds same-day trades that move you, shown the same way as trade results (the table's columns are the sites you'd accept), with suggestions if there are only a few. Moonlighting and Jeopardy shifts aren't included. Swap Locations will be redesigned in a later version.

## Pickup Moonlighting

*For beta and alpha testers, for your own shifts only.*

1. Download the Available Shifts file from ShiftAdmin (**Schedule → Available Shifts → Excel version → Download Excel file**) and attach it to the chat.
   <!-- SCREENSHOT: ShiftAdmin Available Shifts, Excel version -->
2. Claude tells you the date of the file (the first date in its title row; if the title row has none, when the file was last saved, and Claude says so). If it's more than a day old, it asks **Use it anyway** / **I'll download a new one**, since open shifts change every day.
3. Give the dates you're interested in, plus the sites and shift times you'd work.
4. Claude lists only the open shifts you can legally take, by date and in your site order. Short-rest M3 shifts are listed separately, with a warning. Back-to-back shifts are left out unless you've turned them on; Claude says how many it left out.

This works best on a computer, since it needs the downloaded file.

## Run it for a colleague

If you chose *I'm an advanced user*, Claude asks who you're running it for; choose **Someone else** and type their name. At the Standard level, just say "run this for Dr. Example." Claude then uses their name instead of "you". Their preferences and blocked dates are saved separately from yours, and blocked dates you enter for them are never sent to update the roster. Pickup Moonlighting is only for yourself.

## For administrators

If you help clinicians find trades, you're set up as an administrator. Each time, Claude asks which workflow you'd like first, then, for Trade Shifts and Swap Locations, which clinician you're helping today, and works with that clinician's preferences and schedule. Emails are written from you on their behalf, with them copied. Anything you tell Claude about a clinician is used for their searches and sent to the maintainer for the roster.

If you're both an administrator and a clinician, Claude asks at each start which role you're working in today. As an administrator you skip your own profile, role and preference questions; as a clinician you use the skill like anyone else. Your clinician setup happens the first time you start as a clinician.

## Coming soon

Two workflows are on the way. If you pick one, Claude tells you what it will do and offers the others.
- **Call Off Helper:** find someone to take a shift at the last minute (for beta clinicians and administrators).
- **Schedule Inquiry and Planning:** ask questions about the schedule and try out changes (for administrators).

## Demo mode

To show someone the skill, type **"demo"** when you start it, or your name followed by "Demo" at the name check (for example "Alex Example Demo"). You still need the passphrase and a real roster name. Claude uses default settings, skips the setup questions and goes straight to finding a shift trade. Nothing you do in a demo is saved. If the live schedule can't be downloaded, the demo uses an archived copy of the schedule and says so.

## Test mode

Beta and alpha testers may be asked at startup whether they'd like to run this version's testing program, for the first week after a version comes out. You can also say **"start test mode"**. Claude walks you through each test, with its notes in a box headed TEST GUIDE, records what you say and what happened, and sends the results with your feedback. Before tests that need a fresh start, Claude saves a copy of your settings and puts them back at the end. You can stop at any time and send only what you've done.

## Messages

After you pick who to contact, Claude tells you how they like to be reached (each person's preference for up to 5 people, a one-line summary for more), then asks how you'd like to send, and warns you about anyone your choice doesn't suit. Then it drafts the messages in that format:

- **Bulk email:** one group email, with all the addresses ready for Outlook's To line and an **Open in Outlook** button.
- **Text individually:** a short text for each person with only their shifts, ready to copy.
- **Email individually:** a personal email for each person, each with an **Open in Outlook** button.
- **Each person's preferred way:** texts for people who prefer texts, emails for everyone else.

You can copy and paste any draft, or open it in your CCHMC email: the **Open in Outlook** button opens Outlook on the web in your browser with the email ready to send. Check it, then click Send. If clicking doesn't open your browser, right-click the button, choose **Copy link**, and paste it into your browser's address bar. Emails opened this way end with a one-line note about the skill, after your signature. If an email is too long for the button, Claude says so and gives you the text to copy and paste instead.

## Finishing up

When a task is done, Claude asks **"Anything else?"** **Another search** / **I'm done**. After I'm done:

1. **Blocked-date sharing:** if your blocked dates differ from what the roster has, Claude may offer to share them so colleagues can see when you're not available. Only the dates and shift times are shared, never what they're for. You choose; if you say no, Claude asks again only now and then.
2. **Your own feedback:** anything you'd like to pass on.
3. **Sending your feedback** (see Feedback below): with Auto-send on, at the end of every session; with it off, a reminder every third session, or right away when something critical came up.
4. **Closing:** the skill closes. To use it again, start a new chat and ask for it.

If you say "stop" or "bye" in the middle of a task, Claude asks: **Wrap up** (about a minute) or **Close now**. Nothing you've told Claude is lost either way. The skill also closes after an hour with no activity once finishing up has started.

## Updates

When a new version is out, Claude tells you when you start the skill, shows what changed, and offers **Update now** or **Not now**. Update now gives you a **Save skill** button; click it and you're done. Not now means Claude won't ask again for a day. You can also say **"check for updates"** any time.

Versions ending in .00 (like 0.02.00) are stable releases, and the others are betas. An alpha, like this version, is an early preview before a beta. If the automatic update can't connect, Claude walks you through downloading the new version from the [download page](README.md#download) and uploading it.

## Beta program

Beta versions get new features first, but they may not work perfectly. Installing a beta puts you in the beta program, and beta testers are always offered the newest version. Say **"join the beta"** or **"leave the beta"** any time. Installing an alpha works the same way; say **"leave the alpha"** to leave. Once you install a beta, you're not offered alphas unless you ask.

Beta testers are asked to send their feedback. Each time a tester doesn't (including choosing "save it for later"), it counts as a warning. After three, the next time Claude explains that declining again means leaving the beta program. Sending or downloading your feedback resets the count. You can rejoin any time. If you've left the beta, Claude asks once about each new beta, and you can install it just that once without rejoining.

## Feedback

You can give feedback at any time: say something like **"tell the maintainer that the list was confusing"**, or just point out a mistake. Claude notes it and passes it on at the end. If a problem stops you from going on, Claude offers to send it right away.

At the end of a session, Claude puts together your feedback, anything that went wrong, and usage data, and keeps it on your computer. With Auto-send usage data and feedback on (the default), it's sent to the maintainer at the end of every session. With it off, Claude reminds you to send it, or download it and email it, every third session (when three sessions' feedback is waiting), or right away when something critical came up. You can also ask to send it any time. A large send goes in a few numbered parts. It only includes what's needed to fix each item, never anyone's full schedule. Claude never writes a password, passphrase or username into your feedback, even when quoting you, and before anything is sent, downloaded or saved, the skill also removes anything that looks like patient information, a username or a password, and tells you if it removed something.

**Usage data** (how you use the skill: which features, your search settings, how many results you got, and which Claude plan and model you use) is sent automatically with your feedback by default (the setting is called *Auto-send usage data and feedback*). With it on, Claude asks at the end whether there's anything you'd like to pass on, then sends your feedback automatically when it's due. Say **"stop sending usage data"** any time; then Claude asks each time whether to send it, download it and email it to the maintainer, or save it for later. If sending fails, Claude keeps your feedback and tries again next time.

With each stable release, the skill thanks the people whose feedback and usage data helped, and tells you how yours helped. If you'd rather not be named, just say so.

### Is my feedback private?

Yes. Your feedback is encrypted on your computer before it leaves, then sent privately through GitHub, the site that hosts this skill and its feedback tool. Only the maintainer can unlock and read it. No one else, including GitHub, can see what's in it.

## Claude may ask for permission

While you use the skill, Claude or the Claude app may ask for permission to do something. Here is each one and why it matters. **Claude never asks for your ShiftAdmin username or password.** You can say no to any request, and you can always ask Claude why it's needed.

| Permission | Why the skill needs it |
|---|---|
| Running code (code execution) | The program that reads the schedule and checks the rules runs as code. Without it, nothing works. |
| Allowed websites: `www.shiftadmin.com` | To download the division schedule. Without it, attach the schedule file each time. |
| Allowed websites: `raw.githubusercontent.com` | To check for and install updates. Without it, update by hand from the download page. |
| Allowed websites: `api.github.com` | To send feedback privately. Without it, download the feedback file and email it. |
| Memory | To remember your passphrase and where your Local Data folder is, so you don't have to give them each time. Your settings are in the Local Data folder, not in memory. Without memory, Claude asks for the passphrase each time. |
| A folder on your computer (the Local Data folder) | A folder named CinciPEM ShiftMate Local Data that the ShiftMate desktop extension makes in your home folder (the folder with your user name; Mac: Finder, Go, Home), where the skill keeps your settings, preferences, blocked dates, request history, unsent feedback and logs, encrypted. If extensions are blocked, you can make the folder yourself and connect it as your Cowork working folder; Claude walks you through it. The skill can't run without it. |
| Saving the skill (the **Save skill** button) | To install an update in one click. |
| Opening a file you attach | For the Available Shifts file (moonlighting) or a schedule file. |

How to allow websites, code execution and memory is in [Setting up Claude](CLAUDESETUP.md#3-turn-on-three-settings).

## Your help level

During setup you choose how much guidance you'd like: **Walk me through everything**, **Standard**, or **I'm an advanced user**. With *Walk me through everything*, Claude offers Trade Shifts and tells you about the other workflows as they become available to everyone. Say **"give me more explanation"** or **"less explanation"** any time to change it. If Claude uses a word you don't know, ask. If you use a word Claude doesn't know, it'll ask you what you mean and remember it.

## Troubleshooting

| What you see | What to do |
|---|---|
| Claude says the schedule can't be downloaded | Add `www.shiftadmin.com` to allowed websites ([how](CLAUDESETUP.md#3-turn-on-three-settings)), or attach the schedule file when Claude asks |
| Claude asks for the passphrase again | Memory may be off, or a new version uses a new passphrase. After 5 wrong tries, the passphrase pauses for 24 hours |
| Setup says your name isn't on the roster | Check the spelling; use your first and last name. After three tries it pauses for 24 hours; ask the maintainer to add you |
| The page beside the chat didn't open | Say so; Claude asks the same questions in the chat |
| Nothing happens after pressing Save on a page | Save copies one line. Click in the chat box, paste (Ctrl+V on Windows, ⌘V on a Mac) and send it |
| Swap Locations or Pickup Moonlighting isn't offered | They're for beta and alpha testers in this version. Say "join the beta" if you'd like to try them |
| Updates never show up | Add `raw.githubusercontent.com` to allowed websites, or check the [download page](README.md#download) |
| Feedback can't be sent automatically | Add `api.github.com` to allowed websites, or download the feedback file and email it |
| Clicking Open in Outlook doesn't open your browser | Right-click it, choose Copy link, and paste it into your browser's address bar |
| Something looks wrong | Say so in the chat. Claude will try to fix it and note it as feedback |
