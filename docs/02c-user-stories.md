# 02c · User stories for every Must
> Summary: one short story and a few checkable "done when" lines for each Must in the Sol OS MVP ([02-definition.md](02-definition.md), reshaped in #30). Design builds the apps to these lines; Development tests against them. Later and dropped features have no stories. Shoulds (18 calendar, 24 goal research) are the first to cut and get stories only if built.

Status: draft for Shaked's approval · Writer: Product strategist, Opus 5.5 (medium) · Reviewer pass: Opus 5.5 (high), 2026-11-20, fixes applied
Builds on: [02-definition.md](02-definition.md), [02b](02b-who-and-success.md), [research M1-M6](research/how-sol-improves-you.md) (PR #11), [decisions.md](decisions.md). "I" is Shaked.

## Applies to every story
- Hebrew first, right to left, with a Hebrew/English toggle; mixed Hebrew and English in one sentence works everywhere (#2, #17).
- Calm words only: never "missed", "behind", "failed" or a count of missed days (#15, P4, P11).
- Never a fight (P19): any fix takes one step, saying it again fixes it, anything can be skipped, Sol never asks the same thing twice.
- Works on phone, iPad and computer, synced through sign-in (#12, #21). Phone is the main size.
- Every app is built from one shared set of components; changing a component changes it in every app (#30).
- Every action has its own documented API route (#28).
- Sol quietly counts days opened (S6), never shown as a streak.

## Sol OS
**25 · Home screen** (J2)
When I open Sol, I want every app on one home screen, so that I see my whole system at a glance.
- Each app is a tile with one live number ("3 tasks", "2 topics to recall").
- Today is the biggest tile; one tap opens it.
- The record button is on the home screen and inside every app.
- A Later app does not appear until it is built.

## Record
**1 · Voice or text capture** (J1)
When something comes up, I want to tap once and talk, or paste text, so that it is out of my head in seconds.
- One tap starts recording, one tap stops.
- The audio is saved on the device before it is sent; if the network fails, nothing is lost and Sol retries on its own.
- While I talk, a rough text preview shows (Assumption: Scribe live mode or phone dictation).
- Pasted or typed text goes through the same steps as voice.
- A one-sentence task goes from tap to saved in 15 seconds or less (S4).

**2 · Understanding step** (J1)
When I say or paste something messy, I want Sol to turn it into clean entries, so that I never fill a form.
- One note can create entries in several apps (P8): "call the lecturer tomorrow and I did 20 minutes of Figma" makes a task and a learning entry.
- Spelled-out numbers become numbers; English words written in Hebrew letters become English (#17).
- A feeling ("tired, stressed") becomes a mood entry (#23).
- If Sol is unsure about a part, it marks that part on the read-back card instead of guessing silently.
- Sol adds my 3-5 closest past fixes as examples when it reads a new note (M1).

**3 · Read-back card** (J1, S5)
When Sol has understood a note, I want to see what it understood, so that I can trust it without checking every time.
- The card shows each entry with its app, value and date.
- I can fix an entry by voice ("not today, tomorrow") or with one tap on that field.
- If I ignore the card, the entries save after a short moment (P9). Assumption: about 10 seconds, tuned in 3c.
- Each fix is saved as what I said, what Sol got and the right answer (M1, used by story 29).

**26 · Usuals**
When I log the same thing often, I want one tap to log it, so that repeats cost nothing.
- Sol offers an item as a usual after I log it 3 times (Assumption); I can also make one by voice.
- One tap on a usual logs it with the same values, and the read-back card still shows.

**4 · One entry list (in the background)**
When anything is logged, I want it kept in one list underneath every app, so that every app, the map and the weekly review use the same data.
- Every entry from every app is stored in one list; each app shows its own part of it.
- I can edit or delete an entry from the app that shows it; a delete can be undone for a short while (Assumption).
- Changing an entry updates every number that uses it. The History screen itself is Later (#30).

## Today and tasks
**10 · Today** (J2, J4, S3)
When I open Sol in the morning, I want my day on one calm screen, so that I know what to do without feeling overloaded.
- It shows today's tasks, calendar events (when feature 18 is built), "today" goals with their step, topics due for recall, and "continue where you left off".
- Tasks and calendar events are visually separate (#26).
- Growing goals do not appear; a finished task leaves the list (Assumption: kept under "Done today").
- "Continue where you left off" shows the last skill, topic or goal step I logged.
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
- After 2 or more days away (Assumption, tuned in 3c), Sol opens with "Welcome back" and offers a one-sentence re-plan.
- When I tell Sol about a slip on a goal ("I smoked today"), it says "Welcome back" and offers a one-sentence re-plan.
- No count of missed days; a task past its time has no red colour and no word "overdue".

## Goals and growth
**5 · Goals** (J5)
When I want to improve something, I want to add a goal by voice or text, so that it becomes a clear next step.
- A goal can be about anything: health, learning, money, quitting smoking (#30).
- Each goal has a long target, this week's step and one if-then plan; Sol asks for the if-then plan once, and I can skip it (P1, P19).
- Each goal is marked "today" or "growing"; only "today" goals appear on Today (#24).
- A new goal starts with honest credit for what I have already done, if I tell Sol (P18).
- I can log progress on a goal by voice ("cooked at home tonight"), and the totals only go up (P2).

**15 · Learning** (M5)
When I practice a skill, I want to log the minutes and what stuck, so that I remember what I learned.
- I can log minutes per skill by voice ("40 minutes of Figma").
- After a session, Sol asks once "What stuck?"; I answer in my own words or skip. Sol saves my words, never a summary it wrote.

**23 · Spaced recall**
When I learned something, I want it to come back at the right time, so that it stays with me.
- A "What stuck?" answer comes back after about 1, 3, 7, 21 and 60 days (Assumption: tuned in 3c).
- Sol first asks me to say it from memory, then shows my original words.
- After seeing my words I tap or say "got it" or "not yet". "Got it" moves it to the next gap; "not yet" brings it back in 1 day (Assumption). Nothing is marked as a failure.

**27 · Living map, first version**
When I learn and set goals, I want to see my knowledge grow as a map, so that I see my mind expanding.
- Every skill, goal and "What stuck?" answer adds to a topic on the map; a topic grows as I log more.
- Tapping a topic shows its notes, sessions and recall state.
- I can rename, merge or delete a topic by voice or one tap.
- The first version has no links between topics and no suggested topics; those come step by step after the MVP (#29, #30).

**16 · Calm**
When I take a calm moment, I want to log it in one sentence.
- "10 minutes of calm" makes a mindfulness entry; minutes add up per week.

## Weekly
**13 · Weekly review, Saturday evening** (J6, S1, S2, M3, M4, M6)
When it is Saturday evening, I want five minutes to see how my week went, so that I feel the week mattered.
- Same short steps in the same order every week, with a clear ending; it takes about 5 minutes, and Sol times it (M6).
- Sol shows plan against what happened ("you planned 5 home meals and made 3"); if the gap repeats, it proposes a smaller step (M3).
- The summary quotes my own entries and names one thing that did not go well, kindly (M4).
- I react by voice and Sol adjusts next week's steps through the read-back card.
- It asks: "Did you forget anything that wasn't in Sol?" (S1) and "How did Sol feel this week: calm, okay or heavy?" (S2), then one reflection question (#23). Everything can be skipped.

**14 · Weekly wins** (P7)
When I do something well this week, I want Sol to name it, so that I see real wins.
- Each week Sol shows 1 to 3 wins, each a count from real entries ("cooked at home 4 times").
- No points, levels, titles or streaks.

## Sol improves itself
**29 · Sol Lab, first version** (M2)
When Sol has been used for a while, I want it to suggest how it can serve me better, so that it keeps improving without me designing it.
- Once a week a scheduled Claude reads Sol's quiet counts (S3-S6), my Saturday answers (S1, S2) and my read-back fixes, and writes a short report with suggested changes.
- Each suggestion says what would change and why; nothing changes in Sol until I approve it.
- Every read-back fix is added to a test set of real sentences; it is run before any change to how Sol understands, and a change that makes it worse is not shipped.

**28 · Claude app connector** (#28, #30)
When I am already talking to the Claude app, I want it to read and write Sol, so that I can use Sol from there too.
- From the Claude app I can add a task, log an entry, ask what is on today, and mark a task done.
- Entries made from the Claude app go into the same list and show up in every app.
- Sign-in protects the connector, so only I can reach my data.
- Assumption: mixed Hebrew and English works in the Claude app (untested, #28).

## Gate check
- Every Must has a story: 1, 2, 3, 4, 5, 10, 11, 12, 13, 14, 15, 16, 19, 23, 25, 26, 27, 28, 29. Not here: 6 (dropped), 7, 8, 9, 17 (Later); 18 and 24 (Shoulds).
- M7 (one in, one out) waits for Shaked's answer.
