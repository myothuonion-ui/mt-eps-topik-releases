# MT EPS TOPIK Releases

Public update and download repository for the MT EPS TOPIK desktop and Android apps.

## Stable channel

The app checks `version.json` once per day and also supports a manual **Check for Updates** action from Settings.

Current stable manifest: **v1.1.0**

Expected release assets for v1.1.0:

- `MT-EPS-TOPIK-Android-v1.1.0.apk`
- `MT-EPS-TOPIK-Windows-v1.1.0.exe`

## Release policy

- Android stable releases must be signed with the same permanent release keystore for every future update.
- Signing keys and API keys must never be committed to this public repository.
- Release binaries are distributed through GitHub Releases; `version.json` only points the app to those assets.
- Card template designs are outside this repository and remain locked unless explicitly approved for a future version.
