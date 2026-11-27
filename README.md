# AI VIDEO STUDIO untuk Android

Aplikasi mandiri (tanpa server): HP memanggil API Runway langsung. API key dan galeri disimpan di dalam aplikasi di HP Anda.

## Cara 1: build APK lewat GitHub (tanpa Android Studio)
1. Buat akun dan repository baru di github.com (boleh private).
2. Unggah semua isi folder ini ke repository, termasuk `.github/workflows/build-apk.yml`.
   Folder tersembunyi (diawali titik) sering tidak ikut terunggah dari HP. Jika begitu, pakai "Add file > Create new file", ketik nama `.github/workflows/build-apk.yml`, lalu tempel isi file tersebut.
3. Buka tab Actions > Build APK > Run workflow. Tunggu sekitar 5-10 menit.
4. Buka hasil run tersebut, unduh artifact `AI-VIDEO-STUDIO-apk`, ekstrak zip-nya, lalu pasang `app-debug.apk` di HP (izinkan "pasang dari sumber tidak dikenal").

## Cara 2: Android Studio
1. Pasang Node.js 20+ dan Android Studio.
2. Di folder ini jalankan: `npm install`, `npx cap add android`, `npx cap sync android`, lalu `npx cap open android`.
3. Di Android Studio pilih Build > Build APK(s), atau jalankan langsung ke HP.

## Memakai aplikasi
Buka tab Pengaturan, tempel API key Runway (buat di dev.runwayml.com), lalu Simpan.

## Biaya dan batasan
- Runway berbayar (kredit). Setiap klik "Buat video" meminta konfirmasi dulu.
- Durasi 5 atau 10 detik per video. Rasio 1:1 hanya untuk gambar ke video.
- Tautan video Runway cepat kedaluwarsa, jadi simpan hasilnya.
- Ini APK debug untuk pemakaian pribadi, bukan untuk dirilis di Play Store.
- Belum diuji di perangkat dan belum diuji dengan API key asli.
- 
