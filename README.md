# Agnes Tachyon AI Companion

A non-commercial, unofficial Windows fan companion with push-to-talk, fast
cloud Whisper transcription, streaming chat, an original code-drawn Agnes
desktop companion, multimodal screen awareness, and live web verification.

Version 6.2.0 uses `openai/gpt-oss-120b` for conversation,
`groq/compound-mini` for current facts, `qwen/qwen3.6-27b` for vision, and
`whisper-large-v3-turbo` for fast speech recognition.

## Release highlights

- The installed desktop pet is now an original code-drawn Agnes companion;
  the flask-shaped Lab Core remains only as the setup guide's decorative
  control.
- Groq Orpheus provides lively, direction-aware speech with automatic Edge
  neural-voice fallback and no bundled character voice clone.
- Verified downloads update an existing copy in place, preserve its settings
  and protected credentials, skip first-install pages, and restart Agnes when
  finished.
- The private owner console can reuse an existing GitHub CLI sign-in, making a
  signed release possible without copying the same token into another tool.

## Easy Options

Open `Options.exe` in an installed build, or run `src/options_main.py` while
developing, to:

- choose Fastest, Balanced, or Smartest mode;
- click once and press the exact physical push-to-talk key; Numpad and
  left/right modifier keys stay distinct;
- select real microphone and speaker devices;
- configure the built-in animated Agnes companion or an optional licensed pet;
- control live screen reading, spoken pet reactions, and local memory;
- enable smooth fades, animated tabs, and responsive button effects;
- allow live web lookup for recent hardware, prices, news, and current facts.

The default desktop pet is an original, code-drawn Agnes companion rather than
the flask fallback used by older builds. The AI can animate her or talk to an
optional configured external pet. Deaths, misses, victories, danger warnings,
achievements, clicks, snacks, and tray interactions produce fresh AI-written
spoken reactions rather than rotating canned lines. Music dances intentionally
do not start a competing voice response. No speech or thinking textbox is
displayed. The interactive Lab Core in the locally running setup guide remains
as a decorative setup control; it is not the desktop pet.

The rights-safe public build uses Groq-hosted Orpheus for expressive English
speech and automatically falls back to the standard Microsoft Edge neural
voice when Orpheus is unavailable. Neither path is an official Agnes Tachyon
voice or a bundled voice clone. Locally supplied voice-conversion files can be
configured only when the user has the required model, recording, performer,
and redistribution permissions.

Groq may require the account owner to accept the Orpheus model terms once.
Options provides an **Enable natural voice access** button that opens Groq's
official approval page. Until that is accepted, speech continues through the
Edge neural fallback instead of failing or going silent.

At runtime Agnes receives the current date and detected PC/GPU details.
Time-sensitive questions and unfamiliar product names use Groq Compound Mini
live search when web knowledge is enabled. The vision loop observes the active
monitor, skips repeated static frames, rejects low-confidence events, and
treats visible screen text as untrusted data.

## Run

1. Open Options and enter the provider key. Agnes
   stores it in Windows Credential Manager; it is never written to `config.toml`.

   An environment variable can be used instead:

   ```powershell
   $env:GROQ_API_KEY = "your-key"
   ```

2. Start the app:

   ```powershell
   .\venv\Scripts\python.exe .\src\main.py
   ```

Supported variables are
`GROQ_API_KEY`, `OPENAI_API_KEY`, and `GEMINI_API_KEY`.

Only one AI companion instance is allowed at a time. Starting it again asks
the existing tray process to open Options instead of launching a duplicate.

Saving Options updates the running talk-button and microphone hooks
automatically. The tray’s polished **Play with Agnes** menu works independently
of the automatic AI-reaction toggle. **Make her dance** randomly chooses the
first of two music-backed routines, then avoids immediately repeating one,
prevents overlaps, and returns the pet to idle when the track ends. The public
Lab Core uses two original procedural soundtracks; optional external pets use
only locally supplied, licensed media.

Agnes and standalone Options check a pinned, owner-signed update channel after
startup. Update notices cannot be created by changing a public JSON file: the
manifest must verify against the Ed25519 public key embedded in the apps.
When a user selects **Download update**, the installer streams inside the app
with animated progress, transfer speed, and clear verification stages. Files
come only from the pinned GitHub release host; their signed byte size and
SHA-256 are checked before the verified installer launches automatically. If
Agnes is already installed, the installer switches to a focused in-place
update, replaces the compiled app files in the same folder, skips fresh-setup
pages, preserves settings, protected keys, and voice choices, then restarts
Agnes automatically. A first installation still uses the normal guided setup.
Signed required notices remain enforced after a restart even when the network
is unavailable, and live listening, screen reactions, speech, and pet actions
pause until the required update is installed or Agnes exits.

## Performance profiles

- `whisper-large-v3-turbo` is the fast default speech-recognition model.
- `whisper-large-v3` is the highest-accuracy listening option.
- The active monitor is sampled every few seconds when live awareness is
  enabled. Unchanged frames are skipped to reduce latency, network use, and
  cost.
- Expressive Orpheus speech starts sentence-by-sentence while generation
  continues, with automatic Edge neural-voice fallback.
- New speech cancels stale responses, reactions are bounded and deduplicated,
  and recordings stop safely at 90 seconds.

## Windows installer

Run `installer/build_release.ps1` to compile, lint, type-check, test, audit
dependencies, build both PyInstaller applications, and compile
`dist/AgnesTachyonSetup.exe`. The release installs only compiled applications,
runtime configuration, documentation, notices, and the original icon—never
`src`, build scripts, virtual environments, requirements, VBS, or batch
launchers.

The public installer intentionally excludes Desktop Gremlin, extracted
character assets, and the unlicensed Tachyon voice model. These materials
cannot be made part of y4x5lol's ownership merely by adding a notice. See
`PROJECT_LICENSE.txt`, `THIRD_PARTY_NOTICES.md`, and `RIGHTS_AUDIT.md`.

The current Qt interface officially supports 64-bit Windows 10 version 1809 or
newer and 64-bit Windows 11.
