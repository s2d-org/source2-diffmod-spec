# Deadlock Profile

Status is reference.
Game id is `deadlock`.
Steam app id is `1422450`.

## Sources

Game files live under `.../common/Deadlock/game`.
Decompile targets from `citadel/pak01_dir.vpk`.
If a raw file is absent there, read `core/pak01_dir.vpk` next.
Read the game build id from `citadel/steam.inf` keys `VersionDate` and `VersionTime`.

## Suffix map

The suffix map matches spec section 5.
Raw suffixes are `.cfg`.

## Compile

Take `panorama_config.txt` from the CSDK.
Run the compiler with the game dir as cwd.
Place outputs under an addon dir such as `citadel_addons/badge`.

Example decompile:

```sh
Source2Viewer-CLI -i citadel/pak01_dir.vpk -d -o /tmp/fresh -f panorama/styles/hud.vcss_c
```
