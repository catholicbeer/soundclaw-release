# soundclaw-release

Public SoundClaw release bundles, manifests, checksums, and install artifacts derived from approved stable builds.

This repo is a derived public distribution surface. It is not the source of
truth for product development, runtime source, skill source, Pi provisioning,
asset authoring, or release-manager tooling.

## Source of Truth

Architecture-owned release policy lives in the private `soundclaw`
architecture repo:

- `docs/public-release-repo.md`
- `docs/release-and-compatibility.md`
- `docs/git-usage.md`

Repo-local contributor rules live in `AGENTS.md`.

## Allowed Changes

Normal release commits should be produced only by the documented publication
workflow from an approved stable tuple.

Allowed release output includes:

- `manifest.env`
- `checksums.txt`
- `LICENSE-ATTRIBUTION.md`
- public release notes
- `source-tuple.env`
- installable release bundles under `releases/<release-id>/`

Do not hand-fix generated release output here. If an artifact is wrong, fix the
owning private repo or the release generation process, then publish a fresh
approved output.

## Local Hook

This repo uses a local pre-commit tripwire that rejects ordinary manual commits.
The release publication process may set `SOUNDCLAW_PUBLIC_RELEASE_COMMIT=1`
only while creating the intended publication commit.

The hook is a local safety check, not the real authority. Branch protections and
the architecture repo release policy are still the durable controls.

## Current Layout

- root `manifest.env`, `checksums.txt`, and `LICENSE-ATTRIBUTION.md` describe
  the current published release payload
- `releases/<release-id>/` retains the release-specific manifest, checksums,
  source tuple, release notes, license attribution, and bundle

## Validation

For a release bundle, extract it and run checksum validation from the extracted
bundle root:

```bash
sha256sum -c checksums.txt
```

Also confirm the release metadata names the approved source tuple and that no
private paths, hostnames, topology, logs, credentials, or secrets were added.
