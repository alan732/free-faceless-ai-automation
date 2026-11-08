# Free Faceless AI Automation

Create narrated, animated vertical Shorts for YouTube, TikTok, and Instagram Reels using a local video-generation workflow.

> **Project status:** Documentation and compatibility review in progress. The supplied starter pack describes itself as a **Claude Code skill**. Antigravity compatibility has not yet been verified, so this repository does not claim one-click Antigravity support.

## What the workflow is designed to produce

- A written short-form script
- Local AI voice generation with Kokoro
- Word-level speech timing and captions with Whisper
- Programmatically animated scenes
- Sound effects and background music
- MP4 rendering through headless Chrome and FFmpeg
- Optional YouTube upload through Zapier, only after the channel owner confirms the upload details

The original guide describes a local workflow and lists Antigravity as its AI assistant. However, the supplied ZIP's own README and SKILL instructions specify Claude Code (or Claude with a linked computer). Follow the compatibility notes in this repository until Antigravity support is tested.

## Six included visual formats

| Style | Intended format |
|---|---|
| Deep Dive 3D | 3D science and “what happens if…?” explainers |
| Night File 3D | Dark mystery and true-crime storytelling |
| Inside Out | Flat 2D explainers and x-ray-style cutaways |
| Stick Story | Stick-figure survival scenarios |
| Paper Atlas | Historical stories with paper-map visuals |
| Tall Tale 3D | Funny true stories in a stylized 3D world |

## Requirements stated by the supplied starter pack

- Claude Code (or Claude with a linked computer)
- Node.js 22+
- FFmpeg
- Google Chrome
- Python 3.10+
- Approximately 1 GB of storage for the voice and speech-recognition models
- On Windows, the instructions specify Git Bash (installed with Git for Windows)

These are the starter pack's stated requirements, not yet independently tested on every operating system or machine.

## Getting started

1. Obtain the original Faceless Shorts starter pack from its creator.
2. Review its own README and SKILL instructions before installing.
3. On Windows, use Git Bash as specified by the starter pack.
4. Run the setup and self-test commands from the starter pack's instructions.
5. Generate a test short and inspect the rendered frames, captions, audio, and final MP4 before publishing.

The detailed setup guide is being prepared. Do not assume that the PDF's “one-click Antigravity setup” has been validated for this ZIP.

## Important compatibility note

The supplied PDF says to open the template folder in Antigravity and ask Antigravity to install Node, FFmpeg, Python, Kokoro, and Whisper. In contrast, the ZIP's README says to install the folder as a Claude skill at ~/.claude/skills/faceless-shorts/, and its SKILL instructions describe Claude Code workflows. These instructions are not interchangeable without testing. This project will document the verified path and clearly label anything experimental.

## Licensing and redistribution

The supplied ZIP's README makes claims about original code/assets and mentions licenses for some dependencies, but the archive does not include a top-level project license granting redistribution of the complete pack. **This repository therefore does not currently redistribute the ZIP's source files or assets.** Before adding them, we will verify the original creator's permission and the licenses/notices for bundled third-party files.

Do not treat the starter pack's statements about use in generated videos as permission to rehost or redistribute the source archive.



## Contributions

Issues and suggestions are welcome. Please include your operating system, tool versions, and the exact error output when reporting a setup problem.

---

**Note:** “Free” refers to the local tools and workflow described by the starter pack. Hardware, electricity, internet access, and third-party services such as Zapier may have their own costs or limits.
