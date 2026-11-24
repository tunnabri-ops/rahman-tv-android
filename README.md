# RAHMAN TV — Android App

RAHMAN TV is a live TV streaming app for Android: 300+ live channels, live
sports events, movies and Bangla dramas in a YouTube-style interface.

- **Live TV** — channels from the BDStreamHub admin panel, fetched live, so
  new channels and live events appear without reinstalling the app
- **Live Events** — currently running matches at the top of the feed
- **Movies** — public-domain films from Internet Archive (verified direct links)
- **Natok** — Bangla dramas from official YouTube channels (embedded player)
- **Player** — auto-detects the stream format: m3u8 (HLS), mpd (DASH),
  mp4 / mkv / webm (native)

## How it works

The app is a WebView wrapper around the RAHMAN TV web app
(`app/src/main/assets/rahman-tv.html`). The web app fetches the channel list
live from the admin panel's `channels.json`, so the channel list and live
events stay fresh while the app shell ships inside the APK.

## Install

Download the APK from the latest GitHub Actions run
(**RahmanTV-Android** artifact) and install it on your phone
(allow "Install unknown apps" once). Android 7.0+ required.

## Build it yourself

Push to `main` and GitHub Actions builds a debug APK automatically
(`.github/workflows/build-apk.yml`), or build locally:

```sh
gradle assembleDebug
# APK: app/build/outputs/apk/debug/app-debug.apk
```

Requires JDK 17 and the Android SDK (API 34).
