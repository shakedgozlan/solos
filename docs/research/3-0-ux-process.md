# 3-0 · How we make Sol's UX excellent
> Summary: strong teams go **things → places → paths → words → structure → test**, and only then style. For Sol that is six small UX steps (3a-3f), then a UX gate, then UI with Atomic Design. Recommended: **option B**, a grey, unstyled but working prototype on Shaked's phone, copied into Figma for comments; Shaked needs Figma only once, for about 10 minutes in UI.

Date: 2026-11-20 · Role: Researcher (Opus 5.5 high lead, 4 Sonnet 5.5 reading workers) · Status: decided, option B with a Figma mirror (#34) · Reviewer pass: Opus 5.5 high, fixes applied
Builds on: [02-definition.md](../02-definition.md), [02c-user-stories.md](../02c-user-stories.md), [decisions.md](../decisions.md). Sources: [3-0-ux-process-sources.md](3-0-ux-process-sources.md).

**How sure we are.** Strong = wide research or long industry practice. Moderate = a few studies or one strong authority. Opinion = practitioners, no studies. Workers could not open nngroup.com, basecamp.com, material.io or figma.com directly and read them through search results, so those points are marked "unverified".

**Shaked decides:** one option (A, B or C). Two decisions follow from it: UX steps come before Atomic Design (changes part of #31), and in B the coded prototype, not Figma, is the main copy of the design (changes part of #5, where Claude designs in Figma).

## What research says good teams do
1. **Name the things before the screens.** Object mapping (Sophia Prater's method: list the objects, how they relate, what you can do with each, what each holds) settles the nouns before any layout, so every app uses the same model instead of inventing its own (Opinion, widely taught; [Adobe Design](https://adobe.design/ideas/why-ux-designers-should-create-object-maps-and-how-to-start)). For Sol: Task, Entry, Goal, Direction, Usual, Mood, Topic, Recall item, Review, App. They all sit on one entry list (#30, story 4).
2. **Decide the places and how you move between them.** NN/g found visible navigation is used far more than hidden menus, and a home screen that only lists sections costs an extra tap on every move (Moderate, unverified). Sol's home grid is such a list, so it likely needs a small always-visible bar for the 3-4 most used places (Assumption, to test).
3. **Draw paths, not pictures.** Basecamp's Shape Up writes each flow as places, the buttons in them and arrows between them, in plain words with no visual design, and sketches only when the arrangement itself is the problem (Opinion, long practice). Each flow also needs its "not ideal" moments: empty, loading, error, partly understood, offline, microphone refused. Assumption: AI-built apps tend to cover only the smooth path.
4. **Write the real words and data first.** Screens are built around real Hebrew text and realistic data, never placeholder text, in both directions (Hebrew and the English toggle, #2). Mixed text ("פגישה עם Dana ב-14:30") is a known weak spot of right-to-left layouts (Moderate, Material, Apple and Microsoft RTL guides, unverified).
5. **Structure with hierarchy rules, not decoration.** One main thing per screen; size, weight and spacing carry importance; related things sit closer together (Opinion, Refactoring UI). Hebrew readers scan from the top right down the right edge (Moderate, NN/g eye tracking, unverified). A home tile shows one number and one short label, readable at a glance (Moderate, dashboard research and Apple widget guidance; "about 2 seconds" is an Assumption). Main actions sit at the bottom, in thumb reach (Moderate).
6. **Test the real thing, small and often.** Three small rounds of testing beat one big one (Strong, NN/g, unverified). With one user, the best methods are a short diary of real moments ("I wanted to capture something and couldn't") and Wizard of Oz testing, where a person or script plays a smart part that isn't built yet (Moderate, NN/g, unverified). The limit: the builder can't see first-use confusion and tends to report intentions, not behavior, so log what happened and write predictions before each test (Moderate). One optional round with 3-5 friends on a single screen offsets this.
7. **Keep one main copy between design and code.** Design and code drift apart through undocumented states, hard-coded values and two diverging copies (Opinion, Figma's own guides). Teams building with AI now often prototype in code and send it to Figma as editable frames (Opinion, [Figma](https://www.figma.com/blog/the-future-of-design-is-code-and-canvas/)). The trap is polishing that prototype before the core questions are answered ([Google Design](https://design.google/library/code-is-a-design-material)).
8. **Save, then offer undo.** People click through "are you sure?" by habit; undo works better (Moderate, Aza and Jef Raskin). This supports the read-back card that saves on its own (story 3); watch whether Shaked stops reading it.

Skipped on purpose: job stories (02c stories already start "When I..."), opportunity trees and team rituals such as Shape Up's cycles; they solve alignment between people, and Sol has one.

## Avoiding the "AI look"
Designers describe "AI slop" as sameness, not ugliness: purple gradients, one default font, three equal cards with an icon in a circle, emoji as icons, glow, glass, badges everywhere (Opinion, several designer sources). What makes AI-made work look intended:
- A short written design brief before any screen (mood, one accent, two fonts, spacing rules, a "never" list), followed on every screen.
- Real content and every state designed; generic work shows most in empty and error moments.
- Tiles sized by importance, not an even grid; one signature element (likely the record button).
- References picked by Shaked's taste from real apps (Mobbin), not the model's defaults.
- A separate critic on every screen, so Claude never approves its own work.

**Tools:** the anti-slop rule set (with its mobile, visual and accessibility checks) while building; Mobbin for how real apps solve each screen; the Hebrew design-critique skill as the critic; Figma's own skills for writing to Figma; automatic accessibility checks in the test browser. One builder rule set and one critic, because stacking several pulls in different directions (Assumption, Claude's reading of each skill).

## The UX steps
| Step | What Claude makes | What Shaked does | Shaked's time (Assumption) |
|---|---|---|---|
| 3a Things | Object map: every noun in Sol, how they link, what you can do with each | Listen, tap "right / not quite", one voice note | 10 min |
| 3b Places | Screen list with every state, and two ways to move around Sol | Pick one | 10 min |
| 3c Paths | Six core flows as simple diagrams (capture and read-back, morning Today, add a goal, recall, Saturday review, welcome back), with the "not ideal" moments | Walk through, mark what feels wrong | 20 min |
| 3d Words | Real Hebrew and English text and sample data for every screen and state; tone rules | Fix any line that doesn't sound like you | 15 min |
| 3e Structure | Grey screens: position, size and order only, no colour or chosen fonts, in both directions | React to 2 layouts of Home and Today | 20 min |
| 3f Test | Prototype on your phone; predictions written first; 5 real tasks timed (a task saved in 15 seconds or less, measure S4); a week of voice-diary notes | Use it in real life, a few voice notes | 10 min a day |
| UX gate | Test notes turned into fixes; 03-ux.md written | Approve | 10 min |

Then UI with Atomic Design: design brief and references, then design tokens (the named colours, sizes and spacing), then small parts up to full screens, dressing the grey structure.

## Three options: where the UX lives
**A · Figma first.** Claude builds every step in Figma and FigJam through the connector; you review a Figma click-through; code starts after UI.
- For: everything in your own tool and profession; easy to lay variants side by side and comment on them.
- Against: a Figma click-through can't test the microphone, Hebrew typing or the installed app on the phone, the heart of Sol (#17). Figma's agent tools report gaps (custom fonts, size limits per call; unverified). The design is rebuilt in code later, where the two drift.

**B · Real prototype on your phone (recommended).** 3a-3d are short pages and diagrams. From 3e, the grey screens are a real coded prototype on your phone, with the real microphone and right-to-left Hebrew. The voice step uses the real ElevenLabs Scribe and Sol's understanding step (#17) where ready, and scripted replies where not. Each round is copied into Figma as frames for comments. The prototype grows into the app in Phase 4.
- For: tests voice, speed and right-to-left in real life; one main copy, no rebuild.
- Against: Development work starts earlier (Assumption: about 2-3 Claude sessions for the prototype); Figma becomes a viewing copy, not where design is made; risk of polishing too early. Guard: 3e-3f stay grey until the UX gate.

**C · Build now, learn by using.** After 3a-3d, skip 3e-3f and build the MVP with plain styling, fixing what hurts in daily use.
- For: fastest; no throwaway work.
- Against: weakest evidence; structural mistakes surface after they're built, when changes cost most, and the brief's lesson is that costly changes made the earlier app hard to finish.

**Recommendation: B.** It follows the research order and tests the real phone with the real voice, with no double work. Assumption: UX takes about one calendar week, most of it the real-use week in 3f.

## Where Shaked touches Figma
- **During UX (option B): nothing required.** Optional: comment on a frame, or move something if that is faster than describing it.
- **Once in UI:** about 10 minutes to check the Hebrew fonts look right and publish the shared library (Assumption: Figma may need your account for this).

## Critique of the ask
UX before UI is right. One refinement: "how things sit on the page" is the bridge between them, so 3e settles structure with no style, and UI only dresses it.
