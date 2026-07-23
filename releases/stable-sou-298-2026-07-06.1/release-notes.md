# stable-sou-298-2026-07-06.1

Final public release approved by RTW issue SOU-298 from the exact public
dev/RC `dev-sou-297-2026-07-04.1`.

This release adds UTF-8-safe asset-library publication and supported index
repair, preserves index metadata during atomic replacement, isolates
unavailable assets without disabling valid playback, and pins the Runtime
service to `C.UTF-8` on legacy-locale hosts.

RTW proved canonical GitHub download and checksum verification, install and
reinstall identity, Unicode playback, bounded unavailable-asset degradation,
valid-asset continuity, restart recovery, rollback, and source preservation.
