# 1. Architecture

1. Voice loop: wake word, speech-to-text, LLM with a fixed persona prompt, text-to-speech.
2. Care engine: scheduled check-ins and reminders with a local store of user preferences.
3. Safety layer: medical and crisis intents are detected and routed to fixed, reviewed answers and emergency contacts.
4. Later: a small desk device (speaker + screen face) running the same software.

## Proposed stack
- Python or TypeScript voice pipeline (Pipecat)
- Whisper STT, Piper TTS
- Local LLM (Ollama) or hosted Claude
- SQLite for reminders

## Open bases to fork
- [pipecat-ai/pipecat](https://github.com/pipecat-ai/pipecat) — Open-source framework for real-time voice agents.
- [openai/whisper](https://github.com/openai/whisper) — Speech-to-text, multilingual.
- [rhasspy/piper](https://github.com/rhasspy/piper) — Fast local text-to-speech voices.
- [ollama/ollama](https://github.com/ollama/ollama) — Run local LLMs for a private companion.
