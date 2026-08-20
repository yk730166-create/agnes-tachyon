# Rights Audit

Audit date: 1 August 2026. This is a practical project audit, not a substitute
for advice from a qualified intellectual-property lawyer.

| Material | Current status | Public distribution |
| --- | --- | --- |
| Original `src/` application code and UI | Claimed for y4x5lol under `PROJECT_LICENSE.txt` | Compiled release only; source stays private |
| Original installer/configuration/docs/tests | Claimed for y4x5lol | User docs are public; installer source, owner tools, and tests stay private |
| Current Agnes character icon | Kritzkingvoid/other character rightsholders; not claimed for y4x5lol | Included at the project owner's direction |
| Setup Lab animation code/effects | Original code claimed for y4x5lol; sprite artwork is excluded | Yes for the code |
| Setup Lab Agnes source sheets and derived transparent clips | Third-party fan-project artwork; not claimed for y4x5lol | Only compressed runtime clips are included at the project owner's direction; permission not independently verified |
| Bundled Desktop Gremlin Agnes model, animation sheets and matching sounds | Kritzkingvoid/other rightsholders; no ownership claimed by y4x5lol | Included at the project owner's direction for personal, non-commercial use |
| Python and Qt dependencies | Third-party open-source licenses | Yes, only while complying with each license |
| Desktop Gremlin binary/code/assets | Kritzkingvoid/other rightsholders; no license found | Included at the project owner's direction; **permission not independently verified** |
| Umamusume/Agnes names, design, official assets | Cygames and/or other rightsholders | Limited unofficial, non-commercial fan use only; no ownership transfer |
| Fish Audio model `e34bac0a56564919ae6be88f5c80bfe5` | Public third-party community model/service; no model weights, sample audio, API keys, or official recordings are bundled | API use only, under Fish Audio's terms and applicable voice/rightsholder rights |
| Official or extracted recordings/sprites/sounds | Original publishers, artists, performers, and/or contributors | **No verified permission** unless separately licensed |

## Changes made from this audit

1. Added a narrow proprietary license for y4x5lol's original project
   materials. It deliberately excludes all third-party content.
2. Added specific creator attribution and rightsholder notices.
3. At the project owner's explicit direction, the installer now bundles the
   Desktop Gremlin executable and a strictly curated Agnes-only character pack,
   including her matching animations, sounds and icon. Other character packs,
   the unlicensed Tachyon voice model, and raw website sprite sheets remain out
   of the public repository.
4. Release defaults use the bundled real Agnes model and the linked Fish Audio
   community voice through its API. No unrelated speech fallback is presented
   as Agnes, and the voice is not described as an official release.
5. Added the project license, notices, and this audit to installed copies.
6. The two tray music dances use the matching Agnes sound files and stop when
   their tracks finish. The Setup Lab uses compressed previews of those tracks.
7. Replaced the visible procedural desktop fallback and generated character
   marks with the bundled real Agnes model and icon. A procedural emergency
   renderer remains code-only but is hidden whenever the real bundle is valid.

## What cannot be “made yours”

A notice cannot transfer somebody else's copyright, trademark, performer
rights, or model license. Only the actual rightsholder can grant or assign
those rights. To redistribute the excluded material, obtain a written license
that clearly permits copying, modification, bundling, and redistribution in
this specific project. Keep that written permission with the release records.

## Release rule

Only the output of the current exact allowlisted installer configuration should
be shared. It permits the Agnes-only Companion bundle and rejects every other
character pack, voice model, source tree, owner tool and build artifact.
