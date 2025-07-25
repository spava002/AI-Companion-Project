## AI Companion — Overview

**Disclaimer for Prospective Employers**  
The source code for this project is private.  If you would like a guided walkthrough or a live demonstration of the system, please contact me directly and I’ll be happy to showcase the implementation, discuss design choices, and answer questions in detail.

## What Is It?
An **AI Companion** that listens, understands, reacts, and *comes to life* on screen in near‑real‑time.

* **Speech To Text** - Low‑latency ASR streams audio and produces transcripts on the fly.
* **Who Said What?** - Speaker diarization splits the conversation; speaker‑recognition embeddings identify known voices.
* **Reasoning & Memory** - An LLM uses tool calling to perform actions, and maintains short term memory for current conversations, and a vector DB for long‑term memory.
* **Text To Speech** - A TTS engine synthesises the reply with minimal delay.
* **Visual Persona** - Sentiment analysis drives dynamic emotion changes through the VTube Studio API.
* **Discord Calls** - Paired with a discord bot, the companion can join discord voice calls with multiple people, where it can listen and respond - being part of the conversation.
* **Natural Conversation Flow** - With a toggleable feature, the AI can be interrupted mid-speech and will pause to listen, allowing for more fluid, human-like interactions. It also uses conversational context and speaker tracking to determine the right moments to respond - especially useful in multi-speaker environments!
* **Play Together** *(experimental)* - The Companion can act inside a Unity game via socket commands while you play alongside it.

All components are **stream‑pipelined** so the companion speaks & animates all within a few seconds.

## Tech Stack
* **Main Tools** - Python, [LangChain](https://github.com/langchain-ai/langchain)
* **Speech Processing** - [Silero-VAD](https://github.com/snakers4/silero-vad) (Voice Activity Detection)[Faster‑Whisper](https://github.com/SYSTRAN/faster-whisper) (ASR), [Pyannote](https://github.com/pyannote/pyannote-audio) (Segmentation), [Speechbrain](https://github.com/speechbrain/speechbrain) (Speaker Embeddings & Speaker Recognition)
* **Language** - OpenAI & Vector DB (Qdrant)
* **Audio** - [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS)
* **Avatar** - [VTube Studio API](https://github.com/DenchiSoft/VTubeStudio)
* **Discord VoiceCalls** - [Discord API](https://github.com/Rapptz/discord.py)
* **Game** - Unity, C# & Sockets
* **ML Libraries** - NumPy & Torch

## Key Features
1. **Streaming Pipeline** - Words, emotions, and speech appear with very low perceived latency.
2. **Emotion‑Aware Voice & Expressions** - Custom trained sentiment classifier modifies avatar expression to match what is being said.
3. **Tool‑Calling Skills**
   * Web Search
   * VTube Studio scene control (toggle props & trigger movements)
   * In‑game actions (move to locations, follow the player, mount/dismount) over sockets
5. **Memory** - Short term for each conversation; long‑term via vector DB, recalling and injecting context of past sessions.

## Demos 
 
[![Watch the video](https://img.youtube.com/vi/EWs77U05xxU/0.jpg)](https://www.youtube.com/watch?v=EWs77U05xxU)

## Roadmap
- **Expand Discord Capabilities**
- **Vision Capabilities**
- **Expand Functionalities To Allow Game Playing**

## Contact
*Email*: **spava002@fiu.edu**  
*LinkedIn*: **https://www.linkedin.com/in/sebastian-pava**

Feel free to reach out for more information, collaboration, or feedback!
