# Rights Audit

Audit date: 28 July 2026. This is a practical project audit, not a substitute
for advice from a qualified intellectual-property lawyer.

| Material | Current status | Public distribution |
| --- | --- | --- |
| Original `src/` application code and UI | Claimed for y4x5lol under `PROJECT_LICENSE.txt` | Yes, under y4x5lol's chosen terms |
| Original installer/configuration/docs/tests | Claimed for y4x5lol | Yes |
| Original flask/speed lab icon | Claimed for y4x5lol | Yes |
| Original animated Lab Core mascot | Claimed for y4x5lol | Yes |
| Original procedural Lab Core dance music | Claimed for y4x5lol; synthesized at runtime with no samples | Yes |
| Python and Qt dependencies | Third-party open-source licenses | Yes, only while complying with each license |
| Applio runtime | Third-party MIT software plus its Terms of Use | Yes, license notices and terms must be preserved |
| Desktop Gremlin binary/code/assets | Kritzkingvoid/other rightsholders; no license found | **No verified permission** |
| Umamusume/Agnes names, design, official assets | Cygames and/or other rightsholders | Limited unofficial, non-commercial fan use only; no ownership transfer |
| Tachyon RVC model and index | Unknown source/license; voice/rightsholder interests | **No verified permission** |
| Official or extracted recordings/sprites/sounds | Original publishers, artists, performers, and/or contributors | **No verified permission** unless separately licensed |

## Changes made from this audit

1. Added a narrow proprietary license for y4x5lol's original project
   materials. It deliberately excludes all third-party content.
2. Added specific creator attribution and rightsholder notices.
3. Changed the public installer configuration so it does not bundle Desktop
   Gremlin, character sprites/sounds, or the unlicensed Tachyon voice model.
4. Changed release defaults to use the standard neural voice and the original
   Lab Core mascot, with no external pet executable. A user can configure
   optional files locally only after obtaining the necessary rights.
5. Added the project license, notices, and this audit to installed copies.
6. Added two original procedural Lab Core dance tracks with no sampled or
   extracted audio and added release checks that reject packaged media leaks.

## What cannot be “made yours”

A notice cannot transfer somebody else's copyright, trademark, performer
rights, or model license. Only the actual rightsholder can grant or assign
those rights. To redistribute the excluded material, obtain a written license
that clearly permits copying, modification, bundling, and redistribution in
this specific project. Keep that written permission with the release records.

## Release rule

Only the output of the current rights-safe installer configuration should be
shared publicly. Older setup builds that include `Companion` or `Voice` assets
must be treated as private audit artifacts and must not be redistributed.
