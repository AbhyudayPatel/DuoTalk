# DuoTalk

DuoTalk is a pair of AI Audio Agents for real-time voice conversation, using Google Gemini and LiveKit. The agents can engage in either a friendly discussion or a debate on a user-specified topic, with each agent taking on a distinct persona and voice.

## Features
- **Dual AI Voice Agents:** Two agents converse with each other, each with a unique voice and persona
- **Conversation Modes:** Choose between a friendly discussion or a debate format
- **Custom Topics:** Users specify the topic for the conversation at runtime
- **Real-Time Audio:** Uses Google Gemini's real-time model for natural, spoken dialogue
- **Robust Error Handling:** Handles session errors, interruptions, and retries gracefully
- **Voice Personas:** Different voices for each agent (Puck and Charon)

## Requirements
- Python 3.8+
- [LiveKit Agents SDK](https://github.com/livekit/agents)
- [Google Gemini API access](https://aistudio.google.com/)
- Required Python packages:
  - `livekit-agents`
  - `python-dotenv`
  - `google-genai`

## Setup
1. **Clone the repository** and navigate to the project directory.

2. **Install dependencies:**
   ```bash
   pip install livekit-agents livekit-api python-dotenv google-genai
   ```

3. **Set up your environment variables:**
   - Create a `.env` file in the project root
   - Add your Google Gemini API key:
     ```env
     GEMINI_API_KEY=your_gemini_api_key_here
     ```

## Usage
Run the application with:
```bash
python dual_voice_agents.py console
```

### User Inputs
When you start the program, you will be prompted for:

1. **Topic Selection:**
   - The program will ask: `Enter the topic for the conversation:`
   - Type any topic you want the agents to discuss (e.g., "The future of AI", "Climate change", "Space exploration", etc.)

2. **Conversation Mode:**
   - You will be prompted:
     ```
     Select conversation mode:
     1. Friendly discussion
     2. Debate format
     Enter your choice (1 or 2):
     ```
   - Enter `1` for a friendly, collaborative discussion
   - Enter `2` for a debate with opposing viewpoints

### How It Works
- **Friendly Mode:** The agents engage in a supportive, collaborative discussion about the topic
- **Debate Mode:** One agent takes an optimistic perspective while the other takes a skeptical stance
- The conversation runs for up to 12 turns (configurable)
- Each agent has a distinct voice: "Puck" and "Charon"
- Agents respond in one line to optimize API costs

## Configuration
You can customize the following in the code:

- **Maximum Turns:** Default is 12 turns. Modify `max_turns` in the `ConversationState` dataclass
- **Voices:** Default voices are "Puck" and "Charon". Change these in the voice parameters
- **Model:** Currently uses `gemini-2.5-flash-preview-native-audio-dialog`

## Code Structure
- `ConversationState`: Manages conversation state and settings
- `DualPersonaAgent`: Main agent class with dual persona support
- `get_conversation_mode()`: Handles user input for conversation mode
- `run_friendly_conversation()`: Manages friendly discussion flow
- `run_debate_conversation()`: Manages debate flow with optimist/skeptic roles
- `safe_generate_reply()`: Handles agent responses with error handling and retries

## Error Handling
The application includes comprehensive error handling:
- Session health monitoring
- Automatic retries for failed responses
- Graceful cleanup on errors
- Detailed logging for debugging

## License
MIT License