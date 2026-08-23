# Proxy Cloud — Android app releases

Signed APK releases for the **Proxy Cloud** Android VPN client. This repository
holds binaries only — the application source is private.

Proxy Cloud routes selected apps on the device through a mesh of relay nodes
over WebSocket, QUIC or a direct peer-to-peer link, and falls back to a direct
connection whenever that is faster. It is a per-app VPN: only the apps you pick
go through the tunnel, everything else keeps using the normal network.

## Install

Pick **one** of these and stay with it — the site build and the Play build are
separate applications, and Android will only let one of them hold the VPN at a
time.

| Source | Package | Notes |
| :--- | :--- | :--- |
| [Releases here](../../releases/latest) | `cloud.proxyapp.app` | Same signed APKs the app's own updater serves |
| [proxyapp.cloud/get](https://proxyapp.cloud/get) | `cloud.proxyapp.app` | The primary channel, with a mirror for users in Russia |
| Google Play (internal testing) | `cloud.proxyapp.android` | Ask for an invite |

Two APKs per release, one per ABI: `arm64-v8a` for anything current,
`armeabi-v7a` for older 32-bit devices. If you are unsure, take `arm64-v8a`.

Installing is manual: download, then allow installation from this source when
Android asks. The app does not install updates by itself — it checks for one and
opens the download page.

## Updates

The app has its own update channel and keeps using it regardless of where you
installed from, so a release published here is not the only way you hear about a
new version.

## Verifying a download

Every APK here is the byte-identical artefact published to the project's own
distribution channel — built and signed on a workstation, never in CI, so the
signing key is not held by any build service. Compare the SHA-256 of a file
downloaded here with the one from `https://dl.proxyapp.cloud/manifest.json` if
you want to check that for yourself.

## Links

- Download page and install instructions: <https://proxyapp.cloud/get>
- Privacy policy: <https://proxyapp.cloud/privacy>
- Terms: <https://proxyapp.cloud/offer>
