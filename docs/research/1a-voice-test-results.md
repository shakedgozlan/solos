# 1a voice test: results
Updated: 2026-11-19 · by: Researcher 1a-test (Opus 5.5, high) · Status: done, ElevenLabs Scribe approved (decisions.md #17)

> **Recommendation: ElevenLabs Scribe.** On the three read sentences it made no meaning errors. ivrit.ai made two: Wolt became "וולד", and "של אוכל בחוץ" (the budget category) became nonsense. On the noisy free-speech clip ElevenLabs was clearly cleaner. Neither engine writes most English words in English letters, and ElevenLabs writes numbers as words ("שמונים ושתיים נקודה ארבע"). Sol's AI step must turn both into clean data, which it needs to do anyway. Soniox was dropped (decision #16).

## Setup
- Recordings: Shaked's 5 clips (/mnt/project-files/voice-test/). 1-3 are read sentences with known text; 4-5 are free speech of about 55 s (5 is noisy).
- ivrit.ai: `ivrit-ai/whisper-large-v3-turbo-ct2`, faster-whisper on CPU (4 cores, int8), language "he". Speed: 5 s for a 10 s clip, 13 s for a 55 s clip.
- ElevenLabs Scribe: run by Shaked on the ElevenLabs website (the API key in the environment was the key ID, not the key). Exact model and settings the site used: Assumption, latest Scribe with Hebrew.
- Raw transcripts: /mnt/project-files/voice-test/results/ (kept out of the repo, personal content).
- Scoring: word error rate (WER: the share of words wrong) after removing punctuation, with spelled-out numbers converted to digits; plus a hand count of what matters for goal updates.

## Results

| | ivrit.ai Whisper | ElevenLabs Scribe |
|---|---|---|
| WER, sentences 1 / 2 / 3 | 29% / 18% / 25% | 29% / **6%** / 25% |
| Numbers heard right (5) | 5 of 5, as digits | 5 of 5, **as words** |
| English words in English letters (8) | 0 | 2 (Atomic Habits) |
| English words recognizable in Hebrew letters | 7 of 8 (Wolt lost) | **8 of 8** |
| Meaning errors in sentences 1-3 | 2 (brand, budget category) | **0** |
| Misheard phrases, free speech 4 / 5 | 1 / 4 | 1 / 0 (see note) |
| Extras | Clean text | Adds fillers ("אמ"), sound tags ("[נשימה]") and timestamps; strip in Sol |

Most of the remaining WER is English written in Hebrew letters ("וורקאוט" vs "workout"), which both engines do. Note on 4-5: the references were built from both transcripts and are not yet confirmed by Shaked, so the 4-5 count leans toward whichever engine made sense where they disagreed. ElevenLabs' one miss in 4 was "Claude", heard as "בקלות"; ivrit.ai got it right.

## What it means for Sol
- Speech-to-text alone does not produce clean data. A short AI step after it must turn "שמונים ושתיים נקודה ארבע" into 82.4 and "וורקאאוט" into workout. Plan it in architecture (Phase 2/4).
- ElevenLabs needs no model hosting, and its free tier covers Sol's volume (1a research). ivrit.ai would need Sol to run a server with the model (Assumption: a small CPU server is enough at this speed).
- Worth testing in the API later: ElevenLabs' setting for a second language (English), which may keep more English in English letters (Assumption).
- Wispr Flow (Shaked's idea): a dictation keyboard, not a service Sol can call (Assumption: no public speech API). Not tested.

## Next
1. Done: Shaked approved ElevenLabs Scribe (#17).
2. Shaked confirms references for 4-5 (/mnt/project-files/voice-test/references-4-5-draft.md). Optional; it won't change the pick.
3. Shaked saves the real `sk_` ElevenLabs key before development (Phase 4).
