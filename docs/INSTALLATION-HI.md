# इंस्टॉलेशन गाइड (दिए गए Starter Pack के अनुसार)

> स्थिति: यह गाइड आपके दिए ZIP के README और SKILL निर्देशों के आधार पर तैयार की गई शुरुआती ड्राफ्ट है। अभी आपके PC पर इन commands का परीक्षण नहीं हुआ है। ZIP में Claude Code का workflow बताया गया है; Antigravity support अभी verify नहीं है।

## 1. जरूरी चीजें

- Claude Code (या linked computer वाला Claude)
- Node.js 22 या नया version
- FFmpeg
- Google Chrome
- Python 3.10 या नया version
- Windows पर Git for Windows के साथ Git Bash
- Kokoro voice और Whisper model के लिए लगभग 1 GB खाली disk space

## 2. Skill folder रखें

ZIP extract करने के बाद उसके `faceless-shorts` folder को इस location पर रखने के निर्देश दिए गए हैं:

- macOS/Linux: `~/.claude/skills/faceless-shorts/`
- Windows: Claude Code की संबंधित skills directory इस्तेमाल करें। Exact path की पुष्टि अपने installation में करें और Git Bash से commands चलाएँ।

Folder के अंदर की files को अलग-अलग move या rename न करें।

## 3. Setup चलाएँ

Git Bash खोलें, skill folder में जाएँ और चलाएँ:

```bash
bash scripts/setup.sh
```

जब तक `All set` न दिखे, प्रक्रिया पूरी न मानें। दिए गए निर्देशों के अनुसार setup Node.js, FFmpeg और Chrome जाँचता है, Python virtual environment बनाता है और Kokoro तथा Whisper models डाउनलोड करता है। किसी भी install prompt को पढ़कर ही स्वीकार करें।

## 4. Self-test चलाएँ

```bash
bash scripts/selftest.sh
```

आगे तभी बढ़ें जब `SELFTEST PASSED` दिखे। इसके बाद test से बनी contact sheet और video clip खोलकर देखें।

## 5. पहला test Short बनाएँ

Claude Code का नया session शुरू करें और यह sample prompt दें:

> Make a Deep Dive 3D short: what happens if you crack your knuckles?

Build शुरू करने से पहले script और shot plan review करें। Publish करने से पहले final video, captions, audio और contact sheet जाँचें।

## 6. Error आए तो ये जानकारी रखें

- Windows/macOS/Linux का version
- `node --version`
- `python --version`
- `ffmpeg -version` की पहली line
- पूरा error message और वह command जिससे error आया

GitHub issue या chat में API keys, passwords, access tokens या private channel credentials कभी share न करें।

## जरूरी Compatibility Note

साथ वाली PDF Antigravity workflow बताती है, लेकिन दिए ZIP का README और SKILL file Claude Code installation समझाते हैं। दोनों workflows को एक जैसा न मानें। Antigravity के निर्देश तभी जोड़ेंगे जब अलग से test करके support confirm हो जाएगा।
