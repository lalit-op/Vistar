# Vistar

Vistar is a TV-first streaming interface packaged as a **TizenBrew app module** for compatible Samsung Smart TVs.

## Current prototype features

- Remote-control navigation and visible focus states
- M3U playlist loading from a user-supplied URL
- Channel groups/categories, search, favourites and recently played
- HTML5 video playback with clear playback error messages
- Local settings saved in browser storage
- Optional public India playlist shortcut

## Install through TizenBrew

1. Publish this repository on GitHub.
2. In TizenBrew, add the module using the repository identifier:
   `lalit-op/Vistar`
3. Launch **Vistar** from TizenBrew.

TizenBrew app modules are hosted web pages. This project therefore uses standard web APIs and does **not** assume that Samsung's native `tizen` or `webapis` objects are available inside the module.

## Configure a playlist

Open **Settings** and paste an M3U/M3U8 playlist URL that you are authorized to access. The built-in India playlist shortcut points to the community-maintained iptv-org India playlist:

`https://iptv-org.github.io/iptv/countries/in.m3u`

Playlist hosts must allow browser CORS requests for remote loading to work. Some streams may not play because of codec, DRM, CORS, network, or TV browser limitations. This app does not bypass subscriptions, DRM, or provider access controls.

## Important compatibility note

This is an initial TizenBrew web-module build, not a native Samsung TV application. HTML5 video support varies by TV model, firmware, stream format, and codec. It must be tested on the target Samsung T5500 TV before claiming device-level compatibility.

## Project status

Prototype foundation: manifest and TV interface. Jio account login, subscription entitlement filtering, provider-specific stream resolution, DRM playback, and a real EPG feed are not implemented in this Tizen build. Those require authorized provider integration and valid service/API access.
