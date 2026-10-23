# Ludo Adda (Android app)

Is folder mein Ludo Adda game ka Android project hai (Capacitor). APK GitHub par apne aap banta hai,
aapke phone ya computer par Android Studio ki zaroorat nahi.

## APK banane ke steps

1. github.com par free account banao aur ek **naya repository** banao (naam: `ludo-adda`).
2. Is folder ki saari files us repository mein upload karo (Add file > Upload files).
   `.github` folder bhi upload hona chahiye. Agar mobile par ho to `.github/workflows/build-apk.yml`
   ko "Create new file" se bana kar content paste karo.
3. Repository mein **Actions** tab kholo > **Build APK** > **Run workflow**.
4. Lagbhag 5 se 10 minute baad build poora hoga. Us run par jao aur neeche **Artifacts** mein
   `ludo-adda-apk` download karo (zip, andar `app-debug.apk`).
5. APK ko phone mein kholo aur install karo (Settings mein "Install unknown apps" allow karna pad sakta hai).

## Play Store ke liye (baad mein)

Play Store ko **signed AAB** chahiye, ye debug APK nahi chalega. Uske liye:
- Google Play Console account (ek baar ki fees),
- apna signing key (keystore),
- app icon (512x512), screenshots, privacy policy page.

Ye sab ke liye bata dena, main signed AAB wala workflow aur listing ka text bana dunga.

## App ka package ID

`com.ludoadda.game`. Play Store par daalne se pehle ise `capacitor.config.json` mein apni pasand se
badal sakte ho, upload ke baad ye badla nahi ja sakta.
