# Ideas
Weekly digest from the Idea scout. Newest week at the top. Not read by default.
The Product manager reviews it once a week. Shaked moves ideas into 06-backlog.md or rejects them.

## Review of "Jake's Brain" (repo + video shared by Shaked, 2026-11-20)
Source: [github.com/jake17007/jakes-brain](https://github.com/jake17007/jakes-brain) and a 44-second video by its author. A one-person "second brain": about 20 small apps (notes, tasks, food, workout, goals, habits, finances...) inside one iPhone home-screen app, run from the author's own Linux PC. No license file, so it is a reference for ideas only; no code is copied. Video audio was not transcribed (ElevenLabs key is still the key ID); its on-screen captions were read instead.

| Idea | Where it comes from | Which focus area it serves | Size (S/M/L) | Note |
|------|---------------------|----------------------------|--------------|------|
| **Claude connector for Sol**: Shaked talks to the Claude app (Shaked already uses it) and Claude reads and writes Sol, like it does Notion | `server/apps/connector.js`, `deploy/connector/` | All (capture) | M | Strongest idea. Uses the Max plan instead of paid API calls for that path. Proposed to Shaked as a decision (2026-11-20) |
| Build Sol's server as one simple API route per action, each described in a header comment | `SPEC.md`, `server/apps/goals.js` | All (cheap changes) | S | Makes the connector, export and future changes cheap. Fits the "changes must be cheap" lesson. Hand to the Architect (05) |
| Each area is a small self-contained module on one shared kit of components | `web/apps/<id>/`, `web/kit.js` | All | S | Same lesson as the earlier attempt: change once, not page by page. Architect + Design system |
| "Usuals": the same meal or expense logged with one tap, same numbers every time | Food app, `food_search` in the connector | Money, Food | S | Good fit for eating out vs cooking. Candidate for the read-back card (3) |
| Change Sol from the phone: ask Claude Code, it pushes, the app updates itself in about a minute | README "Making changes" | Process | S | For Phase 5. Free hosting with auto-deploy gives the same result without a home PC |
| Goals with milestones or a measurable start, target and check-ins | `server/apps/goals.js` | Goals | S | Already covered by feature 5; useful as a data-model reference |

Rejected or parked (one line each, so the scout doesn't suggest them again):
- Hosting Sol on a home PC with a tunnel: needs a computer always on; Sol uses free cloud hosting (#12).
- Native iPhone shell for notifications: needs a paid Apple developer account; Sol uses web push (feature 11).
- Bank connection (SimpleFIN): never, #11.
- Habits with streaks: against Sol's no-guilt principles (non-goals).
- Obsidian-style graph of everything, "brains with APIs talking to each other": looks good in a video, no daily use for Sol's goals.
- Private Instagram, YouTube feed, local ChatGPT, server stats: unrelated to self-improvement.

## Week of YYYY-MM-DD
| Idea | Where it comes from (link) | Which focus area it serves | Size (S/M/L) | Scout's note |
|------|----------------------------|----------------------------|--------------|--------------|

Rejected or parked (one line each, so the scout doesn't suggest them again):
- 
