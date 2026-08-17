# Build Web (Situs Internet)

Kelebihan utama Flutter generasi baru adalah kemampuannya yang tidak hanya terbatas pada layar HP, tetapi juga bisa merambah ke layar *browser* internet (seperti Google Chrome atau Mozilla Firefox).

Dengan kode yang sama persis saat kamu membuat daftar absen siswa sebelumnya, kamu bisa menyulapnya menjadi *website* nyata.

**Analogi:** Mengubah aplikasi menjadi web itu ibarat **menerjemahkan buku**. Buku aslimu ditulis dalam bahasa Indonesia (Dart). Ketika diterjemahkan, isinya sama persis, namun bahasanya diubah secara ajaib menjadi bahasa Inggris (HTML dan JavaScript) agar bisa dibaca oleh orang peramban web asing.

## Perintah Mengubah ke Web

Untuk menyuruh oven Flutter agar mencetak kodemu menjadi format situs web, jalankan perintah ini di terminal:

```bash
flutter build web
```

Kecepatan proses ini biasanya jauh lebih singkat dibandingkan membuat APK.

## Lokasi Hasil Web

Setelah sukses, Flutter akan menghasilkan satu map khusus yang berisi gabungan dokumen HTML, CSS, dan JavaScript siap pakai. Kamu bisa menemukan *folder* hasil panennya di rute berikut:

`[Folder Proyekmu]/build/web/`

Semua isi di dalam folder **`web`** tersebut adalah situs internet aslimu. Kamu bisa menyerahkan folder tersebut kepada teknisi *hosting*, atau mengunggahnya secara mandiri dan gratis ke layanan internet seperti GitHub Pages atau Vercel agar karyamu bisa langsung diakses seluruh dunia lewat *link* URL!
