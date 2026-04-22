# CaptionCast 🎙

**Free, real-time closed captions overlay for streamers.**  
Powered by [Deepgram](https://deepgram.com) Nova-2 · Works with OBS, Streamlabs, and any browser-source streaming software · Windows & macOS

---

## Features

- 🎤 Select any microphone / audio input device
- 🔑 Bring your own free Deepgram API key ($200 free credits = hundreds of hours)
- 📺 OBS Browser Source overlay — plug and play
- 🔇 Auto-clears after configurable silence delay
- 🖥 Runs in your system tray (stays out of your way)
- 🔒 API key stored locally — never shared

---

## Quick Start

### 1. Get a Free Deepgram Key
1. Sign up at [console.deepgram.com/signup](https://console.deepgram.com/signup) (no credit card needed)
2. Go to **API Keys** → **Create a New API Key**
3. Copy the key (it's only shown once!)

### 2. Install & Run CaptionCast
```bash
npm install
npm start
```

### 3. Set Up the Overlay
1. Go to the **Overlay** tab in CaptionCast
2. Copy the URL shown (e.g. `http://localhost:47891/overlay`)
3. In OBS: **Sources → + → Browser Source**
4. Paste the URL, set size to **1920 × 200**, position at bottom of scene

### 4. Go Live
1. Select your mic in the **Stream** tab
2. Paste your Deepgram API key and click **Save**
3. Click **▶ Start Captions**

---

## Building

```bash
# Windows
npm run build:win

# macOS
npm run build:mac
```

Outputs go to the `dist/` folder.

---

## Tech Stack

- **Electron** — cross-platform desktop shell
- **Deepgram Nova-2** — real-time speech-to-text
- **Express + WebSocket** — serves overlay and relays captions
- **Web Audio API** — microphone capture at 16kHz

---

## Notes

- macOS may prompt for microphone permission on first launch — allow it
- The overlay auto-reconnects if CaptionCast is restarted while OBS is open
- Interim (partial) captions appear slightly transparent; final captions are solid white
- CaptionCast minimises to the system tray — double-click the tray icon to reopen

---

## License

MIT — free for personal and commercial streaming use.
