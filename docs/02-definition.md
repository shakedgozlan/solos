# 02 · Definition (MVP)
> Summary: step 2a, the MVP feature list, rewritten on 2026-11-20 from Shaked's own description of a good day with Sol. Scope B is approved (#22): talk or paste text to Sol, confirm what it understood, and see calm, cumulative progress on health, learning and money. Mornings show what can be moved today; Saturday evening shows how patterns changed. **One open decision: whether Sol holds tasks in the MVP.**

Status: scope B approved (#22, #23); rewritten from Shaked's answers, tasks decision open · Writer: Product strategist, Opus 5.5 · Reviewer pass: Opus 5.5 (high), 2026-11-20
Builds on: [00-brief.md](00-brief.md), [01-discovery.md](01-discovery.md), [decisions.md](decisions.md), principles P1-P17 in [1b](research/1b-behavior-science.md#2-design-principles-for-sol). "#n" means line n in decisions.md.

## In Shaked's words (2026-11-20)
| Question | Shaked's answer | What it changes |
|---|---|---|
| Morning | Today's tasks; my goals; can I do something on a goal today, or does it just grow with time; continue what I started; short tips, not 20-minute reads | Today screen (10), goal types (5), tasks decision |
| During the day | Not sure. With Instinct I talk when I need something, like adding a task I just got details on. What do people usually expect from apps like this? | Usage rhythm below; tasks decision |
| End of week | Saturday evening, not Sunday. A good week = I can see my patterns changing (ordered out 4 times last week, less now) | Weekly review (13) |
| Would delete it if | It feels like fighting it, annoying, frustrating | P19 |
| Extra | Text too: paste a lecturer's message and get tasks, instead of reading it aloud. As little work as possible | Capture (1) |
| Tips | Instinct already sends them, so not in the MVP | Learning drops moved to Later |

**Usage rhythm (Assumption: based on how habit and journaling apps are built, not measured):** Sol is designed for two visits a day, morning (see the day) and evening (log the day), plus quick captures whenever something comes up. It must never need more.

## Feature list
**From:** *Shaked* = Shaked asked for it; *Claude* = Claude added it from research; *Both* = Shaked's goal, Claude's way of doing it. **Priority:** Must = in the MVP; Should = in the MVP, first to cut; Later = after the MVP.

| # | Feature | What it does | From | Priority |
|---|---|---|---|---|
| 1 | **Voice or text capture** | One big record button on every screen; or paste or type text (a lecturer's message, a note). Audio is saved first, then transcribed (ElevenLabs Scribe, #17), with a rough live preview (Assumption: Scribe's live mode or phone dictation can show it) | Shaked | Must |
| 2 | **Understanding step** | AI turns what Shaked said or pasted into entries: amounts, categories, Hebrew-lettered English fixed. One note can make several entries (P8). A feeling ("tired, stressed") becomes a mood entry (#23) | Claude | Must |
| 3 | **Read-back card** | Shows what Sol understood; fix by voice or tap, or ignore and it saves (P9) | Claude | Must |
| 4 | **One entry stream + history** | Every entry in one shared list; areas are views of it. Scroll, edit, delete | Claude | Must |
| 5 | **Goals** | Each goal: long target, this week's step, one if-then plan (P1). Each goal is marked **"today"** (something Shaked can do today) or **"growing"** (moves with time, nothing to do today), so the morning shows only what can be acted on | Both | Must |
| 6 | **Smoking** | Quit date and countdown, pills, cigarettes logged, smoke-free days and money not spent | Both | Must |
| 7 | **Money** | Spending by voice or text (eating out its own category), "left to spend", 1 or 2 named savings goals | Both | Must |
| 8 | **Food and weight** | "Ate out / cooked at home" (counts for money too), weigh-ins, weekly trend | Both | Must |
| 9 | **Reading** | Current book, chapter a day (#18), more is a bonus | Shaked | Must |
| 10 | **Today screen** | Top to bottom: today's tasks (if the tasks decision says yes), calendar events, goals marked "today" with their step, "continue where you left off", one progress line per area | Shaked | Must |
| 11 | **Notifications** | Morning push and at most one evening check-in; Shaked picks times (P12). iPhone/iPad with iOS 16.4+, once Sol is on the Home Screen | Shaked | Must |
| 12 | **Welcome-back flow** | After a gap or slip: "Welcome back", a one-sentence re-plan, never a missed-days count (P4) | Both | Must |
| 13 | **Weekly review, Saturday evening** | Five minutes by voice. Sol shows how patterns changed against Shaked's starting point and last week ("ate out 4 times a week before, once this week"), Shaked reacts, Sol adjusts next week's steps; ends with one reflection question (#23) | Both | Must |
| 14 | **Short-term achievements** | Few weekly wins ("cooked at home 4 times"), no points (P7) | Shaked | Must |
| 15 | **Learning skills** | Minutes per skill, "What stuck?" after a session | Shaked | Must |
| 16 | **Mindfulness minutes** | "10 minutes of calm" by voice | Shaked | Must |
| 17 | **Export and import** | Export as Markdown and JSON; import a Markdown file through the read-back card | Shaked | Must |
| 18 | **Calendar in the morning** | Today's iCloud Calendar events on Today, read by Sol's server with an encrypted app-specific password. Risk: events Instinct failed to sync will be missing | Shaked | Should |
| 19 | **Tasks (light)** | *Decision open.* Add a task by voice or text, see today's tasks in the morning, mark done by voice. No reminders, no calendar writing | Shaked | ? |
| 20 | **Learning drops** | Short tips on Shaked's skills during the day | Shaked | Later (Instinct has it) |
| 21 | **Garmin** | Steps, sleep, workouts. Assumption: Garmin's program is for businesses and may refuse a personal project | Shaked | Later |
| 22 | **Long-term achievements** | 100 smoke-free days, first book, flight fund half way | Shaked | Later |
| 23 | **Spaced recall** | Old "What stuck?" answers come back at growing intervals | Claude | Later |

## Principles added for Sol
- **P18, already started** (Shaked's idea, #23): every goal starts with honest credit for what Shaked has already done (books read this year, money saved, pills bought), never fake progress. Endowed progress, Nunes and Drèze 2006 (Assumption: later studies show a smaller effect).
- **P19, never a fight** (Shaked, 2026-11-20): every correction takes one step; saying it again fixes it; anything can be skipped; Sol never asks twice. If a flow needs more than that, it is redesigned, not explained.

Always (already decided): Hebrew first with RTL and a toggle (#2); sign-in and sync on phone, iPad, computer (#12); installable web app (#21); calm tone, no "missed", "behind" or "failed" (#15).

## Build plan and cuts
Built in two steps (#22): features 1-10 usable on the phone by day 7 (Assumption: Claude's estimate), then 11-18 in week two. If time runs short, cut in this order: 18 calendar; then shrink 14 to 2 or 3 fixed wins; then shrink 17 to JSON export only. Note: #4's two weeks also cover Design, architecture and the real-use test (3c).

## Not in the MVP (non-goals)
- Reminders, calendar writing and a full assistant (v2, #9). Instinct keeps those.
- Any bank, card or account connection, ever (#11).
- Apple Health (needs a real app, #21), Notion, Google Calendar (#22).
- A full Mind and emotions area beyond mindfulness, mood entries and the reflection question (#23); Relationships (#10).
- Streaks, points, leaderboards, calorie or page counting, investments.
- Cross-area insights: needs months of data.

## Open
- **Tasks in the MVP (19):** Shaked's morning and daytime answers both start with tasks, but #9 left tasks in Instinct. Decision for Shaked.
- 2b: persona, jobs to be done, success metrics. 2c: user stories for every Must.
- For the real-use test (3c): weekly or monthly budget, notification count, rest day, savings pledge.

## Gate: ready for Design when
- [x] Shaked approved the MVP scope and non-goals (2a; #22, #23)
- [ ] Tasks decision (19)
- [ ] Every Must feature has a user story with acceptance criteria (2c)
