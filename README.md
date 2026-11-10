# source2-diffmod-spec

A DiffMod holds plain diffs over decompiled sources.

This repo holds the Source 2 DiffMod spec and game profiles.
Spec text is canonical in `spec/`.
The site mirrors the spec for reads.

## Reference implementation

Modbox is the reference implementation.
It lives at https://github.com/rszyma/deadlock-modbox.
Its mods hold example DiffMods.

## Tree

```text
spec/v1.md          # core spec, frozen per major version
profiles/deadlock.md  # reference profile, v1 scope
decompilers.md       # decompiler id registry
SPEC-CHANGELOG.md
site/index.html     # landing, served at source2-diffmod.org
site/spec/index.html  # spec, served at source2-diffmod.org/spec
```

## Edit

If you change the spec, add a changelog line.
Never edit a frozen version.
Freeze each release with a tag such as `v1`.

## Serve

Deploy `site/` to `source2-diffmod.org`.
The spec page lives at `/spec`.
Pages deploys `site/` on push to `main`.
