# 🎤 DuoTalk  [![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/AbhyudayPatel/DuoTalk)
<div align="center">


**🤖 AI Audio Agents in Real-Time Conversation**

*Experience the future of AI interaction with two agents engaging in dynamic voice conversations*

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![LiveKit](https://img.shields.io/badge/LiveKit-Agents-green.svg)
![Gemini](https://img.shields.io/badge/Google-Gemini-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

</div>

---

## 🌟 Overview

DuoTalk brings AI conversations to life with **two distinct AI audio agents** powered by Google Gemini-realtime and *LiveKit*. Watch as they engage in real-time voice conversations, whether collaborating in friendly discussions or debating opposing viewpoints on any topic you choose.

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🎭 **Dual & Quad AI Voice Agents** | Two or four agents with unique voices and personas |
| 💬 **Conversation Modes** | Choose between friendly discussion, debate, or roundtable format |
| 🌀 **Roundtable Feature** | Four agents share diverse perspectives in a dynamic roundtable |
| 🎯 **Custom Topics** | Specify any topic for dynamic conversations |
| 🔊 **Real-Time Audio** | Natural spoken dialogue using Gemini's latest models |
| 🛡️ **Robust Error Handling** | Smart retry logic and graceful error recovery |
| 🎪 **Voice Personas** | Distinct voices: **Puck** (optimist, pragmatist) & **Charon** (skeptic, theorist) |

## 🏗️ Code Architecture
![image](https://github.com/user-attachments/assets/e3a6fa09-b5da-45c5-b97d-5621f0255769)

## 📋 Requirements

> **Prerequisites for running DuoTalk**

- 🐍 **Python 3.8+**
- 🔗 **[LiveKit Agents SDK](https://github.com/livekit/agents)**
- 🧠 **[Google Gemini API](https://aistudio.google.com/)**

## 🚀 Quick Setup

### 1️⃣ Clone & Navigate
```bash
git clone https://github.com/AbhyudayPatel/DuoTalk.git
cd DuoTalk
```

### 2️⃣ Install Dependencies
```bash
pip install livekit google.genai livekit-agents livekit-api python-dotenv google-genai livekit-plugins-google
```

### 3️⃣ Environment Configuration
Create a `.env` file in your project root:
```env
# Add your Google Gemini API key
GOOGLE_API_KEY=your_gemini_api_key_here
```

> 💡 **Tip:** Get your API key from [Google AI Studio](https://aistudio.google.com/)

## 🎮 Usage

### 🏃‍♂️ Starting DuoTalk
```bash
# For 2 agents (friendly/discussion/debate):
python dual_voice_agents.py console
# For 4 agents (roundtable/friendly/debate):
python four_agents_duotalk.py console
```

### 📝 Interactive Setup

#### Step 1: 🎯 Choose Your Topic
```
Enter the topic for the conversation: _
```
**Examples:**
- `The future of AI and robotics`
- `Climate change solutions`
- `Space exploration and Mars colonization`
- `The ethics of genetic engineering`

#### Step 2: 🎭 Select Conversation Mode
```
Select conversation mode:
1. Friendly discussion (2 agents)
2. Debate format (2 agents)
3. Roundtable discussion (4 agents)
Enter your choice (1, 2, or 3): _
```

| Mode | 🤝 Friendly Discussion | ⚔️ Debate Format | 🌀 Roundtable |
|------|------------------------|-------------------|-------------------|
| **Style** | Collaborative & supportive | Opposing viewpoints | Diverse perspectives |
| **Tone** | Encouraging dialogue | Direct & contrary | Dynamic & engaging |
| **Personas** | Agent1 & Agent2 | Optimist vs Skeptic | Optimist, Skeptic, Pragmatist, Theorist |
| **Voices** | Puck & Charon | Puck & Charon | Puck & Charon (multiple roles) |

## ⚙️ Configuration

<details>
<summary>🔧 <strong>Customization Options</strong></summary>

| Setting | Default | How to Change |
|---------|---------|---------------|
| 🔄 **Max Turns** | 12 turns | Modify `max_turns` in `ConversationState` |
| 🎤 **Agent Voices** | Puck & Charon | Update voice parameters in code |
| 🤖 **AI Model** | `gemini-2.5-flash-preview-native-audio-dialog` | Change model string |
| 💬 **Response Length** | One-line responses | Modify instructions in `DualPersonaAgent` |

</details>


### 🧩 Core Components

| Component | 🎯 Purpose |
|-----------|------------|
| `ConversationState` | 📊 Manages conversation state and settings |
| `DualPersonaAgent` | 🎭 Main agent class with dual persona support |
| `get_conversation_mode()` | 📝 Handles user input for conversation mode |
| `run_friendly_conversation()` | 🤝 Manages friendly discussion flow |
| `run_debate_conversation()` | ⚔️ Manages debate flow with optimist/skeptic roles |
| `safe_generate_reply()` | 🛡️ Handles responses with error handling and retries |

## 🛡️ Error Handling & Reliability

DuoTalk is built with **enterprise-grade reliability**:

<details>
<summary>🔍 <strong>Comprehensive Error Management</strong></summary>

| Feature | Description |
|---------|-------------|
| 📊 **Session Health Monitoring** | Real-time health checks |
| 🔄 **Automatic Retries** | Smart retry logic for failed responses |
| 🧹 **Graceful Cleanup** | Proper resource management |
| 📝 **Detailed Logging** | Comprehensive debugging information |
| ⏱️ **Timeout Protection** | Prevents hanging operations |
| 🔧 **Recovery Mechanisms** | Automatic error recovery |

</details>


## 📄 License

**MIT License** - See LICENSE file for details

*Experience the future of AI conversation today!*

</div>
