# Research · How similar apps work
> Summary: No existing app combines what Sol needs: voice in mixed Hebrew and English, turned into structured updates (goal progress, spending, smoke-free days, reading) across health, learning and money, with no guilt. Each category solves one slice well and fails on the same three things: logging fatigue, streak guilt, and English-only input. Sol's opening is "say it once, Sol files it everywhere", with a confirm step and cumulative progress that never resets to zero.

Step: Discovery 1c · Role: Researcher (Opus 5.5 high lead, Sonnet 5.5 reading workers) · Date: 2026-11-19
Raw notes and all source links: [similar-apps-notes.md](similar-apps-notes.md)

## Evidence level (read first)
The search tool mostly returned titles and links, not page text. Five key sources were opened and read in full (marked **read**). Everything else is from source titles plus background knowledge and is marked *Assumption*. Treat the patterns as direction, not proof. The real test is Shaked's own use (step 3c).

## Per category

| Category | Apps looked at | What works | What users complain about | Takeaway for Sol |
|---|---|---|---|---|
| Life dashboards | Exist, Gyroscope, Bearable, Daylio, Notion life OS | All data in one place; insights across areas; Daylio's tap-only entry | Manual entry is too much effort or easy to forget (17% of Exist users, **read**); Notion setups need constant upkeep *(Assumption)* | The "one place" promise is valued, but manual entry kills it. Voice must replace the tapping |
| Habit trackers | Streaks, Habitica, Finch, Habitify, Loop, Atoms | One-tap check-in, widgets, gentle framing (Finch) | Streak resets make one missed day feel like failure; gamification gets tiring *(Assumption, several 2025-26 posts)* | Replace streaks with a rolling "days this week" count or a strength score |
| Voice AI journals | Rosebud, Reflection, Mindsera, Day One, Voicenotes, AudioPen | Talking beats a blank page; weekly theme summaries; under-a-minute check-ins | Output is reflection, not action; generic AI summaries; AI paywalls ($13-15/month); a lost recording when transcription stalled (Rosebud) | Sol turns voice into data and actions, not mood reports. Save audio first, transcribe after |
| Quit smoking | Smoke Free, QuitNow!, Kwit, Quit Genius, QuitSure | Money-saved and health-milestone counters; craving tools; CBT exercises | Counter reset to zero after a slip feels shaming; paywalls; childish badges *(Assumption)* | Never reset. Show cigarettes not smoked and shekels saved as totals; a slip is a data point plus "what happened?" |
| Budget and savings | YNAB, Goodbudget, Toshl, Cashew, Monarch, Copilot, Riseup | Envelope "left to spend" per category; goal ring with projected finish date | Logging fatigue after a few weeks; price ($15/month for YNAB, **read**, but from a promotional post); setup overhead | Manual-only fits Sol's no-bank rule (decisions #11). Voice makes manual logging cheap |
| Reading trackers | Goodreads, StoryGraph, Hardcover, Bookly, Readwise | Optional goals (StoryGraph); add a book by scanning | Yearly book count with a "behind" banner adds pressure *(Assumption)*; Hebrew editions missing or mislabeled on Goodreads (librarian threads) | Track minutes or sessions, not a yearly count. Book lookup must allow a voice fallback when a Hebrew title is missing |

## Findings that change what we build
1. **Quit-smoking apps alone barely work; engagement is what matters.** A 2023 meta-analysis of 9 trials (12,967 people) found apps alone had no clear effect (odds ratio 1.03); apps plus medication did better (1.79), and higher adherence helped (1.48) (**read**). A 2024 trial of Smoke Free found no difference when the app was simply offered (6.8% vs 7.0% quit at six months), because only a quarter of people used it (**read**). *So:* Sol's smoking feature should be about keeping Shaked engaged (two-second voice logging, links to money and health), not about a clever programme. Worth asking Shaked whether a doctor or nicotine replacement is part of the plan; Sol can track it but does not advise on it.
2. **Voice journals stop at reflection.** None of the reviewed apps turns a voice note into goal progress, a spending entry or a habit check. This is Sol's clearest gap, and Shaked's favorite tool (Instinct AI) already proves the habit.
3. **Mixed Hebrew and English speech is the biggest technical risk, as the brief said.** Stock Whisper handles mixed Hebrew and English poorly; a community fine-tune halved its error rate but writes Hebrew words in Latin letters. A 2026 benchmark of mixed-language speech ranked ElevenLabs Scribe V2, AssemblyAI and Gemini at the top and Whisper turbo last, but it did not include Hebrew. *So:* test Scribe V2, Gemini, Soniox and AssemblyAI on Shaked's own recordings before choosing. No app reviewed documents Hebrew/English mixing.
4. **Hebrew-first manual tracking is an open niche** *(Assumption)*. Israeli budget apps (Riseup and others) depend on bank connections; no Hebrew voice-first budget, quit or reading app was found.
5. **Cross-area links are unclaimed.** No app connects eating out (money) with eating healthier (health), or cigarette money with a savings goal. These are natural for Sol because one voice note can touch several areas.

## UI patterns (Mobbin, iOS references)
- **Voice capture:** a bottom bar with a stop button and a "Transcribing" state ([ChatGPT](https://mobbin.com/screens/0069ce94-7f48-4420-b6eb-594f6f5bbdbd), [Notion](https://mobbin.com/screens/19af1746-3789-4c9e-b777-51f4933602e1)); a live transcript under an animated orb ([Meta AI](https://mobbin.com/screens/fca8709b-7a3a-4ce9-995d-3bd6677c5dd4)); a Voice / Transcribed toggle with a confirm check before saving ([5 Minute Journal](https://mobbin.com/screens/f428c771-bcb0-494a-bab6-7448fda2232b)). The last one is closest to Sol's confirm step.
- **Today list with a mic next to "+"**: [Numo](https://mobbin.com/screens/56b83c22-8c1d-434f-af72-541afb702b46) puts a mic button beside the add button on the home screen, which is the right place for Sol's main action.
- **Streak screens to avoid:** reset-to-zero counters and "can you make it to 3?" pressure ([Insight Timer](https://mobbin.com/screens/e50c7520-4ca8-4eb4-b615-fc8e416efe63), [Duolingo](https://mobbin.com/screens/739be3b0-b1a3-4d8b-a2aa-e387c07be210)). [Bloom](https://mobbin.com/screens/177c6522-6829-49a3-8ede-fddd53c7f2df)'s calm week row ("showing up is what counts") is a gentler tone, though its colors are off-limits for Sol.
- **Savings goal:** a ring with "X of Y" and a target date plus milestones ([Rocket Money](https://mobbin.com/screens/4dd0e004-24b3-4efa-8e10-2af3b11251b9)); a projection line toward the target ([Copilot](https://mobbin.com/screens/05aab1e8-fbad-4e62-8a25-9503b57af6ae)); a plain "on track" label ([Quicken](https://mobbin.com/screens/95f838ed-a395-42b8-8db9-08c17550e6c6)).
- **Game-like habit homes** ([Finch](https://mobbin.com/screens/529f7643-124b-4819-bb6a-34f941ab1816), [Life Reset](https://mobbin.com/screens/a5c4c578-d50c-46e9-b53a-7c56e42f91bd)) are useful for tone ideas only; levels and pets are likely too childish for Sol *(Assumption, Shaked to judge)*.

## Gaps Sol can fill (input for Definition)
1. **Voice to structured updates in Hebrew and English**, with a short read-back to confirm or fix in one tap.
2. **One note, several areas:** "ate out, 80 shekels, no cigarettes today" updates money, health and smoking at once.
3. **No-reset progress:** totals and rolling weeks instead of streaks; a slip or missed day never wipes progress.
4. **Money that means something:** cigarette money and skipped deliveries flow into a named savings goal ("3 more days of the flight").
5. **Audio is never lost:** save first, transcribe after, retry quietly.
6. **Calm, adult tone:** no badges, no ads, no "behind" banners.

## What this changes in Sol (all six gaps kept, Shaked 2026-11-19)
Three gaps are one engine to build; three are rules every screen follows.

**The engine (most of the build effort)**
- **Voice pipeline (gaps 1, 5):** record, save on the device first, transcribe in the background, retry quietly, then turn the text into structured entries with the Claude API. Works offline. Every entry keeps its source note, so a mistake is easy to trace and fix.
- **Read-back card (gap 1):** after each note, Sol shows what it understood ("Ate out, 80 shekels: Money · Eating out. No cigarettes: Smoking") and Shaked confirms or fixes it in one tap. This is the one place typing may happen.
- **One shared stream of entries (gap 2):** areas are views on the same entries, not separate pages with separate data. One note can update several areas. This also fixes the earlier version's "every change on a specific page" problem (brief, Earlier attempt).
- **Home screen:** the mic is the main button. The "+" or manual entry is secondary.

**The rules**
- **No-reset progress (gap 3):** no streak counters anywhere. Progress is totals and rolling 7-day counts. Smoking shows cigarettes not smoked and shekels saved; a slip is an entry plus an optional "what happened?" note, never a reset. Reading shows total minutes. Words like "missed", "behind" and "failed" are not used in copy or notifications.
- **Money that means something (gap 4):** savings goals can be fed by other areas: cigarette money and skipped deliveries move into a named goal, shown in real terms ("3 more days of the flight"). Sol needs baselines from Shaked: cigarettes per day, pack price, typical eating-out spend.
- **Calm, adult tone (gap 6):** no badges, levels or pets. "Achievements" (brief) become milestones in real terms ("a month without smoking", "₪500 toward the flight").

**Effect on the plan:** the speech-engine test becomes the first technical task, and the data model (one stream of entries) is decided before screens are designed. The feature list itself is set in Definition (step 2a).

## Open questions for Shaked
- Which speech engines to test first (recommend Scribe V2 and Gemini, with Soniox as a third).
- Smoking: quit date or step-down plan (already open in the brief); the research leans toward whatever keeps daily engagement easiest.
- Reading goal: minutes per day, sessions per week, or no number at all.
