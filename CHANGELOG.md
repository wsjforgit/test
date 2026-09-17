# Changelog

All application releases are versioned separately from the empirical/inference model revisions.

## [1.0.0-rc2] - 2026-09-17

- Portable Windows x64 application packaged as a single EXE.
- Embedded browser UI served only on `127.0.0.1`.
- Windows Raw Input polling-rate sampling and physical CPI/DPI calibration.
- Empirical Delta Force sensitivity model v2.
- Three-round player-performance inference algorithm v3.
- HIP FOV measured model for 90/100/110/120.
- ADS FOV 90-120 treated as approximately flat from supplied measurements.
- MDV options limited to 1.33 and 1.78.
- H/V/ADS-H/ADS-V treated as linear specialty-test parameters.
- Added build-time version injection and `--self-test` for Windows CI validation.

## Historical

- RC1 build sandbox retained on branch `delta-sensitivity-rc1-build`.
