# SoundClaw dev release surface dev-sou-248-2026-06-25.1

promotion_gate: dev-release-surface
release_class: dev-release-surface
wdr_issue: SOU-248
intended_rtw_issue: SOU-222
not_rtw: true
not_stable: true
public_repo: catholicbeer/soundclaw-release
public_readiness_evidence: Linear SOU-222 public-readiness audit for dev-sou-248-2026-06-25.1
bundle: soundclaw-pi-release-dev-sou-248-2026-06-25.1.tar.gz
bundle_sha256: 18c98833e2dd207a549327377acdc017ad550d55e7b99eeeb008bab6b8849a9c

This dev/RC surface publishes the exact Phase 2 global-volume hotfix tuple approved by SOU-248 WDR so SOU-222 RTW can fetch the candidate through the public release path.

Source tuple:

- soundclaw: origin/dev@a59b6da5d825309427ad5427d3982202981cd32e; unchanged; issues SOU-248, SOU-222
- soundclaw-runtime: origin/dev@d2bd384bf56f1ba437d33c0bf412e3b48f2de8dd; issues SOU-246, SOU-248, SOU-222
- soundclaw-pi-kit: origin/dev@6eae2e9ab7ba174a56fa0bfebfd633c0ccd5f20c; unchanged; issues SOU-248, SOU-222
- soundclaw-skills: origin/dev@5daa0ecc124e232b13ab95fef9aad16ae40d14ec; issues SOU-247, SOU-248, SOU-222
- soundclaw-asset-library: origin/dev@72400d11ff889191b48f3b71f241dafae28c0b37; unchanged; release label asset-library-main-72400d1

Candidate evidence:

- SOU-248 WDR PASS promoted these refs to dev.
- Local WSL bundle preflight passed for dev-sou-248-2026-06-25.1.
- Public-readiness scans found no local paths or obvious credential patterns in retained candidate output.
- This surface is not stable, not latest, and not RTW output.
