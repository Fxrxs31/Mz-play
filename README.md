
# MZPlay Predictor Numbers (Android)

**Input**: tekan butang 0–9  
**Klasifikasi**: 0–4 = Small (S), 5–9 = Big (B)  
**Paparan**: sejarah nombor + kategori.  

> Nota: Permainan rawak. Aplikasi hanya bantu analisis statistik/corak — tiada jaminan tepat.

## Cara build APK (Android Studio)
1. `File ▸ Open` dan pilih folder projek ini.
2. Tunggu Gradle sync selesai. (Jika diminta, pilih versi Gradle/Plugin yang disyorkan).
3. `Build ▸ Build APK(s)` → APK di `app/build/outputs/apk/debug/app-debug.apk`.
4. Hantar ke telefon anda dan pasang (aktifkan `Install unknown apps`).

## Cara build APK (Command Line)
```bash
# di root projek
./gradlew assembleDebug
# fail: app/build/outputs/apk/debug/app-debug.apk
```

## Build di GitHub Actions (tak perlu komputer kuat)
1. Buat repo GitHub baharu dan muat naik semua fail projek ini.
2. Buka tab **Actions** → aktifkan Workflows.
3. Fail workflow disertakan di `.github/workflows/android.yml`.
4. Push ke `main`/`master` atau run **Run workflow** secara manual.
5. APK boleh dimuat turun di **Actions ▸ Artifacts** (nama `app-debug`).

## Ubah suai
- `MainActivity.kt` mengandungi UI butang 0–9 dan logik klasifikasi.
- Boleh tambah ramalan/analitik lanjut mengikut keperluan.
