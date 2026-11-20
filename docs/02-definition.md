# 02 · Definition (MVP)
> Summary: step 2a, the MVP feature list. **Recommended scope: B, "Voice loop + daily rhythm"**: one voice note becomes confirmed entries across smoking, food and weight, mindfulness, reading and learning, and money; Sol shows them as progress that never resets, opens each day with a brief that includes the calendar, reaches out with a morning push, and closes each week with a five-minute voice review. Persona, success metrics and user stories follow in 2b and 2c, after Shaked picks a scope.

Status: scope B approved by Shaked, 2026-11-20 (decisions.md #22); learning drops (19) added after, pending Shaked's OK · Writer: Product strategist, Opus 5.5 · Reviewer pass: Opus 5.5 (high), 2026-11-20 · Date: 2026-11-20
Builds on: [00-brief.md](00-brief.md), [01-discovery.md](01-discovery.md), [decisions.md](decisions.md), principles P1-P17 in [1b](research/1b-behavior-science.md#2-design-principles-for-sol). "#n" means line n in decisions.md.

## MVP in one sentence
Shaked talks to Sol once or twice a day in mixed Hebrew and English, confirms what Sol understood, and sees calm, cumulative progress on health, learning and money in one place, without typing.

## Ranked feature list
Ranked by how much Sol fails without it. **Priority** is for scope B: Must = the brief requires it; Should = wanted, has a fallback; Could = later. "A / B / C" shows which scope option includes it.

| # | Feature | What it does | Why it is in | Priority | A | B | C |
|---|---|---|---|---|---|---|---|
| 1 | **Voice capture** | One big record button on every screen. Audio is saved first, then transcribed (ElevenLabs Scribe, #17). Rough live preview while speaking (Assumption: Scribe's live mode, or the phone's own dictation, can show it) | The heart of the product; "audio never lost" (#15); typing is the deal breaker | Must | ✓ | ✓ | ✓ |
| 2 | **Understanding step** | AI turns the transcript into entries: amounts, numbers, categories, Hebrew-lettered English fixed. One note can make several entries (P8) | Speech gives text, not data (Insight 5); one note updates several areas (Insight 2) | Must | ✓ | ✓ | ✓ |
| 3 | **Read-back card** | Shows what Sol understood as editable chips; fix by voice or tap, or ignore and it saves (P9) | Speech errors are likely; a fix must cost less than a form | Must | ✓ | ✓ | ✓ |
| 4 | **One entry stream + history** | Every entry lives in one shared list; areas are views of it. A simple history to scroll, edit or delete | Data model before screens (Insight 2); changes stay cheap, unlike the earlier version | Must | ✓ | ✓ | ✓ |
| 5 | **Goals with three layers** | Each goal: long target, this week's step, one if-then plan, all set by voice (P1) | Strongest evidence (Insight 4) | Must | ✓ | ✓ | ✓ |
| 6 | **Smoking** | Quit date and countdown, pills taken, cigarettes logged, smoke-free days and money not spent (cumulative) | Pain 4; quit plan decided (#14) | Must | ✓ | ✓ | ✓ |
| 7 | **Money** | Spending by voice with category (eating out is its own), "left to spend" this period, 1 or 2 named savings goals fed by other areas | Pain 4; no bank links (#11); labeled goals work (Insight 7) | Must | ✓ | ✓ | ✓ |
| 8 | **Food and weight** | "Ate out / cooked at home" (counts for money too, P15), weigh-in by voice, weekly trend | Pain 4; low detail keeps logging alive (Insight 6) | Must | ✓ | ✓ | ✓ |
| 9 | **Reading** | Current book, chapter a day (#18), extra counts as a bonus | Shaked's own target | Must | ✓ | ✓ | ✓ |
| 10 | **Today screen** | Opens with: this week's steps, today's progress, one line per area, the last few entries | "A good day" in the brief; the one place to look | Must | ✓ | ✓ | ✓ |
| 11 | **Notifications** | Morning brief push and at most one gentle evening check-in; Shaked picks times (P12). Works on iPhone and iPad with iOS 16.4 or later once Sol is added to the Home Screen; Sol asks permission after a tap; a small server sends the scheduled pushes | Shaked asked for them; the brief's skip-a-week test needs Sol to reach out | Must | | ✓ | ✓ |
| 12 | **Slip and welcome-back flow** | After a gap or a slip: "Welcome back", a one-sentence re-plan, never a missed-days count (P4) | Never feel bad for missing a day (brief) | Must | copy only | ✓ | ✓ |
| 13 | **Weekly voice review** | Sunday, five minutes: Sol reads back the week, Shaked reacts by voice, Sol adjusts next week's steps (P5, P6) | Feedback beats tracking alone; the fresh-start moment | Must | | ✓ | ✓ |
| 14 | **Short-term achievements** | Few weekly wins ("cooked at home 4 times"), no points (P7) | The brief's "good day" includes achievements | Must | | ✓ | ✓ |
| 15 | **Learning skills** | Minutes per skill, "What stuck?" after a session (P16) | Learning new skills is an MVP goal (brief, #10) | Must | | ✓ | ✓ |
| 16 | **Mindfulness minutes** | "Did 10 minutes of calm" by voice; reuses the minutes log from 15 | "Start with mindfulness" is an MVP Health goal (brief, #10) | Must | | ✓ | ✓ |
| 17 | **Export and import** | Export everything as Markdown and JSON; import a Markdown file of notes or goals, which Sol turns into entries through the same read-back card | Brief success line: Sol "can take content in, add to it and export it" | Must | | ✓ | ✓ |
| 18 | **Calendar in the morning brief** | Today's iCloud Calendar events at the top of Today. Read by Sol's server, not the browser, with an app-specific password (needs two-factor sign-in, opens wider iCloud access, so stored encrypted) | The brief is calendar plus goals (#19). Risk: events Instinct failed to sync (#19) will be missing. Fallback: brief without calendar | Should | | ✓ | ✓ |
| 19 | **Learning drops** | Short research-based paragraphs on Shaked's chosen skills, sent as pushes during the day. Shaked picks how many (start at 3, up to 7) and can say "more like this" or "less". Each drop links to Shaked's skill goals and can be saved as a note | Shaked's favorite Instinct feature (2026-11-20). Sol can make it personal: it knows the skills goals and the "What stuck?" answers. Assumption: about $1/month of Claude API at 7 a day. Pure content, never a task, so it does not break P12 | Should | | ✓ | ✓ |
| 20 | **Garmin** | Steps, sleep, workouts on Health | Zero-typing body data. Assumption: Garmin's official developer program is for businesses and may refuse a personal project | Could | | | ✓ |
| 21 | **Long-term achievements** | Milestones: 100 smoke-free days, first book, flight fund half way | Brief parked it if the MVP starts with short-term only | Could | | | ✓ |
| 22 | **Spaced recall in the brief** | Old "What stuck?" answers return at growing intervals (P16) | Light learning boost; needs weeks of data first | Could | | | ✓ |

Always in every option (already decided): Hebrew first with RTL and a Hebrew/English toggle (#2); sign-in and secure sync across phone, iPad and computer (#12); installable web app (#21); calm tone with no "missed", "behind" or "failed" (#15).

## Scope options
| | A · Voice loop only | **B · Voice loop + daily rhythm (recommended)** | C · Full first version |
|---|---|---|---|
| Features | 1-10, 12 as copy | 1-19 | 1-22 |
| Build time (Assumption: Claude's estimate, build only) | About 1 week | About 2 weeks, tight | About 3 to 4 weeks |
| Shaked's project time | Lowest | Within 1-2 h a day | Over the target |
| What Shaked gets | Talk, confirm, see progress. Must remember to open Sol | Sol also reaches out (push, brief, learning drops) and closes each week | Everything in B plus Garmin data and long-term milestones |
| Main risk | Fails the brief: no push, no achievements, no export, and Sol only waits | Push server, calendar access, sign-in and sync all land in two weeks | Garmin may refuse; repeats the earlier version's "never finished" |

**Recommendation: B, built in two steps.** B is the smallest scope that meets the brief: a good day (brief, calendar, progress, achievements; tasks stay in Instinct, #9, #19) and the success test ("if Shaked skips Sol for a week, something is missing"), which needs Sol to reach out, not only wait. To keep the "never finished" risk low, A is usable on the phone by day 7, then 11-19 are added in the second week. Items 20-22 need outside approval or weeks of data, so they gain nothing by being early.

If time runs short, cut in this order (they move to the first update, not lost): 18 calendar (brief works without it); then 19 learning drops (Instinct keeps sending them meanwhile, #9); then shrink 14 to 2 or 3 fixed weekly wins; then shrink 17 to JSON export only, with import next.

Note: the two-week target in #4 also covers Design, architecture and the real-use test (3c). Assumption: B's build fits only if Design stays small (shared components, a few screens).

## Not in the MVP (non-goals)
- Sol's own AI assistant for tasks, reminders and calendar writing (v2, #9). Instinct AI keeps that job, including tasks sorted by importance.
- Any bank, card or account connection, ever (#11).
- Apple Health (needs a real app, #21), Notion.
- Google Calendar: after the MVP (#22).
- Mind and emotions (beyond mindfulness minutes) and Relationships areas (#10).
- Streaks, points, leaderboards, calorie or page counting. Investments.
- Cross-area insights ("you spend more on days you smoke"): needs months of data.

## Open for later Definition steps
- 2b: persona, jobs to be done, success metrics.
- 2c: user stories with acceptance criteria for every Must feature.
- Left to the real-use test (3c): weekly or monthly budget, notification count, rest day, savings pledge.

## Gate: ready for Design when
- [x] Shaked approved the MVP scope and non-goals (this step, 2a; #22)
- [ ] Every Must feature has a user story with acceptance criteria (2c)
