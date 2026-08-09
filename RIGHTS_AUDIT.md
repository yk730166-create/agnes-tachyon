# Rights Audit

Audit date: 1 August 2026. This is a practical project audit, not a substitute
for advice from a qualified intellectual-property lawyer.

| Material | Current status | Public distribution |
| --- | --- | --- |
| Original `src/` application code and UI | Claimed for y4x5lol under `PROJECT_LICENSE.txt` | Compiled release only; source stays private |
| Original installer/configuration/docs/tests | Claimed for y4x5lol | User docs are public; installer source, owner tools, and tests stay private |
| Original current companion icon | Claimed for y4x5lol | Yes |
| Setup Lab animation code/effects | Original code claimed for y4x5lol; sprite artwork is excluded | Yes for the code |
| Setup Lab Agnes source sheets and derived transparent clips | Third-party fan-project artwork; not claimed for y4x5lol | Only compressed runtime clips are included at the project owner's direction; permission not independently verified |
| Original code and procedural drawing used for the desktop Agnes companion | Claimed for y4x5lol; this does not claim the Agnes Tachyon name, identity, or official design | Yes, as original project material in this unofficial fan project |
| Original procedural companion dance music | Claimed for y4x5lol; synthesized at runtime with no samples | Yes |
| Python and Qt dependencies | Third-party open-source licenses | Yes, only while complying with each license |
| Applio runtime | Third-party MIT software plus its Terms of Use | Yes, license notices and terms must be preserved |
| Desktop Gremlin binary/code/assets | Kritzkingvoid/other rightsholders; no license found | **No verified permission** |
| Umamusume/Agnes names, design, official assets | Cygames and/or other rightsholders | Limited unofficial, non-commercial fan use only; no ownership transfer |
| Tachyon RVC model and index | Unknown source/license; voice/rightsholder interests | **No verified permission** |
| Groq-hosted Canopy Labs Orpheus speech | Third-party online model/service; no model weights or character recordings are bundled | API use only, under the providers' current terms |
| Microsoft speech used by `edge-tts` | Third-party online service and client library | API/service use and library distribution under their respective terms |
| Official or extracted recordings/sprites/sounds | Original publishers, artists, performers, and/or contributors | **No verified permission** unless separately licensed |

## Changes made from this audit

1. Added a narrow proprietary license for y4x5lol's original project
   materials. It deliberately excludes all third-party content.
2. Added specific creator attribution and rightsholder notices.
3. The public installer does not bundle the Desktop Gremlin executable, code,
   sounds, other character packs, or the unlicensed Tachyon voice model. The
   Setup Lab now includes only compressed transparent clips derived from the
   separately attributed Agnes action/emote sheets at the project owner's
   direction. Raw sheets remain private and are not installed or published.
4. Changed release defaults to use Groq-hosted Orpheus speech with automatic
   Edge neural-voice fallback and an original code-drawn desktop companion,
   with no external pet executable. Neither voice path is described as an
   official or exact character voice. A user can configure optional files
   locally only after obtaining the necessary rights.
5. Added the project license, notices, and this audit to installed copies.
6. Added two original procedural companion dance tracks with no sampled or
   extracted audio and added release checks that reject packaged media leaks.
7. Replaced the older flask desktop fallback with original procedural drawing
   and animation code. The desktop app mascot remains code-drawn. The guide
   control now plays separately attributed derived Agnes clips in place.

## What cannot be “made yours”

A notice cannot transfer somebody else's copyright, trademark, performer
rights, or model license. Only the actual rightsholder can grant or assign
those rights. To redistribute the excluded material, obtain a written license
that clearly permits copying, modification, bundling, and redistribution in
this specific project. Keep that written permission with the release records.

## Release rule

Only the output of the current allowlisted installer configuration should be
shared. Older setup builds that include `Companion` or `Voice` assets must be
treated as private audit artifacts and must not be redistributed.
