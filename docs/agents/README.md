# Agent playbook: models and effort
Read when a thread starts, to pick its model and effort. Not loaded on every turn.

Shaked is on the Max plan. Default to Opus 5.5 and tune effort per task. Lowering effort saves more than any prompt does.
- low: quick questions, small edits, copy and CSS tweaks.
- medium: everyday work, most code stories, briefs, design-system tasks.
- high: research synthesis, MVP definition, UX structure, architecture, code review, gate reviews, a bug that medium could not fix.
- xhigh: only a hard, hard-to-undo decision after high fell short.
- max: never by default.
- Sonnet 5.5: well-specified coding stories (medium) and research reading workers (low). Opus reviews Sonnet's code.
- Haiku 5.5 at low: mechanical work only (status updates, renames).
- Fable 5.2: last step of the ladder (Opus medium, high, xhigh, then Fable). Only when Opus at xhigh could not solve it, and only with Shaked's OK.
- Each thread states its role (docs/agents/), model and effort when it starts.
- At low or medium, run a real check before calling code done.
