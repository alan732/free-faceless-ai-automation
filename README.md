# 🎬 Free Faceless AI Automation

### Create Animated AI Shorts Locally — Without Paid AI Video APIs

An open-source documentation project exploring automated faceless video creation using local AI tools, programmatic animation, AI voiceovers, synchronized captions, sound effects, and video rendering.

Create engaging vertical videos for:

- YouTube Shorts
- Instagram Reels
- TikTok

The original starter pack provides six different animation styles and a workflow for turning a simple topic into a narrated, animated video.

> **Project Status:** fully wokring . The supplied starter pack is documented primarily for Claude Code. Antigravity compatibility is experimental and has not yet been independently verified.

---

## ✨ Features

The original starter pack describes the following capabilities:

- AI-assisted script generation.
- Local AI voice generation using Kokoro.
- Word-level speech timing using Whisper.
- Programmatically generated animated scenes.
- Automatic caption synchronization.
- Sound effects and background music.
- Video rendering using headless Chrome and FFmpeg.
- Frame-by-frame visual quality checks.
- Optional YouTube uploading through Zapier.

The workflow is designed to run primarily on your own computer rather than relying on paid AI video-generation APIs.

---

## 🎨 Six Animation Styles

The starter pack includes six distinct visual styles.

| Style | Description |
|---|---|
| Deep Dive 3D | 3D science, medical, and body explainers. |
| Night File 3D | Dark mysteries, unsolved cases, and true-crime stories. |
| Inside Out | Clean 2D explainers with X-ray-style cutaways. |
| Stick Story | Stick-figure survival scenarios and storytelling. |
| Paper Atlas | Historical storytelling with animated paper maps. |
| Tall Tale 3D | Funny true stories featuring cartoon characters in 3D environments. |

### 1. Deep Dive 3D

Designed for science, health, and body-related explainers.

Examples:
- What happens if you swallow gum?
- What happens if you hold your breath?
- What happens when an insect stings you?

### 2. Night File 3D

Designed for mysterious, dark, and suspenseful storytelling.

Examples:
- Unsolved mysteries.
- Historical crimes.
- Strange real-world incidents.

### 3. Inside Out

Designed for simple and engaging 2D educational videos.

Examples:
- Human body explainers.
- Science facts.
- What-happens-if scenarios.

### 4. Stick Story

Designed for survival situations and hypothetical scenarios.

Examples:
- What would you do if the power went out for three days?
- How would you survive in an emergency?

### 5. Paper Atlas

Designed for historical storytelling.

Examples:
- Ancient civilizations.
- Historical battles.
- Famous historical events.

### 6. Tall Tale 3D

Designed for funny true stories and unusual real-world events.

Examples:
- Strange historical stories.
- Unusual business stories.
- Clever loopholes and unexpected events.

---

## ⚙️ How It Works

The original workflow follows this general process:

```text
       VIDEO TOPIC
            |
            v
      SCRIPT CREATION
            |
            v
     KOKORO AI VOICE
            |
            v
    WHISPER WORD TIMING
            |
            v
     ANIMATED SCENES
            |
            v
   CAPTIONS & SOUND EFFECTS
            |
            v
      VIDEO RENDERING
            |
            v
       FINAL MP4


       Technology Behind the Project
Technology	Purpose
Kokoro	Local AI voice generation
Whisper	Speech recognition and word timing
Python	Audio and AI processing
JavaScript	Animation and video logic
Three.js	3D visual development
Chrome	Automated frame capture
FFmpeg	Video and audio rendering
NumPy	Audio processing


These technologies are described in the supplied starter pack. Their exact versions and compatibility should be checked before installation.
💻 System Requirements
The original starter pack lists the following requirements:
Software	Requirement
Node.js	Version 22+
Python	Version 3.10+
FFmpeg	Required
Google Chrome	Required
Git	Required for Git Bash on Windows
Claude Code	Documented AI assistant


Storage Requirements
The starter pack downloads approximately:
- Kokoro voice model: 340 MB.
- Whisper speech-recognition model: 500 MB.
Additional storage is required for dependencies, project files, and rendered videos.
🚀 Installation Guide
Step 1: Download the Starter Pack
Obtain the original Faceless Shorts starter pack from its creator.

Download page:

https://nafay3d.com/#library

Extract the downloaded ZIP file into a folder on your computer.
Step 2: Install Required Software
Install the required dependencies:
1. Node.js 22 or newer.
2. Python 3.10 or newer.
3. FFmpeg.
4. Google Chrome.
5. Git for Windows (if using Windows).
Step 3: Claude Code Setup
The supplied starter pack documents Claude Code as its supported AI workflow.

Install the skill into the following directory:
~/.claude/skills/faceless-shorts/

The folder should contain:
faceless-shorts/
│
├── SKILL.md
├── README.md
│
├── scripts/
│   ├── setup.sh
│   ├── selftest.sh
│   ├── new_video.sh
│   ├── voice.py
│   ├── words.py
│   └── estimate.py
│
└── styles/
    ├── deep-dive/
    ├── night-file/
    ├── inside-out/
    ├── stick-story/
    ├── paper-atlas/
    └── tall-tale/

Step 4: Run the Setup Script
Open Git Bash or a compatible terminal inside the extracted project folder.

Run:
bash scripts/setup.sh

The setup process checks dependencies, prepares the Python environment, and downloads the required voice and speech-recognition models.

Expected success message:
All set

Step 5: Run the Self-Test
Execute:
bash scripts/selftest.sh

Expected success message:
SELFTEST PASSED

Inspect the generated contact sheet and test video before proceeding.

Important: These commands follow the original starter pack's instructions. They have not yet been independently verified on every Windows or macOS configuration.
🎥 Creating Your First Video
Once the original starter pack is installed and working, you can create a video project.

Example:
bash scripts/new_video.sh deep-dive my-first-video

This creates a new project using the selected animation style.

Other available styles:
deep-dive
night-file
inside-out
stick-story
paper-atlas
tall-tale

Example Video Prompt
Create a 35-second animated short.

Topic: What happens if you swallow chewing gum?

Style: Deep Dive 3D.

Requirements:

- Strong hook in the first two seconds.
- Engaging narration.
- Animated 3D scenes.
- Word-synchronized captions.
- Appropriate sound effects.
- Fast-paced storytelling.
- Vertical 9:16 format.
- Natural ending that encourages replay.

The original workflow uses script.json and JavaScript shot definitions to construct the video.
🎙️ Voice Generation
The original starter pack uses Kokoro for local AI voice generation.

It also supports different voice options.

To list available voices:
SKILL/scripts/py SKILL/scripts/voice.py --list

The default voice specified in the original instructions is:
am_michael

Custom Voice Recording
The workflow also documents support for using your own recorded audio.

Example:
SKILL/scripts/py SKILL/scripts/words.py <project> --audio your-recording.m4a

📝 Automatic Captions
Whisper is used to calculate word-level speech timings.

This allows captions to synchronize with the narration.

The original quality guidelines recommend:
- One to three words per caption.
- Highlighting the currently spoken word.
- Correct spelling.
- Mobile-friendly text sizing.
- Accurate synchronization with narration.
🎬 Video Quality Control
Visual quality control is an important part of the original workflow.

Before delivering a video, the system generates a contact sheet containing frames from the rendered animation.

The frames should be inspected for:
- Incorrect animations.
- Overlapping objects.
- Caption positioning.
- Visual inconsistencies.
- Timing problems.
- Audio synchronization.
The original instructions emphasize that frames should be reviewed before the final video is delivered.
📺 YouTube Automation
The original starter pack describes an optional YouTube upload workflow using Zapier.

This is separate from video generation.

The process involves:
1. Generating the final MP4.
2. Preparing an accessible video URL.
3. Connecting the YouTube account.
4. Providing upload information.
5. Confirming the upload settings.
6. Uploading the video.
Important distinctions:
- Video generation is documented in the starter pack.
- YouTube uploading is an optional integration.
- Daily scheduled publishing is not established as a built-in feature.
Automated scheduling may be added as a separate feature in a future version.
🤖 Antigravity Compatibility
The supplied PDF describes using Google Antigravity as an AI assistant.

PDF instructions:
1. Download Antigravity.
2. Download the Faceless Shorts template pack.
3. Open the extracted folder in Antigravity.
4. Ask the AI assistant to configure the required dependencies.
5. Generate the first video using a natural-language prompt.
However, the original ZIP identifies itself as a Claude Code skill.

Therefore:
- Claude Code is the documented workflow.
- Antigravity support is not yet verified.
- Antigravity installation instructions will be published only after successful testing.
We aim to make the workflow accessible through multiple AI coding assistants where technically possible.
🔒 Safety & Important Notes
Before running installation scripts:
- Review scripts before executing them.
- Download dependencies from trusted sources.
- Never share API keys or authentication tokens.
- Back up important files.
- Inspect generated videos before publishing.
- Verify the licensing of third-party assets.
Do not assume that permission to use generated videos automatically grants permission to redistribute the original source code or template pack.


📜 Credits & Licensing
The original Faceless Shorts starter pack was obtained from:

https://nafay3d.com/#library

This repository is an independent documentation and compatibility project.

The original starter pack does not include a top-level project license granting redistribution of the complete source archive.

Therefore, its source files and assets are not redistributed here unless the necessary permissions and third-party licensing requirements are verified.

Third-party dependencies retain their respective licenses.
⭐ Support the Project
If you find this project useful:
- Star this repository.
- Share it with other creators.
- Report bugs.
- Suggest improvements.
- Contribute documentation.
Every contribution helps improve the project.
Built for creators who want to explore local AI-powered video automation.

Repository: https://github.com/alan732/free-faceless-ai-automation
