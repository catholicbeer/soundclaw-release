# SoundClaw stable public release stable-sou-205-2026-06-14.1

Release class: final public release / stable.

Publication gate: SOU-205 RTW final after Wave 4 dev release live proof.

RTW evidence:

- public RTW candidate: dev-sou-207-2026-06-14.3
- RTW issue: SOU-205
- target host: honcho@SoundClaw
- install proof: public GitHub asset fetched, tarball digest verified, bundle checksums verified, bootstrap/smoke-test passed, runtime deployed, library promoted, skills synced, setup evidence recorded
- policy proof: `policy hold`, `familiar prove-policy-block --scene`, `policy status`, and `runtime push-events` proved `manual_hold_active` and `automatic_action_blocked` without playback, followed by `policy clear` and `policy resume` back to normal

Stable source tuple:

- soundclaw: origin/stable@2108e4a20cec5977634bc2fce6bb8a973e4d0dcb; issues SOU-200, SOU-204, SOU-207, SOU-205
- soundclaw-runtime: origin/stable@00214d423f108ae2c434f90b17ab60112d5c4e3a; issues SOU-201, SOU-206, SOU-207, SOU-205
- soundclaw-pi-kit: origin/stable@73be4682c3a892108f4a94d8f51705923c08dc8d; issues SOU-203, SOU-207, SOU-205
- soundclaw-skills: origin/stable@4c3b417b1b021a46f76e4b7b262459b1814e142a; issues SOU-202, SOU-204, SOU-207, SOU-205
- soundclaw-asset-library: origin/stable@93d255df04ee1f690aa3630af19fddf2c49bfe15; unchanged
- soundclaw-release: derived publication surface; issue SOU-205

Selected default skills: manage-output show-outputs runtime-health soundclaw-version set-volume manual-policy

This stable release includes the Wave 4 runtime-owned manual policy surface and Familiar automatic-action block proof hook:

- `soundclawctl policy status`
- `soundclawctl policy hold`
- `soundclawctl policy clear`
- `soundclawctl policy resume`
- `soundclawctl familiar prove-policy-block --scene <path> [--json]`
