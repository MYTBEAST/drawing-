# Drawing App (Android, Kotlin)

A simple native Android drawing app: draw with your finger, pick colors, adjust undo/clear, and save your drawing to the gallery.

## What's included
- Full Android Studio project (Kotlin, no external drawing libraries)
- `DrawingView.kt` — custom View handling touch drawing on a Canvas
- `MainActivity.kt` — wires up color swatches, undo, clear, save-to-gallery
- GitHub Actions workflow (`.github/workflows/build.yml`) that **automatically builds a debug APK** every time you push to `main`

## How to upload this to GitHub (from your phone)
1. Create a new repository on GitHub (e.g. via the GitHub app or mobile browser).
2. Use a file manager / GitHub mobile app / a Git client app to upload this entire `DrawingApp` folder, preserving the folder structure.
3. Push to the `main` branch.

## How to get the actual .apk file (no computer needed)
Once pushed to GitHub:
1. Go to your repo → **Actions** tab.
2. The "Build APK" workflow runs automatically on push (or trigger it manually via "Run workflow").
3. When it finishes (green check), open the workflow run → scroll to **Artifacts** → download `app-debug-apk`.
4. Unzip it — that's your installable `app-debug.apk`. Transfer it to an Android phone and open it (you'll need to allow "install from unknown sources").

## How to build it yourself in Android Studio (if you get to a computer)
1. Open Android Studio → **Open** → select the `DrawingApp` folder.
2. Let Gradle sync (it will auto-generate the Gradle wrapper).
3. Run ▶ on an emulator/device, or **Build → Build Bundle(s)/APK(s) → Build APK(s)**.

## Notes
- Minimum Android version: 8.0 (API 26).
- The Gradle wrapper jar isn't included (binary file) — Android Studio generates it automatically on first open, and the GitHub Actions workflow uses a hosted Gradle install instead, so no manual step is needed either way.
