# Build the APK (about 5 minutes)
Requires: Node.js 18+, Android Studio (includes the Android SDK and Java).

    npm install
    npx cap add android
    npx cap sync android

Then either:
- Android Studio: `npx cap open android` -> Build > Build APK(s)
  (output: android/app/build/outputs/apk/debug/app-debug.apk)
- Command line: `cd android && ./gradlew assembleDebug`

Copy app-debug.apk to your phone, open it, and allow "Install unknown apps".

# Using it
Join the ESP32-CAR WiFi, open the app, keep IP 192.168.4.1.
If Android asks "This network has no internet, stay connected?", choose Yes.

# No-install option: build the APK online with GitHub (free)
1. Create a free GitHub account and a new repository.
2. Upload ALL files from this folder (including the hidden .github folder).
3. Open the repo's "Actions" tab -> "Build APK" -> wait ~5 minutes.
4. Open the finished run -> download "ESP32-Car-APK" (a zip containing app-debug.apk).
5. Send the APK (or the zip) on Discord. Friends install it by opening the file and allowing unknown apps.
