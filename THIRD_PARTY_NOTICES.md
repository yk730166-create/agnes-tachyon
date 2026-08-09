# Third-Party Notices

Audit date: 1 August 2026.

This project contains or can interoperate with third-party material. Nothing
in `PROJECT_LICENSE.txt` claims that material for y4x5lol.

## Umamusume and Agnes Tachyon

Agnes Tachyon, Umamusume: Pretty Derby, associated names, character designs,
official audiovisual material, and game content belong to Cygames and/or their
respective rightsholders. The official terms state that service text, images,
programs, and other information remain with Cygames or the relevant
rightsholder. The official derivative-work guidelines permit limited fan
activity but exclude, among other things, rights-infringing content and
commercial use beyond ordinary fan activity.

This software is an unofficial, non-commercial fan project and is not endorsed
by Cygames.

- Official portal: https://umamusume.jp/
- Derivative-work guidelines: https://umamusume.jp/derivativework_guidelines/
- Terms and rights information: https://umamusume.jp/terms/

## Desktop Gremlin

Desktop Gremlin was created by Kritzkingvoid (Kurt Velasco):

- Repository: https://github.com/KurtVelasco/Desktop_Gremlin
- Support: https://ko-fi.com/kritzkingvoid

The repository did not declare a software license when checked on 27 July
2026. A public repository and an author credit do not by themselves grant
permission to copy or redistribute its code, binary, sprites, sounds, or
documentation. Those materials remain under their respective authors' and
rightsholders' rights.

At the project owner's direction, the personal, non-commercial installer now
includes the compiled Desktop Gremlin runtime plus only its Agnes character
pack, matching sounds, and real Agnes icon. It deliberately excludes every
other character pack. The public Setup Lab contains compressed WebM and Ogg
previews derived from the same Agnes assets; raw PNG sheets remain outside the
public repository. These files are third-party fan-project material and are
not claimed as y4x5lol's original artwork. Obtain written permission before
redistributing them beyond uses allowed by the applicable rightsholders.

## Tachyon voice-conversion files and voice identity

The local files named `Tachyon.pth` and
`added_IVF1267_Flat_nprobe_1_Tachyon_v2.index` arrived without a license or
verifiable provenance statement. No permission was found to redistribute
them. They are not owned by y4x5lol merely because they are stored in this
folder.

The voice, performances, recordings, likeness, and other personal rights of a
voice performer remain with that performer and/or the applicable
rightsholders. The rights-safe public setup does not contain these model files.
Do not advertise converted speech as an official or exact performer's voice,
and do not distribute the model or generated impersonations without the
necessary permissions.

## Applio

Applio is Copyright (c) 2026 AI Hispano and is distributed under the MIT
License. Its Terms of Use require users to own or have explicit permission for
audio/material processed with it. Applio's license covers Applio software, not
an independently obtained character voice model or its training data.

- Source and license: https://github.com/IAHispano/Applio
- Terms: https://github.com/IAHispano/Applio/blob/main/TERMS_OF_USE.md

## Compiled Python dependencies

The compiled applications include third-party packages under their own
licenses. Important direct dependencies include:

| Component | License |
| --- | --- |
| PySide6 and Shiboken6 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only |
| cryptography | Apache-2.0 OR BSD-3-Clause |
| edge-tts | LGPL-3.0 |
| httpx | BSD-3-Clause |
| keyboard, mss, toml | MIT |
| OpenAI Python library | Apache-2.0 |
| NumPy | BSD-3-Clause |
| Pillow | HPND |
| psutil | BSD-3-Clause |
| pygame | LGPL |
| pywin32 | PSF |
| sounddevice | MIT |
| truststore | MIT OR Apache-2.0 |
| PyInstaller bootloader | GPL-2.0-or-later with bootloader exception |

Package licenses apply to those components only. Their inclusion does not
transfer their copyrights to y4x5lol. Source and corresponding license texts
are available from each package's official project page and installed package
metadata.

## Hosted speech services

The default expressive speech path calls the Groq-hosted
`canopylabs/orpheus-v1-english` model by Canopy Labs. When that request cannot
be completed, Agnes automatically falls back to the Microsoft speech service
used by `edge-tts`. These are third-party online services governed by their
providers' current terms; the installer does not contain their hosted model
weights or training data.

The included voice choices are general service voice personas. They are not
advertised as an official or exact Agnes Tachyon voice, and the public build
does not bundle official recordings or an unlicensed character voice model.

- Groq Orpheus documentation: https://console.groq.com/docs/text-to-speech/orpheus
- Groq terms: https://groq.com/terms-of-use/
- Microsoft services agreement: https://www.microsoft.com/servicesagreement/

## Online services

Groq, the Canopy Labs Orpheus model hosted there, Microsoft speech services
used by `edge-tts`, and any configured OpenAI or Gemini service are external
services governed by their own current terms. API access does not transfer
ownership of service models, brands, voices, or third-party input content.
