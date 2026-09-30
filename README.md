# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.19-test** (versionCode **13009**).

- [Download MT EPS TOPIK Android v1.1.19-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.19-test.apk)
- Package: `com.mteps.topik.dev`
- SHA-256: `bd7fa493ce2cc496faff058d8544c4966a4df2dc16eea1c9680f6b8aa05807bd`
- Add range preserves existing chapter settings; Apply template and clearing numeric fields are covered by UI interaction tests.
- Multiple daily start times, unlimited planned posts, post gaps, and sequential chapter continuation are supported without a 60-question global cap.
- Output choices: Telegram Quiz, My Template, or Auto. Template cards contain four choices plus a spoiler answer and Myanmar explanation.
- Gemini generates, NVIDIA independently reviews the complete chapter source, and Gemini performs final QA. Card layout is reviewed before queueing; prepared images/audio remain private on the server until posting.
- Users connect their own Telegram bot token, channel ID, Gemini key, and NVIDIA reviewer key. Credentials remain encrypted per account in Supabase Vault.
- 28 tests and Android CI passed; package metadata, stable test signing, bundled web assets, and checksum were verified. The backend migration/functions are deployed and minute cron returns HTTP 200. Live AI/Telegram delivery still requires an account connection and an integration check.

The Android app checks `version.json` and supports **Check for Updates** from Settings. To replace an earlier 1.1.19-test build, download this corrected APK directly; its higher versionCode permits updating the existing test package.

## Stable channel

The permanent-key stable release remains separate from the test package. A stable Android release must use package `com.mteps.topik` and the same permanent signing key for every future update.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the in-app updater to a trusted public APK and checksum.
