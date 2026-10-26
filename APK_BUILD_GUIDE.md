# CHANDAN WIZARD CHESS — APK Build Guide (GitHub)

**devloped by CHANDAN®**

Is project ko GitHub ke through APK banane ke liye sabhi zaroori files already setup kar di gayi hain:
1. `.github/workflows/build-apk.yml` — GitHub Actions auto-build workflow
2. `capacitor.config.json` — Mobile app configuration (`com.chandan.wizardchess`)
3. `public/manifest.json` — Web App Manifest (PWA / WebAPK support)
4. `public/assets/icon.svg` — HD App Icon

---

## Method 1: GitHub Actions Se Automatic APK Download (Sabse Aasan Tarika)

1. Is project ko apne **GitHub Repository** mein push karein (`main` ya `master` branch par).
2. GitHub par apni repository open karein aur **Actions** tab par click karein.
3. Wahan **"Build Chandan Wizard Chess APK"** workflow automatically start ho jayega.
4. Run complete hone par (green checkmark aane ke baad) us build par click karein.
5. Bottom mein **Artifacts** section mein aapko **`CHANDAN-WIZARD-CHESS-apk`** download link mil jayega!
6. Use download karein, unzip karein, aur apne Android phone par install kar lein!

---

## Method 2: PWABuilder / Bubblewrap Se 1-Click APK (Direct WebAPK)

Agar aapne website deploy ki hui hai (e.g. Vercel, Netlify, ya GitHub Pages):
1. [PWABuilder.com](https://www.pwabuilder.com) par jayein.
2. Apni live website ka URL dalein.
3. "Package for Stores" -> "Android" par click karein aur ready-to-install APK download karein.

---

## Method 3: Apne Computer Par Local APK Build Karna (Optional)

```bash
# 1. Install dependencies & build
npm install
npm run build

# 2. Capacitor install karein
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap add android
npx cap sync android

# 3. Android Studio mein open karein ya direct build karein
npx cap open android
# Ya terminal se:
cd android && ./gradlew assembleDebug
```
Output APK location: `android/app/build/outputs/apk/debug/app-debug.apk`
