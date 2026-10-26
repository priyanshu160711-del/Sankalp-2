# Sankalp (Android, all-in-one)

## APK kaise banayein (Android Studio ke bina)
1. github.com par free account -> New repository (Private) banayein.
2. Is folder ki saari files upload karein (Add file > Upload files; `.github` folder bhi).
3. Repo ke "Actions" tab me "Build APK" khud chalega (~5 min). Khatam hone par run kholkar neeche "Sankalp-APK" download karein.
4. Zip se `app-debug.apk` nikalkar phone me install karein (Unknown sources allow karein).

## App ke andar
Block tab: Accessibility, PIN, Block/Study mode, apps, keywords, START. Sab app me.
Android ka rule: Accessibility ek baar system screen par ON hoti hai (app wo screen khud kholta hai).
Isse bhi bachna ho: PC se ek baar (USB debugging ON) chalayein:
    adb shell pm grant com.studylock.app android.permission.WRITE_SECURE_SETTINGS
Uske baad app "ON karo" dabate hi khud ON kar leta hai, Settings nahi khulti.

## Test mode
`Prefs.kt` me `TEST_MODE = true`: PIN nahi, Unlock button chalta hai. Asli use ke liye false karein.
