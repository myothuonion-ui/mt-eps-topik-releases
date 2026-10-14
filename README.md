# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.21-test** (versionCode **13011**).

- [Download MT EPS TOPIK Android v1.1.21-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.21-test.apk)
- Package: `com.mteps.topik.dev`
- SHA-256: `b1b2d84e8250d1861152ecd9745342af70b95f6565daded48b2cefeb59629553`
- **Auto → Connection** needs only a BotFather token and channel link/ID. Public links, public post links, @usernames, private t.me/c message links and -100… IDs are supported. Add the bot as a channel admin with post permission.
- Connection verifies the bot and admin rights without AI requests or automatically posting a message. Use **Send test** explicitly. Private invite-only links require the numeric channel ID or a private message link.
- **Settings → Database** signs into the original Content Bank. Telegram operates independently of that account; database Sign Out keeps the bot connected. There is no Telegram signup.
- Add Gemini/NVIDIA keys in API Keys when generating questions. They are synchronized separately and remain encrypted with the bot credentials in Vault.
- The selected B palette uses a smaller, simple MT monogram, updated Android density/adaptive icons and a 32 px contained app-header logo.
- Telegram Studio retains text and Mint Studio/Exam Sheet/Soft Panels images, editing with QA, custom branding, reading albums, Preview → Publish, global/per-plan pause and owner-wide daily caps.
- 53 application tests, rolled-back database ownership/rotation/grant checks, mobile/desktop connection/settings checks and 48/72 px launcher checks passed. Original Auth/Content Bank code and database counts are preserved. Android CI verified version, existing development signer, bundled assets and checksum. No real Telegram messages were sent during validation.

This APK updates the existing test package with the same signing certificate and a higher versionCode. The app supports **Check for Updates** from Settings.

## Stable channel

The permanent-key stable release remains separate from the test package. Stable Android releases use package `com.mteps.topik` and the same permanent signing key for future updates.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the updater to the public APK and checksum.
