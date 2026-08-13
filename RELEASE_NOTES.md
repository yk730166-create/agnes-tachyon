# Agnes Tachyon AI Companion 6.5.2

## 6.5.2 — Options that stay in their lane

I cleaned up the AI section in Options so choice boxes behave like choice
boxes instead of letting accidental typing create broken settings.

- Every dropdown is selection-only, including the AI brain and picture model.
- Changing the AI company now refreshes both model lists and the server address
  together, so mismatched provider/model combinations are much harder to make.
- Direct choices now include Groq, OpenAI, Google Gemini, DeepSeek, xAI,
  Mistral AI, Together AI, Ollama, and LM Studio.
- OpenRouter is included for people who want one compatible key for its wider
  provider catalog.
- Cloud keys stay in Windows Credential Manager; local providers need no key.
- Old unknown provider values fall back safely instead of leaving Options in a
  half-valid state.

## 6.5.1 — Fish voice without normal credit charges

This small required follow-up switches the exact Agnes voice to Fish Audio's
official `s2.1-pro-free` API model string.

- The same public Agnes voice reference remains pinned.
- Speech uses Fish's free developer model under its current fair-use terms,
  instead of the normal pay-as-you-go S2 Pro model.
- There is no automatic paid-model fallback, so Agnes cannot quietly spend
  normal TTS credits if the free endpoint is unavailable.
- Existing 6.5.0 settings migrate automatically.
- API keys remain per-user secrets in Windows Credential Manager. No Fish key
  is embedded in the EXE, installer, website, update notice, or GitHub files.

## 6.5.0 — One voice, properly wired

I replaced every built-in desktop speech path with the Fish Audio S2 Pro voice
the project now uses: `64e74b61065540f4abed3a0f30cf14d9`.

- Old Groq Orpheus and Windows neural voice settings migrate to Fish, so an old
  config cannot randomly bring the wrong Agnes voice back.
- Fish keys are stored in Windows Credential Manager. No shared secret is
  embedded in the EXE, installer, config, guide, or GitHub page.
- Options now has a clear Fish key field and shows Fish's exact returned credit
  balance alongside conversations, tokens, vision reviews, voice characters,
  and listening time.
- Fish S2 Pro receives the clean spoken answer directly with natural pacing;
  failures stay honest instead of swapping to a robotic substitute.
- The public Setup Lab no longer pretends a random browser voice is Agnes. Its
  built-in questions remain instant and text-only; the installed app owns the
  exact voice path.
- Existing settings migrate in place, the optional Applio installer choice
  remains available, and private API keys never enter the release package.

## 6.4.1 — One Agnes, a real dance stop, and the full meter

This is the last cleanup pass for today. It removes the second-character flash,
makes dance completion use the control path DesktopGremlin actually accepts,
and turns the small vision counter into a useful whole-AI activity monitor.

- The retired code-drawn Agnes can no longer appear. If the packaged model is
  closing, restarting or unavailable, the tray stays running without revealing
  a substitute character.
- Music completion now briefly sends DesktopGremlin its documented Escape
  command through the active-window path, then restores the user's foreground
  window. The model returns to idle without waiting for a mouse hover and
  without playing another emote sound.
- **AI credit & usage monitor** now shows today's total AI requests,
  conversations, picture reviews, provider-reported tokens, generated voice
  characters and listening time. The automatic-vision guard and daily limit
  remain directly beneath the overall totals.
- The meter stores counters only. Provider dashboards remain the exact source
  for account credits and service limits.

## 6.4.0 — The stream-aware dance repair

This one fixes the interaction mix-up and makes screen awareness feel live
without quietly feeding every frame to a paid model.

- **Make her dance** now uses only the two original Uma music routines already
  used by the Setup Lab. The unrelated short-video sounds are gone from the
  random dance pool.
- A music dance returns Agnes to idle as soon as its measured track duration
  ends. Old timers and stale audio completions cannot stop a newer dance.
- **Poke Agnes** now plays her real surprised animation instead of the ordinary
  click reaction.
- Screen awareness now watches the foreground app locally at up to 10 FPS,
  keeps the strongest recent transitions, and sends only useful keyframes to
  the picture model. Asking “what's that?” always captures a fresh full-quality
  frame for the answer.
- The new **Live vision credit guard** in Screen & Pet shows today's automatic
  reviews, skipped frames and conversations, and enforces a user-controlled
  daily cloud-review limit. Local watching continues when the limit is reached.
- Website answers now prefer the best available Microsoft multilingual natural
  voice, speak in short thoughts with tiny human pauses, and use gentler prosody
  instead of one flat robotic paragraph.
- App speech leaves ordinary questions and exclamations undirected, matching
  Orpheus's natural-conversation guidance. Emotional cues remain only where
  they actually help.
- Usage records contain counters only—never prompts, screenshots, transcripts,
  API keys or spoken text.

## 6.3.9 — The optional voice engine is back

This is a small voice-focused update. Normal installs stay the same size, and
automatic updates do not suddenly pull several gigabytes onto anyone's PC.

- Setup once again has an unchecked option to download official Applio 3.6.4.
  The 4.6 GB archive is pinned to its release revision and exact SHA-256 before
  Inno Setup extracts it. It also checks for the 13 GB of temporary free space
  needed for the download and unpacking step.
- Added a second optional checkbox for Windows file compression after Applio is
  installed. If compression is unavailable, the voice engine still works.
- Agnes automatically finds Setup's per-user Applio folder. The converter now
  prefers Applio's matching embedded Python and native packages instead of
  accidentally mixing them with an unrelated system Python.
- Removed the forced “fast paced” direction from ordinary Orpheus lines. Groq
  recommends no direction for natural conversation, so regular speech now has
  a less acted, less robotic cadence while real questions and emotional lines
  can still use restrained directions.
- Licensed RVC voice models use a slightly stronger index blend, the full
  output volume envelope, and Applio's recommended consonant protection. Old
  untouched defaults migrate automatically; custom tuning stays unchanged.
- Applio remains optional and does not include or download a character voice
  model. A matching `.pth` and `.index` that the user may legally use are still
  selected in Options.

## 6.3.8 — The updater now lets Agnes stay awake

This is a small but important follow-up to 6.3.7. The files were installing
correctly, but the Agnes process started by Windows Setup could still think it
belonged to the old frozen app and close shortly afterward.

- The updater now starts the replacement as a completely fresh Agnes process,
  so she stays running after Setup closes.
- The fix is also built into Setup itself. That means the already released
  6.3.7 updater can move to this version safely instead of needing a manual
  reinstall first.
- The 100% state still waits for the signed installer acknowledgement, and the
  app still preserves settings, protected keys, voice choices, and user files.
- Added a full restart-chain regression check so a future updater cannot quietly
  bring this same bug back.

## 6.3.7 — She finally stops making you wait

This one is mostly about making Agnes feel awake instead of making you wonder
whether Windows ate her.

- Agnes and Options now use one installed shared runtime instead of unpacking
  the same huge bundle on every launch. Her model also starts before the heavy
  AI/audio interface loads. On the test PC, real Agnes appeared in about 1.83
  seconds instead of 6.65 seconds.
- Normal chat automatically uses the quick brain, while hard comparisons,
  plans, debugging, and other serious questions keep the larger smart brain.
- If a reply really is taking time, Agnes says “Wait, let me think” once. Fast
  answers stay fast and do not get an unnecessary filler line.
- Talking immediately pauses any screen-analysis request already in flight, so
  live vision can no longer stand in front of your answer in the queue.
- Live screen awareness now watches the foreground app, keeps two recent frames
  for visible transitions, and only reacts when the newest frame proves an
  event with usable confidence.
- The missing food dish is finally included. Giving Agnes a snack no longer
  asks DesktopGremlin to load an asset that setup forgot to install.
- Dance now has four Agnes routines instead of two. The two added short tracks
  come from the existing Tachyon music in this project, use different Agnes
  emotes, and stop exactly with their music.
- The update screen now waits for Windows Setup itself to confirm that it
  accepted the existing Agnes folder. If Setup cannot really begin, Agnes
  stays open and shows a useful retry message instead of sitting at 100%.
- The Setup Lab gives each action its own clean symbol, keeps text inside its
  cards at small window sizes, and plays Agnes at her natural animation speed.
- The installer replaces the old one-file runtime during this required update,
  keeps settings and voice choices, and removes files from the retired layout.

## 6.3.6 — The bug-focused compatibility pass

- Required updates now hide the exact real Agnes window whether the prompt was
  opened by the tray companion or standalone Options, so she cannot cover the
  title, notes, progress, or controls.
- Hides every visible window owned by the exact configured companion process,
  rather than assuming the model can expose only one surface.
- If the external .NET renderer is blocked or exits on a stripped-down Windows
  installation, Agnes now appears through the built-in fallback after a short
  startup grace period and switches back if the real window later becomes ready.
- Slow-drive installer verification uses an active indeterminate progress state
  with honest status details instead of appearing frozen at 100%.
- Completes the final success glow before application shutdown instead of
  cutting the last animation frame short.
- Removes the confusing disabled action buttons once a verified handoff starts,
  gives ordinary release notes enough room to avoid a scrollbar, and tightens
  title wrapping for Windows display scaling.
- Refines the native installer progress window to identify every managed surface
  being refreshed, while keeping settings, protected keys, and voice choices.
- Adds an explicit runtime compatibility check for Windows 10 build 17763, the
  oldest build supported by the frozen Qt 6 runtime. This includes Enterprise
  LTSC 2019, LTSC 2021, LTSC 2024, and every Windows 11 release.
- Corrects the real Agnes outro metadata from two conflicting, truncated frame
  counts to the sprite sheet's actual 69 populated frames, and removes two
  advertised actions whose image files do not exist.

## 6.3.5 — A handoff that cannot sit frozen at 100%

- Starts the already verified Windows updater before Agnes begins her bounded
  AI, audio, tray and model shutdown, removing the frozen-looking gap between
  download completion and installation.
- Keeps the update window above the desktop model, hides Agnes during required
  maintenance, and replaces the generic status orb with her real portrait.
- Shows the branded Windows installation progress surface immediately and
  shortens the final handoff animation without losing verification.
- Replaces the entire managed guide-media and Agnes model directories on every
  update, removes known legacy source/build leaks, recreates all managed
  shortcuts with the current icon, and refreshes the Windows shell icon cache.
- Preserves user configuration, protected API keys, optional licensed voice
  files and local preferences while replacing every release-owned file.

## 6.3.4 — The real Agnes model, native 60 FPS, and full companion bundle

- Replaced every generated character mark with the real bundled Agnes icon and
  made the exact Agnes desktop model the installed default.
- Added the complete Agnes-only movement, action, emote, dance and matching
  sound bundle while explicitly excluding every other Desktop Gremlin model.
- Upgraded the Setup Lab preview to native 60 FPS VP9 clips and connected its
  two genuine music dances so animation returns to idle when the track ends.
- Replaced the completion and feedback placeholders with the real Agnes mark,
  removed the procedural-model startup flash, and tightened startup migration
  so existing installs automatically adopt the bundled model.
- Refined model/provider selection, reaction repetition control, screen-event
  confidence handling, audio-device discovery, feedback safety and release
  build checks.

## 6.3.3 — Buttery guide motion, consistent local voice, and public cleanup

- Moved the Setup Lab model from JavaScript canvas cropping to double-buffered,
  transparent 30 FPS VP9 video. The browser now decodes one active clip on its
  media path, crossfades actions, and no longer expands a 30.6-megapixel idle
  sheet in memory.
- Replaced the six-question demo with 36 fixed local answers across About,
  Talking, Vision, AI brain, Updates, and Fun groups. The category tabs are
  keyboard-friendly and keep the card compact on small screens.
- Fixed the first-answer voice race by waiting for Windows/browser voices to
  finish loading, consistently preferring a compatible natural voice, and
  using a brisk, slightly lower delivery based on the character's official
  researcher presentation. No official recording or voice clone is bundled.
- Replaced the abstract flask/AI-looking mark with an original hand-drawn
  copper-haired portrait used by the app, taskbar, installer, and Setup Lab.
- Removed raw sprite PNGs from both the installer payload and public website.
  Only the derived transparent runtime clips required by the live preview are
  published; app source, raw sheets, voice models, owner tools, secrets, and
  build folders remain private.
- Rewrote the public README in y4x5lol's direct voice, without development
  commands or private release-console instructions.
- Fixed the brand-icon builder for current PySide releases, hardened video load
  and transition failure cleanup, and expanded media/public-payload regression
  checks.

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
- The current public installer includes only the curated Desktop Gremlin Agnes
  bundle and still excludes every other character and the unlicensed Tachyon
  voice model.
- Publisher and original-project ownership metadata use only `y4x5lol`.
