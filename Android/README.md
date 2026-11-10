# Paxx12 for Android

This Android project provides six separate installable Android applications for a Snapmaker U1 running Paxx12 mUlt1ACE firmware. Each APK opens one printer web interface in its own app window, uses the matching Paxx12 launcher name and icon, asks for the printer's IP address on first launch, and stores that address for later launches.

The saved printer IP can be changed at any time by tapping the IP button in the app toolbar. Changing it reloads that app using the new address.

## Apps and web routes

| Android app | Interface | Route |
| --- | --- | --- |
| Paxx12 · mult1ACE | MultiACE dashboard | `/multiace/` |
| Paxx12 · fluid | Fluidd printer interface | `/` |
| Paxx12 · Configuracion Paxx12 | Paxx12 firmware configuration | `/firmware-config` |
| Paxx12 · Pantalla Remota | Remote touchscreen | `/screen` |
| Paxx12 · Cámara Snapmaker | WebRTC camera stream | `/webcam/webrtc` |
| Paxx12 · Filament | Filament Manager | `/filament/` |

## Installable APKs

Open the corresponding APK from the `APKs` folder on the Android phone:

- `Paxx12-multiace-Android.apk`
- `Paxx12-fluidd-Android.apk`
- `Paxx12-configuracion-Android.apk`
- `Paxx12-pantalla-Android.apk`
- `Paxx12-camara-Android.apk`
- `Paxx12-filament-Android.apk`

Each app prompts for the U1's IPv4 address the first time it is opened. Tap the IP button in the app toolbar to change the saved address later. The IP is stored separately in each app and is not preconfigured in the APK.

Each app builds as a distinct APK with its own Android package ID and launcher icon. All six share the same WebView implementation and store the IP locally in that app's preferences.

