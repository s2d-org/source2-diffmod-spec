# Decompiler registry

Status is draft.
Each decompiler has a short id.
Builders read the id from the DiffMod header.
The id maps to one tool and one release line.
Same id plus same version MUST give byte-identical cleartext for same VPK input.

## Issue a new id

Send a pull request that adds one row.
Use a short lowercase slug, for example `mytool`.
Point at public tool sources.
Point at a tagged release with decompile tests.
Take the first free slug.
Never reuse a dead id.
Add a changelog line.

Builders MUST NOT fail a build on an unknown id.
Log a warning.

## Table

| id | tool | home |
| --- | --- | --- |
| `source2viewer-cli` | Source2Viewer-CLI | https://github.com/ValveResourceFormat/Source2Viewer |

Take the version from the upstream release tag, for example `20.1`.
Quote the tag verbatim.
It reads all Source 2 games.
The game list lives at s2v.app.
