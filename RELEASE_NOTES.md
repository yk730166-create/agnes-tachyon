# Agnes Tachyon AI Companion 6.3.2

## 6.3.2 — Smoother guide model and local spoken answers

- Replaced large-sheet CSS repaints with an anchored 300×300 canvas renderer
  using the model's intended frame timing.
- Added a 32 KB instant poster and one-sheet-at-a-time lazy loading. The guide
  no longer downloads or decodes all animation sheets during startup.
- Added richer hologram, activity, and local-voice visuals around Agnes.
- Added six built-in setup questions with cheerful spoken answers through the
  device voice. They use no AI call, API key, tracking, or screen capture.
- Hardened animation cancellation, image-load failure handling, reduced-motion
  behavior, responsive layout, and installer asset verification.

## 6.3.1 — Setup Lab Agnes model update

- Replaced the Setup Lab's simple drawn preview with the actual separately
  attributed Agnes action and emote sprite sheets.
- Agnes stays anchored inside the lab core while playing idle, intro, hover,
  click, sleep, and randomized dance/reaction sequences.
- Fixed animation pause/resume cleanup when the guide is hidden or VFX is
  disabled, and added exact sprite-grid and installer-payload regression checks.

## 6.3.0 — Application, guide, and updater refinement

## Highlights

- Fresh installs now launch Agnes herself before the setup guide, and the old
  glass/flask preview has been replaced by a smooth copper-haired, pale-coat
  animated Agnes design shared with the built-in desktop companion.
- Easy OpenAI modes now select the current provider-specific Luna, Terra, and
  Sol models instead of carrying a Groq model across providers. Wrong-service
  model IDs are caught before saving while custom local model names stay valid.
- Live reactions remember recent wording, retry once instead of repeating a
  canned line, and require explicit confidence before treating screen text as
  a death, miss, victory, danger, or achievement.
- Hardened runtime cleanup across microphone hooks, speech subprocesses,
  screenshot buffers, generated voice files, local memory, diagnostics, and
  the per-user single-instance channel.
- Updated the OpenAI SDK, PyInstaller, Ruff, and the cryptography runtime; the
  latter closes the dependency advisory detected during the release audit.
- Anonymous feedback remains one-click and sign-in-free. The live receiver now
  forces every untrusted spreadsheet field to plain text, preventing submitted
  messages from becoming formulas in the owner inbox.

- Fixed update checks and downloads on Windows systems where GitHub was
  trusted by Windows but rejected by Python's bundled certificate list. Agnes
  and standalone Options now use the native Windows certificate store for
  HTTPS without disabling certificate validation. GitHub host restrictions,
  the owner-signed manifest, installer size limit, and SHA-256 verification
  remain enforced.
- Replaced the older flask desktop fallback with an original, code-drawn Agnes
  companion. Her expressions, movement, reactions, dances, and interaction
  states are rendered by the app without downloaded sprites or extracted game
  assets. The locally running guide now uses a matching original, code-drawn
  Agnes preview instead of the old decorative flask.
- Fixed the fresh-install handoff: setup now starts Agnes automatically while
  still opening the local guide when Edge is available. On systems without
  Edge, the same Agnes process opens native Options, avoiding duplicate-window
  and startup-race bugs.
- Added expressive Groq Orpheus speech with direction-aware delivery and an
  automatic Microsoft Edge neural-voice fallback. Options links to Groq's
  official one-time model-terms page when the account has not enabled Orpheus.
  The public build does not bundle or claim an official character recording,
  performer voice, or unlicensed voice-conversion model.
- Rebuilt verified installs as focused in-place updates. After the signed
  download passes its size and SHA-256 checks, an existing installation skips
  fresh-setup pages, replaces only compiled app files in the same location,
  preserves settings, protected keys, and voice choices, then restarts Agnes
  automatically with the update.
- The owner Release Console now reuses an existing GitHub CLI sign-in when one
  is available, without displaying or persisting another token. A manually
  pasted fine-grained token remains available as the fallback.
- Guide Agnes activation is now a persistent online state instead of a
  one-second flash. Her pulsing energy ring, faster dual orbits, ambient sparks,
  and online status remain active across guide reloads; clicking her again
  settles the preview down with its own smooth effect. The hero headline
  also uses a safer responsive scale and column gap so it cannot overlap or
  escape its card at narrow desktop sizes or browser zoom.
- Added privacy-safe feedback and bug reporting to Options, the tray, and the
  locally running Setup Lab. The anonymous form accepts a typed message without
  GitHub or any sign-in; the owner-only Release Console securely syncs new
  reports as readable text files into a chosen local folder on launch and every
  five minutes.
- Reworked all four Options tabs with crisp Qt-painted vector symbols instead
  of font-dependent emoji. Labels now elide safely, selection indicators stay
  inside their tab, and hover/selection motion remains smooth from minimum size
  through maximized high-DPI layouts.
- Hardened the Setup Lab at 320–1920 pixels and 125–200% zoom so hero copy,
  filter chips, long repair titles, buttons, legal notices, and feedback actions
  remain inside their containers.
- The three-step celebration now plays the supplied `yay sound effect.mp3`
  byte-for-byte from the self-contained guide, with no network request or
  generated substitute.
- Added an owner-controlled update channel. Agnes and standalone Options check
  a pinned Ed25519-signed release notice in the background, offer optional or
  required prompts, stream the setup into a private per-user cache, and verify
  its signed byte size and SHA-256 before launch. One **Download update** click
  now stays inside Agnes with smooth progress, live transfer details, animated
  verification, a completion transition, and automatic installer launch.
  Required notices remain owner-signed and enforced across offline restarts;
  live listening, vision, speech, and companion actions pause while one is
  waiting.
- Added a separate `AgnesReleaseConsole.exe` owner build with the Agnes theme,
  live publication progress, a required-update checkbox, GitHub release
  publishing, Windows Credential Manager storage, and encrypted signing-key
  backup/restore. It is never included in the public installer.
- Rebuilt the locally running Setup Lab logo and responsive layout. Narrow
  windows, browser zoom, long labels, status rows, cards, and troubleshooting
  text now stay inside their containers.
- Added a three-step completion celebration with original VFX, the bundled
  completion sound, accurate progress semantics, and protection against corrupt
  saved progress.
- Fixed window-state animation races, off-screen restore geometry, minimum-size
  taskbar transitions, maximized title-drag clamping, and fake rounded native
  menu corners.
- Replaced the crowded Options interaction grid with one clear, reliable tray
  menu. The refreshed native menu now has modern spacing, hover states,
  high-DPI procedural icons, a clear busy state, and Windows Contrast Theme
  support.
- **Make her dance** now chooses between the two genuine music routines,
  prevents immediate repeats and overlapping interactions, and stops the
  animation when the matching song ends. Stale completion events cannot stop a
  newer dance, and external-pet resets never steal keyboard focus.
- Added two original, procedurally synthesized music tracks for the public
  code-drawn companion. They add no downloaded assets or multimedia dependency,
  stop cleanly for listening and speech, and keep the release rights-safe.
- Added release gates for exact installer/spec payload allowlists, embedded
  audio or third-party pet leaks, publisher metadata, and stale executable
  versions.
- Rebuilt the Setup Lab's pointer aura around a self-stopping GPU spring, fixed
  its lag and rubber-banding, and added Full, Calm, and Off VFX profiles that
  respect touch, reduced-motion, and high-contrast settings.
- Added an interactive Agnes guide preview, ambient telemetry, richer
  lightweight VFX, smoother card tracking, and a searchable repair center with 28 practical
  fixes for voice, AI, screen awareness, installation, updates, and app problems.
- Rebuilt the locally running Setup Lab with the Agnes visual theme, animated
  companion VFX, fluid section reveals, interactive setup progress, responsive layouts,
  keyboard focus states, high-contrast support, reduced-motion support, and a
  clean print view.
- The Setup Lab has no trackers, remote assets, account names, or machine
  directories. The installer opens it in Edge application mode when available,
  hiding the local file address; the native Options setup page is the
  privacy-safe fallback when Edge is unavailable.
- Added an original, rights-safe animated Agnes desktop mascot. It can be
  dragged, clicked, double-clicked, scrolled, fed, poked, surprised, and asked
  to dance. AI and screen events animate it automatically.
- Rebuilt Options transitions with race-safe sliding tabs, inertial scrolling,
  hidden scrollbars, stable maximize/restore behavior, smooth title controls,
  high-DPI support, keyboard navigation, focus indicators, and immediate
  reduced-motion behavior.
- Added second-launch activation: starting Agnes while it is already running
  opens the existing Options window instead of creating another process.

## Smarter and faster

- Conversation, current-fact research, vision, and transcription keep the
  proven `openai/gpt-oss-120b`, `groq/compound-mini`, `qwen/qwen3.6-27b`, and
  `whisper-large-v3-turbo` model paths while speech gains the expressive
  `canopylabs/orpheus-v1-english` voice path.
- Current questions use `groq/compound-mini`, while normal conversation stays
  on `openai/gpt-oss-120b` for fast streaming.
- Vision uses `qwen/qwen3.6-27b` in non-thinking mode, skips static frames,
  requires structured event confidence, and no longer mistakes visible words
  for live gameplay events.
- Speech recognition rejects silence before making an API call and keeps Groq
  transcription separate from other selectable chat providers.
- New speech cancels stale generation and playback. AI reactions are bounded,
  deduplicated, and processed latest-first to prevent emote or voice spam.
- TTS, microphone capture, screen capture, network streams, background tasks,
  and optional converter processes now have bounded cleanup and timeouts.

## Reliability and privacy

- Older configurations are migrated and repaired without overwriting stored
  choices or reintroducing unlicensed asset paths.
- Logs rotate automatically; API keys and the Windows user profile path are
  redacted. The tray diagnostics panel reveals the current computer's log
  location only when requested.
- API keys remain in Windows Credential Manager.
- The public installer still excludes Desktop Gremlin, extracted game assets,
  and the unlicensed Tachyon voice model.
- Publisher and original-project ownership metadata use only `y4x5lol`.
