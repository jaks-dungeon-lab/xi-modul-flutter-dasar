# Image (Gambar)

Aplikasi daftar siswa buatan kita sebelumnya masih menggunakan ikon sederhana. Sekarang, kita akan memperbarui kode dan mengganti ikon tersebut menjadi sebuah foto (pas foto) sungguhan menggunakan *widget* **Image**.

## Menggunakan Gambar Lokal (Image.asset)

Karena pas foto tersebut adalah elemen visual yang wajib dan penting bagi desain aplikasi, kita wajib menanamkannya langsung ke dalam folder proyek agar aman.

1. Buat folder baru bernama `assets/` di dalam folder utama proyek Fluttermu (sejajar posisinya dengan folder `lib/`).
2. Pindahkan *file* pas foto ke dalam folder tersebut (misalnya kita beri nama `profile.jpg`).
3. Wajib! Daftarkan *file* tersebut di dalam pengaturan konfigurasi utama `pubspec.yaml` tepat di bawah tulisan `flutter:`
   ```yaml
   flutter:
     assets:
       - assets/profile.jpg
   ```
4. Setelah beres, panggil gambarnya di dalam kode Dart menggunakan fungsi `Image.asset`:
   ```dart
   Image.asset('assets/profile.jpg')
   ```

## Menerapkan ke Studi Kasus Daftar Siswa

Mari kita perbarui rancangan daftar siswa kita. Temukan dan hapus komponen *Icon* yang berada di sisi kiri, lalu ganti menggunakan *widget* `Image.asset` dengan pengaturan ukuran pas foto resmi.

```dart
// HAPUS KODE LAMA INI:
// const Icon(Icons.person, size: 60, color: Colors.blue),

// GANTI MENJADI KODE BARU INI:
Image.asset(
  'assets/profile.jpg', // Nama file foto lokal yang sudah kamu daftarkan
  width: 80,
  height: 110,
  fit: BoxFit.cover, // Secara otomatis memotong tepi gambar agar ukurannya pas dan tidak gepeng
)
```

Jalankan kembali aplikasimu atau lakukan *hot reload*. Sekarang, aplikasi daftar siswamu akan terlihat sangat realistis, tajam, dan hidup karena sudah memiliki identitas wajah yang nyata!
