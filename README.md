# 🤖 Jarvis — AI Voice Assistant
 
A futuristic, real-time **voice AI assistant** built with [LiveKit Agents](https://docs.livekit.io/agents/) and powered by **Google Gemini Realtime**. Jarvis listens, thinks, and responds naturally — like a premium intelligent assistant.
 
---
 
## ✨ Features
 
- 🎙️ **Real-time voice interaction** via LiveKit WebRTC
- 🧠 **Powered by Google Gemini Realtime** — low-latency, high-quality responses
- 🔊 **AI noise cancellation** using `ai_coustics` for crystal-clear audio input
- 💬 **Conversational & context-aware** — remembers the flow of the conversation
- 🛠️ **Full-stack capable** — coding help, debugging, research, productivity, and more
- 🎯 **Jarvis-style personality** — intelligent, professional, and engaging
---
 
## 📁 Project Structure
 
```
.
├── agent.py          # Main agent logic — LiveKit session, voice model, room I/O
├── prompt.py         # System prompts for agent instructions and response style
├── requirements.txt  # Python dependencies
├── .env              # Environment variables (API keys) — not committed
└── README.md
```
 
---
 
## 🚀 Getting Started
 
### 1. Clone the repository
 
```bash
git clone https://github.com/your-username/jarvis-voice-agent.git
cd jarvis-voice-agent
```
 
### 2. Create a virtual environment
 
```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```
 
### 3. Install dependencies
 
```bash
pip install -r requirements.txt
```
 
### 4. Configure environment variables
 
Create a `.env` file in the root directory:
 
```env
LIVEKIT_URL=wss://your-livekit-server.livekit.cloud
LIVEKIT_API_KEY=your_livekit_api_key
LIVEKIT_API_SECRET=your_livekit_api_secret
GOOGLE_API_KEY=your_google_api_key
```
 
> 💡 Get your LiveKit credentials at [livekit.io](https://livekit.io) and your Google API key from [Google AI Studio](https://aistudio.google.com).
 
### 5. Run the agent
 
```bash
python agent.py dev
```
 
---
 
## 🧠 How It Works
 
1. A user connects to a LiveKit room (via web or mobile frontend).
2. The agent joins the room and starts an `AgentSession` using **Google Gemini Realtime**.
3. Audio input is enhanced in real time using **ai_coustics** noise cancellation.
4. Jarvis processes speech, generates intelligent responses, and speaks back.
---
 
## 🔧 Configuration
 
You can customize Jarvis's behavior by editing the prompts in `prompt.py`:
 
| Variable | Purpose |
|---|---|
| `AGENT_INSTRUCTIONS` | Core personality, rules, and capabilities of the agent |
| `AGENT_RESPONSE` | Response generation style and formatting guidelines |
 
To change the voice, update the `voice` parameter in `agent.py`:
 
```python
llm=google.realtime.RealtimeModel(
    voice="Puck",       # Change to any supported Google voice
    temperature=0.8,
)
```
 
---
 
## 📦 Dependencies
 
| Package | Purpose |
|---|---|
| `livekit-agents` | Core agent framework |
| `livekit-agents[google]` | Google Gemini Realtime integration |
| `livekit-plugins-noise-cancellation` | ai_coustics audio enhancement |
| `python-dotenv` | Environment variable management |
 
---
 
## 🛡️ Safety & Ethics
 
Jarvis is designed to:
- ✅ Provide accurate, helpful, and honest responses
- ❌ Never generate harmful, illegal, or unethical content
- ❌ Never fabricate facts or expose sensitive information
---
 
## 🤝 Contributing
 
Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.
 
---
 
## 📄 License
 
[MIT](LICENSE)
 
---
 
> *"Sometimes you gotta run before you can walk."* — Tony Stark
 
