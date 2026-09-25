# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.16-test**

- [Download MT EPS TOPIK Android v1.1.16-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.16-test.apk)
- Package: `com.mteps.topik.dev`
- SHA-256: `e795913873405aae2e686ed2451ab213a125c90c9d46fd7b9958e0c743ae02b6`
- Includes Telegram Channel automation, per-chapter question plans, Smart Full Chapter generation, scheduling, quiz polls, captions, and run history.

The Android app checks `version.json` and also supports **Check for Updates** from Settings.

## Stable channel

The existing permanent-key stable release remains separate from the test package. A stable Android release must use package `com.mteps.topik` and the same permanent signing key for every future update.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the in-app updater to a trusted public APK and checksum.
- Card template designs remain unchanged unless explicitly approved.
