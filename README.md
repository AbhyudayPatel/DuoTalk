# 🎤 DuoTalk
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
| 🎭 **Dual AI Voice Agents** | Two agents with unique voices and personas |
| 💬 **Conversation Modes** | Choose between friendly discussion or debate format |
| 🎯 **Custom Topics** | Specify any topic for dynamic conversations |
| 🔊 **Real-Time Audio** | Natural spoken dialogue using Gemini's latest models |
| 🛡️ **Robust Error Handling** | Smart retry logic and graceful error recovery |
| 🎪 **Voice Personas** | Distinct voices: **Puck** (optimistic) & **Charon** (skeptical) |

## 🏗️ Code Architecture
![image](https://github.com/user-attachments/assets/e3a6fa09-b5da-45c5-b97d-5621f0255769)

## 📋 Requirements

> **Prerequisites for running DuoTalk**

- 🐍 **Python 3.8+**
- 🔗 **[LiveKit Agents SDK](https://github.com/livekit/agents)**
- 🧠 **[Google Gemini API access](https://aistudio.google.com/)**

### 📦 Required Python Packages
```bash
livekit-agents
livekit-api  
python-dotenv
google-genai
```

## 🚀 Quick Setup

### 1️⃣ Clone & Navigate
```bash
git clone https://github.com/AbhyudayPatel/DuoTalk.git
cd DuoTalk
```

### 2️⃣ Install Dependencies
```bash
pip install livekit-agents livekit-api python-dotenv google-genai
```

### 3️⃣ Environment Configuration
Create a `.env` file in your project root:
```env
# Add your Google Gemini API key
GEMINI_API_KEY=your_gemini_api_key_here
```

> 💡 **Tip:** Get your API key from [Google AI Studio](https://aistudio.google.com/)

## 🎮 Usage

### 🏃‍♂️ Starting DuoTalk
```bash
python dual_voice_agents.py console
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
1. Friendly discussion
2. Debate format
Enter your choice (1 or 2): _
```

| Mode | 🤝 Friendly Discussion | ⚔️ Debate Format |
|------|------------------------|-------------------|
| **Style** | Collaborative & supportive | Opposing viewpoints |
| **Tone** | Encouraging dialogue | Direct & contrary |
| **Personas** | Agent1 & Agent2 | Optimist vs Skeptic |
| **Voices** | Puck & Charon | Puck & Charon |

### 🎪 Experience the Magic
- 🔄 **12 turns** of dynamic conversation (configurable)
- 🎵 **Distinct voices** for each agent
- 💰 **Optimized responses** (one-line format to save API costs)
- 🔊 **Real-time audio** with natural speech patterns

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

## 🆘 Troubleshooting

<details>
<summary>❓ <strong>Common Issues & Solutions</strong></summary>

### 🔑 API Key Issues
```bash
# Error: Invalid API key
✅ Solution: Verify your Gemini API key in .env file
```

### 🌐 Network Problems
```bash
# Error: Connection timeout
✅ Solution: Check internet connection and API limits
```

### 🔊 Voice Issues
```bash
# Error: Voice not available
✅ Solution: Verify voice availability in your region
```

### 📦 Installation Problems
```bash
# Error: Package not found
✅ Solution: Ensure all packages are installed correctly
pip install --upgrade livekit-agents python-dotenv google-genai
```

</details>

---

<div align="center">

## 📄 License

**MIT License** - See LICENSE file for details

## 🙏 Acknowledgments

| Technology | Purpose |
|------------|---------|
| 🔗 **[LiveKit](https://livekit.io/)** | Real-time communication platform |
| 🧠 **[Google Gemini](https://ai.google.dev/)** | Advanced AI language model |
| 🔧 **[python-dotenv](https://github.com/theskumar/python-dotenv)** | Environment management |

---

*Experience the future of AI conversation today!*

</div>
