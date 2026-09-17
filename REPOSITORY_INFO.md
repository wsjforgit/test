# Repository Information

- Remote repository: `wsjforgit/test`
- Default branch: `master`
- Historical RC1 branch: `delta-sensitivity-rc1-build`
- Current application version: `1.0.0-rc2`
- Current model versions: empirical `v2`, inference `v3`

## Version policy

Application versions use semantic-style prerelease numbering:

- Release candidates: `1.0.0-rc2`, `1.0.0-rc3`, ...
- Stable release: `1.0.0`
- Backward-compatible feature update: `1.1.0`
- Breaking redesign: next major version

Every application update must update:

1. `VERSION`
2. `VERSION.json`
3. `CHANGELOG.md`
4. the application-visible/exported version when applicable
5. GitHub source on `master`
6. Windows build artifact/release through GitHub Actions

Model revisions are tracked separately in `VERSION.json` so app version and algorithm version are not confused.
