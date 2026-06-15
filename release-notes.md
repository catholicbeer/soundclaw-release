# SoundClaw dev release surface dev-sou-207-2026-06-14.3

Release class: dev release surface / RC candidate, not RTW final, not stable, not latest.

Publication gate: SOU-207 main -> dev WDR plus public-readiness gate.

Source tuple:

- soundclaw: origin/dev@2108e4a20cec5977634bc2fce6bb8a973e4d0dcb; issues SOU-200, SOU-204, SOU-207
- soundclaw-runtime: origin/dev@00214d423f108ae2c434f90b17ab60112d5c4e3a; issues SOU-201, SOU-206, SOU-207
- soundclaw-pi-kit: origin/dev@73be4682c3a892108f4a94d8f51705923c08dc8d; issues SOU-203, SOU-207; unchanged from prior Wave 4 dev surface
- soundclaw-skills: origin/dev@4c3b417b1b021a46f76e4b7b262459b1814e142a; issues SOU-202, SOU-204, SOU-207; unchanged from prior Wave 4 dev surface
- soundclaw-asset-library: origin/dev@93d255df04ee1f690aa3630af19fddf2c49bfe15; issue n/a; unchanged
- soundclaw-release: derived publication surface; issue SOU-207

Selected default skills: manage-output show-outputs runtime-health soundclaw-version set-volume manual-policy

This dev surface supersedes dev-sou-204-2026-06-14.1 for SOU-205 RTW because it includes the SOU-206 runtime-owned proof hook:

- soundclawctl familiar prove-policy-block --scene <path> [--json]

This dev surface is intended to feed RTW testing. It is not a final public release.
