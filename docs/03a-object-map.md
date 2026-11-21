# 3a · Object map: every kind of thing Sol holds
> Summary: Sol holds **two families of things**. *Lasting things* stay and change over time (direction, goal, topic, task, recall card, usual, calendar event). *Moments* are entries: something that happened, logged once (progress, minutes learned, what stuck, calm, mood, task done). Every moment comes from a **note** and points to a lasting thing. Screens are views over these, never their own data.

Date: 2026-11-21 · Role: Designer (Opus 5.5, high) · Status: Shaked's taps in (2026-11-21, #35); Garmin waits for one decision. Page: https://claude.ai/artifact/KLoGvAk2n68QnELgYd3tSF (db picks/object-map)
Builds on: [02c-user-stories.md](02c-user-stories.md), [decisions.md](decisions.md) #30, #32, #34, [3-0 research](research/3-0-ux-process.md).

## Method
Object mapping, from Sophia Prater's ORCA process: list the **O**bjects (the nouns people talk about), their **R**elationships, the **C**alls to action (what you can do with each) and the **A**ttributes (what each holds), before any screen ([A List Apart](https://alistapart.com/article/ooux-a-foundation-for-interaction-design/), [Adobe Design](https://adobe.design/stories/leading-design/why-ux-designers-should-create-object-maps-and-how-to-start)). How sure: Opinion, widely taught practice, no controlled studies. Why it fits Sol: every app reads the same entry list (story 4), so a name used two ways in two apps would break numbers everywhere. One rule from the method: one thing, one name, no synonyms.

## Where things come from
| Thing | What it is | Holds | Links to | You can |
|---|---|---|---|---|
| **Note** | What you said or pasted, kept as it was | Audio or text, time, Sol's reading of it (the read-back card) | Creates one or more moments or lasting things (P8) | Record, paste, replay, fix the reading |
| **Fix** | A correction you made on a read-back card | What you said, what Sol got, the right answer | Belongs to a note; joins Sol Lab's test set (M1, story 29) | Nothing directly; it is made when you fix |

## Lasting things
| Thing | What it is | Holds | Links to | You can |
|---|---|---|---|---|
| **Direction** | Where you see yourself in 5-20 years | Name, your words, horizon | Has many goals | Add, rename, archive |
| **Goal** | Active goal, 3-4 at most (#32) | Long target, this week's step, if-then plan, "today" or "growing", state (active, waiting, finished), starting credit (P18) | Belongs to one direction; has progress moments; feeds a topic | Add, log progress, change step, pause, finish |
| **Topic** | Something you learn or grow in; a node on the Living map | Name, total minutes, notes, recall state | Has learning minutes, recall cards, goals | Rename, merge, delete (story 27) |
| **Task** | Something to do once | Text, time (optional), reminder, open or done | May come from a note | Add, set time, mark done, delete |
| **Recall card** | One "What stuck?" answer that comes back | Your own words, next date, gap step | Belongs to a topic; made from a "what stuck" moment | Recall, "got it", "not yet" (story 23) |
| **Usual** | A one-tap repeat of something you log often | The moment it copies, with its values | Makes a moment each time it is tapped | Tap, create by voice, remove (story 26) |
| **Calendar event** | A fixed-time item read from iCloud | Title, time | None; read-only, never written (#26) | View (Should, feature 18) |

## Moments (entries in the one list)
Each moment has a time, the note it came from and one lasting thing it points to. Totals only go up (P2).
| Moment | Points to | Example |
|---|---|---|
| Progress | A goal | "Cooked at home tonight" |
| Learning minutes | A topic | "40 minutes of Figma" |
| What stuck | A topic (and makes a recall card) | "Auto layout wraps like flexbox" |
| Calm | Calm minutes for the week | "10 minutes of calm" |
| Mood | The day | "Tired, stressed" (#23) |
| Task done | A task | "Called the lecturer" |

## Looking back and Sol improving
| Thing | What it is | Holds | Links to |
|---|---|---|---|
| **Weekly review** | Saturday evening's five minutes | Plan against what happened, 1-3 wins, your answers (S1, S2, reflection), time taken | Reads the week's moments and goals; changes next week's steps through a read-back card |
| **Win** | A count from real moments, "cooked at home 4 times" | Number, label, the moments behind it | Lives inside one weekly review; not stored on its own |
| **Lab report** | Sol Lab's weekly suggestions | Suggestions, each with what changes and why | Reads fixes, quiet counts (S3-S6) and review answers; you approve each suggestion |

## Screens are views, not things
Each app is a window onto the same things: **Today** shows open tasks, "today" goals with their step, recall cards due and the last thing you logged; **Goals** shows directions and goals; **Learning** and the **Living map** show topics; **Calm** shows calm minutes; **Review** and **Lab** show their own. The record button makes a note from anywhere.

## Three choices for Shaked
1. **Skill and topic: one thing or two?** Recommended: one, called topic. Learning minutes, recall cards and the map all hang on it, and the method's "one thing, one name" rule says two near-identical nouns confuse every screen. Against: a skill you practise and a subject you read about may feel different to you.
2. **Your original note: attached to each entry, or its own list?** Recommended: attached ("from your note", tap to replay), with no separate notes list in the MVP, because the History screen is Later (#30) and audio is never lost either way (#15). Against: no single place to scroll through everything you said.
3. **A goal's weekly step: part of the goal, or a task on Today?** Recommended: part of the goal, logged as progress, so tasks stay "do once and done" and goal totals only go up (P2). Against: you can't tick it off like a task.

## Shaked's own list (voice note, 2026-11-21)
Tasks, goals and what I learn; also my schedule and "my algorithm", the mind map: keep the information I grow through, keep it safe, offer it back, put it into an algorithm. Shaked expects more things and asked for help finding them.

**Added from it:** **About you**, Sol's picture of Shaked (what works, patterns, the words Shaked uses, read-back fixes), readable and correctable by Shaked; and **things Sol offers back** (recall, an old note that fits today, a smaller step after a heavy week). In the MVP both stay small and are built from what is already planned (fixes, Saturday answers, recall, M3).

**Candidates to jog the list** (on the page, Now / Later / No): ideas, questions, things you save, books, money, meals and weight, workouts and sleep, projects, people, decisions, journal. Books, money and food were moved to Later in #30; a Now tap on them comes back as its own decision.

## Shaked's taps (2026-11-21, #35)
- **Now:** tasks, goals and directions, topics, skills, map, schedule (still a Should), usuals, Saturday review and wins, About you, things Sol offers back, **ideas**, **people**, **decisions** (new), **workouts and sleep from Garmin** (new, pending its own decision).
- **Later:** calm minutes and mood (both were in the MVP: stories 16 and part of 2; #23), books, money, meals and weight (as in #30), journal, projects, questions, things you save.
- **Choices:** skills and topics are **two things** (Claude recommended one; a skill counts minutes, a topic holds knowledge, and a skill links to one or more topics); the original note stays **attached** to what it made; a goal's weekly step stays **part of the goal**.

New lasting things from the taps:
| Thing | What it is | Holds | Links to | You can |
|---|---|---|---|---|
| **Skill** | Something you practise | Name, minutes per week, total | Has learning minutes; feeds one or more topics | Rename, merge |
| **Idea** | A thought to keep, not act on yet | Your words, date, the note | May link to a topic or goal | Add by voice, move to task or goal |
| **Person** | Someone in your life | Name, what they said, things to follow up | Tasks and notes that mention them | Add by voice, see their notes |
| **Decision** | A choice you made and why | The choice, your reasons, date | May link to a goal or direction | Add by voice, look back on it |
| **About you** | Sol's picture of you | What works, patterns, your words, your fixes | Built from fixes, Saturday answers, quiet counts | Read, correct |
| **Body day** | Garmin data for a day (if approved) | Sleep, steps, workouts | Read-only, like the calendar | View |
