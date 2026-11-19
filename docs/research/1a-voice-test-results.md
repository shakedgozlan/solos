# 1a voice test: results
Updated: 2026-11-19 · by: Researcher 1a-test (Opus 5.5, high) · Status: **partial** (ElevenLabs not run yet)

> **Summary.** Only ivrit.ai Whisper turbo has run so far. It got every number right (5 of 5) and kept the meaning of 2 of the 3 read sentences. But it writes every English word in Hebrew letters ("וורקאוט", "דצמבר"), and in sentence 3 it turned "של אוכל בחוץ" (the budget category) into nonsense. ElevenLabs is blocked by a wrong saved key. Soniox is dropped (Shaked, 2026-11-19: $10 minimum top-up, not worth it). **No engine is recommended yet.** The pick comes after ElevenLabs runs.

## Setup
- Recordings: Shaked's 5 clips (/mnt/project-files/voice-test/). 1-3 are read sentences with known text; 4-5 are free speech (5 noisy), 52-56 s each.
- ivrit.ai: `ivrit-ai/whisper-large-v3-turbo-ct2`, faster-whisper on CPU (4 cores, int8), language "he", beam 5. Speed: 5 s for a 10 s clip, 13 s for a 55 s clip.
- Raw transcripts: /mnt/project-files/voice-test/results/ (kept out of the repo, personal content).
- Scoring: word error rate (WER, the share of words wrong) after removing punctuation; plus a hand count of numbers and English words that came out usable.

## Results, recordings 1-3

| | ivrit.ai Whisper | ElevenLabs Scribe |
|---|---|---|
| Strict WER (English must be in English letters) | 29% / 18% / 25% | not run |
| Numbers right (82.4, 35, 9,000, 20, 64) | **5 of 5** | not run |
| English words in English letters | 0 of 8 | not run |
| English words recognizable when read in Hebrew letters | 7 of 8 (Wolt became "וולד") | not run |
| Meaning errors that would break a goal update | 1: "של אוכל בחוץ" became "שלא אחרי בחוץ" | not run |
| Recordings 4-5 (free speech) | Reads fluently; 2-3 unclear phrases each. Scored once Shaked confirms the references | not run |

What this means in plain words: ivrit.ai hears Hebrew and numbers well, but it has no way to write English as English. Sol's AI step could still understand "וורקאוט" or "גרמין", but brand names like Wolt get lost, and one wrong word in a category name puts money in the wrong budget.

## Blocked or dropped
- **ElevenLabs Scribe:** the saved network secret is the key's ID, not the `sk_…` key (ElevenLabs error `api_key_id_used_as_api_key`, seen from two separate sessions). Waiting on Shaked to save the real key.
- **Soniox:** dropped by Shaked (decisions.md #14).
- **Wispr Flow** (Shaked's idea, 2026-11-19): a dictation keyboard, not a service Sol can call (Assumption: no public speech API; to verify). Can be tested by Shaked dictating sentences 1-3 and pasting the text.

## Next
1. Shaked confirms references for 4-5 (/mnt/project-files/voice-test/references-4-5-draft.md).
2. Run ElevenLabs on all 5 with Hebrew main and English secondary; score the same way.
3. Recommend one engine. Leaning (Assumption until tested): ElevenLabs, if it keeps English in English letters with the same number accuracy, since its free tier covers Sol's volume and it needs no model hosting.
