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

## Compiled Python dependencies

The compiled applications include third-party packages under their own
licenses. Important direct dependencies include:

| Component | License |
| --- | --- |
| PySide6 and Shiboken6 | LGPL-3.0-only OR GPL-2.0-only OR GPL-3.0-only |
| cryptography | Apache-2.0 OR BSD-3-Clause |
| httpx | BSD-3-Clause |
| comtypes, keyboard, mss, pycaw, toml | MIT |
| OpenAI Python library | Apache-2.0 |
| NumPy | BSD-3-Clause |
| ONNX Runtime | MIT |
| PyAudioWPatch / PortAudio | MIT |
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

## Local music classification

YAMNet was created by Google. The packaged ONNX model is the unmodified-weight
conversion from Audio Magic, revision `f25b741c2f0bdc6d7e6db24b5fddda23347dbafd`.
The model and conversion are under Apache 2.0; AudioSet labels are CC BY 4.0.
The full model license is installed beside the model in `_runtime/assets/audio`.
The model checks short, in-memory speaker-audio buffers for music versus speech.
It does not transcribe audio or identify songs, and no sound is saved or uploaded.

- Original model: https://github.com/tensorflow/models/tree/master/research/audioset/yamnet
- ONNX conversion: https://huggingface.co/audiomagic/yamnet-onnx
- AudioSet ontology: https://research.google.com/audioset/ontology/index.html
- ONNX Runtime: https://github.com/microsoft/onnxruntime
- PyAudioWPatch: https://github.com/s0d3s/PyAudioWPatch

## Hosted speech service

The speech path calls Fish Audio S2.1 Pro Free with two selectable public
community model IDs: `e34bac0a56564919ae6be88f5c80bfe5` (shown in Options as
“Agnes - Normal”) and `cd5782d09b8e4c30941bfc431372ba63` (shown as
“Agnes - Adult”). Fish Audio reported both model pages as public when checked
on 20 August 2026. Public availability is not an ownership transfer or a promise
that every possible use is licensed. The model, generated voice, service, and
underlying performances remain subject to Fish Audio's terms and applicable
rightsholder rights. The installer contains no Fish model weights, sample audio,
API key, or official recording and does not claim this is an official voice.
Fish announced `s2.1-pro-free` as a fair-use developer tier and, when checked
on 13 August 2026, said the free window was extended through 31 August 2026.
Availability and terms can change; Agnes has no automatic paid TTS fallback.

- Model page: https://fish.audio/m/e34bac0a56564919ae6be88f5c80bfe5
- Model page: https://fish.audio/m/cd5782d09b8e4c30941bfc431372ba63
- Fish Audio API documentation: https://docs.fish.audio/api-reference/introduction
- Fish Audio terms: https://fish.audio/terms

## Online services

Fish Audio, Groq, and any configured OpenAI or Gemini service are external
services governed by their own current terms. API access does not transfer
ownership of service models, brands, voices, or third-party input content.
