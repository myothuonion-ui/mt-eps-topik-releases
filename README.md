# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Android test channel

Current Android test build: **v1.1.22-test** (versionCode **13012**).

- [Download MT EPS TOPIK Android v1.1.22-test](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.22-test.apk)
- [SHA-256 checksum](https://raw.githubusercontent.com/myothuonion-ui/mt-eps-topik-releases/main/downloads/MT-EPS-TOPIK-Android-v1.1.22-test.apk.sha256)
- Package: `com.mteps.topik.dev`
- SHA-256: `b053beecc41b48c3f7cd460a94f30727db49736f4e03801af83175b902d4526d`
- Selected logo **C**: a compact book/conversation mark, Android adaptive/round icons and a 32 px app-header image.
- **Auto → Connection** accepts a BotFather token and channel link/ID. Add the bot as channel admin with permission to post.
- **Test channel delivery** lets you type a test message and choose **Send test**. It uses the bot/channel directly and requires no AI key. Current admin/post rights are rechecked. Confirmed delivery shows the Telegram message ID, channel and a link to the delivered message; errors remain visible beside the action.
- **Settings → Database** remains the original Content Bank sign-in. Telegram works independently of it, and database Sign Out keeps the bot connected.
- Gemini/NVIDIA keys are used for question generation and review. Telegram and Create now share the same Gemini model fallback list; temporary model failures try the next model.
- Production build, TypeScript, 61 application tests, Android package/version/signature checks and Windows CI passed. Actual Telegram channel posting remains unverified and should be confirmed through the app Test button.

This APK updates the existing test package using the same signing certificate and a higher versionCode. The app supports **Check for Updates** from Settings.

## Stable channel

The permanent-key stable release remains separate from the test package. Stable Android releases use package `com.mteps.topik` and the same permanent signing key for future updates.

## Release policy

- Never commit signing keys or API keys to this public repository.
- Test builds use package `com.mteps.topik.dev`; stable builds use `com.mteps.topik`.
- `version.json` points the updater to the public APK and checksum.
