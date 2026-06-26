# SoundClaw dev release surface dev-sou-252-2026-06-25.1

promotion_gate: dev-release-surface
release_class: dev-release-surface
wdr_issue: SOU-252
intended_rtw_issue: SOU-222
not_rtw: true
not_stable: true
public_repo: catholicbeer/soundclaw-release
public_readiness_evidence: Linear SOU-252 public-readiness audit for dev-sou-252-2026-06-25.1
bundle: soundclaw-pi-release-dev-sou-252-2026-06-25.1.tar.gz
bundle_sha256: c598c767aa05d81f6e4dc163c50ed96aa6dd7047cfd29a4ec992e4d652900fdf

This dev/RC surface publishes the exact Phase 2 global-volume attenuation hotfix tuple approved by SOU-252 WDR so the user can test and decide whether to accept it for SOU-222 RTW.

Source tuple:

- soundclaw: origin/dev@a59b6da5d825309427ad5427d3982202981cd32e; unchanged; issues SOU-252, SOU-222
- soundclaw-runtime: origin/dev@6a4f08197d46b9e3e9d89a41c0b7016da07ddae0; issues SOU-250, SOU-252, SOU-222
- soundclaw-pi-kit: origin/dev@6eae2e9ab7ba174a56fa0bfebfd633c0ccd5f20c; unchanged; issues SOU-252, SOU-222
- soundclaw-skills: origin/dev@f46aec336f342b50248e76704bd0264fa756530f; issues SOU-251, SOU-252, SOU-222
- soundclaw-asset-library: origin/dev@72400d11ff889191b48f3b71f241dafae28c0b37; unchanged; release label asset-library-main-72400d1

Candidate evidence:

- SOU-252 WDR PASS promoted these refs to dev.
- Local WSL bundle preflight passed for dev-sou-252-2026-06-25.1.
- Runtime global volume now uses a 60 dB attenuation curve: 100% is unity, 0% is mute, and 18% maps to roughly 0.0035 amplitude.
- Operator UI slider max is 100%.
- This surface is not stable, not latest, and not RTW output.
