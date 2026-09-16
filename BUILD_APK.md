# Building the Android APK for Vayam Sarvada Tracker

This project is configured with a complete, production-ready Android Studio project inside the `android/` directory. All existing app functionalities, animations, sound cues, confettis, and local storage mechanisms are 100% preserved.

---

## 📁 Android Project Structure

The generated native project is located in `/android`:
```
/android
  ├── app/
  │   ├── build.gradle                              # Android build configuration & SDK targets
  │   └── src/
  │       └── main/
  │           ├── AndroidManifest.xml               # App name, package & permissions
  │           ├── assets/public/                    # Compiled React web application
  │           ├── java/com/vayamsarvada/tracker/    # MainActivity.java
  │           └── res/                              # App icons, splash screens, strings
  ├── build.gradle                                  # Top-level Gradle script
  ├── gradlew & gradlew.bat                         # Gradle wrapper scripts for Linux/Mac & Windows
  ├── settings.gradle
  └── variables.gradle
```

---

## 🚀 How to Build the APK

### Option 1: Using Android Studio (Recommended & Easiest)

1. **Download / Export the Project**:
   - In Google AI Studio, click the top right menu and select **Export to ZIP** (or push to GitHub).
   - Unzip the folder on your computer.

2. **Open the Android Project**:
   - Open **Android Studio** (download from [developer.android.com/studio](https://developer.android.com/studio) if needed).
   - Click **Open** (or *File > Open*).
   - Select the `android/` folder inside the unzipped project directory.

3. **Build the APK**:
   - In Android Studio, go to the top menu: **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
   - Android Studio will compile Gradle and build the APK.

4. **Locate Your APK**:
   - Once the build completes, a popup notification will say **"APKs generated successfully"**.
   - Click **locate** in the popup, or find the file directly at:
     ```
     android/app/build/outputs/apk/debug/app-debug.apk
     ```

---

### Option 2: Using the Command Line (Terminal / Command Prompt)

Prerequisites: Have Java (JDK 17 or 21) and Android SDK installed on your computer.

1. **Navigate into the `android` folder**:
   ```bash
   cd android
   ```

2. **Run the Gradle assemble command**:
   - On **macOS / Linux**:
     ```bash
     chmod +x gradlew
     ./gradlew assembleDebug
     ```
   - On **Windows** (PowerShell or CMD):
     ```cmd
     gradlew.bat assembleDebug
     ```

3. **Find your generated APK**:
   ```
   android/app/build/outputs/apk/debug/app-debug.apk
   ```

---

## 📲 How to Install the APK on Your Android Device

1. **Direct Transfer**:
   - Send `app-debug.apk` to your phone via WhatsApp, Telegram, Google Drive, or USB cable.
   - Open the file on your Android phone and tap **Install** (enable "Install unknown apps" if prompted).

2. **Via ADB (for developers)**:
   - Connect phone via USB with USB Debugging enabled:
     ```bash
     adb install android/app/build/outputs/apk/debug/app-debug.apk
     ```

---

## 🔄 Making Future Updates to the App

Whenever you modify any code in `src/` or `index.html`:
1. Run:
   ```bash
   npm run cap:sync
   ```
   *(This automatically runs `npm run build` and copies the updated web bundle into `android/app/src/main/assets/public`)*
2. Re-run `./gradlew assembleDebug` or click **Build > Build APK(s)** in Android Studio.
