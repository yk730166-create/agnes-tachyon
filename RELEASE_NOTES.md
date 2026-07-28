# Agnes Tachyon AI Companion 6.1.2

## Highlights

- Lab Core activation is now a persistent online state instead of a one-second
  flash. Its brighter liquid, pulsing energy ring, faster dual orbits, ambient
  sparks, and `CORE ONLINE` status remain active across guide reloads; clicking
  it again produces a boost burst without switching it off. The hero headline
  also uses a safer responsive scale and column gap so it cannot overlap or
  escape its card at narrow desktop sizes or browser zoom.
- Added privacy-safe feedback and bug reporting to Options, the tray, and the
  locally running Setup Lab. Public builds open a pinned, prefilled GitHub issue
  with no embedded owner token; the owner-only Release Console mirrors reports
  into a chosen local feedback folder on launch and every five minutes.
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
- Added two original, procedurally synthesized music tracks for the public Lab
  Core. They add no downloaded assets or multimedia dependency, stop cleanly
  for listening and speech, and keep the release rights-safe.
- Added release gates for exact installer/spec payload allowlists, embedded
  audio or third-party pet leaks, publisher metadata, and stale executable
  versions.
- Rebuilt the Setup Lab's pointer aura around a self-stopping GPU spring, fixed
  its lag and rubber-banding, and added Full, Calm, and Off VFX profiles that
  respect touch, reduced-motion, and high-contrast settings.
- Added an interactive Lab Core, ambient telemetry, richer lightweight VFX,
  smoother card tracking, and a searchable repair center with 28 practical
  fixes for voice, AI, screen awareness, installation, updates, and app problems.
- Rebuilt the locally running Setup Lab with the Agnes visual theme, animated lab-core
  VFX, fluid section reveals, interactive setup progress, responsive layouts,
  keyboard focus states, high-contrast support, reduced-motion support, and a
  clean print view.
- The Setup Lab has no trackers, remote assets, account names, or machine
  directories. The installer opens it in Edge application mode when available,
  hiding the local file address; the native Options setup page is the
  privacy-safe fallback when Edge is unavailable.
- Added an original, rights-safe animated Lab Core desktop mascot. It can be
  dragged, clicked, double-clicked, scrolled, fed, poked, surprised, and asked
  to dance. AI and screen events animate it automatically.
- Rebuilt Options transitions with race-safe sliding tabs, inertial scrolling,
  hidden scrollbars, stable maximize/restore behavior, smooth title controls,
  high-DPI support, keyboard navigation, focus indicators, and immediate
  reduced-motion behavior.
- Added second-launch activation: starting Agnes while it is already running
  opens the existing Options window instead of creating another process.

## Smarter and faster

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
