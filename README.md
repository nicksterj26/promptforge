# ⚡ PromptForge

> Turn your messy thoughts into perfect AI prompts — instantly, offline, and for free.

PromptForge is a lightweight, single-file HTML app that takes your raw "word vomit" and transforms it into a polished, optimized prompt for **Claude** or **Gemini** — powered entirely by a local AI model (no API keys, no subscriptions, no internet required after setup).

![PromptForge Dark Mode](https://img.shields.io/badge/theme-dark%20mode-black?style=flat-square)
![Offline](https://img.shields.io/badge/works-offline-brightgreen?style=flat-square)
![No API Key](https://img.shields.io/badge/API%20key-not%20required-blue?style=flat-square)
![Powered by Ollama](https://img.shields.io/badge/powered%20by-Ollama-orange?style=flat-square)

---

## ✨ Features

- 🧠 **Brain dump → polished prompt** in seconds
- 🤖 **Claude & Gemini** optimized outputs (different prompt styles for each)
- 🎨 **5 tone options** — Professional, Casual, Technical, Creative, Concise
- 🎙️ **Voice input** — speak your thoughts instead of typing
- 🕐 **Prompt history** — last 20 prompts saved automatically
- 🔗 **Quick links** to open Claude and Gemini directly
- 💻 **100% offline** — runs on your machine via Ollama
- 📄 **Single HTML file** — no install, no build step, no dependencies

---

## ☕ Support This Project

If PromptForge saves you time, consider buying me a coffee!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-donate-yellow?style=for-the-badge&logo=buy-me-a-coffee)](https://buymeacoffee.com)

Every coffee keeps this project going and motivates new features. Thank you! 🙏

---

## 🚀 Getting Started

### Prerequisites

You need **Ollama** installed on your machine. It's free, open source, and runs entirely locally.

---

### Step 1 — Install Ollama

**Windows:**
1. Go to [ollama.com](https://ollama.com)
2. Click **Download for Windows**
3. Run the installer — Ollama will appear in your system tray when running

**Mac:**
1. Go to [ollama.com](https://ollama.com)
2. Click **Download for Mac**
3. Open the `.dmg` and drag Ollama to your Applications folder
4. Launch Ollama from Applications

---

### Step 2 — Download the llama3.2 Model

Open a terminal (PowerShell on Windows, Terminal on Mac) and run:

```bash
ollama pull llama3.2
```

This downloads the model (~2GB). You only need to do this once.

---

### Step 3 — Allow PromptForge to Talk to Ollama (CORS fix)

This is a one-time setup per machine so your browser can communicate with Ollama.

**Windows (PowerShell):**
```powershell
setx OLLAMA_ORIGINS "*"
```
Then fully quit Ollama from the system tray and relaunch it.

**Mac (Terminal):**
```bash
launchctl setenv OLLAMA_ORIGINS "*"
```
Then restart Ollama.

> **Tip:** If you ever restart your Mac, you may need to run the `launchctl` command again before launching Ollama.

**Alternative (no restart needed):** Instead of the above, you can always launch Ollama from the terminal with:
```bash
# Windows PowerShell
$env:OLLAMA_ORIGINS="*"; ollama serve

# Mac Terminal
OLLAMA_ORIGINS="*" ollama serve
```
Leave this terminal window open while using PromptForge.

---

### Step 4 — Download & Open PromptForge

1. Download `promptforge.html` from this repo
2. Open it in **Google Chrome** or **Microsoft Edge**
3. Make sure Ollama is running in the background
4. Start generating prompts!

---

## 🎮 How to Use

1. **Choose your AI** — Select Claude or Gemini depending on where you'll paste the prompt
2. **Brain dump** — Type (or speak 🎙️) your raw, unpolished thoughts
3. **Pick a tone** — Professional, Casual, Technical, Creative, or Concise
4. **Generate** — Hit the button or press `Cmd/Ctrl + Enter`
5. **Copy & paste** — Use the Copy button, then paste into Claude or Gemini

---

## 🖥️ Compatibility

| Platform | Supported | Notes |
|----------|-----------|-------|
| Windows + Chrome | ✅ | Recommended |
| Windows + Edge | ✅ | Works great |
| Mac + Chrome | ✅ | Recommended |
| Mac + Safari | ⚠️ | Voice input may not work |
| Firefox | ⚠️ | Voice input not supported |

---

## 🔧 Troubleshooting

**"Cannot connect to Ollama" error:**
- Make sure Ollama is running (check your system tray on Windows, menu bar on Mac)
- Make sure you set `OLLAMA_ORIGINS="*"` and restarted Ollama
- Try running `ollama serve` in a terminal with ORIGINS set inline (see Step 3)

**Voice input not working:**
- Use Chrome or Edge
- Make sure you allowed microphone permissions when prompted
- Check that your browser has microphone access in system settings

**Blank output:**
- Check that `llama3.2` is fully downloaded (`ollama pull llama3.2`)
- Open browser console (F12 → Console) and check for error messages

---

## 🛠️ Tech Stack

- Pure HTML, CSS, JavaScript — zero dependencies, zero build tools
- [Ollama](https://ollama.com) — local AI model runner
- [llama3.2](https://ollama.com/library/llama3.2) — the underlying language model
- Web Speech API — for voice input

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request.

Ideas for future features:
- [ ] Custom model selector (swap llama3.2 for any Ollama model)
- [ ] Export history as markdown
- [ ] More AI targets (Perplexity, ChatGPT, etc.)
- [ ] Prompt templates / presets

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

*Built with ❤️ and a lot of word vomit.*
