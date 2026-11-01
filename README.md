# TranGL-Releases
Public Releases


# 🌐 TranGL — Real-Time Screen OCR & Translation Overlay

TranGL reads text from games or applications on your screen via OCR and displays the translation directly on top — in real-time.

![Python 3.11+](https://img.shields.io/badge/Python-3.11+-blue.svg)
![PyQt6](https://img.shields.io/badge/GUI-PyQt6-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Features

| Feature | Description |
|---------|-------------|
| **Multi-Region OCR** | Draw multiple OCR boxes on screen, each with independent settings |
| **Real-Time Capture** | Captures only the defined regions (~5ms per region) using `mss` |
| **Translation Overlay** | Shows translated text directly on screen with semi-transparent background |
| **Click-Through Window** | Overlay stays on top but doesn't block mouse clicks |
| **Multi-Language** | Auto-detect source language, translate to any target language |
| **Hotkey Controls** | Global hotkeys work even while playing games |
| **Profile System** | Save/load OCR region layouts per game |
| **Smart Detection** | Skips OCR & translation when text hasn't changed (saves ~80-90% of API calls) |

## 🌐 Translation Engines (3 Tiers)

| Tier | Provider | API Key? | Notes |
|------|----------|----------|-------|
| 🟢 Default | **Google Translate** | ❌ Free | Works out of the box |
| 🔵 API Key | **DeepL** / **OpenAI** | ✅ Required | Higher quality translation |
| 🟣 Local AI | **Ollama** | ❌ Local | 100% offline, requires local server |

## 🚀 Quick Start

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Install Tesseract

- **Windows:** Download the official installer from [UB-Mannheim/tesseract](https://github.com/UB-Mannheim/tesseract/wiki) (`https://github.com/UB-Mannheim/tesseract/wiki`)
- Run the installer and add Tesseract to your `PATH` (default: `C:\Program Files\Tesseract-OCR`), or set the path in settings

### 3. Run

```bash
python main.py
```

### 4. Usage

1. **Draw Regions** — Click `⬜ Draw Region` or press `Ctrl+Shift+R`
2. **Click and drag** to draw OCR boxes on the text areas you want to translate
3. Press **Enter** to confirm regions
4. Click **▶ Start** or press `Ctrl+Shift+S` to begin OCR scanning
5. Translations appear on the overlay automatically!

## ⌨️ Hotkeys

| Hotkey | Action |
|--------|--------|
| `Ctrl+Shift+T` | Toggle overlay visibility |
| `Ctrl+Shift+S` | Start/Stop OCR scanning |
| `Ctrl+Shift+R` | Draw new OCR regions |
| `Ctrl+Shift+C` | Show/Hide control panel |
| `Ctrl+Shift+I` | Toggle click-through mode |
| `Ctrl+Shift+D` | Toggle debug mode |

## 🔧 Configuration

### Using Ollama (Local AI)

1. Install [Ollama](https://ollama.ai)
2. Pull a model: `ollama pull qwen2.5:7b`
3. In TranGL Control Panel → Local AI → set URL to `http://localhost:11434`
4. Click **Test Connection**
5. Select Ollama as default translator

### API Keys

Enter API keys in Control Panel → API Keys section:
- **DeepL**: Get free key at [deepl.com/pro](https://www.deepl.com/pro)
- **OpenAI**: Get key at [platform.openai.com](https://platform.openai.com)



