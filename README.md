# Agnes Tachyon desktop companion

Hey, this is my Agnes fan companion for Windows. I made it because I wanted an
Agnes who actually hangs out on the desktop, talks back, reacts to games, and
does not need ten confusing windows just to change a microphone.

The current version is **6.5.0**. It supports 64-bit Windows 10 version 1809 or
newer—including Enterprise LTSC 2019, LTSC 2021, and LTSC 2024—and all 64-bit
Windows 11 releases.

## What she does

- push-to-talk chat with a key you choose by pressing it;
- spoken answers, microphone and speaker selection;
- local screen watching at up to 10 FPS, with paid vision requests reserved
  for useful keyframes and direct visual questions;
- the real bundled Agnes desktop model with movement, clicks, snacks, emotes,
  random actions and the two original Uma music dances;
- live lookup for newer hardware, news and other facts that can change;
- signed in-app updates with a proper download and install progress screen;
- feedback and bug reports without a GitHub account.

I tried to keep Options understandable even if you are not a computer expert.
The easy defaults are safe to start with, and **Check my setup** explains what
is missing instead of throwing a wall of error text at you.

## Install

1. Open the [latest release](https://github.com/yk730166-create/agnes-tachyon/releases/latest).
2. Download `AgnesTachyonSetup.exe`.
3. Run it, open Agnes Options, and follow the three setup steps.
4. Create a Groq key for chat/listening and a Fish Audio key for Agnes's voice.
   Both keys are stored in Windows Credential Manager, not in a readable file.

Setup also offers an unchecked **optional high-quality voice engine** task. It
downloads the official Applio 3.6.4 package only when selected, verifies its
exact SHA-256 before extraction, and needs about 13 GB free temporarily. The
normal Agnes install and every automatic update skip that 4.6 GB download.

After that, start Agnes normally. When I publish an update, Agnes shows it in
the app. Press **Download update** and the app checks the signed file, installs
it in place, preserves settings and protected keys, then restarts.

## The AI and voice

The default setup uses:

- `openai/gpt-oss-120b` for the main conversation;
- `groq/compound-mini` for current web facts;
- `qwen/qwen3.6-27b` for screen understanding;
- `whisper-large-v3-turbo` for fast speech recognition.

Every desktop answer now uses Fish Audio S2 Pro with the public
`64e74b61065540f4abed3a0f30cf14d9` Agnes model. The app does not silently
switch to an unrelated Windows or Groq voice. Each user supplies their own Fish
API key, which remains protected in Windows Credential Manager. This is a
third-party community voice model, not an official recording or a claim of
ownership over a performer’s voice.

For a voice model that the user has permission to use, the optional Applio path
now prefers Applio's matching embedded Python runtime and stronger, cleaner RVC
defaults. Setup does not include or silently fetch a character voice model;
choose both its `.pth` model and matching `.index` file in Options.

The Setup Lab has 36 fixed questions that work without an AI request. Its public
web page shows those answers silently instead of exposing a Fish key or imitating
Agnes with a generic browser voice. The installed app speaks them with Fish. The setup-guide preview also
uses native 60 FPS transparent video instead of making the browser crop huge images
frame by frame.

## Privacy without weird promises

- Screen awareness is off until you enable it.
- The normal vision loop does not save a screenshot collection.
- The Screen & Pet usage monitor shows Fish's exact returned credit balance and counts conversations, picture reviews,
  provider-reported tokens, voice characters and listening time, and limits
  daily automatic vision reviews; the provider dashboard remains the exact
  quota source.
- API keys are protected by Windows Credential Manager.
- The guide has no analytics and makes no AI request for its fixed answers.
- Feedback goes to the private owner inbox instead of a public GitHub Issue.

The GitHub Pages site has to publish its `index.html` and the compressed Agnes
animation clips or a browser cannot display them. Browser files cannot be
honestly “encrypted” while still running for everyone. This repo therefore
contains only the public page, the minimum runtime clips, release notes and
rights documents. It does **not** contain the app source, raw sprite sheets,
voice models, build folders, owner tools, API keys or signing
keys. The signed installer contains the compiled Agnes runtime needed for the
desktop model.

## If something breaks

Right-click the tray icon and open **About and diagnostics**. Copy only the last
useful error line, then use **Report a bug**. Never send an API key.

Common fixes are also built into the Setup Lab: microphone permissions, wrong
speaker, Numpad keys, voice access, old environment keys, update problems,
screen awareness and startup issues.

## Rights

This is a non-commercial, unofficial fan project by **y4x5lol**. Agnes Tachyon,
Umamusume: Pretty Derby, official character material and official performances
belong to Cygames and their respective rightsholders. The animated guide clips
come from separately attributed third-party fan sprite material and are not
claimed as my artwork. The real character icon, model, animation sheets and
matching sounds are attributed third-party fan material too. The app interface,
updater, integration logic and documentation are original project work.

See [PROJECT_LICENSE.txt](PROJECT_LICENSE.txt),
[THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md), and
[RIGHTS_AUDIT.md](RIGHTS_AUDIT.md) for the boring but important details.
