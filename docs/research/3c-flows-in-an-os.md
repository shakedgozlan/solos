# 3c research · How "flows" work in an app built like an operating system
> Summary: Shaked's instinct is right. An operating system has no single flow. It has **a few verbs that work the same everywhere** (record, find, go Home, undo, send to another app), **shared things** (our 3a object map), **rhythms** (the moment, the day, the week) and **stable places** (spatial memory). Recommended: 3c becomes **"Loops and verbs"**: three rhythm loops drawn on the map of Sol's places, a grid of which verb works in which app, and 10 to 12 "When I..." moments, with step-by-step flows only for the few real sequences.

Date: 2026-11-21 · Role: Researcher (Opus 5.5 high lead, 4 Sonnet 5.5 reading workers) · Status: waiting for Shaked's pick · Reviewer pass: none (not a gate; self-review done)
Builds on: [3-0 UX process](3-0-ux-process.md), [03a object map](../03a-object-map.md), 03b places (#36), [decisions.md](../decisions.md) #34-#36.
Page: see docs/status.md for the link.

**How sure we are.** Strong = wide research or long practice. Moderate = a few studies or one strong authority. Opinion = practitioners. The workers could not open most pages in full (the network blocked nngroup.com and others), so every point below was read through search results and is **unverified at page level**.

## What Shaked asked
Before 3c (planned as six core flows), find out how flows work in an OS-like product, because using Sol feels like a way of working, not one path. Maybe it should be spatial.

## What the research says
1. **Operating systems are verbs and nouns; apps are containers.** Apple's App Intents splits everything into *actions* and *entities* (things), and exposes them to Siri, Spotlight and widgets without opening the app. Android's share sheet works on verbs ("send this") that any app can answer (Moderate, Apple and Android docs). No authority states "apps are just containers" as a rule; it is our reading of these two systems (Opinion).
2. **One verb behaves the same everywhere.** Jef Raskin (designer of the original Macintosh project) argued against *modes*, where the same action does different things in different places, because even experienced people make mistakes with them (Opinion, long-cited). For Sol: record must work the same in all eight apps. Sol sorts the note; the app you are in never changes what record does (Assumption: it can still be used as a hint).
3. **A way of working is loops at three speeds.** GTD runs capture, clarify, organize, reflect, engage around one trusted inbox, held together by a weekly review (Strong, long practice). Things and Todoist use one inbox processed daily (Moderate). Sunsama turns the day into two bookends: a morning plan and an evening close that makes you move or drop each unfinished task (Moderate, vendor docs). So the "flows" of a life OS are **moment, day and week loops**, not screen sequences.
4. **Personal systems die from upkeep.** Notion "life OS" setups are abandoned when maintaining them becomes the hobby and the structure is someone else's (Opinion, blogs; no hard data found). Tools that last keep a few fixed types and let the tool do the sorting (Opinion). This supports Sol's "you talk, it sorts" rule.
5. **UX teams don't draw one flow for systems like this.** NN/g separates user flows (one short task), journey maps (one person, one scenario) and wider maps (Strong). Single-path flows fit worst when you can enter from anywhere (Opinion). What fits: **core loops** (Amy Jo Kim; Moderate), **job stories** ("When I..., I want to..., so I can...", Klement and Intercom; Moderate), **day-in-the-life scenarios** (Alan Cooper, *About Face*; Moderate) and an **object-by-action grid** from object mapping (Sophia Prater; Opinion). A small state chart (Harel) covers things with states, such as a note being captured, saved, or partly understood (Strong as long practice).
6. **"Spatial" works as stable places, not as an endless canvas.** People find things by location when the layout never moves: Data Mountain (Microsoft, 1998) and CommandMaps (Scarr and Cockburn, 2012) showed faster finding for practiced users (Moderate). Moving items to "helpful" new spots hurts; highlighting them in place helps (Findlater and McGrenere; Moderate). Zoomable and canvas interfaces have thin or mixed evidence and sprawl on big boards (Moderate to Opinion). Apple's visionOS keeps windows where people put them (Moderate).
7. **"Where I was" can be an object.** Apple's Quick Note and Handoff save the place you were as a link that can reopen it (Moderate). For Sol: every recording keeps a link back to what it made and where it came from (already in #35: "the original note stays attached").

## What this means for Sol
- Sol's flows are **three loops on one inbox** (the entry list, #30): the moment (say it, Sol sorts it, read-back, it lands in its app), the day (morning plan, doing, close), the week (Saturday review).
- **System verbs** are the same in every app: record, find, Home, back to last app, undo, and "turn into" (an idea becomes a task or goal).
- **Home never reorders itself.** Suggestions and numbers light up on the icon or in the widget; icons stay put. Record is always in the same spot.
- The **Map app** is the one place for a canvas; it should not become how you move around Sol.
- Two ideas for later steps, not new scope: a short evening close in the Sol app (Sunsama's shutdown), and a Saturday review in three parts: clear the inbox, review goals and learning, then new ideas (GTD). Both go to docs/ideas.md unless Shaked wants them in 3c.

## Options for what 3c produces
| | What Claude makes | Good | Weak | Shaked's time (Assumption) |
|---|---|---|---|---|
| **A. Loops and verbs** (recommended) | The 3 loops drawn on the map of Sol's places (Home and 8 apps); a grid of system verbs by app; 10-12 "When I..." moments, each with where it starts; short step lists only for the real sequences (first-time setup, read-back fix, Saturday review); every hard moment attached to its loop | Matches how OS teams and life-OS methods think (findings 1-5); is spatial in the way evidence supports (finding 6); checkable: every app has an entry, an action and a way back | Less of a story; feels more like a map than a day | 20 min |
| **B. Three days in the life** | Three told-through days (a normal day, a reserve-duty day, coming back after 3 days off), moving across apps; requirements pulled from them | Easy to feel and correct by voice; Cooper's classic method for "no single path" | Hard to check that nothing is missing; a story covers the paths it tells, not the rest | 20 min |
| **C. Spatial map only** | One drawn map of Home and the 8 apps as places, with arrows for how things travel (a note goes to Learning, an idea becomes a task) | Closest to Shaked's "spatial" instinct; one picture | Shows movement, not rhythm (morning, evening, Saturday); hard moments and verbs get lost | 15 min |

**Recommendation: A.** Evidence: findings 3 and 5 (rhythm loops and job stories fit multi-entry products; Strong to Moderate) and finding 6 (spatial = stable places; Moderate). A already contains C's map as its main picture. One B-style day can be written later, in 3f, as the script for the real-use test.

## Open
- Shaked picks A, B or C, or mixes, on the page. Then the 3c step in 3-0 (six flows) is replaced and logged in decisions.md.
