# TripMate: an AI travel planner

Enter a destination, budget, trip length and travel style, and TripMate builds a personalised plan: a day-by-day itinerary, top attractions, where to stay, transport, an estimated budget breakdown and travel tips. You can then ask follow-up questions like *"cheaper hotels?"* or *"swap day 2 for something outdoors"*.

It comes in two versions:

| Version | File | Highlights |
|---|---|---|
| Desktop app | `TripMate_Desktop_Voice.ipynb` | Tkinter GUI, 🎤 voice input, 🔊 spoken answers, live streaming, save plan to .txt |
| Telegram bot | `TripMate_Telegram_Bot.ipynb` | Guided 4-question chat, style buttons, `/save` sends the plan as a file, optional private mode |

## Run it
```bash
ollama pull llama3.2:1b
pip install -r requirements.txt
```
- **Desktop:** open the notebook and Run All Cells. The window opens on its own.
- **Telegram:** create a bot with @BotFather, then set your token before running:
  ```bash
  set TELEGRAM_BOT_TOKEN=your-token-here      # Windows
  export TELEGRAM_BOT_TOKEN=your-token-here   # macOS/Linux
  ```
  Run all cells and send `/start` to your bot.

**Notes:** voice input uses Google's speech recognition, so it needs internet. Speech output (pyttsx3) works offline. The microphone is recorded with `sounddevice`, so it also works on Python 3.14, where PyAudio won't install.

**Stack:** Python · Tkinter · Ollama · Telegram Bot API · SpeechRecognition · pyttsx3
