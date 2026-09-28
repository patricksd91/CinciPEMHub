# CinciPEM ShiftMate: beta versions

**Version:** 0.01.82

Beta versions try out new features before they reach everyone, and they may not work as expected. Each entry lists what changed since the release before it (beta or stable), then any known bugs that are still open. Stable releases are in CHANGELOG.md.

<!-- Entry format (the skill reads it): "## <version> — <YYYY-MM-DD>", then bullets. -->

## Known issues
<!-- The skill shows these at startup (at most 4 lines). Plain, user-facing words; "None" if there are none. -->
- Needs the ShiftMate desktop extension; hospital-managed computers aren't tested yet.
- During test mode, other ShiftMate chats on this computer use the test data too.
- Swap Locations is being redesigned for the next version.

## 0.01.82 — 2026-09-28
Alpha, for the schedule administrators. (Version numbers now end in two digits; 0.01.82 comes after 0.01.08.)
- New for administrators: **Schedule Inquiry and Planning**. **Shift Search** finds shifts by date, clinician, site, time, day, shift type and role, on a page beside the chat. **Replace Clinician** shows who could cover a departing clinician's shifts, and why the rest can't be covered. **Coverage Snapshot** shows who's working where. **Enhancement Shifts** lists nice-to-have shifts that could become core coverage. **Moonlighting Offers** lists open shifts to post and who could take them.
- Start the skill with **/cincipem-shiftmate**.
- The desktop extension now reaches the schedule, update and feedback sites itself.
- Setup uses less of your usage limit.

## 0.01.08 — 2026-09-27
Alpha: an early preview for a few testers, not for general use.
- New name: CinciPEM ShiftMate. Delete the old CinciPEM Shift Swap skill once this one is installed.
- The workflows have one name each: Trade Shifts, Swap Locations and Pickup Moonlighting. Swap Locations and Pickup Moonlighting are for beta and alpha testers for now.
- The skill always starts the same way (title and known issues, privacy notice, passphrase, welcome) and then does what your first message asked.
- Your settings, answers and feedback are kept encrypted in a Local Data folder in your home folder (CinciPEM ShiftMate Local Data), through the ShiftMate desktop extension. Claude's memory keeps only your passphrase and where that folder is.
- Setup has 9 named steps and tells you how many questions are left. Your details, role and ratings are on pages beside the chat: press Save, then paste the line into the chat.
- Sites and shift times are rated 1 to 9. Holiday is now three shift times (day, evening and overnight): your old Holiday rating now applies to all three holiday times. Please check them on the ratings page.
- Back-to-back shifts are left out unless you ask for them. Setup asks whether you'd like them.
- Blocked dates and vacation exceptions can be a whole day, one shift time, or exact hours.
- Trade Shifts: "your usual" and "your most recent" settings, summary mode, "show me everything", clearer messages when few or no trades fit, and every reason when you ask why someone wasn't offered.
- You choose how to send before Claude drafts the messages. An email too long for the Open in Outlook button comes as text to copy.
- Swap Locations suggests the sites you rated higher than the ones you're leaving.
- Pickup Moonlighting starts with the Available Shifts file and checks how old it is.
- At each new version, confirm your saved settings, change something, or start fresh.
- Demo mode: type "demo" to show the skill with default settings. Nothing is saved.
- Test mode: testers can say "start test mode" to run this version's tests.
- Give feedback any time ("tell the maintainer that…"). At the end, Claude asks "Anything else?", finishes up, and closes the skill. Each session's feedback is its own file. With Auto-send on, it's sent at the end of every session; with it off, Claude reminds you to send it (or download and email it) every third session, or right away when something critical is waiting. A big send goes in numbered parts.
- Administrators who are also clinicians choose their role at each start. Call Off Helper and Schedule Inquiry and Planning are listed as coming soon.
- The user guide has a new section: Claude may ask for permission.

## 0.01.07 — 2026-09-24
Test build (not published).
- A new title banner with your name, credentials and role.
- Setup checks your name against the roster (three tries), confirms the name people call you, your credentials, contact details and role, and asks you to rank and rate your locations and shift times.
- Sites are always listed in your order; results tables and lists follow it.
- Returning users see all their saved answers at once and can start right away.
- Availability now counts only shifts you're eligible for and says why a time of day was left out.
- Location switch explains thin results and suggests what to loosen.
- Answer buttons for every fixed choice, with "Something else" when it makes sense.
- Claude answers help questions from the user guide, learns your terms, and reminds you that you can ask "why".
- Feedback: privacy check before anything is sent, a clearer note on how it's sent, usage data on by default (you can turn it off), and thank-you messages with each stable release.
- Updates: a version ending in .00 is stable; beta testers always get the newest version.
- Administrators can run the skill for the clinicians they help.
- Outlook drafts end with a one-line note about the skill. Big group emails get more than one Open in Outlook button so each one works.
- Results say which options are on the same day you're giving up, and what would fill an empty row.
- Giving away an ML shift shows who could take it, grouped by level.
- Location switch tells you how many shifts it covers before asking the rest.
- When there's an update, you see what's new before deciding.
- If your first message already says what you need, Claude gets to it first.
