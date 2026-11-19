# 1b · What makes self-improvement stick
> Summary: Sol should make every goal a **small weekly step with an if-then plan**, show **progress that never resets to zero**, treat a **slip as information, not failure**, and let Shaked log **one messy voice sentence** that Sol turns into an editable card. Evidence is strongest for progress monitoring, if-then plans and self-compassion after lapses; weakest for apps, gamification and voice logging, which we must test ourselves in 3c.

Date: 2026-11-19 · Role: Researcher (Opus 5.5 high lead, 4 Sonnet reading workers) · Status: for 1c synthesis
Sources and how well each was checked: [1b-sources.md](1b-sources.md)

**How sure we are.** "Strong" = meta-analysis or Cochrane review. "Moderate" = several trials or one good field study. "Weak" = small, lab-only or observational. Workers could read only some sources in full (marked in 1b-sources.md). Anything not read is from known literature and is marked **Assumption** until re-checked.

## 1. What the evidence says, in short

| Theme | Finding | Strength |
|---|---|---|
| Habits | Habits take weeks to months (median about 2 months, range 4 to 335 days), not 21 days | Moderate |
| Habits | Stable timing, morning practice and self-chosen habits form faster | Moderate |
| Habits | If-then plans ("When I finish coffee, I read 10 min") raise goal attainment, medium to large effect | Strong |
| Habits | Missing one day does not hurt habit formation (Lally 2010) | Assumption |
| Goals | Monitoring and recording progress helps people reach goals | Strong |
| Goals | Specific goals with feedback beat "do your best"; near-term subgoals help long goals | Strong |
| Goals | New week, new month and birthdays make people start again (fresh-start effect) | Moderate |
| Achievements | Gamification gives small, short-lived gains; tangible rewards can weaken inner motivation | Moderate |
| Achievements | A broken streak sharply lowers motivation afterwards | Moderate |
| Tone | A self-compassion message after a slip leads to *less* repeat slipping, not more | Moderate |
| Tone | Confidence after a slip predicts how long until the next one; the first slip does not decide the outcome | Weak to moderate |
| Tracking | Most people stop using health apps; many tracking lapses are pauses, and people come back | Strong (dropout) / moderate |
| Voice | Spoken logs capture richer detail than typed ones; chatbots for behavior change look promising but evidence is early | Weak to moderate |
| Smoking | Gradual cut-down works as well as an abrupt quit date | Strong |
| Smoking | Nicotine replacement or medication roughly doubles to quadruples success | Moderate to strong |
| Smoking | Supportive text messages help (+50%); smoking apps alone show no proven effect yet | Moderate / weak |
| Weight | Weighing yourself helps inside a plan with feedback, not alone; daily vs weekly makes no difference | Moderate |
| Weight | Food logging is linked to weight loss but people stop doing it over time | Assumption |
| Learning | Recalling what you learned and spacing reviews beats rereading | Strong |
| Reading | No good evidence on minutes vs pages goals | Weak |
| Money | Labeling money for a specific goal ("Flight") increases saving | Moderate |
| Money | Fewer savings goals can mean more saving | Weak to moderate |
| Money | People avoid looking at their finances when news is bad (ostrich effect) | Moderate |
| Money | Budget categories make people weigh trade-offs and spend more carefully | Moderate |
| Money | Cooking at home links to better diet and lower cost (mostly observational) | Assumption |

## 2. Design principles for Sol

### Across all areas
1. **Every goal has three layers.** A long goal (target weight, flight fund), this week's step, and one if-then plan said by voice. Sol asks for the if-then plan when a goal is created. *Why: if-then plans and near-term subgoals are the best-supported tools.*
2. **Progress only goes up.** Show cumulative totals ("41 smoke-free days", "₪1,200 toward the flight", "9 hours read this month") and "4 of 7 days this week". No consecutive streak that drops to zero. *Why: broken-streak effect; lapses are normal.*
3. **No deadline on habits.** A habit shows as "building", never "day 12 of 21". *Why: real timelines vary from weeks to almost a year.*
4. **A slip is information.** After a slip Sol says something like "Welcome back. What happened?" and offers a one-sentence re-plan. Never a count of missed days, never red failure states. *Why: self-compassion reduces the what-the-hell spiral; confidence after a slip matters.*
5. **Fresh starts are built in.** Sunday evening and the 1st of the month bring a short "new week" moment: last week's wins, this week's step. *Why: fresh-start effect.*
6. **Weekly review by voice.** Five minutes, once a week: Sol reads back the numbers, Shaked reacts by voice, Sol adjusts the steps. This is Sol's version of "accountability". *Why: recorded progress plus feedback works better than tracking alone.*
7. **Achievements reward competence, not activity.** Short-term: weekly ("Cooked at home 4 times"). Long-term: milestones ("100 smoke-free days", "First book finished", "Flight fund half way"). Few, meaningful, no points economy. *Why: informational feedback supports motivation; heavy gamification fades.*

### Voice logging
8. **One sentence, any order, any language mix.** "שילמתי 60 שקל על פלאפל and I skipped the cigarette after lunch" becomes two entries. Messy or partial is fine; Sol fills structure.
9. **Confirm with a card, never block.** Sol shows what it understood as an editable card; Shaked fixes it by voice or a tap, or ignores it and it saves. *Why: speech errors are likely in mixed Hebrew/English; a correction must cost less than a form.*
10. **Less detail beats more detail.** Log "ate out / cooked at home", not calories. Log "read 20 min", not page numbers. *Why: logging burden is the main reason people stop.*

### Tone and notifications
11. **Invite, don't instruct.** "Want to…", "You could…", never "You should" or "You failed". Name what went well first.
12. **Few notifications, chosen by Shaked.** A morning brief and at most one context reminder a day per area; easy snooze; reminders never escalate after being ignored. Cadence stays adjustable because evidence on frequency is weak.

### Per area
13. **Smoking.** Shaked picks a quit date *or* a step-down plan; Sol presents both as equally good. Log cigarettes by voice ("smoked 2"). Show smoke-free days and money not spent on cigarettes, both cumulative. Sol mentions, once and gently, that nicotine replacement or medication raises success and is worth asking a doctor about (Assumption: Israeli health funds offer cessation programs; check before saying so in-app). A short daily supportive check-in works like the proven text-message programs.
14. **Weight.** Weigh-in by voice at any frequency Shaked picks. Show a weekly trend, not daily jumps (design inference, not tested). Weight sits inside a plan: eating at home, movement from Garmin, weekly review.
15. **Eating out links health and money.** One log ("ate out, ₪70") counts for both the eating-out budget and the healthy-eating goal. A home-cooked meal is a win in both areas.
16. **Learning and reading.** Goals in minutes (a choice to test, not proven). After a session Sol asks "What stuck?" and saves the answer. The morning brief resurfaces old answers at growing intervals, a light form of spaced recall.
17. **Money.** Few labeled savings goals (start with one or two), each with a name, amount and date. Category budgets with eating out as its own category. A calm weekly "where you stand" line instead of alerts. Spending is logged only by voice (decisions.md #11).

## 3. Open questions to test in 3c (real-use test)
- Does voice logging in mixed Hebrew/English stay accurate enough that correcting costs less than typing? (Also for the speech-engine thread.)
- Weekly or monthly budget period?
- Minutes or pages for reading?
- How many notifications before they annoy Shaked?
- Is a "rest day" needed on top of "4 of 7 days", or is that enough?
- Is a savings "lock" or pledge wanted? (Evidence is bank-enforced; an app-only pledge is untested.)

## 4. What this research did not cover
Speech-to-text engines (separate thread), Garmin and Apple Health access, mindfulness (parked). Food-cost and cooking studies were found but not read.
