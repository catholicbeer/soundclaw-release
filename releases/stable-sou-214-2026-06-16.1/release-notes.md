# SoundClaw stable release stable-sou-214-2026-06-16.1

Release class: final stable release.

This release promotes the Phase 1 Wave 5 performance and recovery validation tuple after SOU-213 WDR and SOU-214 RTW proof.

Source tuple:

- soundclaw: origin/stable@8654b9cb04c9adc10e98b9a57c3b79b5a2c6357a; issues SOU-210, SOU-213, SOU-214
- soundclaw-runtime: origin/stable@a8d31be0a3cc5541c0eea0c5e8b0cc5202812c8d; issues SOU-211, SOU-213, SOU-214
- soundclaw-pi-kit: origin/stable@1dd79a13b1185bf47ca69fd4f62730d195ebda9d; issues SOU-212, SOU-213, SOU-214
- soundclaw-skills: origin/stable@4c3b417b1b021a46f76e4b7b262459b1814e142a; unchanged for this wave
- soundclaw-asset-library: origin/stable@93d255df04ee1f690aa3630af19fddf2c49bfe15; unchanged for this wave

Selected default skills: browse-assets manage-output manual-policy play-asset runtime-health set-volume show-asset show-outputs soundclaw-onboarding soundclaw-version stop-playback validate-config

RTW evidence summary:

- Public dev candidate installed from the GitHub release-id path before stable promotion.
- Bundle checksum verification passed on the target Pi.
- Corrected Wave 5 proof used logical output nave and all command-status rows passed.
- Manual play p95/p99: 592ms / 592ms against 600ms / 1000ms targets.
- Manual stop p95/p99: 378ms / 378ms.
- Runtime proof command: 223ms; after service restart: 245ms.
- SOU-208 packaging-preflight evidence remains the prior completed packaging prerequisite.

Install asset:

- soundclaw-pi-release-stable-sou-214-2026-06-16.1.tar.gz
- sha256: 4b6565e0455a43eba39400689c12aad64aef72373b9a027e50626753dc83cd0d
