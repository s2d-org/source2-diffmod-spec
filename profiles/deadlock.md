# Deadlock Profile

Status is reference.
Game id is `deadlock`.
Steam app id is `1422450`.
This profile covers spec version 1.

## Game files

Game files live under `.../common/Deadlock/game`.
Decompile targets from `citadel/pak01_dir.vpk`.
If a raw file is absent there, read `core/pak01_dir.vpk` next.
Read the game build id from `citadel/steam.inf` keys `VersionDate` and `VersionTime`.

## Suffix map

The map has three rows.

| Cleartext suffix | Compiled suffix |
| --- | --- |
| `.css` | `.vcss_c` |
| `.xml` | `.vxml_c` |
| `.js` | `.vjs_c` |

Raw suffixes are `.cfg`.

## Decompile

Decompile with Source2Viewer-CLI in decompile mode.
Pin the decompiler per spec rule 11.

```sh
Source2Viewer-CLI -i citadel/pak01_dir.vpk -d -o /tmp/fresh -f panorama/styles/hud.vcss_c
```

## Compile

Take `panorama_config.txt` from the CSDK.
Run the CSDK resourcecompiler from the game dir.
Place outputs under an addon dir such as `citadel_addons/badge`.
Example VPK name: `pak75_dir.vpk`.

```sh
deadlock-resourcecompiler -v -f -game "Z:\modroot\game\citadel" "Z:\modroot\content\citadel_addons\badge\panorama\layout\hud.xml"
```

## Reference implementation

Modbox is the reference implementation for this profile.
Its repo lives at https://github.com/rszyma/deadlock-modbox.
