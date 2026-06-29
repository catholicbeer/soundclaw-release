# SoundClaw dev release surface dev-sou-234-2026-06-22.1

promotion_gate: dev-release-surface
release_class: dev-release-surface
wdr_issue: SOU-234
intended_rtw_issue: SOU-235
not_rtw: true
not_stable: true
public_repo: catholicbeer/soundclaw-release
public_readiness_evidence: Linear SOU-235 public-readiness audit for dev-sou-234-2026-06-22.1
bundle: soundclaw-pi-release-dev-sou-234-2026-06-22.1.tar.gz
bundle_sha256: 5f331cd1d1063c55b1736732b7fea3ceacdd234f539103b6ffc356f30c611546

This dev/RC surface publishes the exact Phase 1b operator-console tuple approved by SOU-234 WDR so SOU-235 RTW can fetch the candidate through the public release path.

Source tuple:

- soundclaw: origin/dev@890513721f7de65384c928d08424bc89ddffce1c; issues SOU-230, SOU-234, SOU-235
- soundclaw-runtime: origin/dev@378a36fe9868d080211a31a855200bc8d44a0125; issues SOU-231, SOU-234, SOU-235
- soundclaw-pi-kit: origin/dev@4109c5e0ed9aa607f8c8de778c1fbd98a4958e2b; issues SOU-232, SOU-234, SOU-235
- soundclaw-skills: origin/dev@adb6dd7ec011ff647cd6ce6d55c1e13620143f97; issues SOU-233, SOU-234, SOU-235
- soundclaw-asset-library: origin/main@93d255df04ee1f690aa3630af19fddf2c49bfe15; unchanged; release label asset-library-main-93d255d

Candidate evidence:

- SOU-234 WDR PASS promoted these refs to dev.
- SOU-234 target-Pi proof rendered Play/Stop controls, output selector, asset selector/list, global volume control, accepted play/stop/volume command envelopes, and restored volume to 100%.
- This surface is not stable, not latest, and not RTW output.




