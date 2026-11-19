# TDS Expert data

Daily changes for the TDS Expert phone app, published by the TDS Expert sync every weekday.

- `manifest.json` lists the published files and holds the latest sync report, **locked**.
- `changes/` holds one file per sync run that changed data sheets, **locked**. Files are only added, never changed.
- Everything is sealed to the app's key and can only be opened with the app password. This repository contains no
  readable data.
- `tools/seal-overlay.mjs` is the sealer the sync uses (one file, needs only Node.js), with the app's public key in
  `tools/public-key.txt`. The public key can lock data but cannot open it.

The app checks this repository when it opens (at most every 3 hours). Do not edit the files by hand.

Installing the app: **https://loukis13.github.io/tds-expert-data/** (the page is in `docs/`). Android phones download
`TDS-Expert.apk` from the latest [release](https://github.com/loukis13/tds-expert-data/releases/latest); the release is
made by `.github/workflows/android-apk.yml` from the Expo build named in `release/android.json`.

- [Privacy policy](PRIVACY.md)
- [Support](SUPPORT.md)
