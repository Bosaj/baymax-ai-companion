# Baymax AI Companion

> A warm, voice-first AI companion inspired by Baymax: check-ins, reminders and carefully scoped wellness support.

**Status:** pre-alpha scaffold (no code yet). **Feasibility rating:** 5/10 — strong emotional appeal; the hardware robot is out of scope for v1.
**Idea:** #03 in the owner's ideas backlog. **Author:** Oussama EL HADJI. Part of the Bosaj ideas portfolio (sibling repo: `dual_portfolio_hub`).

---

## Problem

People want a companion that checks on them, reminds them about water, medicine and sleep, and answers kindly. Current assistants are transactional and have no caring personality.

## Why build it (gap analysis)

A physical care robot is far harder and more expensive than software. Start with a voice app that has a consistent warm personality and clear limits. It must never present itself as a doctor: anything medical gets a "please talk to a professional" path and emergency numbers.

## Prior art & open bases to fork

- [pipecat-ai/pipecat](https://github.com/pipecat-ai/pipecat) — Open-source framework for real-time voice agents.
- [openai/whisper](https://github.com/openai/whisper) — Speech-to-text, multilingual.
- [rhasspy/piper](https://github.com/rhasspy/piper) — Fast local text-to-speech voices.
- [ollama/ollama](https://github.com/ollama/ollama) — Run local LLMs for a private companion.

## Proposed architecture

1. Voice loop: wake word, speech-to-text, LLM with a fixed persona prompt, text-to-speech.
2. Care engine: scheduled check-ins and reminders with a local store of user preferences.
3. Safety layer: medical and crisis intents are detected and routed to fixed, reviewed answers and emergency contacts.
4. Later: a small desk device (speaker + screen face) running the same software.

## Tech stack (proposed)

- Python or TypeScript voice pipeline (Pipecat)
- Whisper STT, Piper TTS
- Local LLM (Ollama) or hosted Claude
- SQLite for reminders

## Roadmap

- v0.1 — Voice loop with Baymax persona (EN/FR/Darija).
- v0.2 — Reminders and daily check-ins.
- v0.3 — Safety layer for medical and crisis topics.
- v0.4 — Desk device prototype (Raspberry Pi + screen face).

---

## For LLM agents & contributors continuing this project

This repo is a **scaffold**: README + standard files, no implementation yet. If you are an AI agent asked to "continue developing", read this section first.

- Keep the persona in one versioned prompt file with tests for tone and refusals.
- The safety layer is not optional: write its tests before adding wellness features.

**Ground rules:** keep this README in sync with reality as you build; prefer forking/reusing the bases above over greenfield code; write tests for anything correctness-critical; never commit secrets (see `.gitignore`); follow Conventional Commits (see `CONTRIBUTING.md`).

## Getting started

```bash
# nothing to run yet — this is a scaffold.
```

## License

[MIT](LICENSE) — © 2026 Oussama EL HADJI
