# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.20-test** (versionCode **13010**).

- [Download MT EPS TOPIK Android v1.1.20-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.20-test.apk)
- Package: `com.mteps.topik.dev`
- SHA-256: `d356e0c173aca94345c86544a29edc9784ca22a8943c1f9b58db978f88bbd155`
- Selected navy/turquoise MT logo and Balance shell; the manual Create flow and existing manual themes remain available.
- **Auto → Telegram Studio** separates generated Preview drafts from the publishing Queue. Edit the passage, question, choices, answer, Myanmar explanation and listening transcript; save to run QA again before publication.
- Choose Text or per-question Mint Studio, Exam Sheet and Soft Panels images. Customize logo image/text, footer, position and opacity. Long readings become an album of up to ten pages; each complete album counts as one question.
- Global/per-plan Pause, owner-wide daily caps and at least one-minute spacing apply to publication. Overdue posts are Held until explicitly rescheduled; Resume does not burst-send them.
- Gemini generates, NVIDIA reviews and Gemini performs final and image QA. Bundled HarfBuzz shaping fixes Myanmar text in server PNGs. Prepared images and audio remain private until posting.
- Users connect their own Telegram bot/channel and Gemini/NVIDIA keys. Credentials remain encrypted per account in Supabase Vault.
- 43 application tests, 13 database transaction checks, 30 browser checks, 21 rendered PNG pages and the deployed Edge render probe passed. Android CI verified package metadata, the existing test signer, bundled web assets and checksum. Live AI generation, TTS and Telegram delivery require the account connection and were not sent during validation.

The Android app checks `version.json` and supports **Check for Updates** from Settings. This APK updates the existing test package with the same signing certificate and a higher versionCode. Open **Auto → Connection**, save a plan, generate a preview, then publish approved drafts to a future queue. New plans start with automation disabled.

## Stable channel

The permanent-key stable release remains separate from the test package. A stable Android release must use package `com.mteps.topik` and the same permanent signing key for every future update.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the in-app updater to a trusted public APK and checksum.
