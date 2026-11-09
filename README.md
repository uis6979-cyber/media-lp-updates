# Media LP — update manifest

This public repository holds only `version.json`, the file Media LP reads to know whether a
newer version exists. The app source code stays private.

`version.json`:

```json
{
  "versionCode": 2,            // integer; must be > the installed versionCode to notify
  "versionName": "1.1",        // shown to the user
  "notes": "What's new…",      // optional changelog shown in the dialog
  "url": "https://t.me/..."    // where the user downloads the new APK (e.g. a Telegram post)
}
```

To release an update: build the signed APK, share it (e.g. on Telegram), then bump
`versionCode`/`versionName` here and set `url` to the download link.
