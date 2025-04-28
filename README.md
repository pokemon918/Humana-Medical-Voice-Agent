# AI-Powered Voice Agent for Medical Practice

## Overview

This project is a prototype for an AI-powered voice agent designed to handle incoming calls for a medical practice. It focuses on demonstrating the voice interaction workflow for appointment scheduling and management using advanced AI technologies.

## Core Features

### Voice Interaction
- Real-time voice conversations using ElevenLabs' conversational AI
- Natural language understanding and response generation
- Seamless voice-to-text and text-to-voice conversion

## Technologies Used

### Core Services
- **ElevenLabs**: Voice generation and conversational AI
- **Twilio**: Call handling and SMS functionality
- **OpenAI**: Natural language processing and understanding

### Backend Stack
- FastAPI: Modern, fast web framework
- WebSocket: Real-time audio streaming
- Pydantic: Data validation
- Langchain: AI/LLM integration framework

## Setup Requirements

1. Clone the repository:
   ```bash
   git clone https://github.com/pokemon918/Humana-Medical-Voice-Agent
   cd Humana-Medical-Voice-Agent
   ```

2. Create a virtual environment:
   ```bash
   python -m virtualenv venv
   source venv/bin/activate # On Windows: venv\Scripts\activate
   ```

3. Install Dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Update the env file with your own credentials and keys based on .env.example file.

5. Run the Application:
   ```bash
   python manage.py
   ```

6. Start ngrok tunnel:
   ```bash
   ┌──────────────────────────────────────────────────┐
   │  1. Install ngrok from https://ngrok.com         │
   │  2. Open terminal and run:                       │
   │     $ ngrok http 5000                            │
   │                                                  │
   │  📋 Copy the Forwarding URL:                     │
   │     https://[your-ngrok-subdomain].ngrok.app     │
   │     or                                           │
   │     https://[your-ngrok-subdomain].ngrok-free.app│
   └──────────────────────────────────────────────────┘
   ```

7. Configure Twilio:
   ```bash
   ┌──────────────────────────────────────────────────┐
   │  Update Twilio Webhook URL:                      │
   │  1. Go to Twilio Console                         │
   │  2. Find your phone number                       │
   │  3. Set Webhook URL to your ngrok URL            │
   └──────────────────────────────────────────────────┘
   ```

8. Call your Twilio phone number and test the application.

## Project Structure

```
app/
├── core/
│   ├── config.py           # Configuration settings
│   ├── logger.py           # Logging setup
├── routers/
│   └── main.py            # Main API routes
├── services/
│   ├── twilio_sms.py      # SMS functionality
│   └── twilio_audio_interface.py # Audio handling
└── utils/                  # Utility functions
```

## Future Enhancements

- Advanced appointment availability checking
- Multi-language support
- Enhanced security measures
- Comprehensive logging and monitoring
- Additional EHR integrations
