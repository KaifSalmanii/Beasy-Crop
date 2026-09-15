# Beasy Crop — Android APK

App id: `com.kaifsalmani.beasycrop`  
App name: **Beasy Crop**

The site (`index.html`) is wrapped with Capacitor as a native Android app (camera + storage permissions).

## Option A — Android Studio (easiest on your PC)

1. Install [Android Studio](https://developer.android.com/studio).
2. Open this folder: `android/`
3. Let Gradle sync.
4. Menu: **Build → Build Bundle(s) / APK(s) → Build APK(s)**
5. APK path: `android/app/build/outputs/apk/debug/app-debug.apk`

Install on phone: copy APK, enable **Install unknown apps**, tap to install.

## Option B — GitHub Actions

1. Repo Settings → Actions → allow workflows.
2. Push this branch or run **Build Android APK**.
3. Download the **BeasyCrop** artifact (`app-debug.apk`).

## Option C — Command line

```bash
npm install
mkdir -p www && cp index.html www/index.html
npx cap sync android
cd android && ./gradlew assembleDebug
```

APK: `android/app/build/outputs/apk/debug/app-debug.apk`

This is a **debug** APK (fine for personal use). For Play Store you need a signed **release** APK/AAB.
