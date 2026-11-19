# 1a · Voice input and Instinct export
Researcher thread · Opus 5.5 (high) lead, Sonnet 5.5 reading workers · 2026-11-19

> **Summary.** Cost is not the problem: every serious speech-to-text (STT) engine costs well under $1/month at Sol's volume (1 to 5 hours of audio a month). The problem is accuracy on Shaked's mixed Hebrew/English speech, and **no public benchmark tests Hebrew-English mixing**. So the decision must come from a test on Shaked's own voice. Shortlist: **ElevenLabs Scribe v3, Soniox, ivrit.ai Whisper turbo** (OpenAI as an optional 4th). The free browser dictation (Web Speech API) is out: one language at a time. **Instinct:** we could not identify the app with certainty; the best name match (instinct.com) has no confirmed export, API or iCloud link. Waiting on a screenshot from Shaked.

## 1. Speech-to-text options
Prices from official pricing pages, seen 2026-11-19. "Unconfirmed" = not stated on an official page.

| Engine | Batch price | Free tier | Hebrew | Mixed languages in one note |
|---|---|---|---|---|
| ElevenLabs Scribe v3 | $0.20/h | ~4.5 h/month (free plan) | Hebrew not named on models page (Unconfirmed) | Yes: `secondary_language_codes`; live mode has `multilang_mode` |
| Soniox | ~$0.10/h | Unconfirmed | Yes | Language hints exist; mixing Unconfirmed |
| ivrit.ai Whisper large-v3-turbo | Free (open model) | Free | Hebrew-specialized | Not designed for it (Unconfirmed) |
| OpenAI `gpt-transcribe` | Unconfirmed (realtime variant $0.017/min) | None | Unconfirmed | `languages` hint parameter. Older whisper-1 / gpt-4o-transcribe shut down 2027-02-26 |
| AssemblyAI Universal-2 / STT-3.7 | $0.15/h / $0.21/h | 185 h free | Universal-2: yes, "Good" tier (10-25% WER) | STT-3.7 has code switching (32 languages, Hebrew Unconfirmed) |
| Deepgram Nova-3 | $0.0058/min | $200 credit | Yes | Hebrew in `multi` mode Unconfirmed |
| Google Chirp 2/3 | $0.016/min (batch $0.003) | $300 credit | Yes (`iw-IL`, some regions only) | Unconfirmed |
| Azure Speech | Unconfirmed | 5 h/month realtime | Yes (he-IL) | LLM Speech auto-detects; Hebrew Unconfirmed |
| Gemini Flash (audio prompt) | ~$0.001-0.002/min (Assumption from token rate) | Yes, data used by Google | Unconfirmed | Prompt-driven |
| Web Speech API (browser) | Free | Free | he-IL on iOS Unconfirmed | **No**: one `lang` per session |
| Apple on-device dictation | Free | Free | Yes in keyboard | Native apps only, not reachable from a web app (except the keyboard mic inside a text field) |

Sources: elevenlabs.io/pricing/api · soniox.com/pricing · huggingface.co/ivrit-ai · developers.openai.com/api/docs/guides/speech-to-text · assemblyai.com/pricing · deepgram.com/pricing · cloud.google.com/speech-to-text/pricing · learn.microsoft.com/azure/ai-services/speech-service/language-support · ai.google.dev/gemini-api/docs/pricing · developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition

### Evidence on Hebrew quality (weak, so we test)
- One small blog test (Times of Israel, phone-quality audio, ~120 words, author sells a related service): word error rate Soniox 14-18%, ivrit.ai turbo 25%, gpt-4o-transcribe 61%, Gemini Flash 70%+. Anecdotal.
- ivrit.ai reports 5-7% WER on its public Hebrew leaderboard (clean audio). Could not read the leaderboard page directly.
- The one code-switching benchmark found (ServiceNow, 2025) covers only European languages; ElevenLabs Scribe and AssemblyAI ranked top, stock Whisper last.
- No benchmark covers Hebrew script with English words in one sentence, which is exactly Shaked's speech.

### Why this shortlist
- **Scribe v3:** only engine with an explicit setting for a second language in the same recording; cheapest well-known option; free tier covers Sol's whole volume.
- **Soniox:** best Hebrew result in the only Hebrew comparison found; very cheap.
- **ivrit.ai turbo:** free, best on pure Hebrew. Tells us whether a Hebrew-only model mangles the English words.
- **OpenAI (optional):** new model with a language hint, but older OpenAI models did badly on Hebrew. Test only if setup is cheap.

### Notes for architecture (Phase 2/4)
- Every API engine needs a small server step so the API key never sits in the web app (Assumption: a serverless function on a free tier).
- Fallback that costs nothing: the iPhone keyboard mic inside a text box. It handles Hebrew but not mixing well (Assumption, also tested if Shaked wants).
- At 1-5 h/month, any shortlisted engine costs under $1/month, inside the ~$10 budget.

## 2. Instinct AI
- Shaked's description: iPhone voice-note app that creates reminders, a daily plan and summary, and manages the iCloud calendar.
- Best name match found: **Instinct (instinct.com)**, Spear Street Technology, San Francisco. It is a "no-app" agent used by iMessage, WhatsApp, phone call or a web workspace. No App Store listing found. Confirmed integration: Google Workspace (Calendar, Tasks, Gmail). iCloud, export (Markdown, PDF, CSV), API, webhooks, Shortcuts, Hebrew: all Unconfirmed. Sources: instinct.com/privacy-policy, builtin.com/articles/instinct-ai, eesel.ai/blog/instinct-ai-review.
- Shaked's screenshot (2026-11-19) shows a desktop notification from "Instinct" with a white round "I" icon. That fits instinct.com (it reaches people through iMessage and a Mac app), so this is most likely the app (Assumption: icon not yet matched against an official source). Shaked (2026-11-19): Instinct connects to iCloud Calendar and often has trouble with that connection.
- Implication: Sol should read iCloud Calendar itself (Apple's standard calendar protocol, CalDAV, with an app-specific password), not depend on Instinct. Sol cannot fix Instinct's own connection. In v2, Sol's assistant writes to iCloud directly and the problem goes away. Feasibility to confirm in architecture (Assumption).

### Realistic ways for Sol to get Instinct's data, most to least practical
1. **Read the calendar and reminders it writes.** If Instinct writes to iCloud Calendar/Reminders (or Google Calendar/Tasks), Sol reads those directly. Works without Instinct's cooperation.
2. **A daily iPhone Shortcut** that reads Reminders and Calendar and sends them to Sol. One-time setup, no typing after.
3. **Manual export per note** (share sheet, copy, .md). Unconfirmed; contradicts "no typing", so last resort.
4. **Official API, webhook or Zapier.** None found.

Daily summaries are likely unreachable by any of these. Fits decision #9: in the MVP Sol reads the calendar; Sol's own assistant replaces Instinct in v2.

## 3. Voice test plan (step 1a-test)
1. Shaked records 5 clips (requested 2026-11-19): 3 read sentences with known text (health, learning, money, each mixing Hebrew and English plus numbers), 2 free notes, one in a noisy place.
2. Run each clip through each shortlisted engine with the same settings (Hebrew main, English secondary where supported).
3. Score: word error rate against the reference text; separately count **English words** and **numbers** that came out right, since those drive goal updates.
4. Shaked listens to nothing; they get one table and a recommendation, then approve the engine.
5. Needs: network access to the engines' sites and API keys (free tiers), set in the project's cloud environment.
