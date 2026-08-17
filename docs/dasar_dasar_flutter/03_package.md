# Package (Pub.dev)

Ketika kamu membutuhkan fitur khusus seperti mengambil gambar dari kamera atau memutar video, kamu tidak harus membuatnya sendiri dari awal. Kamu bisa menggunakan **package**.

Berikut adalah contoh struktur asli dari *file* **`pubspec.yaml`** pada aplikasi bawaan (*Counter App*):

```yaml
name: counter_app
description: "A new Flutter project."
publish_to: 'none'
version: 1.0.0+1

environment:
  sdk: ^3.12.2

dependencies:
  flutter:
    sdk: flutter
  cupertino_icons: ^1.0.8

dev_dependencies:
  flutter_test:
    sdk: flutter
  flutter_lints: ^6.0.0

flutter:
  uses-material-design: true
```

## Membedah File `pubspec.yaml`

Setiap baris di *file* ini memiliki fungsi penting. Berikut adalah penjelasan untuk baris-baris utamanya:

- **`name:`**: Nama proyek aplikasimu (harus huruf kecil tanpa spasi, dipisah *underscore*).
- **`description:`**: Penjelasan singkat tentang apa kegunaan aplikasimu.
- **`version:`**: Versi aplikasi saat ini. Digunakan nanti saat kamu ingin merilis aplikasi ke *Play Store* atau *App Store*.
- **`environment:`**: Batasan versi Dart SDK yang diizinkan untuk menjalankan kode ini (contoh: minimal versi 3.12.2).
- **`dependencies:`**: Daftar paket atau pustaka utama yang menjadi jantung aplikasimu. Semua *package* dari pub.dev yang dibutuhkan aplikasimu saat dijalankan (*runtime*) akan ditulis di sini.
- **`dev_dependencies:`**: Daftar paket yang hanya digunakan saat proses pengembangan (misalnya paket *testing* atau *linter* untuk merapikan kode). Paket ini tidak akan ikut terinstal di HP pengguna.
- **`flutter:`**: Pengaturan khusus dari mesin Flutter, misalnya `uses-material-design: true` yang memastikan ikon bawaan dari *Material Design* tersedia.

## Penggunaan Perintah `flutter pub`

Untuk mengatur seluruh *package* di atas, kamu akan sangat sering menggunakan perintah di terminal yang disebut **`flutter pub`** (atau `dart pub`). Berikut adalah perintah utamanya:

- **`flutter pub get`**: Membaca *file* `pubspec.yaml` dan mengunduh seluruh *package* yang terdaftar ke dalam komputermu. Ini wajib dijalankan setiap kali kamu menambahkan *package* baru.
- **`flutter pub add [nama_package]`**: Cara instan untuk mencari dan menambahkan *package* versi terbaru langsung ke dalam `pubspec.yaml` sekaligus mengunduhnya otomatis.
- **`flutter pub upgrade`**: Memperbarui versi semua *package* yang kamu gunakan ke versi paling mutakhir yang diizinkan oleh pengaturan proyekmu.

## Referensi Pencarian Package

Di mana kamu bisa menemukan *package* yang bagus? Berikut adalah tiga sumber utama yang wajib kamu tahu:

| Nama Situs | Penjelasan | Tautan |
|------------|------------|--------|
| **Pub.dev** | Toko aplikasi resmi bawaan Dart dan Flutter. Semua *package* yang kamu unduh aslinya berasal dari sini. Sangat lengkap dan terpercaya. | [pub.dev](https://pub.dev) |
| **Flutter Gems** | Katalog *package* yang disusun sangat rapi berdasarkan kategori (misalnya kategori UI, Database, Map). Sangat cocok jika kamu sedang bingung mencari nama spesifik *package* yang kamu butuhkan. | [fluttergems.dev](https://fluttergems.dev) |
| **Flutter Awesome** | Kumpulan contoh antarmuka (*UI*) dan pustaka populer yang telah diseleksi oleh komunitas. Berguna jika kamu sedang butuh inspirasi visual. | [flutterawesome.com](https://flutterawesome.com) |
