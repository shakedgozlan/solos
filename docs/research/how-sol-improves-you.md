# How Sol keeps improving you
> Summary: Sol makes Shaked better by **closing small loops, not by adding things**. Three loops carry the whole idea: every capture teaches Sol Shaked's words (corrections become examples), every Saturday compares plan with what really happened and changes **one** thing, and every learning session ends with Shaked saying it back in their own words. The approved core loop stands. Four small changes fit inside existing MVP features; everything else goes to Sol Lab or Later. The strongest guard against over-dreaming is a rule: **one in, one out**.

Date: 2026-11-20 · Role: Researcher (Opus 5.5 high lead, 4 Sonnet 5.5 reading workers) · Status: for Shaked's review; feeds the Sol OS map and the user stories thread (2c)
Builds on: [1b-behavior-science.md](1b-behavior-science.md) (habits, if-then plans, streaks, self-compassion are not repeated here), [02-definition.md](../02-definition.md), decisions #22-#29.

**How sure we are.** Strong = meta-analysis or widely adopted engineering practice. Moderate = several studies or one good paper. Weak = small or correlational. Opinion = practitioner claim, no studies. Failed = did not replicate. Workers read most sources at search-result level; only some were opened in full. Items not checked this session are marked "unverified".

## 1. The essence, in one paragraph
"Super mind" is not a feature. The evidence says people get sharper through a few boring things done often: recalling instead of rereading, spacing, explaining in their own words, getting feedback, sleeping and moving. Apps and brain games do not make anyone smarter on their own (brain training: near transfer only, Simons 2016, unverified link). So Sol's job is to make those few things almost free, every day, and to change itself only one small step at a time based on Shaked's own data. That is also the cure for what sank the earlier app.

## 2. Does anything change the core loop?
No. "Say it → Sol understands → see your day → Saturday reflection → Sol Lab suggests one improvement" matches all four lenses. Research adds a feedback arrow: Shaked's corrections and Saturday answers flow back into how Sol understands and what Sol Lab suggests.

## 3. Ranked mechanisms

### MVP (inside features already approved; no new screens)
| # | Mechanism | Where in the MVP | Evidence | Source |
|---|---|---|---|---|
| M1 | **Corrections become examples.** Every fix on the read-back card is saved (what Shaked said, what Sol got, the fix) and the closest 3-5 go into the understanding prompt | Features 2-3 (architecture) | Moderate (in-context learning is well replicated; this exact use is our design) | Brown et al. 2020, arxiv.org/abs/2005.14165 (unverified) |
| M2 | **A small test set grows from real mistakes.** 30-100 real sentences with the right result; every new mistake is added; run it before any prompt or model change | Development practice | Strong (practice) | hamel.dev/blog/posts/evals |
| M3 | **Plan vs actual on Saturday.** "You planned 5 home meals and made 3." If the gap repeats, Sol proposes a smaller step | Feature 13 | Strong (planning fallacy; Buehler/Kahneman, unverified here) | — |
| M4 | **Honest Saturday summary.** It quotes Shaked's own entries and names one thing that did not go well, kindly | Feature 13 | Moderate (AI models tend to flatter users) | arxiv.org/abs/2310.13548 |
| M5 | **"What stuck?" said in Shaked's words**, never a summary written by Sol | Feature 15 | Strong (generation effect d≈0.40, Bertsch 2007; writing to learn g≈0.30, but in school students) | pubmed.ncbi.nlm.nih.gov/17645161 |
| M6 | **Saturday is a fixed short ritual**: same prompts, same order, about five minutes, a clear ending | Feature 13 | Weak to moderate (rituals, Norton and Gino; GTD weekly review is opinion) | dash.harvard.edu (Norton and Gino) |
| M7 | **One in, one out.** At most one Sol Lab change at a time. A new active goal or feature asks which one steps back (Assumption: cap of 3-5 active goals, set in 3c) | Feature 5 + Sol Lab | Weak to moderate (goal conflict, correlational) + Shaked's own history | — |

Build cost: M1 is one table and a few prompt lines; M2 is one file; M3-M7 are wording and rules. Assumption: under one day of build in total.

### Sol Lab (the weekly improvement loop, after 2-4 weeks of real use)
| # | Mechanism | Evidence |
|---|---|---|
| L1 | **Experiment ledger.** Each suggestion is a one-week experiment; Shaked says keep or drop on Saturday; Sol writes one lesson and uses it for the next suggestion. Shaked's answer is the signal, never Sol grading itself | Moderate (Reflexion, arxiv.org/abs/2303.11366) |
| L2 | **"What Sol knows about you"**: a short page of facts Sol learned (usual places, names, patterns). A fact needs 3 or more supporting entries and shows why; Shaked can delete it | Moderate (Generative Agents reflection, arxiv.org/abs/2304.03442; Anthropic context engineering) |
| L3 | **Recall with confidence.** Old "What stuck?" answers return at growing gaps (already feature 23); Shaked first says how sure they are (0-100); Sol shows a calm monthly "how well you know what you know" | Strong (retrieval practice, spacing) + moderate (calibration, unverified) |
| L4 | **"Why does that work?"** One follow-up question after a learning note | Moderate (elaborative interrogation, Dunlosky 2013) |
| L5 | **"Still true?"** One old note resurfaces on Saturday | Opinion (Matuschak) |
| L6 | **Experiment ideas with real evidence**, e.g. a 10-minute brisk walk before a hard thinking block. Small effect, cheap | Moderate (exercise and cognition d≈0.29, likely smaller, nature.com/articles/s41562-023-01554-4) |

### Later
- Links between notes ("this relates to what you said on 3 March"): part of the Mind map (#29). Opinion.
- Tiered memory for the v2 assistant (always-on profile plus searchable archive). Moderate (MemGPT).
- Transition moments: reserve duty pause mode, semester start, project end. Weak as an intervention.
- Optional Saturday share-out to one trusted person. Moderate, high variance.
- Decision journal and pre-mortem. Weak; label it as such if built.

## 4. Do not build
| Idea | Why |
|---|---|
| Identity badges and titles ("You are a reader") | Failed: noun-label studies did not replicate (isps.yale.edu, Gerber 2016/2018). Show real done-things instead |
| Willpower or energy meters | Failed: ego depletion, 23 labs, d=0.04 (pmc.ncbi.nlm.nih.gov/articles/PMC4987495) |
| Brain-training games | Near transfer only (Simons 2016) |
| A life score, leaderboards, all-day logging | Self-tracking research: tracking becomes a chore and people leave (Neff and Nafus) |
| "Review your notes" as a study step | Rereading and highlighting rated low (Dunlosky 2013) |
| Hours counters toward mastery | Practice explains about 12% of performance, under 1% in professions (Macnamara 2014) |
| A goal backlog or dream board | Goal overload; Shaked's own history |

## 5. Risks and guards
- **A wrong fact gets stuck** (one misheard sentence becomes "truth"): facts need 3 entries, show their source and can be deleted (L2).
- **Flattery**: M4.
- **Cost grows with memory**: cap the profile at about 1-2k tokens, use only the top 3-5 corrections, cache the stable part. Assumption: stays inside the $10/month limit.
- **Shaked keeps adding** (the main risk): M7, and Sol Lab changes one thing per week.

## 6. Open, for the real-use test (3c)
- Cap on active goals (3, 4 or 5).
- Is Saturday daytime a no-notification rest day? Fits the weekly rhythm; Shaked to confirm.
- When Sol Lab starts: after 2 or after 4 weeks of use.
