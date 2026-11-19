# 00 · Brief
> Summary: **Sol**, a personal, voice-first dashboard for Shaked that turns "I want to improve myself" into a clear daily plan, visible progress and short- and long-term achievements, without typing. For Shaked only.

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
- **AI voice assistant app** ("Instinct AI", confirmed by Shaked). Shaked's favorite tool. Shaked records a voice note and it does the rest: reminders, daily plan, daily summary, and it manages the iCloud calendar. "Useful 200 million times over" because nothing has to be written.
- **iCloud / Apple Calendar**: Shaked rarely uses a calendar directly; the AI app manages it through iCloud.
- **Garmin**: in use (Assumption: for fitness and body data such as steps, sleep, workouts).
- **Notes**: sometimes (Assumption: Apple Notes).
- **Mindfulness**: no tool today.

## A good day with the dashboard
1. Morning: open it and get a daily brief.
2. See today's tasks and reminders, sorted by importance (important, less important).
3. See what Shaked has done and any achievements earned.
4. See where there is room to improve and what needs attention.
Devices: phone, computer and iPad (Shaked, 2026-11-19). Session length: not yet stated.

## Constraints
- Deadline: none. Target a strong MVP in about two weeks, 1 to 2 hours a day of Shaked's time.
- Budget / tools: Max plan; Figma ("gozlans's team"); GitHub repo solos.
- Language and direction: Hebrew first (RTL), Hebrew/English toggle.
- Product name: Sol (repo: solos).
- Platform: phone, computer and iPad. Assumption: one responsive web app that can be installed on all three (a PWA), with phone as the main design size.
- Input: voice first. Manual typing must be the exception, never the main path.
- Connections Shaked asked for: iCloud (Apple) Calendar, Google Calendar, maybe Notion. Garmin is allowed. Money: no connections at all.

## Suggested connections (Claude, for Shaked to choose)
Shaked asked for suggestions. Each needs a feasibility check in Discovery.
- **Garmin Connect**: workouts, steps, sleep, stress. Progress on health goals with zero typing.
- **Apple Health**: weight, steps, mindful minutes; one hub for data from Garmin and other apps.
- **The AI voice app's own data**: tasks and daily summaries, if it can export or share them. Without this, the dashboard sees calendar events only.
- **Speech-to-text inside the dashboard**: so a voice note can update a goal, log a meal, or mark a smoke-free day.

## Deal breakers
- Too much to write. If keeping it current takes typing, Shaked will stop using it.
- What Shaked wants instead: "someone I can talk to, and it does everything."

## Earlier attempt
- What existed: goals, notes, fitness tracking, all fairly broad.
- What did not work (Shaked, 2026-11-19): it was never finished. The design was uncomfortable and looked bad, so Shaked stopped using it. Every change had to be made on a specific page, so changes took a long time. There was so much left to fix that Shaked gave up.
- Lesson: reach a high-quality MVP fast, with a small scope, then improve it step by step. Changes must be cheap (shared components, not page-by-page edits).
- Already decided (decisions.md #3): it was weak in design, code and usability, and is used only as a "what to avoid" reference.
- Screenshots: optional, whenever Shaked has them.

## Claude's critique
1. **The scope is very wide** (six groups, about 20 goals). Resolved: the MVP covers 3 areas (decisions.md #10).
2. **Overlap with Instinct AI.** Resolved: dashboard first, Sol's own assistant replaces Instinct in v2 (decisions.md #9). Remaining risk: if Sol only reads the calendar, the morning brief sees events but likely not Instinct's tasks (Assumption: depends on what Instinct can share).
3. **"Talk and it does everything"** is the heart of the product, not a feature. Discovery must test how voice input can update goals and progress reliably. Waiting for Shaked's view.

## Later (not in the MVP, kept for future phases)
- v2: Sol's own AI assistant replaces Instinct AI (voice; WhatsApp, Telegram or in-app). Includes tasks, reminders, daily plan and summary, calendar.
- Areas parked after the MVP: Mind and emotions (decisions, independence, mindfulness), Relationships.
- Connections: Notion; Garmin if not in the MVP; Instinct AI export (Markdown) during the move to v2.
- Achievements: long-term set alongside the short-term one, if the MVP starts with only one.

## Open questions
- [x] Top 3 areas: Health and body, Learning and skills, Money (decisions.md #10)
- [ ] Can Instinct AI share data? Shaked guesses it can export Markdown (.md) files (Assumption, to check in Discovery)
- [x] Instinct AI: decided (decisions.md #9). Dashboard first; Sol's own assistant (WhatsApp, Telegram or in-app voice) replaces Instinct in v2.
- [ ] v2 assistant: channel and Claude API running cost (check in Discovery)
- [x] Data sources: Garmin may connect. Money never connects to any account or bank; Sol gets money info only from what Shaked says (decisions.md #11)
- [x] Privacy: a secure cloud database is fine (decisions.md #12)
- [ ] Daily use: Shaked says it depends on the day and on what Sol offers. To be learned in the real-use test (step 3c)
