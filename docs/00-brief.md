# 00 · Brief
> Summary: a personal, voice-first dashboard for Shaked that turns "I want to improve myself" into a clear daily plan, visible progress and short- and long-term achievements, without typing. For Shaked only.

Status: draft v1 (2026-11-19), from Shaked's Day 1 answers. Waiting for Shaked's approval.

## Vision
Every morning Shaked opens one place, sees what matters today and how far they have come, and keeps everything up to date by talking to it, not by filling forms.

## Why this project
- Personal reason: Shaked wants to grow on many fronts at once (skills, health, money, independence, emotional growth) and has no single place that shows priorities and progress.
- Portfolio goal: secondary. Usefulness in daily life comes first.

## What "improving myself" covers (Shaked's own list)
Grouped by Claude. Shaked has not yet ranked them.

| Group | What Shaked named |
|-------|-------------------|
| Learning and skills | Learn more, become a better self-learner, read more, tech skills, new useful skills |
| Goals and achievements | Complete goals; a set of achievements, one short-term and one long-term |
| Health and body | Routines, cook healthy food, lose weight, quit smoking |
| Money | Track spending, manage money well |
| Mind and emotions | Emotional and intellectual growth, better decisions, mindfulness, independence from outside approval |
| Relationships | Find a partner |

## How Shaked works today
- **AI voice assistant app** ("Instinct", Assumption: exact app name to confirm). Shaked's favorite tool. Shaked records a voice note and it does the rest: reminders, daily plan, daily summary, and it manages the iCloud calendar. "Useful 200 million times over" because nothing has to be written.
- **iCloud / Apple Calendar**: Shaked rarely uses a calendar directly; the AI app manages it through iCloud.
- **Garmin**: in use (Assumption: for fitness and body data such as steps, sleep, workouts).
- **Notes**: sometimes (Assumption: Apple Notes).
- **Mindfulness**: no tool today.

## A good day with the dashboard
1. Morning: open it and get a daily brief.
2. See today's tasks and reminders, sorted by importance (important, less important).
3. See what Shaked has done and any achievements earned.
4. See where there is room to improve and what needs attention.
Device and session length: not yet stated (open question).

## Constraints
- Deadline: none. Target a strong MVP in about two weeks, 1 to 2 hours a day of Shaked's time.
- Budget / tools: Max plan; Figma ("gozlans's team"); GitHub repo solos.
- Language and direction: Hebrew first (RTL), Hebrew/English toggle.
- Platform: not decided (open question). Assumption: phone first, because the morning brief and voice input happen on the phone.
- Input: voice first. Manual typing must be the exception, never the main path.
- Connections Shaked asked for: iCloud (Apple) Calendar, Google Calendar, maybe Notion.

## Suggested connections (Claude, for Shaked to choose)
Shaked asked for suggestions. Each needs a feasibility check in Discovery.
- **Garmin Connect**: workouts, steps, sleep, stress. Progress on health goals with zero typing.
- **Apple Health**: weight, steps, mindful minutes; one hub for data from Garmin and other apps.
- **The AI voice app's own data**: tasks and daily summaries, if it can export or share them. Without this, the dashboard sees calendar events only.
- **Speech-to-text inside the dashboard**: so a voice note can update a goal, log a meal, or mark a smoke-free day.
- **Bank or card statements** (later): money tracking from a monthly file instead of logging each purchase.

## Deal breakers
- Too much to write. If keeping it current takes typing, Shaked will stop using it.
- What Shaked wants instead: "someone I can talk to, and it does everything."

## Earlier attempt
- What existed: goals, notes, fitness tracking, all fairly broad.
- What did not work: Shaked can't say exactly yet ("something didn't work"). Screenshots will follow.
- Already decided (decisions.md #3): it was weak in design, code and usability, and is used only as a "what to avoid" reference.
- Claude's hypothesis (Assumption, to check against the screenshots): it was a manual-entry tool that covered many areas equally, so it took effort to keep up and gave no clear "what now". This matches deal breaker #1.

## Claude's critique (to discuss, not decided)
1. **The scope is very wide.** Six groups and about 20 goals. A dashboard that tracks all of them equally risks repeating the earlier version. Recommendation: the MVP covers 3 groups well, chosen by Shaked; the rest come later.
2. **Overlap with the AI voice app.** That app already does reminders, daily plans and calendar, and Shaked loves it. Rebuilding that is a large, separate product. But there is a tension: the Vision says "one place", and if the dashboard only reads the calendar, it sees events but likely not the app's tasks or summaries, which the morning brief needs (Assumption: depends on what the app can share). Options to decide in Discovery:
   - A. Complement it: the dashboard reads the calendar the app already fills, and adds what the app lacks (goals, achievements, progress, health, money, reflection).
   - B. Replace it: build our own voice assistant inside the dashboard.
   - C. Hybrid: the dashboard has its own simple voice capture for goal and progress updates, and leaves tasks and calendar to the app.
   First lean: A or C. Needs a check of what the app can export or connect to.
3. **"Talk and it does everything"** is the heart of the product, not a feature. It shapes Discovery: we need to test how voice input can update goals and progress reliably.

## Open questions
- [ ] Top 3 areas for the MVP (from the table above)
- [ ] Exact name of the AI voice app, and can it share data (calendar only, or more)?
- [ ] Phone, computer, or both? When in the day, and for how long?
- [ ] Earlier version: screenshots, and why it was dropped
- [ ] Complement, replace or hybrid with the AI voice app (decided in Discovery)
- [ ] Garmin and money data: connect automatically, or is a short voice note enough?
- [ ] Privacy: health, smoking, weight and money data are sensitive. Where may they be stored?
