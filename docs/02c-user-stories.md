# 02c · User stories for every Must
> Summary: one short story and a few checkable "done when" lines for each of the 18 Must features in [02-definition.md](02-definition.md). Design builds screens to these lines and Development tests against them. Nothing new is added: Shoulds (18 calendar, 24 goal research) and everything Later stay out.

Status: draft for Shaked's approval · Writer: Product strategist, Opus 5.5 (medium) · Reviewer pass: Opus 5.5 (high), 2026-11-20, fixes applied
Builds on: [02-definition.md](02-definition.md) (feature numbers), [02b](02b-who-and-success.md) (jobs J1-J6, measures S1-S7), principles P1-P19, [decisions.md](decisions.md) ("#n").
"I" is Shaked.

## Applies to every story
- Hebrew first, right to left, with a Hebrew/English toggle; mixed Hebrew and English in one sentence works everywhere (#2, #17).
- Calm words only: never "missed", "behind", "failed" or a count of missed days (#15, P4, P11).
- Never a fight (P19): any fix takes one step, saying it again fixes it, anything can be skipped, Sol never asks the same thing twice.
- Works the same on phone, iPad and computer, synced through sign-in (#12, #21). Phone is the main size.
- Every action has its own documented API route, so a connector can be added later (#28).
- Sol quietly counts days opened (S6), never shown as a streak.

## Capture and understanding
**1 · Voice or text capture** (J1)
When something comes up, I want to tap once and talk, or paste text, so that it is out of my head in seconds.
- One record button on every screen; one tap starts recording, one tap stops.
- The audio is saved on the device before it is sent; if the network fails, nothing is lost and Sol retries on its own.
- While I talk, a rough text preview shows (Assumption: Scribe live mode or phone dictation).
- Pasted or typed text goes through the same steps as voice.
- A one-sentence task goes from tap to saved in 15 seconds or less (S4).

**2 · Understanding step** (J1)
When I say or paste something messy, I want Sol to turn it into clean entries, so that I never fill a form.
- One note can create several entries in different areas (P8): "60 shekels on falafel and I skipped the cigarette" makes a money entry and a smoking entry.
- Spelled-out numbers become numbers; English words written in Hebrew letters become English (#17).
- A feeling ("tired, stressed") becomes a mood entry (#23).
- If Sol is unsure about a part, it marks that part on the read-back card instead of guessing silently.

**3 · Read-back card** (J1, S5)
When Sol has understood a note, I want to see what it understood, so that I can trust it without checking every time.
- The card shows each entry with its area, amount and date.
- I can fix an entry by voice ("not 60, 70") or with one tap on that field.
- If I ignore the card, the entries save after a short moment (P9). Assumption: about 10 seconds, to tune in 3c.
- Sol counts fixes.

**4 · One entry stream and history**
When I want to look back or change something, I want all entries in one list, so that nothing is hidden on a separate page.
- Every entry from every area appears in one list, newest first; each area screen is a filtered view of the same list.
- I can edit or delete any entry; a deleted entry can be undone for a short while (Assumption).
- Changing an entry updates every total that uses it.

## Goals and areas
**5 · Goals** (J5)
When I want to improve something, I want to add a goal by voice or text, so that it becomes a clear next step.
- A goal can be in health, learning, money or outside them.
- Each goal has a long target, this week's step and one if-then plan; Sol asks for the if-then plan once, and I can skip it (P1, P19).
- Each goal is marked "today" or "growing"; only "today" goals appear on the Today screen (#24).
- A new goal starts with honest credit for what I have already done, if I tell Sol (P18).

**6 · Smoking**
When I am quitting, I want to see how far I have come, so that every smoke-free day counts.
- I can set and change the quit date; before it, Sol shows a calm countdown.
- I can log pills and cigarettes by voice ("smoked 2").
- Smoke-free days and money not spent are cumulative and never reset to zero after a slip (P2, P13).

**7 · Money**
When I spend, I want to say it in one sentence, so that I know what is left without a spreadsheet.
- A spend entry has an amount and a category; eating out is its own category.
- I set a budget; "left to spend" is the budget minus spending in the period (Assumption: week or month, set in 3c).
- One or two named savings goals, each with a name, amount and date, show progress toward them.
- No bank, card or account connection of any kind (#11).

**8 · Food and weight**
When I eat or weigh in, I want to log it in a word, so that health and money move together.
- "Ate out" or "cooked at home" is one log; "ate out" with an amount also counts as a money entry (P15).
- I can log a weigh-in by voice at any frequency.
- Weight shows as a weekly trend, not daily jumps (P14).

**9 · Reading** (#18)
When I read, I want to log it in one sentence.
- I can set the current book and change it.
- I can log chapters by voice ("read 2 chapters").
- The daily target is one chapter; reading more shows as a bonus, never as a requirement.
- Books finished and chapters read are cumulative.

**15 · Learning skills**
When I practice a skill, I want to log the minutes and what stuck, so that I remember what I learned.
- I can log minutes per skill by voice ("40 minutes of Figma").
- After a session, Sol asks once "What stuck?"; I can answer or skip, and the answer is saved with the session (P16).

**16 · Mindfulness minutes**
When I take a calm moment, I want to log it in one sentence.
- "10 minutes of calm" makes a mindfulness entry with minutes; minutes add up per week.

## Daily rhythm
**10 · Today screen** (J2, J4, S3)
When I open Sol in the morning, I want to see my day in one calm screen, so that I know what to do without feeling overloaded.
- The first screen shows: today's tasks, calendar events (when feature 18 is built), "today" goals with their step, "continue where you left off", one progress line per area.
- The layout is chosen in Design (3a): a Today list, a "Sol OS" home screen of area tiles with live numbers around one record button (docs/ideas.md), or a mix.
- Tasks and calendar events are visually separate (#26).
- Growing goals do not appear on Today; a finished task leaves the list (Assumption: kept under "Done today").
- "Continue where you left off" shows the last book, skill or goal step I logged (Assumption: settled in Design).
- Sol records how long each morning visit takes (S3).

**19 · Tasks with reminders** (J1, J3, S1)
When I get a task, I want to give it to Sol with or without a time, so that I forget nothing.
- I can add a task by voice or pasted text; a pasted message can create several tasks.
- A task with a time sends a push at that time; a task without one waits on Today.
- I can mark a task done with one tap or one spoken sentence.
- Tasks are never written to the iCloud Calendar (#26).

**11 · Notifications**
When the day starts and ends, I want Sol to reach out gently, so that I don't have to remember to open it.
- One morning push and at most one evening check-in; I choose both times (P12). On Saturday the evening check-in opens the weekly review (Assumption).
- Task reminders from story 19 come on top of these, only at the time I set.
- An ignored notification is never repeated or made stronger.
- Works on iPhone and iPad with iOS 16.4 or newer once Sol is added to the Home Screen.

**12 · Welcome back** (P4)
When I come back after a gap or a slip, I want a calm restart, so that I don't avoid opening Sol.
- After 2 or more days away (Assumption: the gap length is tuned in 3c), Sol opens with "Welcome back" and offers a one-sentence re-plan.
- After a logged slip (a cigarette after the quit date), Sol replies "Welcome back" and offers a one-sentence re-plan.
- No count of missed days; a task past its time has no red colour and no word "overdue".

## Weekly and achievements
**13 · Weekly review, Saturday evening** (J6, S1, S2)
When it is Saturday evening, I want five minutes to see how my patterns changed, so that I feel the week mattered.
- Sol shows changes against my starting point and last week ("ate out 4 times a week before, once this week"). Assumption: the starting point is my first week in Sol.
- I react by voice and Sol adjusts next week's steps through the read-back card.
- It asks the two short check questions: "Did you forget anything that wasn't in Sol?" (S1) and "How did Sol feel this week: calm, okay or heavy?" (S2).
- It ends with one reflection question (#23). Everything can be skipped.

**14 · Short-term achievements** (P7)
When I do something well this week, I want Sol to name it, so that I see real wins.
- Each week Sol shows 1 to 3 wins, each a count from real entries ("cooked at home 4 times").
- No points, levels or streaks.

## Data
**17 · Export and import**
When I want my data outside Sol or want to bring notes in, I want export and import.
- Export everything as Markdown and as JSON in one action.
- Import a Markdown file; Sol turns it into entries and shows them on the read-back card before saving.

## Gate check
- 18 of 18 Musts covered (1-17 and 19). Assumptions to settle in Design or the real-use test (3c): auto-save delay, undo window, welcome-back gap, budget period, starting point, "Done today", "continue where you left off", Saturday check-in.
