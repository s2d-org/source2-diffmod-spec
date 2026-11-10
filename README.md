# sv2-diffmod-spec

A DiffMod holds plain diffs over decompiled sources.

This repo holds the SV2 DiffMod spec and game profiles.
Spec text is canonical in `spec/`.
The site mirrors the spec for reads.

## Tree

```text
spec/v1.md          # core spec, frozen per major version
profiles/deadlock.md  # reference profile, v1 scope
decompilers.md       # decompiler id registry
SPEC-CHANGELOG.md
site/index.html     # plain HTML, served at sv2-diffmod.org/spec
```

## Edit

If you change the spec, add a changelog line.
Never edit a frozen version.
Freeze each release with a tag such as `v1`.

## Serve

Deploy `site/` to `sv2-diffmod.org/spec`.
Pages deploys `site/` on push to `main`.
Fix the repo URL in `site/index.html` after first push.
