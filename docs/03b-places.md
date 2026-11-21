# 3b · Places: Sol's apps and how you move between them
> Summary: Sol is an **operating system, not an app**. It opens on **Home**, which works like an iPhone home screen (option A): one big live widget for the main app **Sol**, app icons with small numbers, and a dock with record in the middle. Inside any app, a thin line at the bottom takes you Home (tap or swipe up), and a swipe sideways jumps back to the last app. Record is available in every app.

Date: 2026-11-21 · Role: Designer (Opus 5.5, high) · Status: decided by Shaked (#36). Page: https://claude.ai/artifact/GDQEqtxcwaYQrSmqDVSZzf (version 2; db picks/places-v2)
Builds on: [03a-object-map.md](03a-object-map.md), [02c-user-stories.md](02c-user-stories.md), [3-0 research](research/3-0-ux-process.md), decisions #30-#35.

## How we got here
Version 1 listed 17 screens and offered an app-style bottom bar (A) or a hub (B). Shaked's voice note: both felt like an app, and Sol must feel like a phone's operating system (iPhone or Galaxy home as the reference); fewer, bigger apps; open on Home. Version 2 rebuilt the step around that and gave each app its own comment box.

## Sol's apps (first version)
| App | What's inside |
|---|---|
| **Sol** (the main app) | What's on today, record and the read-back card, each task. The heart of the system |
| **Goals** (name to find, see below) | Directions (5-20 years), 3-4 active goals with this week's step, each goal's page |
| **Learning** | Skills and minutes, topics and their pages, recall |
| **Map** | The Living map; a topic opens in Learning |
| **Ideas** | Thoughts to keep; turn one into a task or goal |
| **Decisions** | Choices made and why |
| **Saturday** | Saturday review with wins, About you, and the Sol Lab report as its last part |
| **Settings** | Language, notification times, Claude app link; first-time setup runs once |

Later: **People** (Shaked, 2026-11-21; tasks catch follow-ups for now). Not apps: calendar (inside Sol, a Should), the entry list (underneath everything, #30), History (Later).

## Moving around (option A, "like an iPhone")
- Home: big widget for Sol on top, app icons with live numbers, dock with Sol, Goals, record, Learning, Ideas.
- In an app: Home line at the bottom (tap or swipe up = Home; swipe sideways = last app). It sits just above the iPhone's own bottom edge, because a swipe from the very edge leaves Sol (Assumption: iOS behaviour for installed web apps; check on the phone in 3e).
- Record: in the dock on Home and as a button in every app (story 1).
- In Hebrew everything mirrors. On iPad and computer: Assumption, the same home in a wider grid; settled in 3e.
- Shaked's notes for UI: the record button in the dock should be a **square** like the app icons, not a circle; Sol's home needs **its own design language**, and the home screen design deserves extra room in UI.

## Hard moments, same answer in every app
First time (one line plus "say your first one") · Loading (skeleton, Shaked's choice) · No internet (saved on the phone, "saved, will send") · Partly understood (marked on the read-back card) · Microphone off (safety net only: text box and one line on how to turn it back on) · Welcome back (after 2+ days, calm line and re-plan, no missed count) · Just deleted ("Deleted · Undo").

## Evidence
Familiar patterns from the phone Shaked uses daily (Jakob's law, NN/g; Opinion). Gestures are harder to discover than buttons (NN/g; Moderate), accepted for one user who already uses iPhone gestures. Bottom middle is easiest to reach one-handed (Hoober 2013; Moderate). Skeletons make waits feel shorter than spinners (NN/g; Moderate).

## Open
- A better name for the Goals app (Shaked). Decided in 3d Words unless Shaked names it sooner.
- Story 25 changes: Home is now a phone-style home screen with a widget and a dock; the main app is "Sol", not "Today".
