
# PROJECT: VOICE-KHATA – Speech Recognition Optimization

You are a senior speech AI engineer and full-stack developer.

We are improving the speech recognition accuracy of VOICE-KHATA.

## Existing technology
- React 18
- Vite
- Tailwind CSS
- Zustand
- Gnani AI Speech-to-Text
- Gnani AI Text-to-Speech

## Primary objective
Improve speech recognition accuracy for Indian bookkeeping commands.

## IMPORTANT RULES
1. Do not modify the existing application yet.
2. First inspect the entire existing codebase.
3. Identify the current Gnani STT and TTS implementation.
4. Identify microphone recording and audio preprocessing logic.
5. Identify language selection and API configuration.
6. Identify audio encoding, sample rate and channel configuration.
7. Identify API credit consumption and request frequency, if available.
8. Never expose API keys or credentials.
9. Do not replace working components without approval.

## Research and optimization

Investigate:
- Gnani API capabilities and limitations.
- Audio preprocessing opportunities.
- Noise reduction and voice activity detection.
- Language identification.
- Indian English and regional language recognition.
- Code-switching between English and Indian languages.
- Bookkeeping-specific vocabulary.
- Number and currency recognition.

## Benchmarking

Prepare an architecture to compare:
1. Existing Gnani STT.
2. Optimized Gnani STT.
3. Google Cloud Speech-to-Text with model adaptation.

Use identical audio recordings for every engine.

Measure:
- Word Error Rate (WER).
- Character Error Rate (CER).
- Numerical accuracy.
- Currency accuracy.
- Transaction intent accuracy.
- Response latency.

## Dataset

Create a dataset structure containing:
- Audio recordings.
- Correct reference transcripts.
- Language.
- Speaker identifier.
- Transaction category.
- Expected numerical values.

## Deliverables

1. Existing architecture report.
2. Gnani integration audit.
3. Audio quality report.
4. Proposed optimization architecture.
5. Google STT comparison architecture.
6. Credit consumption analysis.
7. Step-by-step implementation plan.

Do not start implementation until I approve the audit.
