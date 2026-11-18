# TDS Expert data

Daily changes for the TDS Expert phone app, published by the TDS Expert sync every weekday.

- `manifest.json` says which version is current.
- `overlay.json` holds the changed data sheets, **locked**: it is sealed to the app's key and can only be opened with
  the app password. This repository contains no readable data.

The app checks this repository when it opens (at most every 3 hours). Do not edit the files by hand.
