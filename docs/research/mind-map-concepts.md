# Mind map: research and 3 concepts
> Summary: A "Mind map" app inside Sol's home screen: a living map of Shaked's interests that feeds a short daily learning batch and learns what keeps Shaked curious. The research says the map is only worth building if it *does* something (decides what comes next, shows what fades), and that the best signal is what Shaked can say back, not what Shaked watched. Three concepts below; Claude recommends **A, Living map**.

Status: post-MVP idea. Does not change the approved MVP scope. Researcher thread, Opus 5.5 medium, 2026-11-20. Sources were read at search-snippet level by 3 parallel workers; anything not confirmed is marked "Assumption" or "unverified".

## 1. What the web says works

**Curiosity**
- Curiosity is strongest when you **know a little** about something, not nothing and not a lot (Kang et al. 2009, "the wick in the candle of learning"). Things learned while curious are also remembered better. In plain words: the best next item sits just past the edge of what Shaked already knows.
- People stay curious when they **feel themselves learning** (Oudeyer's "learning progress"), more than when something is merely new. Detail unverified.
- Curiosity is a gap between what you know and what you want to know (Loewenstein). A good item opens a new question.

**Remembering**
- The best-proven learning method is **retrieval**: trying to recall or explain what you learned (meta-analyses, effect size about 0.5 to 0.7). Rereading and highlighting are weak (Dunlosky et al. 2013).
- **Spaced repetition** (Anki, FSRS): bring a topic back just before you would forget it. FSRS lets you pick a target, for example "remember 90%".
- **Math Academy** links topics in a graph: practising an advanced topic gives credit to the simpler topics under it. This is the strongest example of a map that actually schedules learning. Evidence is the company's own.

**Discovery and surprise**
- Spotify balances "more of what you like" with "try something new" (explore and exploit). For one person, a fixed share of the daily batch is enough, for example 1 or 2 of 7 items from a neighbouring topic.
- **Ground News "Blindspot"** shows stories one side of politics ignores. The idea transfers well: show Shaked what their own reading leaves out.
- Pushing the opposite political side at people can backfire (Bail et al. 2018, Twitter). Better: reasoned long-form from the other side, tied to a topic Shaked already cares about.
- **TikTok "Manage topics"** sliders: users can turn topics up or down. Simple and liked; no evidence it helps learning.

**Maps and graphs**
- Obsidian's graph view is often called "pretty but useless": a hairball you look at once. It helps only when it shows structure and the next action.
- Every Noise at Once (a famous music-genre map) died when Spotify cut its data. Lesson: Sol must own its map data.

**AI tutors**
- NotebookLM (Google) turns your own sources into quizzes, flashcards, mind maps and two-host audio. Socratic tutors (Khanmigo, ChatGPT study mode) show modest gains, and people often skip the questions. AI summaries alone can make you remember *less*.

## 2. What content Sol can pull (checked)

| Source | Free for personal use? | Note |
|---|---|---|
| YouTube | Yes | 10,000 units a day; one search costs 100, so about 100 searches a day. Channel feeds (RSS) cost nothing. Shorts have no official filter (use video length). |
| Podcasts | Yes | Podcast Index (free key) and Apple search. Spotify's API is closed to small apps since 2025-2026. |
| Articles | Yes | RSS feeds, Hacker News. Readwise if Shaked uses it. |
| Reddit | Gated | Since late 2025 you must apply and be approved (dates unverified). Fallback: subreddit RSS. |
| Topic neighbours | Yes | Wikipedia links and categories (Assumption, unverified this session); OpenAlex topics (academic). Claude can also suggest neighbours. |
| Instagram, TikTok | No | No API for a personal feed. Shaked can share a link into Sol instead. |
| YouTube transcripts | Partly | No official way for other people's videos; unofficial tools break often. Use title and description, or Sol listens to the audio (heavier). |

## 3. Three concepts

All three share: a finite daily batch (no endless scroll), Hebrew-first, voice-first, Sol owns the map data, and no guilt when Shaked skips a day.

### A. Living map (recommended)
A map of Shaked's topics, like a world map with fog.
- Each topic glows by **how much Shaked knows** and slowly fades if untouched. Explored topics are bright, nearby topics are dim, far ones are fog.
- Daily batch of about 5: 3 items from the **sweet spot** (topics Shaked knows a little), 1 from a **neighbouring** topic one step out, 1 **comeback** (an older topic just before it fades).
- After an item, one voice question: *"What stuck?"* Shaked answers in 20 seconds. That answer, not the watch time, is what makes a topic grow. Recall is the proven way to remember.
- The map learns which neighbour jumps kept Shaked curious, and makes more jumps like those.
- What is new: the map *is* the scheduler (Math Academy idea) and the feedback is spoken recall, not clicks. No consumer app found does this for general interests.
- Risk: the map view can become decoration. Fix: the map always shows the next step ("3 dim topics are ready to open").
- Size: L. The map visual is the hardest part.

### B. Question trail
The map is made of **open questions**, not topics.
- Every item ends with *"What question does this raise?"* Shaked's spoken question becomes a new node, for example "Why do central banks raise rates?"
- Sol's daily batch hunts for answers to Shaked's open questions. A question closes when Shaked explains the answer back.
- What is new: curiosity drives the feed directly (the information gap idea). Very personal; nobody else's map looks like it.
- Risk: some days Shaked won't have a question; the map grows slowly at first. Needs a starter set of questions.
- Size: M. A list or cluster view is enough at first, no complex map.

### C. Two-sides lens
Built for economics, politics and philosophy.
- The map shows **blindspots**: topics and viewpoints Shaked never reads (Ground News idea, applied to one person).
- Weekly: one pair of strong long-form pieces from two sides of a question. Shaked explains the side they disagree with by voice, and Sol rates how fair the summary was.
- What is new: trains thinking, not only knowing. Fits Shaked's goal "better decisions".
- Risk: narrow (weak for culture and design); can feel like homework. Political pairing needs care (the backfire finding above).
- Size: M.

## 4. Recommendation
**A, Living map**, because it covers every area Shaked named, uses the two best-proven methods (recall and spacing), and turns the "reel that surprised me" into a planned neighbour slot. Take two small pieces from the others: B's "what question did this raise?" as an optional second voice prompt, and C's blindspot as one monthly item, not a weekly task.

Build order (Assumption, to refine in Definition after the MVP): first a plain list of topics with strength and one daily batch from YouTube channel feeds, podcasts and RSS; then the voice "what stuck?"; the visual map last, once there is real data to draw.

**Decided:** A, Living map (Shaked, 2026-11-20, decisions.md #29). The map is also the memory of Sol's private agent: every "what stuck?" answer teaches it what keeps Shaked curious. Data stays in Sol's own database. Assumption to check before building: the AI service Sol uses does not train on Sol's data by default.

## 5. Open questions for Shaked
- Starting topics: Claude suggests a 5-minute voice brain-dump to seed the map.
- How long should a daily batch take: 10, 20 or 30 minutes?

## Sources (main)
Kang et al. 2009: cmu.edu/dietrich/sds/docs/loewenstein/WickCandleLearning.pdf · Dunlosky 2013: psychologicalscience.org/journals/pspi/1529100612453266 · Rowland 2014: pubmed.ncbi.nlm.nih.gov/25150680 · Math Academy: justinmath.com/individualized-spaced-repetition-in-hierarchical-knowledge-structures · FSRS: docs.ankiweb.net/faqs/what-spaced-repetition-algorithm · Spotify bandits: arxiv.org/pdf/2307.09943 · Ground News: about.ground.news/blindspot · Bail 2018: pmc.ncbi.nlm.nih.gov/articles/6140520 · Obsidian graph debate: forum.obsidian.md/t/71316 · Every Noise: techcrunch.com/2024/02/12/every-noise-shut-down-spotify-layoffs · NotebookLM: blog.google/technology/google-labs/notebooklm-student-features · Khanmigo: hechingerreport.org/proof-points-khanmigo-math-ai-tutor · YouTube quota: developers.google.com/youtube/v3/determine_quota_cost · Reddit: support.reddithelp.com (Data API Wiki) · Spotify API: developer.spotify.com/blog/2026-02-06-update-on-developer-access-and-platform-security
