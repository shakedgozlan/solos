# Research: the agent-building video (2026-11-21)
> Summary: the X post (viktorcarterr) reposts Anthropic's 37-min Code with Claude London workshop "Ship your first Managed Agent" (Isabella He, Applied AI). It teaches one product, Claude Managed Agents, by building an incident-response agent. Not a guide to automating a company. Three proposals for Sol, awaiting Shaked.

Source: Anthropic YouTube upload https://www.youtube.com/watch?v=19HDQ9HppOA, auto English captions read in full. X audio not transcribed (ElevenLabs key still not the sk_ key; not needed).
Page for Shaked: https://claude.ai/artifact/RHVJnppMgrWEVjHcoE1NGL (answers in db collection "picks", doc "agent-video").

## What the talk says
1. Raw API → Agent SDK → Managed Agents: each takes more plumbing off the developer. "Harnesses should evolve alongside your agents" (workarounds for one model became obsolete with the next).
2. Agent = brain (model, short prompt, tools, skills) + environment (hands) + session. Brain kept apart from hands: safer (no credentials in reach), faster (Anthropic claims >90% lower p95 time to first token; unverified).
3. Short system prompt; most developer time goes to context engineering.
4. Sessions are append-only event logs: resume, replay, delete, webhooks wake them. States idle/running/rescheduling/terminated.
5. "Runbook" skills: give the agent the notes humans use.
6. Human as oversight. Advanced: sub-agents, memory + dreaming (scheduled review of past sessions, keeps preferences and corrections; research preview May 2026), outcomes (rubric + separate grader, iterates), vaults.

## Proposals (not applied; Shaked decides)
- A. Sol learns from corrections: every note and correction saved as an event; nightly review keeps lasting lessons. Now only in architecture (4a) and backlog; nightly review after MVP. Recommended.
- B. "Done when" list (3-5 lines) in every thread brief; Reviewer grades against it, up to 2 fix rounds. Recommended.
- C. Save repeated recipes (approval page, status update, decision log) as skills; trim operating-manual rules at the 2026-12-05 check-in.
- Left out: building Sol on Managed Agents (not needed for MVP; price unknown). Revisit for v2 assistant.

Evidence: Park et al. 2023 (Generative Agents, reflection); Shinn et al. 2023 (Reflexion); Anthropic "Building effective agents" (2024) and context-engineering guidance; Haynes et al. 2009 (WHO surgical checklist); event sourcing (long practice). Managed Agents features from Anthropic announcement via search results; docs not opened.
