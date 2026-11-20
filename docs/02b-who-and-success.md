# 02b · Who Sol is for, and how we know it works
> Summary: Sol is for Shaked only. Its first job is to take every task off Shaked's mind: send it in one go, Sol organizes it, nothing is forgotten, and opening Sol shows everything without overload. Sol works if, after the real-use test, Shaked follows their tasks easily and forgets nothing; it failed if following tasks feels hard or uncomfortable.

Status: approved by Shaked (#26, #27) · Writer: Product strategist, Opus 5.5 (medium) · 2026-11-20
Builds on: [00-brief.md](00-brief.md), [02-definition.md](02-definition.md) (features by number), [decisions.md](decisions.md) ("#n").
**From:** *Shaked* = your words or choice; *Claude* = my addition, for you to accept or drop.

## Who
- **Shaked only** (#1). No made-up persona: everything about you is already in the brief.
- **Two kinds of days** (Shaked): "some days are like this, some like that". Regular days and reserve-duty days. Sol must work on a busy day with only seconds to spare (Claude).

## The moments (Shaked, 2026-11-20)
| Moment | What happens | Time |
|---|---|---|
| Morning | Understand what to do today | About 5 minutes (Shaked) |
| During the day | Mark tasks done or not done; add a task the moment it arrives | A few seconds each (Claude target) |
| End of day | Close the day | Short (Shaked did not set a time) |
| Saturday evening | Weekly review (feature 13) | About 5 minutes (2a) |

Shaked: in total it can take up to an hour on days with more tracking, such as the gym. Tasks alone should take as little time as possible.
**Claude's note:** I'd measure time per moment, not the daily total. An hour spread over the day is fine only if every single touch stays tiny. Gym tracking is not in the MVP (Garmin is Later, feature 21).

## Jobs Sol is hired for
In order of importance. "When... I want... so that..." is a standard way to write why someone opens a product.
| # | When... | I want... | So that... | From |
|---|---|---|---|---|
| J1 | I get a task | to send it to Sol right away, by voice or pasted text, and have Sol organize it | I have no worries and forget nothing | Shaked |
| J2 | I open Sol | to see all my tasks in the simplest, calmest way | I don't feel overloaded and stuck ("I can't do anything") | Shaked |
| J3 | I finish something during the day | to mark it done in seconds | the list stays true without effort | Shaked |
| J4 | I plan my day | to see today's calendar events (classes, submissions, fixed times) next to my tasks, but kept separate | fixed times and flexible tasks don't mix | Shaked (#26) |
| J5 | I look at my goals | to see calm progress on health, learning and money | I know I'm moving | Claude, from 2a |
| J6 | it is Saturday evening | to see my patterns change | I feel the week mattered | Shaked, from 2a |

## Success measures
Sol counts these quietly in the background (Shaked agreed). They appear only in a small "How Sol is doing" section, never as missed days or guilt (#15).
| # | Measure | Target during the real-use test | How it's measured | From |
|---|---|---|---|---|
| S1 | **Nothing forgotten** | 0 forgotten tasks a week | Saturday question: "Did you forget anything this week that wasn't in Sol?" | Shaked's goal, Claude's measure |
| S2 | **Calm, not overloaded** | "Calm" most weeks | Saturday question: "How did Sol feel this week?" calm / okay / heavy | Shaked |
| S3 | **Morning in 5 minutes** | Morning visit 5 minutes or less | Sol times the morning visit | Shaked |
| S4 | **Fast capture** | A task saved in 15 seconds or less | Sol times from tap to saved (Assumption: target, not measured yet) | Claude |
| S5 | **Understood the first time** | At most 1 in 5 read-back cards needs a fix | Sol counts fixes | Claude |
| S6 | **Part of the day** | Opened on 5 of 7 days | Sol counts days opened; never shown as a streak | Claude |
| S7 | **Missed when gone** | A week without Sol feels messier | Asked once, after the test | Shaked, from the brief |

**It failed if** (Shaked): following tasks in Sol is hard or uncomfortable. In numbers: S1 or S2 misses its target two weeks in a row. Then we fix the task flow before adding anything new (Claude).

## Tasks and the calendar (Shaked, 2026-11-20, #26)
Tasks stay in Sol and never go into the iCloud Calendar. The calendar holds only fixed-time things (classes, submissions, appointments); tasks are more flexible. Sol reads the calendar (feature 18) and shows both on Today, separately.
