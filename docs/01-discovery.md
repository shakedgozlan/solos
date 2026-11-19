# 01 · Discovery
> Summary: Shaked wants to improve health, learning and money at once, but most apps built for this ask for typing, punish missed days, or handle English only. Their favorite tool (Instinct AI) proves the real need: talk once and the rest happens. **Strongest insight:** no app turns one mixed Hebrew/English voice note into structured progress across several areas, and that is exactly what Sol should do. **Recommendation:** move to Definition with a voice-first MVP built on one shared stream of entries, ElevenLabs Scribe for speech, and progress that never resets.

Status: draft for the Discovery gate · Writer: Opus 5.5 (medium) · Date: 2026-11-19
Builds on: [00-brief.md](00-brief.md), [decisions.md](decisions.md)

## Problem space
**In one sentence:** Shaked has no single place that shows priorities and progress across health, learning and money, and every way of keeping one current costs typing, which is exactly why they stop.

- **What Shaked tries to do:** reach a target weight, quit smoking, eat out less, read and learn more, spend less, save toward named goals (brief, MVP goals).
- **What gets in the way:**
  - Typing and forms. "Too much to write" is the stated deal breaker (brief).
  - Guilt mechanics. Streaks that reset to zero make one missed day feel like failure, and a broken streak lowers motivation afterwards ([1b](research/1b-behavior-science.md), Moderate).
  - Language. No speech engine is proven on Hebrew and English mixed in one sentence; in Shaked's test even the best one wrote most English words in Hebrew letters ([1a](research/1a-voice-and-instinct.md)).
  - The earlier version: never finished, looked bad, and every change had to be made page by page (brief, Earlier attempt).
- **How Shaked copes today:** Instinct AI by voice for reminders, daily plan and calendar; iCloud Calendar through Instinct (a connection that often breaks); Garmin; notes now and then; nothing for money, reading or mindfulness.

## Audience
Sol has one user (decision #1), so the primary audience is already chosen: Shaked.

| Area | Need | Current tool | Pain (1-5) |
|---|---|---|---|
| Health: smoking | Quit (quit date after reserve duty, #14), see progress that a slip cannot wipe | None | 4 |
| Health: weight and food | Reach target weight, eat out less, cook more | Garmin (activity only) | 4 |
| Learning and reading | Read books, learn new skills | None | 3 |
| Money | Spend less, a budget that holds, named savings goals, no bank links (#11) | None | 4 |
| Daily plan and tasks | Morning brief, priorities | Instinct AI (by voice) | 2: works, but calendar link is unreliable |

Pain scores: Claude's estimate, accepted by Shaked.

## Research done
| Method | Who / how many | Date | Raw notes |
|---|---|---|---|
| Speech-to-text desk review (11 engines) and Instinct AI lookup | Official pricing and docs pages, 2 Instinct reviews, 1 Hebrew blog test, 1 benchmark | 2026-11-19 | [1a-voice-and-instinct.md](research/1a-voice-and-instinct.md) |
| Voice test on Shaked's own speech | 5 recordings (3 read, 2 free speech, one of them noisy) × 2 engines | 2026-11-19 | [1a-voice-test-results.md](research/1a-voice-test-results.md) |
| Behavior science review | Meta-analyses, trials, field studies; 25 findings | 2026-11-19 | [1b-behavior-science.md](research/1b-behavior-science.md), [sources](research/1b-sources.md) |
| Similar apps review | 34 apps in 6 categories, Mobbin UI references | 2026-11-19 | [similar-apps.md](research/similar-apps.md), [notes](research/similar-apps-notes.md) |

Evidence limits: both reviews read only some sources in full; treat them as direction, to confirm in 3c.

## Competitors and alternatives
Full table in [similar-apps.md](research/similar-apps.md).

| Product | What it does well | What it misses | Takeaway for Sol |
|---|---|---|---|
| Instinct AI (Shaked's tool) | Voice note in, reminders and plan out, no typing | No goals or progress; iCloud link does not work properly; data cannot be exported (Shaked) | Proves the voice habit. Its data cannot be exported, so Sol reads iCloud Calendar itself (Assumption: feasible) and replaces Instinct in v2 (#9) |
| Life dashboards (Exist, Bearable, Daylio, Notion) | All areas in one place; cross-area insights | Manual entry is too much effort (17% of Exist users) | "One place" only works if voice replaces the tapping |
| Habit trackers (Streaks, Habitica, Finch) | One-tap check-in, widgets | Streak resets shame; gamification tires *(Assumption)* | Rolling "4 of 7 days" and totals, no streaks |
| Voice journals (Rosebud, Day One, Voicenotes) | Talking beats a blank page | Output is reflection, not data; one lost recording reported | Turn voice into entries; save audio first, transcribe after |
| Quit-smoking apps (Smoke Free, QuitNow!, Kwit) | Money-saved and milestone counters | Counter resets after a slip *(Assumption)*; apps alone made no real difference in a 9-trial meta-analysis | Engagement is the feature: two-second logging, links to money |
| Budget apps (YNAB, Goodbudget, Riseup) | "Left to spend" per category, goal rings | Logging fatigue; Israeli apps depend on bank links *(Assumption)* | Manual by voice fits the no-bank rule (#11) |
| Reading trackers (Goodreads, StoryGraph) | Optional goals, book lookup | "Behind" banners *(Assumption)*; Hebrew editions missing | Avoid a yearly count (target type still open); voice fallback for Hebrew titles |

## Insights
1. **Voice to structured data is the unclaimed gap.** No reviewed app turns a voice note into goal progress, a spending entry and a habit check. Evidence: similar-apps finding 2; Instinct shows Shaked already lives this way. *So what:* the voice pipeline and the read-back card (Sol shows what it understood, Shaked confirms or fixes in one tap) are the MVP's core (#15).
2. **One note should update several areas.** "Ate out, 80 shekels, no cigarettes today" touches money, food and smoking. No app links these. *So what:* areas are views on one shared stream of entries. The data model is decided before screens.
3. **Progress must never reset.** Broken streaks lower motivation; self-compassion after a slip reduces repeat slips (1b, Moderate). *So what:* totals and rolling weeks only; words like "missed", "behind" and "failed" never appear (#15).
4. **Small steps with if-then plans beat big goals.** If-then plans and near-term subgoals have the strongest evidence (1b, Strong). *So what:* every goal has a long target, this week's step and one if-then plan said by voice, plus a five-minute weekly voice review.
5. **Speech-to-text gives text, not data.** Shaked's test: ElevenLabs Scribe made no meaning errors on the read sentences (ivrit.ai made 2), but writes numbers as words and most English words in Hebrew letters. Small test: 5 clips, and the reference text for clips 4-5 is not yet confirmed. *So what:* Scribe is chosen (#17), and an AI step after it is required to produce clean numbers and terms. Cost is not a risk: under $1/month at Sol's volume.
6. **Logging less detail keeps people logging.** People stop logging over time, so less detail per entry should help (1b; design inference, not tested). *So what:* "ate out / cooked at home", "read 20 min", not calories or pages.
7. **Money gets real when it is labeled.** Labeled savings goals increase saving; people avoid bad financial news (1b, Moderate). *So what:* one or two named goals fed by other areas ("cigarette money: 3 more days of the flight") and a calm weekly line instead of alerts.

## Assumptions still untested
- Assumption: fixing a voice entry on the read-back card is quicker than typing it from scratch (test in 3c).
- Assumption: Sol can read iCloud Calendar directly (Apple's standard calendar access with an app-specific password). Confirm in architecture.
- Assumption: ElevenLabs' second-language setting keeps more English in English letters. Not tested yet: the test ran on the website, and the API needs the real key (Phase 4).
- Assumption: Sol can get Garmin and Apple Health data (Shaked wants both, 2026-11-19). Apple Health can only be read by an app installed from Apple's tools, not by a website (Assumption, check in architecture).
- Open for 3c (the real-use test, where Shaked uses a working prototype on the phone for a few days): weekly or monthly budget, how many notifications, whether a "rest day" is needed, whether a savings pledge is wanted.

## Answered by Shaked (2026-11-19)
- **Reading target:** one chapter a day; more is a bonus, never required (#18).
- **Smoking support:** Shaked has quit-smoking pills and plans to take them, not started yet. Sol tracks the pills as part of the plan and does not advise on them. Quit-date method settled (#14); the date comes after reserve duty.
- **Baselines:** rough numbers given (cigarettes per day at home and in reserve duty, tobacco pouch price, eating-out spend). Kept outside the repo, like all personal numbers; Shaked confirms them in Sol at setup.
- **Instinct AI:** confirmed as instinct.com. Its data cannot be pulled out, and its iCloud connection does not work properly. So the MVP morning brief sees calendar events only, read by Sol directly.
- **Platform:** on phone and iPad Sol must feel like a real app, not a website; a website is fine on the computer. How (installable web app or store-style app) is decided in architecture; see the decision card on PR #5.
- **Deferred to architecture:** v2 assistant channel and Claude API cost (brief).

## Gate: ready for Definition when
- [x] Problem stated in one sentence, backed by evidence (Problem space)
- [x] Primary audience chosen by Shaked (Shaked only, #1)
- [x] At least 5 competitors or alternatives reviewed (34 apps in 6 categories, plus Instinct)
- [ ] Shaked approves this summary

**Not blocking the gate:** the real ElevenLabs API key (needed before development, Phase 4); confirming the voice-test references for clips 4-5 (optional).
