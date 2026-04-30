# AGENTS.md

## Repo Purpose

`soundclaw-release` is the public SoundClaw release distribution repo.

It owns:
- generated public release manifests
- checksums
- public release notes
- installable release bundles
- source tuple metadata
- license and attribution files required for public consumption

It does not own:
- SoundClaw product development
- runtime source changes
- skill source changes
- asset library authoring
- Pi host provisioning implementation
- release-manager tooling
- private operational notes, topology, logs, memory, identity, or secrets

## Architecture Authority

For public release repo guardrails, consult the private SoundClaw architecture
repo, `soundclaw`.

Priority docs:
- `docs/public-release-repo.md` in `soundclaw`
- `docs/release-and-compatibility.md` in `soundclaw`
- `docs/git-usage.md` in `soundclaw`

If this repo conflicts with those architecture docs on ownership, provenance,
publication, or public-readiness questions, reconcile the architecture decision
before treating this repo as authoritative.

## Working Rules

- Treat this repo as derived output, not a working source repo.
- Only the documented release publication process should create normal release
  commits here.
- Do not make feature fixes, runtime fixes, skill fixes, asset fixes, or release
  generator fixes directly in this repo.
- If a public artifact is wrong, fix the owning private repo or release process
  first, then publish a new approved release output.
- Do not import private repo history into this repo.
- Do not add local paths, hostnames, credentials, secrets, private logs, private
  topology, or private operational notes.
- Keep every retained release traceable to its `manifest.env`,
  `checksums.txt`, `source-tuple.env`, release notes, and
  `LICENSE-ATTRIBUTION.md` when those files are part of the publication.
- Do not bypass the local commit hook except inside the documented publication
  workflow. The `SOUNDCLAW_PUBLIC_RELEASE_COMMIT=1` escape hatch is for the
  release process, not ordinary maintenance.
- Non-publication maintenance changes should stay small, reviewable, and tied
  back to the architecture repo guardrails.

## Validation

- For release payload changes, extract the bundle and run
  `sha256sum -c checksums.txt` from the extracted bundle root.
- Verify `manifest.env` and `source-tuple.env` name the approved source tuple.
- Review changed public files for local paths, hostnames, private topology,
  credentials, secrets, logs, and private operational notes.
- Confirm license and attribution files are present when publication contents
  require them.
- For repo-policy or hook changes, compare the behavior against
  `docs/public-release-repo.md` and
  `docs/templates/public-release-pre-commit.sh` in `soundclaw`.
- Report the checks performed and the result.

## Done Means

A change is done when:

- the release output is traceable to an approved stable tuple
- checksums validate for the published bundle contents
- public-readiness evidence is named or the maintenance-only scope is explicit
- no private-only information was introduced
- release mistakes were fixed at the owning source or generation layer, not by
  hand-editing generated output here

## Review Focus

When reviewing changes, look especially for:

- manual edits to generated release output
- missing or ambiguous source tuple metadata
- checksum or manifest mismatches
- private paths, hostnames, topology, logs, credentials, or secrets
- source changes that belong in a private development repo
- hook or policy drift from the architecture repo guardrails
