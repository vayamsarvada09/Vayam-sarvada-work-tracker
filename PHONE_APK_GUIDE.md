# 📱 Build Your Android APK From Your Phone (100% Free & Online)

You do **not** need a computer, Android Studio, or any technical setup. You can build and download your APK directly on your Android phone using **GitHub Actions** (a free cloud build system provided by GitHub).

---

## 📂 How to Download the Project ZIP on Your Android Phone

### Recommended: In-App "Project ZIP" Button
1. At the top left of the **Vayam Sarvada Tracker** app screen, tap the blue **"Project ZIP"** button (or **"Direct Link ↗"**).
2. Your phone will download **`vayam-sarvada-tracker.zip`** (around 900 KB).
3. Open your phone's **Files** or **Downloads** app and tap **Extract** on `vayam-sarvada-tracker.zip`.

### Folders Inside the Extracted ZIP:
- **`android/`**: Complete native Android project (with Gradle wrapper, AndroidManifest, and source files).
- **`.github/workflows/build-apk.yml`**: GitHub Actions automated cloud build workflow.
  *(Note for Android phones: Folders starting with a dot `.` like `.github` may be hidden by default in Google Files or Samsung My Files. To view it, tap the 3 dots in Files -> Settings -> toggle "Show hidden files". We have also included a visible copy in `github-workflows/` for your convenience!)*
- **`package.json`** & **`capacitor.config.json`**: Capacitor and dependency settings.
- **`src/`**: All application components, tracker logic, and assets.

---

## ☁️ How the Free Cloud Build Works

We have already added the automated build script (`.github/workflows/build-apk.yml`) to this project. 

As soon as this project is on your GitHub:
1. GitHub's free cloud server automatically boots up.
2. It sets up Node.js, Java, and Android SDK.
3. It compiles your app into an Android APK in about **2 minutes**.

---

## 📥 Step-by-Step: Downloading & Installing the APK on Your Phone

1. Open your repository on **[github.com](https://github.com)** in your phone browser (or using the GitHub mobile app).
2. Tap on the **Actions** tab (look for the play icon ▶️ or "Actions" in the top bar).
3. You will see a workflow run titled **"Build Android APK"** with a yellow spinning circle 🟡 (building) that turns into a green checkmark 🟢 (completed).
4. Tap on the completed build run.
5. Scroll down to the **Artifacts** section at the bottom of the page.
6. Tap on:
   👉 **`Vayam-Sarvada-Tracker-APK`**
7. Your phone will download the ZIP file.
8. Open your phone's **Files** or **Downloads** app, tap the downloaded file to extract `app-debug.apk`.
9. Tap **`app-debug.apk`** and select **Install**!
   *(If prompted "Install unknown apps", toggle "Allow from this source" on your phone).*

---

## ☁️ Using Google Drive In The App

Your app is now equipped with Google Drive integration:
1. **Save Schedule / Backup to Drive**:
   - Tap the **"Save to Drive"** button at the top left of the app.
   - On your Android phone, the share sheet will pop up.
   - Tap **Google Drive** ("Save to Drive") to instantly store your day's schedule, completion times, and video notes.
2. **Attach Google Drive Video Links**:
   - Tap the note icon on any Instagram Reels or YouTube Shorts slot.
   - Paste your Google Drive video link (e.g. `https://drive.google.com/file/...`).
   - A green **"Drive"** badge will appear on that slot. Tapping it opens your video file directly inside the **Google Drive app** on your phone!
3. **Quick Drive Access**:
   - Tap **"Drive App ↗"** in the top bar to open Google Drive anytime to copy video links or check drafts.
