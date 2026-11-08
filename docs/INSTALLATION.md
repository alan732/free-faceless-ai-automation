# Installation Guide

This guide explains how to install and configure the original Faceless Shorts starter pack on your computer.

The documented workflow uses Claude Code and locally installed tools to generate animated short-form videos.

> **Project Status:** These instructions are based on the original starter pack's README, SKILL.md, and installation scripts. They have not yet been independently tested on every operating system or computer.

---

## Table of Contents

1. Overview
2. System Requirements
3. Required Software
4. Download the Starter Pack
5. Install the Claude Code Skill
6. Run the Setup Script
7. Verify the Installation
8. Run the Self-Test
9. Generate Your First Video
10. Available Animation Styles
11. Understanding the Project Structure
12. Troubleshooting
13. Important Safety Notes
14. Antigravity Compatibility
15. Credits and Licensing

---

## 1. Overview

The Faceless Shorts starter pack provides a workflow for creating narrated, animated vertical videos.

The workflow includes:

- Script generation.
- AI voice generation.
- Word-level speech timing.
- Animated scenes.
- Automatic captions.
- Sound effects and music.
- Video rendering.
- Visual quality inspection.

The original starter pack uses local tools rather than paid AI video-generation APIs.

---

## 2. System Requirements

Before installing, make sure your computer meets the following requirements.

| Component | Requirement |
|---|---|
| Operating System | Windows, macOS, or Linux |
| Node.js | Version 22 or newer |
| Python | Version 3.10 or newer |
| FFmpeg | Required |
| FFprobe | Required |
| Google Chrome | Required |
| Claude Code | Documented AI assistant |
| Storage | Approximately 1 GB for AI models |

Additional storage is required for dependencies, project files, and rendered videos.

### Windows Users

Windows users should use Git Bash.

Git Bash is included with Git for Windows.

Download:

https://git-scm.com/downloads/win

---

## 3. Required Software

Install the following software before proceeding.

### Node.js

Download:

https://nodejs.org/

Install Node.js version 22 or newer.

Verify installation:

```bash
node --version

Python
Download:

https://www.python.org/downloads/

Install Python version 3.10 or newer.

Verify installation:
python --version

FFmpeg
FFmpeg is used for video and audio processing.

Windows installation:
winget install ffmpeg

macOS installation:
brew install ffmpeg

Ubuntu installation:
sudo apt install ffmpeg

Verify installation:
ffmpeg -version
ffprobe -version

Google Chrome
Download:

https://www.google.com/chrome/

Install Google Chrome.

The original video engine uses Chrome for automated frame capture.
4. Download the Starter Pack
Obtain the original Faceless Shorts starter pack from its creator.

Official download page:

https://nafay3d.com/#library

Download the ZIP file.

Extract the archive into a folder on your computer.

Do not rename or delete the internal project files.

The extracted folder should contain:
faceless-shorts/
├── README.md
├── SKILL.md
├── scripts/
└── styles/

5. Install the Claude Code Skill
The original starter pack documents Claude Code as its supported AI workflow.

The recommended skill directory is:
~/.claude/skills/faceless-shorts/

Copy the complete extracted faceless-shorts folder into this directory.

Do not rename individual scripts or move files out of their original folders.
Windows Users
Use Git Bash.

The exact Claude Code skills directory can depend on your installation.

Confirm the directory before copying the project.
6. Run the Setup Script
Open Git Bash or a compatible terminal.

Navigate to the installed skill directory:
cd ~/.claude/skills/faceless-shorts

Run:
bash scripts/setup.sh

The setup script performs several operations.
What the Setup Script Does
1. Checks Node.js 22 or newer.
2. Checks FFmpeg and FFprobe.
3. Checks for Google Chrome or a compatible browser.
4. Checks Python 3.10 or newer.
5. Creates a private Python virtual environment.
6. Installs required Python packages.
7. Downloads the Kokoro voice model.
8. Downloads the Whisper speech-recognition model.
AI Models
Model	Approximate Size	Purpose
Kokoro	340 MB	AI voice generation
Whisper small.en	500 MB	Speech recognition and word timing


The actual download size may vary.
Expected Successful Output
All set

If the script reports missing dependencies, install the missing software and run the setup script again.
7. Verify the Installation
Before generating videos, verify that the required tools are available.

Run:
node --version
python --version
ffmpeg -version
ffprobe -version

Check that Chrome is installed.

The setup script also checks the required Python packages and AI models.

Do not proceed if the setup script reports missing dependencies or failed model downloads.
8. Run the Self-Test
The original starter pack includes a self-test script.

This test checks the video-generation workflow across all six animation styles.

Run:
bash scripts/selftest.sh

The test checks:
- Project creation.
- Voice generation.
- Word timing.
- Animation validation.
- Sound generation.
- Video rendering.
- Contact sheet generation.
Important Safety Warning
The original self-test script deletes its existing:
~/faceless-shorts/_selftest/

directory before creating a new test.

Back up anything important in that directory before running the test.

The test may take several minutes or longer depending on your computer and graphics acceleration.
Expected Successful Output
SELFTEST PASSED

If the test fails, inspect the generated log file before attempting another run.

Do not ignore failed animation or audio checks.
9. Generate Your First Video
After successful installation and testing, start a new Claude Code session.

Try this example request:
Make a Deep Dive 3D short:

What happens if you crack your knuckles?

Create an engaging short-form video with:

- A strong opening hook.
- Interesting narration.
- Animated 3D scenes.
- Word-synchronized captions.
- Appropriate sound effects.
- Background music.

Use vertical 9:16 format.

The original workflow follows this general process:
Video Topic
    |
    v
Script Generation
    |
    v
Kokoro Voice Generation
    |
    v
Whisper Word Timing
    |
    v
Animated Scene Creation
    |
    v
Captions and Sound Effects
    |
    v
Video Rendering
    |
    v
Final MP4

Review the generated script and shot plan before allowing the build to proceed.
10. Available Animation Styles
The original starter pack includes six visual styles.
Style	Folder Name	Purpose
Deep Dive 3D	deep-dive	Science and body explainers
Night File 3D	night-file	Mysteries and true crime
Inside Out	inside-out	2D educational explainers
Stick Story	stick-story	Survival storytelling
Paper Atlas	paper-atlas	Historical animations
Tall Tale 3D	tall-tale	Funny true stories


Example Commands
Create a Deep Dive project:
bash scripts/new_video.sh deep-dive my-first-video

Create a Tall Tale project:
bash scripts/new_video.sh tall-tale my-funny-story

Create a Paper Atlas project:
bash scripts/new_video.sh paper-atlas my-history-video

Each style contains its own visual guidelines and example project.

Read the relevant STYLE.md before creating or modifying a video.
11. Understanding the Project Structure
The original starter pack follows this general structure:
faceless-shorts/
│
├── README.md
├── SKILL.md
│
├── scripts/
│   ├── setup.sh
│   ├── selftest.sh
│   ├── new_video.sh
│   ├── voice.py
│   ├── words.py
│   ├── estimate.py
│   └── py
│
└── styles/
    ├── deep-dive/
    ├── night-file/
    ├── inside-out/
    ├── stick-story/
    ├── paper-atlas/
    └── tall-tale/

Important Files
File	Purpose
README.md	Project introduction
SKILL.md	AI workflow instructions
setup.sh	Dependency installation
selftest.sh	Installation and rendering tests
new_video.sh	Creates new video projects
voice.py	AI voice generation
words.py	Word-level speech timing
estimate.py	Estimated caption timing


12. Troubleshooting
Node.js Not Found
Check:
node --version

Install Node.js 22 or newer if necessary.
FFmpeg Not Found
Check:
ffmpeg -version

Install FFmpeg and FFprobe.
Python Environment Problems
Check:
python --version

Make sure Python 3.10 or newer is installed.
Kokoro Model Download Failed
Check your internet connection.

Run the setup script again:
bash scripts/setup.sh

Whisper Model Download Failed
Make sure your computer has sufficient storage and internet access.

Run the setup script again.
Self-Test Failed
Inspect the log file:
~/faceless-shorts/_selftest/selftest.log

Check the error messages before attempting another test.
Video Rendering Problems
Check:
- Chrome installation.
- FFmpeg installation.
- Available storage.
- Graphics acceleration.
- The relevant animation style's instructions.
13. Important Safety Notes
Before running any scripts:
- Review the scripts before executing them.
- Back up important project files.
- Install dependencies from trusted sources.
- Never share passwords or authentication tokens.
- Never publish private API keys.
- Inspect generated videos before uploading.
- Check the licensing of third-party dependencies and assets.
Do not run scripts from sources you do not trust.
14. Antigravity Compatibility
The accompanying PDF describes an Antigravity-based workflow.

It instructs users to:
1. Install Antigravity.
2. Download the Faceless Shorts template pack.
3. Open the extracted folder in Antigravity.
4. Ask the AI assistant to configure the dependencies.
5. Generate a video using a natural-language prompt.
However, the supplied ZIP's README and SKILL.md document Claude Code as the intended AI workflow.

These two sets of instructions are not yet confirmed to be interchangeable.
Current Compatibility Status
AI Assistant	Status
Claude Code	Documented by original starter pack
Google Antigravity	Not independently verified


Antigravity support will be documented only after successful testing.
15. Credits and Licensing
The original Faceless Shorts starter pack was obtained from:

https://nafay3d.com/#library

This repository is an independent documentation and compatibility project.

The original ZIP does not include a top-level project license granting permission to redistribute the complete source archive.

Therefore, the original source files and assets are not redistributed through this repository unless the necessary permissions and licensing requirements are verified.

Third-party dependencies retain their respective licenses.
Support
If you encounter an installation problem, open a GitHub issue.

Include:
- Your operating system.
- Node.js version.
- Python version.
- FFmpeg version.
- The command you executed.
- The complete error message.
Never include passwords, API keys, or private credentials.
