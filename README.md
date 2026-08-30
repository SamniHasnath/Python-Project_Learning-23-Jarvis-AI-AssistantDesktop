# 🤖 Jarvis Assistant Desktop

> **A Python-powered voice assistant for Windows that lets you control your desktop, search the web, get information, play music, and interact with AI — all through voice commands.**

Jarvis Assistant Desktop is a lightweight Python-based personal voice assistant designed for Windows. Simply speak a command, and Jarvis can perform tasks such as checking the time and weather, opening applications, searching the web, playing music, taking screenshots, providing system information, and answering general questions using AI.

---

## ✨ Features

### 🎙️ Voice Interaction

* 🎤 Speech recognition for voice commands
* 🔊 Text-to-speech responses using `pyttsx3`
* 🗣️ Natural voice-based interaction
* 👋 Startup greeting and voice feedback

### 🕐 Time & Date

* Check the current time
* Check today's date
* Ask questions such as:

  * `"What's the time?"`
  * `"What's today's date?"`

### 💻 System Information

Get useful information about your computer:

* 🔋 Battery status
* ⚙️ CPU usage
* 🧠 RAM usage
* 💾 Disk usage
* 🌐 IP address
* 🖥️ Basic system information

### 🌐 Web & Search

Jarvis can interact with the web to help you find information:

* 🔎 Google searches
* 📚 Wikipedia summaries
* ▶️ YouTube searches and playback
* 📰 BBC news headlines
* 🌦️ Weather information

Example commands:

```text
"Search Google for Python tutorials"
"Who is Alan Turing?"
"Search YouTube for relaxing music"
"What's the weather in London?"
"Give me today's news"
```

### 🎵 Media Control

Play local music stored inside:

```text
assets/music/
```

Supported functionality includes:

* ▶️ Play music
* ⏹️ Stop music
* 🎵 Browse available local music

Example:

```text
"Play music"
"Stop music"
```

### 🚀 Application Launcher

Open commonly used Windows applications using voice commands.

Supported examples include:

* 📝 Notepad
* 🧮 Calculator
* 🌐 Web browsers
* 💻 Visual Studio Code
* 🎵 Spotify
* ⚙️ Windows Settings
* And other configured applications

Example:

```text
"Open Notepad"
"Open Calculator"
"Open VS Code"
"Open Spotify"
"Open Settings"
```

### 🛠️ Utilities

Jarvis also provides several useful desktop utilities:

* 📸 Take screenshots
* ⏱️ Set timers
* 🪙 Flip a coin
* 🎲 Roll a dice

Example:

```text
"Take a screenshot"
"Set a timer for 5 minutes"
"Flip a coin"
"Roll a dice"
```

Screenshots are automatically stored in:

```text
screenshots/
```

### 😂 Fun & Information

Need something fun?

Jarvis can provide:

* 😂 Jokes
* 💪 Motivational quotes
* 📰 News headlines
* 🌦️ Weather updates
* ℹ️ General information

Try:

```text
"Tell me a joke"
"Give me a motivational quote"
"What can you do?"
```

### 🧠 AI Fallback

If Jarvis doesn't recognize a command as a built-in feature, the request can be sent to an AI model for a response.

The AI fallback uses an OpenAI API key configured through `.env`.

Example:

```text
"Explain quantum computing simply"
"Give me ideas for a Python project"
"What is machine learning?"
```

> **Note:** AI fallback requires an `OPENAI_API_KEY`.

---

# 🏗️ Project Structure

```text
jarvis-assistant-desktop/
│
├── 📄 main.py
│   └── Application entry point
│       ├── Voice setup
│       ├── Speech recognition
│       ├── Text-to-speech
│       ├── AI fallback
│       └── Main assistant loop
│
├── 📄 commands.py
│   └── Assistant commands
│       ├── Time & date
│       ├── Weather
│       ├── System information
│       ├── Web search
│       ├── Music
│       ├── Application launcher
│       ├── Screenshots
│       ├── Timers
│       └── Fun utilities
│
├── 📄 config.py
│   └── Assistant configuration
│       ├── Assistant name
│       ├── Voice settings
│       ├── Music directory
│       └── Environment configuration
│
├── 📄 requirements.txt
│   └── Python dependencies
│
├── 📁 assets/
│   └── 📁 music/
│       └── Local music files
│
├── 📁 screenshots/
│   └── Saved screenshots
│
├── 📄 .env
│   └── API configuration
│
└── 📄 README.md
    └── Project documentation
```

---

# ⚙️ Requirements

Before running Jarvis, make sure you have:

* 🐍 **Python 3.10 or higher**
* 🪟 **Windows operating system**
* 🎤 Working microphone
* 🔊 Working speakers/headphones
* 🌐 Internet connection for online features
* 🔑 OpenAI API key for AI fallback *(optional)*

> This project currently targets Windows because some commands use Windows-specific functionality such as `notepad.exe` and `ms-settings`.

---

# 🚀 Installation

## 1. Clone the Repository

```bash
git clone <repo-url>
```

Navigate into the project:

```bash
cd jarvis-assistant-desktop
```

---

## 2. Create a Virtual Environment

Creating a virtual environment keeps the project dependencies isolated.

```bash
python -m venv venv
```

---

## 3. Activate the Virtual Environment

### Windows CMD

```bash
venv\Scripts\activate
```

### Windows PowerShell

```powershell
venv\Scripts\Activate.ps1
```

After activation, your terminal should show something similar to:

```text
(venv)
```

---

## 4. Install Dependencies

Install the required packages:

```bash
pip install -r requirements.txt
```

For system monitoring features such as battery, CPU, RAM, and disk usage:

```bash
pip install psutil
```

---

# 🔑 Configure OpenAI API

AI fallback is optional.

Create a file named:

```text
.env
```

in the project root.

Add:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

Example project structure:

```text
jarvis-assistant-desktop/
├── main.py
├── commands.py
├── config.py
├── requirements.txt
├── .env
├── assets/
└── screenshots/
```

### ⚠️ Important

Never upload your real API key to GitHub.

Add `.env` to `.gitignore`:

```gitignore
.env
venv/
__pycache__/
*.pyc
```

---

# ▶️ Running Jarvis

Start the assistant with:

```bash
python main.py
```

Jarvis will greet you and begin listening for voice commands.

---

# 🗣️ Example Commands

| Category       | Example                             |
| -------------- | ----------------------------------- |
| 🕐 Time        | `"What's the time?"`                |
| 📅 Date        | `"What's today's date?"`            |
| 🌦️ Weather    | `"What's the weather in London?"`   |
| 😂 Joke        | `"Tell me a joke"`                  |
| 💪 Motivation  | `"Give me a motivational quote"`    |
| 📝 Apps        | `"Open Notepad"`                    |
| 🧮 Apps        | `"Open Calculator"`                 |
| 💻 Development | `"Open VS Code"`                    |
| 🎵 Music       | `"Play music"`                      |
| ⏱️ Timer       | `"Set timer for 5 minutes"`         |
| 📸 Screenshot  | `"Take a screenshot"`               |
| 🔎 Search      | `"Search Google for Python"`        |
| 📚 Wikipedia   | `"Who is Albert Einstein?"`         |
| ▶️ YouTube     | `"Play Python tutorial on YouTube"` |
| 🔋 System      | `"What's my battery status?"`       |
| 📰 News        | `"Give me the latest news"`         |
| 🧠 AI          | `"Explain machine learning"`        |
| ❌ Exit         | `"Goodbye"`                         |

---

# 🎵 Adding Music

To use the local music feature, place your music files inside:

```text
assets/music/
```

For example:

```text
assets/
└── music/
    ├── song1.mp3
    ├── song2.mp3
    └── song3.wav
```

Then say:

```text
"Play music"
```

Jarvis will scan the configured music directory for playable files.

---

# ⚙️ Configuration

You can customize Jarvis through `config.py`.

### Assistant Name

```python
ASSISTANT_NAME = "Jarvis"
```

You can change it to:

```python
ASSISTANT_NAME = "Friday"
```

or:

```python
ASSISTANT_NAME = "Nova"
```

### Voice Configuration

Customize the speech output using:

```python
VOICE_RATE
VOICE_VOLUME
VOICE_INDEX
```

For example:

```python
VOICE_RATE = 170
VOICE_VOLUME = 1.0
VOICE_INDEX = 0
```

### Music Directory

Configure where Jarvis searches for local music:

```python
MUSIC_DIR = "assets/music"
```

---

# 🧠 How Jarvis Works

The basic workflow is:

```text
              ┌─────────────────┐
              │   User Speaks   │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Speech          │
              │ Recognition     │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Command Router  │
              └────────┬────────┘
                       │
              ┌────────┴────────┐
              │                 │
              ▼                 ▼
       Built-in Command     Unknown Command
              │                 │
              ▼                 ▼
       Execute Action      AI Fallback
              │                 │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Generate Reply  │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Text-to-Speech  │
              └────────┬────────┘
                       │
                       ▼
                 🔊 Response
```

---

# 🧩 Core Components

### `main.py`

The main entry point of the application.

Responsible for:

* Initializing the assistant
* Configuring speech recognition
* Configuring text-to-speech
* Handling the main listening loop
* Sending unmatched requests to AI

### `commands.py`

Contains the assistant's command implementations and command router.

Responsible for:

* Time/date commands
* Weather
* Search
* Music
* Application launching
* Screenshots
* Timers
* System information
* Fun commands

### `config.py`

Contains configurable assistant settings.

Responsible for:

* Assistant name
* Voice configuration
* Music directory
* Environment variables
* Other application settings

---

# 🛡️ Security

If you use an OpenAI API key, make sure it is stored securely.

### Never commit:

```text
.env
```

### Recommended `.gitignore`

```gitignore
# Environment
.env

# Virtual environment
venv/
.venv/

# Python cache
__pycache__/
*.py[cod]

# IDE
.vscode/
.idea/

# Generated files
screenshots/*
```

---

# 🐛 Troubleshooting

### Microphone is not working

Make sure:

* Your microphone is connected.
* Windows has microphone permissions enabled.
* The correct microphone is selected as the default input device.

### Jarvis doesn't understand my voice

Try:

* Speaking closer to the microphone.
* Reducing background noise.
* Speaking more clearly.
* Checking your internet connection if the recognition service requires it.

### AI fallback doesn't work

Check that your `.env` contains:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

Also make sure the required AI package and API configuration are installed correctly.

### `psutil` errors

Install it manually:

```bash
pip install psutil
```

---

# 🚧 Future Improvements

Possible improvements for future versions:

* [ ] 🪟 Modern graphical user interface
* [ ] 🌙 Dark/light themes
* [ ] 🔐 User authentication
* [ ] 🧠 Conversation memory
* [ ] 🤖 More advanced AI agent capabilities
* [ ] 📂 File and folder management
* [ ] 📧 Email automation
* [ ] 📅 Calendar integration
* [ ] 💬 WhatsApp/Telegram integration
* [ ] 🏠 Smart home control
* [ ] 🔍 Advanced system monitoring
* [ ] ⚡ Wake-word detection
* [ ] 🎙️ Continuous listening mode
* [ ] 🌍 Multi-language support
* [ ] 📊 Activity/history dashboard

---

# 📸 Project Preview

Add your project screenshot here:

```markdown
![Jarvis Assistant Desktop](screenshots/jarvis-preview.png)
```

---

# 📚 Technologies Used

| Technology               | Purpose                   |
| ------------------------ | ------------------------- |
| 🐍 Python                | Core programming language |
| 🎤 Speech Recognition    | Voice input               |
| 🔊 pyttsx3               | Text-to-speech            |
| 🧠 OpenAI                | AI fallback               |
| 🌐 Web APIs              | Online information        |
| 💻 Windows APIs/Commands | Desktop automation        |
| 📊 psutil                | System monitoring         |
| 🎵 Local Media           | Music playback            |

---

# 🎯 Project Goals

The main goal of Jarvis Assistant Desktop is to demonstrate how Python can be used to build a practical desktop voice assistant by combining:

**Speech Recognition + Automation + APIs + System Control + AI**

The project is also designed as a learning project for exploring Python automation, voice interfaces, API integration, and AI-powered applications.

---

# 📄 License

This project is intended for **personal and educational use**.

Feel free to modify and extend it for your own learning and experimentation.

---

# 👨‍💻 Author

**Your Name**

If you found this project useful, consider giving the repository a ⭐ on GitHub!

---

## ⭐ Support the Project

If you like this project:

⭐ Star the repository
🍴 Fork the repository
🐛 Report issues
💡 Suggest new features
🚀 Build your own version

---

> **"Your desktop. Your voice. Your assistant." 🤖**

# Jarvis Assistant Desktop

A Python-based voice assistant for desktop. Talk to it, and it'll tell you the time, fetch the weather, crack a joke, open apps, search the web, play music, and more — with an AI fallback (OpenAI) for everything else.

<img width="800" height="600" alt="image" src="https://github.com/user-attachments/assets/6ced6ead-d72f-4cb5-b388-a306c0d0f4e2" />

## Features

- **Voice in / voice out** — speech recognition for input, `pyttsx3` for spoken replies
- **Time & date** — "what's the time", "what's the date"
- **System info** — battery status, CPU/RAM/disk usage, IP address
- **Web & search** — Google search, Wikipedia summaries, YouTube playback
- **Media** — play/stop local music from `assets/music`
- **Apps** — open common apps (Notepad, Calculator, browsers, VS Code, Spotify, etc.)
- **Utilities** — screenshots, timers, coin flip, dice roll
- **Fun & info** — jokes, motivational quotes, BBC news headlines, weather
- **AI fallback** — anything not matched by a built-in command is sent to OpenAI's `gpt-3.5-turbo`

## Project Structure

```
jarvis-assistant-desktop/
├── main.py            # Entry point: TTS/STT setup, AI fallback, main loop
├── commands.py        # All command implementations + command router
├── config.py          # Assistant settings, voice config, .env loading
├── requirements.txt   # Python dependencies
├── assets/
│   └── music/         # Local music files for the "play music" command
└── screenshots/        # Saved screenshots from the "take a screenshot" command
```

## Requirements

- Python 3.10+
- A working microphone and speakers
- Windows (uses Windows-specific commands like `notepad.exe`, `start ms-settings:`, etc.)

## Installation

1. Clone the repository
   ```bash
   git clone <repo-url>
   cd jarvis-assistant-desktop
   ```

2. Create and activate a virtual environment (recommended)
   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

3. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

   For battery/CPU/RAM/disk info, also install:
   ```bash
   pip install psutil
   ```

4. (Optional) Create a `.env` file in the project root for AI fallback replies:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

## Usage

Run the assistant:
```bash
python main.py
```

Jarvis will greet you and start listening. Speak a command — for example:

- "What's the time?"
- "What's the weather in London?"
- "Tell me a joke"
- "Open notepad"
- "Play music"
- "Set timer for 5 minutes"
- "What can you do?"
- "Goodbye" (to exit)

If a command isn't recognized, it's passed to the AI fallback (requires `OPENAI_API_KEY`).

## Configuration

Edit `config.py` to customize:

- `ASSISTANT_NAME` — the assistant's name (default: `Jarvis`)
- `VOICE_RATE`, `VOICE_VOLUME`, `VOICE_INDEX` — text-to-speech voice settings
- `MUSIC_DIR` — folder scanned for playable music files

## License

This project is for personal/educational use.
