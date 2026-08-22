# Agnes Tachyon AI Companion 6.6.13

## 6.6.13 — Stays in the game

This release is mostly the unglamorous stuff that makes Agnes feel dependable.
The full-screen overlay no longer briefly drops behind a game when Windows
reorders topmost windows, and clicking Agnes cannot steal focus from the game.

- Agnes's real model now uses a native no-activate window. It stays clickable
  and draggable on the desktop without becoming the foreground app, closing a
  game, or knocking an exclusive window out of full screen.
- The visibility watchdog refreshes Agnes directly in the topmost band, checks
  more often, and can recover her if Windows briefly hides the model. It no
  longer bounces through NOTOPMOST, which caused visible flashes and gaps.
- Game vision can selectively notice meaningful dialogue choices, real plot
  reveals, genuinely funny NPC lines, broken stealth, boss phase changes, and
  clutch moments. Ordinary subtitles and routine conversations stay quiet.
- Repeated dialogue scenes are fingerprinted for five minutes, each event type
  has its own cooldown, and ambiguous visual changes do nothing until vision
  confirms them. That cuts random emotes and repeated commentary.
- Repeated deaths or mistakes now give Agnes enough session context to offer one
  grounded tip when useful; successful runs get varied encouragement instead of
  the same celebration again.
- Hidden helper windows are excluded from recovery, screen events remain game-
  only and credit-limited, and the full test runner no longer executes private
  network scratch scripts by accident.

## 6.6.12 — A tiny lab partner for real work

Agnes can now help with the thing in front of you instead of only talking about
it. Ask her to improve a visible draft, write a reply, explain an error,
summarize a page, or show you the next safe step. She reads a fresh view, sits
down on her real lab paper while working, and gives you the result in her voice.

- Rewrites and replies are proposals first. Agnes asks before pasting, pins the
  proposal to the original app, and refuses to type if focus changed. Password,
  payment, API-key, token, private-key, and recovery-phrase contexts are blocked.
- “Paste it,” “copy that,” and “never mind” are short, explicit follow-ups. A
  longer answer cannot accidentally approve a desktop action.
- Error help, summaries, and next-click guidance remain read-only. Screen text is
  treated as untrusted evidence, so a page cannot instruct Agnes to bypass the
  confirmation rules.
- The bundled model now has a focus-free controller command for the real sitting
  animation and a reliable return to idle; it does not steal focus from games or
  the user's text field.
- Fish clips receive a completeness check and one clean retry when a service
  response is impossibly short. Normal replies use longer continuous thoughts,
  reducing stitched pauses without allowing hover or movement to cancel speech.
- The Windows paste path, focus pinning, sensitive-target guard, intent detector,
  animation protocol, and speech-cutoff detector received regression coverage.

## 6.6.11 — Faster answers, eyes that actually look

This one is mostly about Agnes feeling awake. Normal Gemini conversations now
use its quick Flash-Lite path while bigger questions still keep the stronger
model you selected. Groq and other compatible providers also have a final guard
that keeps hidden thinking text out of her spoken answer.

- Questions like “do you see the person here?” now attach a fresh focused-app
  view instead of sometimes becoming an ordinary text-only question. Every AI
  provider gets the same clear description of Agnes's real vision, memory,
  voice, game, animation, and music features.
- Game awareness recognizes more moments, including respawns, upgrades,
  discoveries, clutch saves, race-position changes, and puzzles. Reactions can
  include one useful tip when the evidence is clear, but remain cooldown-limited
  and do not continuously spend vision credits.
- Agnes's resting sprite is calmer without lowering the 60 Hz movement/render
  loop. Optional idle movement now waits about five minutes, while dance beats
  have a more obvious nod and accent.
- Required updates are checked before the pet, audio, vision, or AI model starts.
  When one exists, the verified update prompt appears first and Agnes waits until
  the update finishes.
- Visual intent, provider routing, hidden-reasoning cleanup, event parsing,
  configuration migration, and startup behavior received new regression tests.

## 6.6.10 — Calmer idle, smoother conversations

Agnes now gives the desktop room to breathe. Her optional idle movement happens
about once every three minutes instead of repeatedly every few seconds, while
music-driven head bobbing and dance timing stay exactly as they were.

- Options now reads and saves the controller's real idle interval. Existing
  30- or 90-second defaults move to 180 seconds; custom waits stay untouched.
- Spoken replies are grouped into natural thoughts instead of starting a new
  Fish request for every sentence. This removes the stop, pause, suddenly-fast
  pattern that could make a single answer sound stitched together.
- A thinking line that has already begun is allowed to finish cleanly before
  the answer starts, with a strict safety timeout for damaged audio.
- Fish now keeps each short thought in one conditioned generation using its
  documented quality chunk size, and one brief network seam gets a fast retry.
- Agnes - Adult receives a small voice-specific speed correction, while Normal
  and the user's Natural or Quick preference keep their intended pacing.

## 6.6.9 — Agnes listens to her own switches

The desktop behavior controls now do exactly what they say, immediately. Movement,
AI/game reactions and music bobbing are separate from optional self-started emotes
and dances, and both stay off when their switches are off.

- Dance music now starts at a calmer 30% and has its own 0–100% volume slider.
  The real renderer uses volume-aware playback, and a saved change reaches the
  running Agnes without requiring a restart.
- Automatic movement and automatic performances use separate schedules. They
  pause during speech, updates and active music, while every manual tray action
  remains available.
- Both reviewed Fish choices are clearly exposed as Agnes - Normal and Agnes -
  Adult, with a two-row picker that cannot hide the second voice.
- Manual tray update checks immediately report that they started, and their
  success or connection result returns through the tray instead of appearing
  behind a game or another window.
- Renderer audio cleanup, live controller commands, option persistence and the
  beat-synced dance system were regression-tested together.

## 6.6.8 — Agnes found the beat

Dance motion now follows the music instead of running as a completely separate
loop. Agnes analyzes the two packaged songs locally, nods on their strongest
beats, and adds a couple of small flourishes at standout moments.

- Beat timing comes directly from each WAV file and is cached after the first
  analysis. It uses no AI request, network call, or credits.
- The nod and flourish commands animate the real Agnes sprite without changing
  her current dance, stealing game focus, or blocking the tray interface.
- Each new song gets at most two flourishes. Repeating the same song does not
  reset that budget, so a loop cannot make Agnes spam reactions.
- Stale dance timers cannot affect the next song, motion resets cleanly when a
  dance ends, and silent or damaged audio safely falls back to normal dancing.
- Both real songs, the renderer command bridge, timing bounds, and the full app
  regression suite were checked again.

## 6.6.7 — Agnes actually looks before she answers

This fixes screen questions that could reach the AI without a usable picture.
When you ask about a profile, page, popup, game, or anything else visible,
Agnes now captures the focused app at readable quality and adds the wider
monitor view when it contains extra context.

- Screen questions no longer use a canned “yes, I can see” answer. They go
  through the real vision path and carry fresh image data.
- The capture path retries transient Windows failures, falls back to the live
  buffer, masks Agnes herself, and clearly logs a capture failure instead of
  silently pretending that a text-only request had vision.
- Gemini 3 quick chat and vision use its documented low reasoning effort, which
  prevents short output budgets from being consumed by hidden thinking and
  makes simple answers arrive sooner.
- Fish voice choices are now named **Agnes - Normal** and **Agnes - Adult**.
  Both use the same Fish key protected by Windows Credential Manager.
- Check my setup now distinguishes a valid Fish key from an empty Fish API
  balance, so it cannot show a false green result when speech would be blocked.
- Windows capture, synthetic Gemini image reading, voice migration, settings,
  privacy, and the full regression suite were checked again.

## 6.6.6 — The buttons work and Agnes answers

This fixes the annoying one: Agnes no longer says “wait, let me think” and then
leaves you talking to the wallpaper. The old Fish community voice disappeared,
so every existing install now moves to the working Agnes voice automatically.

- Dance, snack, poke, and surprise now use an acknowledged command channel in
  the bundled Agnes model. The tray only reports success after the model really
  receives the action; nothing steals focus or sends a key into your game.
- The retired Fish reference is gone from Options. **Agnes — Natural** is now
  the single working voice, and stale settings recover automatically.
- Small stable questions such as greetings, “who are you?”, features, screen
  awareness, thanks, time, and date answer locally with zero AI credits.
- Ordinary AI chat gets one short, bounded attempt instead of waiting through a
  full timeout and repeating the same slow request. Hard questions still keep
  the larger reasoning path and a retry where it can actually help.
- All 36 Setup Lab voice answers were rebuilt with the same working Agnes voice.
- The companion command path, voice migration, Fish failure recovery, thinking
  cue handoff, conversation history, and the complete test suite were checked
  again for this required fix.

## 6.6.5 — Agnes stays with the game and the conversation

This one fixes the things you can actually feel while using Agnes. She stays
above full-screen games without touching the game window, keeps talking when
you move or hover over her, remembers the conversation, and her tray toys work
without stealing focus.

- Full-screen mode now refreshes only Agnes's verified model window in the
  topmost band. It never activates, resizes, minimizes, closes, or sends keys to
  the game, and mouse input still passes safely through during full screen.
- Hovering over Agnes or ordinary model movement can no longer interrupt her
  voice. Holding the talk key while she speaks remains the deliberate way to
  interrupt her and start a new thought.
- Conversations now survive restarts in a small local history file. It stores
  text only, stays bounded, rejects credential-looking text, and is removed by
  Clear memory alongside saved facts.
- “Wait, let me think” can no longer cancel or swallow the real answer. The cue
  starts only when ready, retires as soon as the answer arrives, and never
  advances the response's speech generation.
- Agnes is masked out of her own screen captures, so “what's that?” describes
  the game or app underneath instead of confidently introducing herself.
- Local and cloud game awareness now cover boss moments, objectives, revives,
  streaks, rare loot, jumpscares, crashes, defeat/damage transitions, result
  screens, and major scene changes with per-event cooldowns to avoid spam.
- Play with Agnes now clicks the real model's native dance, snack, poke, and
  emote hotspots directly. These actions work without keyboard focus and cannot
  leak a key into a full-screen game.
- Options and the tray share a rebuilt command-deck look with clearer page
  names, simpler actions, larger targets, distinct icons, and compact layouts
  that keep every control inside the window.
- The complete 246-test suite, lint gate, voice, vision, lifecycle, game-event,
  fullscreen, memory, tray, installer, and packaged-runtime paths were checked
  again for this required release.

## 6.6.4 — One clean control center

Okay, this one is the proper cleanup pass. Agnes now has one home in Windows,
Options has its own visual identity instead of feeling like an old settings
dialog, and several quiet runtime bugs were fixed while I was in there.

- There is now one Agnes tray/controller icon. The bundled model's old taskbar
  button and legacy tray icon are removed by exact process and file path, so no
  other program can be touched by mistake. Explorer restarts are handled too.
- An Agnes model left behind by an older crash is adopted into the new session
  and closes normally with Agnes instead of surviving every relaunch as a
  duplicate icon or invisible process.
- Options was rebuilt around a cleaner tachyon-lab theme: solid modern surfaces,
  copper Agnes details, cyan status signals, clearer cards, consistent controls,
  and responsive layouts that keep every action visible down to 640×500.
- The tray is now a real Agnes control center with its own status card, larger
  targets, clearer groups, distinct action icons, smoother motion, and the same
  colors as Options instead of a generic right-click menu.
- Screen watching now starts correctly even in Local-only mode, so credit-free
  game detection does not depend on a cloud vision client being available.
- Trusted game events and visual events can no longer announce the same moment
  twice. Java tools and store/launcher windows also stay out of game detection.
- Cancelling a speech-to-text request no longer leaves a background provider
  call blocking the next thing you say. First-run voice prewarming and the
  thinking cue now share one job instead of racing each other.
- A newly saved Credential Manager key wins over an old environment-variable
  key, so replacing a rejected provider key actually takes effect immediately.
- The complete source regression suite, static checks, Windows rendering, tray
  ownership, icon lifecycle, game awareness, voice, vision, updater, installer,
  and packaged-runtime paths were checked again for this required release.

## 6.6.3 — Options finally feels finished

If you skipped 6.6.2, Agnes still performs that one-time settings reset after
this update and clearly opens Options once. Your protected AI-provider and Fish
Audio keys stay. People who already completed the reset are not reset again.

- Options now uses real Windows 11 outer corners without transparent holes.
  Windows 10 keeps a solid square window, and maximized mode is always square.
- The ugly full-row selection rectangles are gone. Keyboard users still get a
  small, clean focus ring on the control they are actually using.
- Footer actions have truthful minimum sizes, so **Save & close** and the other
  icon buttons no longer lose half their text at ordinary window sizes or DPI.
- The Voice page now offers **Agnes — Classic** and the optional, brighter
  **Agnes — Bright** performance. Both use the same protected Fish Audio key,
  and changing voices also changes the cached thinking cue correctly.
- **Check my setup** tests only the AI company currently selected. Gemini uses
  Google's own no-generation model-list check, Fish is checked separately, and
  a rejected key can no longer appear in the “Already working” list.
- The tray menu is roomier, smoother, and easier to scan, with a distinct color
  and symbol for each action instead of a row of near-identical blue icons.
- Minecraft log watching no longer treats every random Java application as
  Minecraft. Local visual-event cooldowns also reset correctly when games
  change, avoiding missed reactions after switching titles.
- A live Windows/DPI pass caught and fixed a tab-focus paint exception before
  release, and the voice, settings, game-awareness, icon, reaction, updater,
  installer, and packaging paths were run through the full regression gate.

## 6.6.2 — Fullscreen stays yours

**Important settings reset:** this required stability update resets every Agnes
option to the new safe defaults. Saved AI-provider API keys and the Fish Audio
key stay protected in Windows Credential Manager. Agnes shows a warning and
opens Options after the update—once no full-screen game is active—so the talk
key, microphone, speaker, AI provider, and game choices can be reviewed.

- Agnes no longer hides, shows, repaints, activates, or reorders her WPF model
  while a game owns full screen. Those window operations could knock some
  exclusive games out of full screen or make a fragile game close.
- Pet actions and the automatic end of a music dance no longer focus Agnes or
  emit a global keyboard event. Every action key is sent only to the verified
  Agnes process, so an Escape, number, or snack key cannot leak into the game.
- The invisible-hitbox safety remains: if exclusive scan-out hides Agnes's
  pixels, mouse input passes through to the game and her exact original window
  style returns after full screen ends.
- Ordinary conversation starts Fish speech from a shorter natural phrase.
  Complex or live-search answers say “Wait, let me think” only after a real
  delay, and a ready answer now interrupts that cue instead of waiting for the
  entire clip to finish.
- Short autonomous game reactions use the fast sibling model from the same AI
  provider, with a smaller answer budget. Full questions still automatically
  use the larger brain when they need deeper reasoning.
- The runtime, installer, and reset profile now share the same current game
  awareness and personality defaults. Local screen-event measurement remains
  at 10 FPS, while bounded cloud reviews and daily limits prevent credit burn.
- Redundant SDK retries were removed from the clean defaults. Agnes still makes
  one deliberate retry for a connection hiccup, but no longer stacks hidden
  retries that make an outage look like a frozen response.

## 6.6.1 — Agnes stays visible, not just clickable

This fixes the strange full-screen case where a game could swallow Agnes's
picture but leave her invisible click area above your controls.

- Borderless and Windows-composed full-screen games now rebuild Agnes's
  transparent WPF drawing surface, raise every Agnes-owned surface together,
  and repaint without stealing keyboard focus.
- The companion's supported one-alpha transparency safeguard is enabled before
  launch. It is visually transparent, but prevents Windows composition from
  keeping an invisible hitbox after dropping the sprite layer.
- Hiding and restoring Agnes now includes spawned items and any other visible
  companion surfaces, so invisible interactive leftovers cannot remain over a
  game.
- While a game is focused, Agnes automatically lets mouse clicks pass through.
  Old exclusive full-screen modes can bypass all safe Windows overlays; those
  games should use Borderless Windowed for visible Agnes, and can no longer
  leave an invisible hitbox blocking the game.
- The watcher checks more quickly during a full-screen game, but slows down on
  the desktop and reuses its process lookup cache to reduce background work.
- Live game awareness still measures events locally at 10 FPS, while JPEG
  creation is now limited to useful transition, settled, and heartbeat frames.
  Detection stays quick with less CPU and memory churn during normal movement.

## 6.6.0 — Agnes actually watches for the moment now

The old screen system waited on a timer. This one watches locally, reacts as
soon as something meaningful happens, and asks the vision model only when it
needs help understanding the moment.

- A new local event engine samples tiny brightness, color, and motion numbers
  while a game is focused. It stores no recording and spends no AI credits.
- Death-screen, impact, result-screen, and other large transitions can trigger
  an immediate animation and a focused two- or three-frame AI confirmation.
  Normal camera movement does not trigger a review.
- Minecraft gets a safe log adapter for official, Prism, Modrinth, ATLauncher,
  MultiMC, and common CurseForge layouts. Your deaths and advancements can be
  noticed instantly with mods or without them, without a picture request.
- COD, GTA, Steam, Xbox, Epic, EA, GOG, Riot, Ubisoft, Unity, Unreal, SDL,
  GLFW, and unfamiliar borderless games are recognized more reliably. Game
  launchers, Discord, browsers, and ordinary maximized apps stay excluded.
- One cloud event request now both identifies the moment and writes the short
  spoken reaction. The old second AI request is gone, and cooldowns prevent
  repeated reactions from piling up.
- Local capture slows down when no game is focused. Screen frames stay only in
  a short memory buffer, and the system never reads game memory, injects code,
  hooks rendering, or sends controls, keeping it friendly to anti-cheat tools.
- Options replaces the confusing check timer with three clear choices: Smart,
  Local only, and Most aware. The usage card now separates local events, safe
  log events, and AI-confirmed events.

This is designed to cover strong visual events in nearly any game, while exact
game adapters provide the fastest results when a game exposes a safe log.

## 6.5.7 — Agnes stays visible and answers sooner

This one fixes the annoying cases where Agnes vanished, protects chat from the
screen watcher, and makes the settings much easier to understand.

- The full-screen watcher now remembers Agnes's exact hidden window and can
  find it while it is hidden, so leaving a game restores her immediately. Even
  an unexpected Windows window-manager error fails visible instead of leaving
  her gone for the rest of the session.
- A maximized Discord, browser, editor, or normal desktop app is no longer
  treated as a full-screen game. Borderless games and games from Steam, Xbox,
  Epic, EA, GOG, Riot, and Ubisoft are recognized more reliably.
- Automatic screen reactions now run only while a likely game is in front.
  Old game context is cleared when you switch away, and Gemini background
  reviews are spaced and capped so they cannot consume the requests Agnes
  needs to hear and answer you.
- The slow-answer cue is prepared once and played locally. It no longer starts
  another Fish generation in front of the real reply, and it triggers based on
  how long you have waited to hear speech—not whether invisible text started.
- Normal answers keep less stale history, use shorter reply budgets, and log
  listening and first-token timing separately so future slowdowns have an exact
  cause instead of one misleading total.
- Game reactions understand more proven moments, including falls, embarrassing
  mistakes, close calls, and failed objectives, while keeping confidence checks
  and cooldowns to avoid random or repeated reactions.
- Options is cleaner and more modern: Start, Talk, Games & Agnes, and More use
  plain wording; one-choice voice/character boxes are gone; answer modes no
  longer secretly change game-watching speed; and the full-screen switch
  explains exactly what it does.
- Gemini choices now include the current stable 3.6/3.5 Flash family, with the
  request compatibility those models need. Windows file metadata was repaired
  so the updater, installer, and both EXEs all report the same version.

## 6.5.6 — Faster answers with a more human voice

This one makes talking to Agnes feel less like waiting on a voice assistant and
more like having someone there with you.

- Short, complete answers start generating speech immediately, the normal chat
  context is smaller, and the “Wait, let me think” line begins sooner only when
  an answer is genuinely taking time.
- Fish voice generation now uses its balanced conversational mode and smaller
  chunks, improving time-to-audio without using the lower-quality fast mode.
- Fish's streaming WAV header is repaired before playback. A short line can no
  longer be misread as a many-hour audio clip and leave speech timing stuck.
- Agnes uses restrained Fish S2 delivery cues chosen from the meaning of her
  line. Wins sound excited, danger sounds concerned, comfort sounds warm, and
  genuine jokes may get a soft chuckle. Plain answers stay plain, so emotions
  do not fire randomly.
- Agnes now receives an honest live summary of her enabled abilities. She knows
  whether screen awareness and local memory are on, knows the talk key, and can
  explain that she inspects fresh frames and reacts to confirmed game events.
- Autonomous screen reactions remain independent from push-to-talk: confirmed
  deaths, misses, wins, danger, achievements, and notable moments can trigger a
  matching animation and spoken reaction while you play.

## 6.5.5 — Agnes can hear you again

I traced the silent push-to-talk problem on a real installed copy. The mic was
recording correctly, but an old Groq key was being rejected while a valid
Gemini key sat unused. This update fixes that split and makes failures obvious.

- Groq, OpenAI, and Gemini now use the selected AI company's key for both chat
  and speech recognition. Other AI companies can still use a separate Groq
  listening key.
- **Check my setup** verifies the selected AI and Fish keys online without
  generating an answer or spending normal text/voice credits. Rejected keys
  are identified clearly instead of being called ready just because text was
  saved.
- A failed or rate-limited transcription now gives a short useful message. A
  slow valid answer says “Wait, let me think” sooner, while normal answers keep
  streaming immediately.
- **Show Agnes over full-screen games** now means exactly that. Off hides Agnes
  during a full-screen app and restores her without stealing focus; on keeps
  her visible. Changing it in Options applies live.
- Game reactions no longer depend on a title list. Agnes can react to proven
  events in familiar or unknown action, racing, sports, sandbox, shooter,
  platform, strategy, RPG, horror, and fighting games—including deaths,
  misses, wins, danger, achievements, bosses, QTEs, checkpoints, objectives,
  discoveries, puzzles, and exceptional moves.
- The local screen stream still watches at up to 10 FPS. Gemini cloud reviews
  are paced to avoid its common free-tier minute limit, and vanished foreground
  windows no longer produce capture errors when switching apps.
- Options wording and health checks now match the packaged Agnes model and the
  settings the runtime actually uses.

## 6.5.4 — One voice path, no extra engine

I removed the optional local conversion engine completely. Agnes now has one
clear desktop speech path through Fish, without a second multi-gigabyte tool or
extra model fields to configure.

- Setup no longer offers, downloads, extracts, or compresses an extra voice
  engine.
- Options no longer shows local converter paths, and **Check my setup** no
  longer reports those retired extras as missing or incomplete.
- The updater removes Agnes's old app-managed `VoiceEngine` folder so an
  existing installation does not keep several gigabytes of unused files.
- Old converter settings are safely removed during configuration migration;
  unrelated settings and files outside Agnes's managed folder stay untouched.
- Fish audio now goes straight to playback, which removes a slow subprocess
  and several failure points from every spoken response.
- The release was rebuilt and checked as a required in-place update for all
  supported Windows 10 and Windows 11 editions.

## 6.5.3 — The guide finally talks

The Setup Lab's 36 quick answers now speak with the same linked Fish Agnes
voice instead of silently showing text. I generated the finished clips during
the owner build, so the public page contains audio but no reusable Fish key.

- Clicking a different question cleanly stops the previous answer, and the
  speaking effects last for the real clip instead of a guessed timer.
- The dance answer speaks first, then starts one of the existing Uma routines,
  so voice and music do not fight each other.
- **Check my setup** now recognizes every supported AI provider, including a
  saved Gemini key, and reports which selected brain is ready.
- Groq push-to-talk and the external companion are clearly grouped as optional
  capabilities instead of failing the whole setup.
- The installed guide includes every voice clip and automatic updates replace
  the voice folder along with the rest of the managed guide assets.

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
- Existing settings migrate in place, and private API keys never enter the
  release package.

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
- TTS, microphone capture, screen capture, network streams, and background
  tasks now have bounded cleanup and timeouts.

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
