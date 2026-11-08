# Installation Guide (Starter-Pack Instructions)

> Status: documentation draft based on the supplied ZIP. The commands below are transcribed from that pack's README and SKILL instructions; they have not yet been tested on your PC. The supplied pack documents Claude Code, not verified Antigravity support.

## 1. Requirements

- Claude Code (or Claude with a linked computer)
- Node.js 22 or newer
- FFmpeg
- Google Chrome
- Python 3.10 or newer
- Git for Windows / Git Bash on Windows
- About 1 GB free disk space for the local Kokoro voice and Whisper speech-timing models

## 2. Install the skill

The supplied pack instructs users to place the extracted `faceless-shorts` folder at:

- macOS/Linux: `~/.claude/skills/faceless-shorts/`
- Windows: use the equivalent Claude skills directory and Git Bash; confirm the exact path for your Claude Code installation before copying.

Do not rename or move individual files inside the skill folder.

## 3. Run setup

From Git Bash, run:

```bash
bash scripts/setup.sh
```

Wait until the script prints `All set`.

The pack says setup checks Node.js, FFmpeg, and Chrome, creates a Python virtual environment, and downloads the Kokoro voice and Whisper model files. Review any install prompts before accepting them.

## 4. Run the self-test

```bash
bash scripts/selftest.sh
```

Continue only when it prints `SELFTEST PASSED`. The skill instructions also say to open and inspect the contact sheet and video clip produced by the test.

## 5. Generate a first test short

Start a new Claude Code session and try the sample request from the supplied README:

> Make a Deep Dive 3D short: what happens if you crack your knuckles?

Review the generated script and shot plan before allowing the build to proceed. Inspect the final video, captions, audio, and contact sheet before publishing.

## 6. Troubleshooting information to collect

If setup fails, record:

- Windows/macOS/Linux version
- `node --version`
- `python --version`
- `ffmpeg -version` (first line is enough)
- The complete error message and the command that produced it

Never share API keys, passwords, access tokens, or private channel credentials in an issue.

## Compatibility warning

The companion PDF describes an Antigravity workflow, but the supplied ZIP's own README and SKILL file document Claude Code installation. Do not assume the Antigravity steps and Claude Code steps are interchangeable. Antigravity support will be documented only after a separate test confirms it.
