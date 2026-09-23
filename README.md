# 🤖 Erisa — Personal AI Assistant

**Erisa** is a private personal AI assistant project focused on combining conversational AI, voice interaction, long-term memory, avatar integration, and mobile connectivity into a single system.

The project is developed primarily as a hands-on exploration of how different AI and software components can work together as one application.

> 🔒 **Source code is private. This repository is a public technical showcase and documentation of the project.**

---

## Overview

Erisa is designed around a modular pipeline that connects speech, AI processing, memory, and voice output.

The current system includes:

* 🎙️ Speech recognition
* 🧠 Local AI model integration
* 🗃️ Long-term memory
* 🔊 Text-to-speech
* 🎭 Avatar integration
* 📱 Mobile control
* 🌐 WebSocket communication
* 🖥️ Desktop control interface

The project is intentionally being developed incrementally, with an emphasis on understanding each component rather than relying entirely on pre-built assistant frameworks.

---

## Architecture

```text
                    ┌──────────────────┐
                    │      User        │
                    └────────┬─────────┘
                             │
                     Voice / Text Input
                             │
                             ▼
                  ┌─────────────────────┐
                  │   Speech / Input    │
                  │     Processing      │
                  └──────────┬──────────┘
                             │
                             ▼
                  ┌─────────────────────┐
                  │   Erisa Controller  │
                  └──────┬───────┬──────┘
                         │       │
              ┌──────────┘       └──────────┐
              ▼                             ▼
      ┌───────────────┐              ┌──────────────┐
      │ Memory System │              │   AI Model   │
      └───────┬───────┘              └──────┬───────┘
              │                             │
              └──────────────┬──────────────┘
                             ▼
                     ┌───────────────┐
                     │ Response / TTS│
                     └───────┬───────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ Voice / Avatar  │
                    └─────────────────┘

                    📱 Mobile Client
                           │
                       WebSocket
                           │
                           ▼
                   ┌─────────────────┐
                   │ Erisa Network   │
                   │     Server       │
                   └─────────────────┘
```

---

## Technology Stack

### AI & Speech

* **Python**
* **Ollama** — local AI model execution
* **faster-whisper** — speech recognition
* **Resemblyzer** — voice identification
* **Kokoro** — text-to-speech

### Application

* Python-based application architecture
* Tkinter desktop control interface
* JSON-based memory storage
* Asynchronous processing and queues
* WebSocket networking

### Avatar

* **VTube Studio**
* Live avatar control
* Audio-driven lip synchronization
* Hotkey-based avatar actions

### Mobile

* Android
* Kotlin
* Jetpack Compose
* WebSocket communication

---

## Current System

The current version runs as a desktop application with a mobile client being developed alongside it.

The desktop application handles the primary AI pipeline while the mobile application acts as a remote interface and communication client.

This separation allows the system to evolve toward a more distributed architecture without requiring the AI processing to run entirely on the phone.

---

## Key Engineering Challenges

### 1. Connecting Multiple AI Components

Erisa combines several independent systems:

```text
Speech
  ↓
Voice Identification
  ↓
Memory Retrieval
  ↓
AI Processing
  ↓
Text-to-Speech
  ↓
Avatar / Audio Output
```

Managing these components while keeping the application responsive has been one of the main architectural challenges.

### 2. Local AI Constraints

The project is designed around consumer hardware rather than dedicated AI servers.

This makes **latency, VRAM, RAM usage, and model size** important design considerations.

### 3. Voice Interaction

Speech recognition and voice identification are handled separately so that the assistant can distinguish between recognized and unknown speakers.

### 4. Mobile Connectivity

The mobile client communicates with the desktop application through WebSockets.

This provides a lightweight communication layer for commands, chat messages, and future remote-control functionality.

---

## Development Philosophy

Erisa is being developed as a **learning-through-building project**.

Instead of treating the assistant as a single AI model wrapped in a user interface, the project explores how individual systems such as speech recognition, memory, networking, TTS, and avatar control can be designed and connected together.

The architecture is expected to evolve as new capabilities are added.

---

## Roadmap

### Current

* [x] Desktop control interface
* [x] Conversational AI pipeline
* [x] Speech recognition
* [x] Voice identification
* [x] Text-to-speech
* [x] Persistent memory
* [x] Avatar integration
* [x] WebSocket server
* [ ] Mobile application refinement

### Future

* [ ] More robust distributed architecture
* [ ] Improved mobile control
* [ ] Remote access
* [ ] Screen/visual understanding
* [ ] More advanced memory retrieval
* [ ] Better resource management
* [ ] Additional automation capabilities

---

## Privacy

Erisa is a personal project and its implementation remains private.

This repository intentionally contains **documentation rather than source code**.

No personal recordings, authentication credentials, private memories, local model files, or other sensitive project data are included.

---

## Author

**Rishabh Singh**

BCA Student · Software Development · AI & Game Development

GitHub: [@rissarty](https://github.com/rissarty)
