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
* **Play Together** *(experimental)* - The Companion can act inside a Unity game via socket commands while you play alongside it.

All components are **stream‑pipelined** so the companion speaks & animates all within a few seconds.

## Tech Stack
* **Main Tools** - Python, [LangChain](https://github.com/langchain-ai/langchain)
* **Speech Processing** - [Faster‑Whisper](https://github.com/SYSTRAN/faster-whisper) (ASR), [Pyannote](https://github.com/pyannote/pyannote-audio) (Diarization), [Speechbrain](https://github.com/speechbrain/speechbrain) (Speaker Embeddings & Speaker Recognition)
* **Language** - OpenAI & Vector DB (Pinecone)
* **Audio** - [GPT-SoVITS](https://github.com/RVC-Boss/GPT-SoVITS)
* **Avatar** - [VTube Studio API](https://github.com/DenchiSoft/VTubeStudio)
* **Discord VoiceCalls** - [Discord API](https://github.com/Rapptz/discord.py)
* **Game** - Unity, C# & Sockets
* **ML Libraries** - NumPy & Torch

## Key Features
1. **Streaming Pipeline**  Words, emotions, and speech appear with very low perceived latency.
2. **Emotion‑Aware Voice & Expressions** - Custom trained sentiment classifier modifies avatar expression to match what is being said.
3. **Tool‑Calling Skills**
   * Web Search
   * VTube Studio scene control (toggle props & trigger movements)
   * In‑game actions (move to locations, follow the player, mount/dismount) over sockets
5. **Memory** - Short term for each conversation; long‑term via vector DB, recalling and injecting context of past sessions.

## Demos 
* Showcases the avatar changing emotions mid‑sentence while speaking and toggling items on its own.
 
https://github.com/user-attachments/assets/4afa6dbc-e7f3-479e-ab3c-798d273acb79

* Unity Demo Pending*

## Roadmap
- **Vision Capabilities**
- **Expand Game**

## Contact
*Email*: **spava002@fiu.edu**  
*LinkedIn*: **https://www.linkedin.com/in/sebastian-pava-485859251/**

Feel free to reach out for more information, collaboration, or feedback!

## Credits
- [VTubeStudio Model](https://steamcommunity.com/sharedfiles/filedetails/?id=2802653785&searchtext=)
