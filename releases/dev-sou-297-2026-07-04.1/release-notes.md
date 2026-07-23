# dev-sou-297-2026-07-04.1

Dev/RC release surface for SOU-297. This is not stable, final, or RTW-approved.

This candidate adds UTF-8-safe asset-library publication and supported index
repair, preserves index permissions during atomic replacement, keeps valid
assets available during bounded library degradation, and pins the Runtime
service to `C.UTF-8` on legacy-locale hosts.

Target-Pi WDR proof passed repair, repeat repair, restart, Unicode playback,
ASCII playback, source preservation, and reinstall checks before this exact
tuple was promoted to `dev`.
