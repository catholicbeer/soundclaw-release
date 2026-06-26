# SoundClaw dev release surface dev-sou-254-2026-06-25.1

promotion_gate: dev-release-surface
release_class: dev-release-surface
wdr_issue: SOU-254
intended_rtw_issue: SOU-222
not_rtw: true
not_stable: true
public_repo: catholicbeer/soundclaw-release
public_readiness_evidence: Linear SOU-254 public-readiness audit for dev-sou-254-2026-06-25.1
bundle: soundclaw-pi-release-dev-sou-254-2026-06-25.1.tar.gz
bundle_sha256: d77a5e22e4f7d6be7c2debe72c23c49f4753fbf229f126729316cd4300891fee

This dev/RC surface publishes the exact SOU-253 HTTP client-disconnect hotfix tuple approved by SOU-254 WDR so the user can test playback stability before deciding whether to accept it for SOU-222 RTW.

Source tuple:

- soundclaw: origin/dev@a59b6da5d825309427ad5427d3982202981cd32e; unchanged; issues SOU-254, SOU-222
- soundclaw-runtime: origin/dev@f675738367bb1b292d0b59c3b195584a2ffedcc5; issues SOU-253, SOU-254, SOU-222
- soundclaw-pi-kit: origin/dev@6eae2e9ab7ba174a56fa0bfebfd633c0ccd5f20c; unchanged; issues SOU-254, SOU-222
- soundclaw-skills: origin/dev@f46aec336f342b50248e76704bd0264fa756530f; unchanged; issues SOU-254, SOU-222
- soundclaw-asset-library: origin/dev@72400d11ff889191b48f3b71f241dafae28c0b37; unchanged; release label asset-library-main-72400d1

Candidate evidence:

- SOU-253 runtime fix is landed on pushed main and selected for SOU-254 WDR.
- Local WSL runtime daemon tests passed: cargo test -p soundclaw-runtime-daemon, 61 tests.
- Local WSL runtime staging passed for aarch64-unknown-linux-gnu and scrubbed build paths from release binaries.
- Local WSL bundle preflight passed for dev-sou-254-2026-06-25.1.
- This surface is not stable, not latest, and not RTW output.