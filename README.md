# Delta Force Sensitivity Tester / 三角洲灵敏度测试器

Windows x64 local sensitivity calibration and specialty-test application for Delta Force.

## Current release

- App: **1.0.0-rc2**
- Empirical model: **v2**
- Player-performance inference: **v3**
- Supported MDV: **1.33 / 1.78**
- ADS mode: **MDV only**

The application runs locally, listens only on `127.0.0.1`, and does **not** inject into or read the Delta Force game process.

## Repository layout

- `VERSION` / `VERSION.json`: application and model version metadata
- `CHANGELOG.md`: version history
- `REPOSITORY_INFO.md`: fixed remote/version policy
- `build/source_<version>.zip.b64`: canonical build source bundle
- `source/`: readable source snapshot automatically synchronized by CI after a successful build
- `.github/workflows/build-windows.yml`: Windows build, self-test, artifact and release pipeline

## Build

Requires Go 1.23+.

```powershell
$version = (Get-Content VERSION -Raw).Trim()
go test ./...
$env:GOOS = "windows"
$env:GOARCH = "amd64"
go build -trimpath -ldflags "-s -w -X main.appVersion=$version" -o "dist/DeltaSensitivityTester_$version`_win-x64.exe" .
```

## Windows self-test

```powershell
.\dist\DeltaSensitivityTester_1.0.0-rc2_win-x64.exe --self-test
```

Expected prefix:

```text
SELF_TEST_OK
```

## Versioning

See `REPOSITORY_INFO.md` and `CHANGELOG.md`.
