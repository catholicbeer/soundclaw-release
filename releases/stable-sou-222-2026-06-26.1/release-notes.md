# SoundClaw stable release stable-sou-222-2026-06-26.1

Release class: final stable release.

This release promotes the Phase 2 global-volume attenuation and SOU-253 HTTP client-disconnect hotfix tuple after SOU-254 WDR and SOU-222 RTW acceptance.

Source tuple:

- soundclaw: origin/stable@a59b6da5d825309427ad5427d3982202981cd32e; issue SOU-222
- soundclaw-runtime: origin/stable@f675738367bb1b292d0b59c3b195584a2ffedcc5; issues SOU-253, SOU-254, SOU-222
- soundclaw-pi-kit: origin/stable@6eae2e9ab7ba174a56fa0bfebfd633c0ccd5f20c; issue SOU-222
- soundclaw-skills: origin/stable@f46aec336f342b50248e76704bd0264fa756530f; issue SOU-222
- soundclaw-asset-library: origin/stable@72400d11ff889191b48f3b71f241dafae28c0b37; release label asset-library-main-72400d1

RTW evidence summary:

- Accepted dev release surface: dev-sou-254-2026-06-25.1.
- User reported the SOU-253 playback crash appeared fixed and approved proceeding to RTW.
- Bundle checksum verification passed on the target Pi before setup mutation for the accepted dev candidate.
- Setup smoke test passed; runtime deploy, library promotion, and skill sync completed for the accepted dev candidate.
- Live API showed runtime running, global volume range 0-100, output wide on channels 1-4, and output trees on channels 9-10.
- Stable lineage guard passed for all behavior repos before stable promotion.
- This final stable bundle passed WSL bundle preflight and public-readiness scanning.

Install asset:

- soundclaw-pi-release-stable-sou-222-2026-06-26.1.tar.gz
- sha256: 096cb64a59d11889afc4bdadfd910fe9fa0ea2cb34b544bac675484ae68f953a