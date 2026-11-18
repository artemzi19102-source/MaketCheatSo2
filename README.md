# CART3R MOBILE

Standalone Android demo application. It does **not** connect to Standoff 2 or any other game, inspect or modify another app's memory, inject code, or bypass anti-cheat.

## Features
- Floating demo HUD using Android's overlay permission.
- Synthetic ESP-style boxes, labels and distances for an illustrative scene only.
- Basic root-presence heuristic (not a security-grade root detector).
- Native C++ module loaded through JNI.
- GitHub Actions workflow to build a debug APK.

## Build
Requirements: JDK 17, Android SDK platform 35, Build Tools 35.0.0, NDK 27.2.12479018, CMake 3.22.1, Gradle 8.9.

Run:
```bash
gradle --no-daemon :app:assembleDebug
```

APK output:
`app/build/outputs/apk/debug/app-debug.apk`

Or push this repository to GitHub, open **Actions**, choose **Build CART3R MOBILE APK**, then select **Run workflow**. Download the `CART3R-MOBILE-debug` artifact after the workflow succeeds.

## Overlay
Launch the app, grant "Display over other apps", then tap "Запустить демонстрационный HUD". Tap "Остановить HUD" to remove it. Android may restrict overlays depending on device vendor and OS settings.
