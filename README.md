# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.17-test**

- [Download MT EPS TOPIK Android v1.1.17-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.17-test.apk)
- Package: `com.mteps.topik.dev`
- SHA-256: `7802f8ab4089fdd1788532afa3d095f4d3a52d770f56b5f440f329716c30c3a3`
- Each signed-in user can connect their own Telegram bot token and channel from the app.
- Telegram credentials and the existing Gemini API key are stored per account in encrypted Supabase Vault.
- Chapter plans support fixed or Smart counts, chapter ranges, and all/sequential/random chapter selection without a 60-question global cap.

The Android app checks `version.json` and also supports **Check for Updates** from Settings.

## Stable channel

The existing permanent-key stable release remains separate from the test package. A stable Android release must use package `com.mteps.topik` and the same permanent signing key for every future update.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the in-app updater to a trusted public APK and checksum.
- Card template designs remain unchanged unless explicitly approved.
