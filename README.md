# Vistar for Samsung TV (TizenBrew)

An independently implemented Samsung-TV web app module inspired by the feature set described in the Android TV Vistaar project. It is not an Android APK port and does not reuse that project's source code.

## TizenBrew module

- Package type: `app`
- Entry point: `app/index.html`
- Module identifier (after publishing this repository): `lalit-op/Vistar`

In TizenBrew, add the repository identifier shown above using the catalogue's GitHub module option. If the catalogue requires a version/tag, use a published release tag rather than assuming `main` is cached immediately.

## Implemented in this build

- TV-oriented dark interface and remote-friendly buttons
- Home, Live TV, Free TV, HD, Guide, Favourites and Recently watched views
- Load an HTTP(S) M3U/M3U8 URL or import a local M3U file
- India free playlist shortcut (iptv-org community playlist)
- Channel category filtering and text search
- Favourites and recently watched channels in local storage
- HTML5 video playback with Fit / Zoom / Stretch, channel up/down and player overlay
- Optional XMLTV guide parsing, matched by playlist `tvg-id`
- Basic input validation and playback/network error messages

## Important limitations

- **Not yet tested on a physical Samsung TV.** Browser, firmware, remote key mapping, supported codecs and playback behaviour vary by model. TizenBrew module pages run as web pages; do not assume Samsung native `tizen` or `webapis` APIs are available inside this module.
- HLS, MPEG-TS, DASH, codecs, cross-origin requests (CORS), cookies and stream provider restrictions depend on the TV browser and source server. A playlist loading successfully does not guarantee its streams will play.
- HD classification is a best-effort name/URL heuristic, not a verified resolution measurement.
- XMLTV guide entries require matching `tvg-id` values. Timezone and programme presentation are basic.
- This build does **not** implement Jio OTP login, Jio account entitlement checks, private provider APIs, Widevine/DRM playback, session-cookie replay, or subscription channel resolution. Those require official/authorised integration documentation and a compatible playback path. Do not enter Jio credentials or OTPs into this app.
- The public India playlist is community-maintained; channels may be offline or change without notice.

## Run and verify

1. Publish the repository on GitHub.
2. In TizenBrew, use the GitHub module install flow with `lalit-op/Vistar`.
3. Open Vistar and test with a playlist you are authorised to use.
4. Test navigation, playback and Back behaviour on the target TV.

This repository has only received static/code-level checks in the development environment. A successful installation and playback test on the Samsung T5500 is still required before claiming device compatibility.

## Original project reference

The Android TV Vistaar README describes its own Android-specific implementation and features. This repository is a clean web implementation of selected user-facing concepts. The original repository currently states that no reuse licence has been chosen; therefore its source code is not copied here.
