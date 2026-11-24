# Pastel Clean — Wear OS 6 Watch Face (OnePlus Watch 4)

A clean, minimalist pastel watch face built with **Watch Face Format (WFF) Version 4** for **Wear OS 6 (Android 16 / API 36)**, sized natively for the **OnePlus Watch 4 (466×466 LTPO OLED)** display.

## Features
- **Top:** Current day name and date (e.g., `Tuesday, 24 Nov`) inside a soft pastel pill.
- **Middle:** Crisp 24-hour digital clock (`HH:mm`).
- **Bottom:** Live battery percentage with a dynamic pastel progress bar.
- **4 Customizable Pastel Themes** (long-press watch face → Customize):
  1. Cream & Sage (Light Pastel)
  2. Mint & Sky (Dark OLED)
  3. Lavender & Peach (Light Pastel)
  4. Rose & Sage (Dark OLED)
- **AOD: Time Only (Toggleable Option):** Enabled by default so Always-On Display shows **only the 24h clock** on a pure `#000000` black OLED background. Toggle **AOD: Time Only** OFF in the watch's Customize menu if you also want Date & Battery shown in AOD.

---

## How to Get the `.apk` File onto Your Computer

### Option A: Cloud Build via GitHub (No Android Studio Required)
1. Unzip this archive and upload the contents of `PastelCleanWatchFace` to a new GitHub repository.
2. Open the **Actions** tab in your GitHub repository → select **Build Wear OS 6 Watch Face APK** → click **Run workflow**.
3. Wait ~2 minutes, then click the completed run and download **`PastelCleanWatchFace-WearOS6-APK`** to your computer. Inside is your ready-to-install `app-debug.apk`.

### Option B: Build Locally in Android Studio
1. Unzip and open `PastelCleanWatchFace` in **Android Studio** (with Android 16 / API 36 SDK installed).
2. Click **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
3. Your APK is saved locally at:
   `app/build/outputs/apk/debug/app-debug.apk`

---

## Install the APK on Your OnePlus Watch 4
1. On your watch: **Settings → System → About → Versions** → tap **Build number** 7 times.
2. Go to **Settings → Developer options** → enable **ADB debugging** and **Wireless debugging**.
3. Run from your computer:
   ```bash
   adb pair <WATCH_IP>:<PAIRING_PORT>
   adb connect <WATCH_IP>:<DEBUG_PORT>
   adb install app-debug.apk
   ```
4. Long-press your watch screen → **Add watch face** → select **Pastel Clean**.
