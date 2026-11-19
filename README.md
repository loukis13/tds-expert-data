# TDS Expert data

Daily changes for the TDS Expert phone app, published by the TDS Expert sync every weekday.

- `manifest.json` says which version is current.
- `overlay.json` holds the changed data sheets, **locked**: it is sealed to the app's key and can only be opened with
  the app password. This repository contains no readable data.
- `tools/seal-overlay.mjs` is the sealer the sync uses (one file, needs only Node.js), with the app's public key in
  `tools/public-key.txt`. The public key can lock data but cannot open it.

The app checks this repository when it opens (at most every 3 hours). Do not edit the files by hand.

- [Privacy policy](PRIVACY.md)
- [Support](SUPPORT.md)
