# Tranzivo Cordova App

Folder ini berisi aplikasi Cordova yang membungkus web app Anda di `www/`.

## Persyaratan

Sebelum mulai, pastikan Anda sudah menginstal:
- Node.js
- npm atau yarn
- Cordova CLI (`npm install -g cordova`)
- Android Studio / Xcode jika akan menjalankan di emulator atau perangkat nyata

## Cara install aplikasi Cordova

1. Buka terminal dan masuk ke folder Cordova:

```bash
cd c:/aplikasipos/cordova-app
```

2. Pasang dependensi Node:

```bash
npm install
```

3. Tambahkan platform Android atau iOS:

```bash
npx cordova platform add android
# atau
npx cordova platform add ios
```

4. Siapkan proyek Cordova:

```bash
npx cordova prepare
```

5. Jalankan aplikasi di perangkat atau emulator:

```bash
npx cordova run android
# atau
npx cordova run ios
```

> Jika Anda hanya ingin membangun paket APK/IPA tanpa langsung menjalankan, gunakan:
>
> ```bash
> npx cordova build android
> # atau
> npx cordova build ios
> ```

## Catatan penting

- Aplikasi Cordova ini menggunakan file web dari `cordova-app/www`.
- Jika Anda ingin memanfaatkan kamera native, gunakan plugin seperti `phonegap-plugin-barcodescanner`.
- Untuk plugin barcode scanner native:

```bash
npx cordova plugin add phonegap-plugin-barcodescanner
```

- Setelah plugin terpasang, Anda bisa mengubah `www/kasir.js` agar memanggil API plugin tersebut.

## Contoh instalasi lengkap di Windows

```bash
cd c:/aplikasipos/cordova-app
npm install
npx cordova platform add android
npx cordova prepare
npx cordova run android
```

Jika butuh, saya bisa bantu menambahkan integrasi native scanner Cordova dan menyesuaikan `www/kasir.js` untuk pemindaian barcode yang lebih stabil di perangkat Android/iOS.
