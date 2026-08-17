# Kelas XI Flutter Dasar

Selamat datang di modul pembelajaran **Flutter Dasar** untuk kelas XI! Modul ini dirancang secara khusus untuk membimbingmu melangkah dari titik nol hingga kamu sanggup merancang, membangun, dan merilis aplikasi *mobile* modern yang siap pakai. 

Kamu akan diajak menyelami dunia pengembangan aplikasi kekinian dengan metode pembelajaran berbasis proyek (*Project-Based Learning*), di mana setiap teori yang diajarkan akan selalu dibuktikan langsung melalui karya visual yang nyata.

---

## Target Pembelajaran

Setelah menuntaskan seluruh bab di dalam modul ini, kamu diwajibkan untuk mampu:

- Memahami konsep arsitektur **Flutter** dan membongkar cara kerja dasar *Widget*.
- Merancang antarmuka pengguna (**UI**) yang indah, fungsional, dan dapat beradaptasi fleksibel (responsif) pada berbagai ukuran layar gawai.
- Mengelola aliran data perantara interaksi halaman dasar melalui *State Management* konvensional.
- Menghidupkan perpindahan alur multi-halaman lewat sistem *Routing* / *Navigation*.
- Mengeksekusi proses pembungkusan akhir kode (*Deployment*) menjadi produk *file* format rilis (seperti APK atau Web) yang siap dipasang secara umum.

---

## Prasyarat Kemampuan

Sebelum memulai materi pertama, pastikan kamu sudah menguasai fondasi kemampuan berikut:

- Dasar-dasar pengoperasian komputer, manajemen *folder*, dan navigasi *file*.
- Logika dasar algoritma pemrograman.
- **Pemrograman Dart**: Modul ini tidak lagi membahas konsep teori bahasa dasar. Kamu diasumsikan telah lulus materi **Dart Dasar**, percabangan **Control Flow**, hingga pemahaman **OOP**. (Referensi: [Modul Dart Programming](https://github.com/smk-icb-ct-rpl-lab/xi-modul-dart-programming.git)).
- Pemahaman struktur dasar web seperti tabel HTML/CSS akan sangat membantu mempercepat pemahamanmu, meski secara teknis hal ini tidak diwajibkan.

---

## Persiapan Perangkat (*Tools*)

Siapkan perangkat keras dan lunak utamamu berikut:

- **Laptop / Komputer**: Direkomendasikan memiliki RAM minimal 8 GB agar proses *build* dan *emulator* bisa berjalan lancar.
- **Flutter SDK**: Komponen inti yang wajib diinstal dan dikonfigurasi ke dalam sistem komputermu ([Panduan instalasi resmi](https://flutter.dev/docs/get-started/install)).
- **Code Editor**: Direkomendasikan menggunakan **Visual Studio Code**, ditambah dengan ekstensi "Flutter" dan "Dart" agar kodemu diwarnai rapi dan mendapat fitur *autocomplete*.
- **Layar Pengujian**: Kamu bisa memakai *emulator* dari Android Studio jika kapasitas RAM memadai, atau menggunakan opsi paling irit: menyambungkan HP Android asli ke laptop menggunakan kabel USB (*Developer Options*).

---

## Mekanisme Belajar

Langkah-langkah yang akan memandu kita di sepanjang modul ini:

1. Membaca dan memahami setiap materi teori secara berurutan.
2. Mempraktikkan langsung contoh kode *widget* ke dalam aplikasimu.
3. Menggabungkan seluruh materi menjadi satu **Studi Kasus** di akhir bab.
4. Menguji pemahamanmu melalui Kuis interaktif pada setiap penutup bab.
5. Mengubah hasil kodemu (*Deployment*) menjadi *file* aplikasi (*installer*) yang siap pakai di ujung perjalanan.

---

## Glosarium

Kumpulan istilah teknis yang akan sering kita temui di sepanjang kelas ini:

- **Widget**: Batu bata atau balok lego penyusun layar aplikasi Flutter. Segala hal yang terlihat di layar (tombol, teks, hingga jarak kosong) adalah *Widget*.
- **Widget Tree**: Struktur hierarki yang menunjukkan letak susunan *widget* mana yang membungkus *widget* lainnya.
- **StatelessWidget**: Tipe *widget* statis yang tampilannya tidak bisa berubah setelah pertama kali digambar di layar (seperti poster).
- **StatefulWidget**: Tipe *widget* dinamis dan interaktif yang tampilannya bisa diperbarui atau berubah kapan saja jika ada aktivitas atau interaksi.
- **State**: Kondisi atau nilai data internal suatu aplikasi yang sedang berjalan pada saat tertentu.
- **Hot Reload**: Fitur andalan Flutter untuk menerapkan perubahan kode secara instan ke dalam layar aplikasi, tanpa perlu melakukan kompilasi ulang dari awal.
- **SDK (Software Development Kit)**: Paket resmi berisi kumpulan alat (*tools*) khusus yang dibutuhkan untuk mengembangkan perangkat lunak.
- **Pubspec.yaml**: Pusat konfigurasi proyek aplikasi. Di dokumen inilah kita mendaftarkan gambar lokal, *font* kustom, hingga menambahkan paket pustaka (*package*) tambahan dari luar.
- **Overflow**: Masalah cacat UI di mana suatu komponen memiliki ukuran yang melebihi batas layar, ditandai dengan munculnya garis peringatan tebal berwarna kuning-hitam di pinggiran layar.
- **Deployment (Build)**: Proses menyusun dan mengubah kode aplikasi (*source code*) menjadi format *file* program jadi yang siap didistribusikan ke pengguna.
- **APK**: Format *file installer* standar untuk aplikasi di sistem operasi Android.
- **IPA**: Format *file installer* eksklusif untuk aplikasi di ekosistem iOS (iPhone/iPad).
