# Build APK (Aplikasi Android)

Setelah lelah mengetik kode berhari-hari, kini saatnya mengubah kodemu menjadi aplikasi nyata yang bisa dipasang di *handphone* Android. Proses membungkus kode mentah ini menjadi *file* siap pakai dinamakan **Deployment** atau **Build**.

**Analogi:** Proses *build* itu persis seperti **memanggang kue**. Kodemu adalah adonan mentah (tepung, telur, gula). Kamu tidak bisa memakan adonan mentah. Kamu harus memasukkannya ke dalam oven (proses *build*) agar berubah menjadi kue matang (*file* APK) yang siap disajikan kepada pengguna.

## Apa itu APK?

**APK** (*Android Package Kit*) adalah format *file* standar yang digunakan sistem operasi Android untuk memasang aplikasi. Jika kamu membagikan *file* berekstensi `.apk` ini ke temanmu via WhatsApp atau *flashdisk*, mereka bisa langsung memasangnya di HP Android mereka tanpa perlu komputer atau kabel.

## Langkah Membangun APK

Untuk mencetak kodemu menjadi APK, buka terminal di VS Code, pastikan kamu berada di dalam folder proyek Flutter, lalu ketik perintah berikut:

```bash
flutter build apk
```

Proses ini akan memakan waktu cukup lama (bisa 2 hingga 10 menit tergantung kecepatan komputermu), karena oven komputer sedang bekerja keras menerjemahkan semua bahasa Dart menjadi bahasa mesin Android murni.

## Mengambil Hasil Panen (Lokasi APK)

Jika proses sudah selesai 100%, terminal akan memberikan informasi di mana *file* tersebut disimpan. Secara bawaan, Flutter menyembunyikannya di dalam ruang brankas berikut:

`[Folder Proyekmu]/build/app/outputs/flutter-apk/app-release.apk`

Ambil *file* **`app-release.apk`** tersebut, pindahkan ke HP Androidmu, dan mulailah pamerkan mahakarya aplikasimu kepada orang tua dan teman-temanmu!
