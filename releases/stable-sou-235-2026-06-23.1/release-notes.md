# SoundClaw stable release stable-sou-235-2026-06-23.1

Release class: final stable release.

This release promotes the Phase 1a/1b operator-console tuple after SOU-234 WDR and SOU-235 RTW proof.

Source tuple:

- soundclaw: origin/stable@890513721f7de65384c928d08424bc89ddffce1c; issues SOU-230, SOU-234, SOU-235
- soundclaw-runtime: origin/stable@378a36fe9868d080211a31a855200bc8d44a0125; issues SOU-231, SOU-234, SOU-235
- soundclaw-pi-kit: origin/stable@4109c5e0ed9aa607f8c8de778c1fbd98a4958e2b; issues SOU-232, SOU-234, SOU-235
- soundclaw-skills: origin/stable@adb6dd7ec011ff647cd6ce6d55c1e13620143f97; issues SOU-233, SOU-234, SOU-235
- soundclaw-asset-library: origin/stable@93d255df04ee1f690aa3630af19fddf2c49bfe15; unchanged

Selected default skills: play-asset show-outputs runtime-health

RTW evidence summary:

- Public dev candidate installed from GitHub release id path: dev-sou-234-2026-06-22.1.
- Bundle checksum verification passed on the target Pi before setup mutation.
- Setup smoke test passed; runtime deploy, library promotion, and skill sync completed.
- Operator proof evidence is recorded in the SOU-235 Linear RTW stable promotion checkpoint.
- Operator console rendered controls check passed for play, stop, output selector, asset selector/list, volume, and /api/control/volume.
- Play accepted for asset ambience_grass on output nave and stop returned playback idle.
- Volume command accepted at 65%, then restored to 100%; final readyz returned ready and soundclaw-runtime.service stayed active.

Install asset:

- soundclaw-pi-release-stable-sou-235-2026-06-23.1.tar.gz
- sha256: 0d7d161b88cc1921d364601f4fd2dcdf0a7ab6ab84e8a7da610a9ee39184c394