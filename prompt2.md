
Continue the VOICE-KHATA speech recognition audit.

IMPORTANT: READ-ONLY MODE. Do not edit application files or make API calls.

Investigate the following:

1. Find every file related to:
   - Gnani STT
   - Gnani TTS
   - Audio recording
   - Microphone permissions
   - Audio conversion
   - API requests
   - Language configuration
   - Speech recognition responses

2. Trace the complete pipeline:

   Microphone
      -> Audio recording
      -> Audio preprocessing
      -> Gnani API
      -> Transcription
      -> Zustand state
      -> Transaction processing
      -> UI

3. Identify:
   - Actual audio MIME type.
   - Actual sample rate.
   - Number of audio channels.
   - Audio encoding.
   - Maximum recording duration.
   - API timeout and retry logic.
   - Language configuration.
   - Error handling.
   - Duplicate API requests.

4. Identify potential causes of:
   - Incorrect transcriptions.
   - Incorrect numerical values.
   - Poor regional language recognition.
   - Code-switching failures.
   - High latency.

5. Examine whether the current implementation supports:
   - Language selection.
   - Multiple language recognition.
   - Automatic language detection.
   - Custom vocabulary.
   - Confidence scores.
   - Streaming transcription.

6. Prepare a proposed multilingual architecture.

7. Prepare a benchmark framework using the
   same audio recordings for Gnani and Google STT.

8. Create a report containing:
   - File paths.
   - Existing implementation details.
   - Problems discovered.
   - Recommended changes.
   - Expected benefits.
   - Risks and API costs.

Do not expose secrets or print .env values.
Do not install dependencies.
Do not modify files.
Do not consume Gnani API credits.

Finish with a prioritized implementation plan.
