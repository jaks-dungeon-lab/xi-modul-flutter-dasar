# Struktur Projek Flutter

Saat kamu pertama kali membuat projek Flutter, kamu akan melihat banyak *folder* dan *file* yang terbuat secara otomatis. Memahami kegunaan masing-masing sangatlah penting.

Berikut adalah visualisasi struktur folder dasar dari projek Flutter:

```text
nama_projek/
├── .dart_tool/       # File konfigurasi internal Dart (otomatis)
├── android/          # Folder khusus untuk build Android
├── build/            # Tempat hasil kompilasi aplikasi (otomatis)
├── ios/              # Folder khusus untuk build iOS
├── lib/              # Folder UTAMA tempat menulis kode Dart
│   └── main.dart     # File utama yang pertama kali dijalankan
├── test/             # Tempat menyimpan kode pengujian otomatis
├── web/              # Folder khusus untuk build Web
├── .gitignore        # Daftar file yang diabaikan oleh Git
├── counter_app.iml   # File pengaturan editor Android Studio/IntelliJ
├── pubspec.yaml      # File pengaturan aplikasi dan package
└── README.md         # Dokumentasi dasar projek
```
## Folder dan File Utama

Berikut adalah bagian yang paling sering kamu gunakan:

- **`lib/`**: Ini adalah "meja kerja utama" kamu. Hampir seluruh kode bahasa pemrograman **Dart** yang kamu tulis akan disimpan di sini.
- **`pubspec.yaml`**: Ini adalah buku catatan daftar kebutuhan. Di sini kamu mengatur versi aplikasi, gambar yang akan dipakai, serta **package** (pustaka) tambahan dari luar.
- **`android/`, `ios/`, dan `web/`**: Folder ini berisi kode khusus jika kamu butuh mengatur sesuatu yang sangat spesifik untuk *platform* tertentu. Umumnya, kamu jarang menyentuhnya pada tahap awal.
- **`test/`**: Tempat untuk menyimpan kode otomatis yang akan mengetes apakah aplikasimu berjalan sesuai rencana.
- **`.dart_tool/`**: Folder tersembunyi berisi konfigurasi otomatis dari *compiler* Dart. Kamu tidak perlu mengubah isinya secara manual.
- **`.gitignore`**: Daftar berisi nama *file* dan *folder* yang akan diabaikan (tidak diunggah) ketika kamu menyimpan projek ke Git/Github.
- **`counter_app.iml`**: *File* konfigurasi internal yang dibuat khusus untuk aplikasi editor seperti *Android Studio* atau *IntelliJ*.
- **`README.md`**: Halaman pengantar utama projekmu. Biasanya digunakan untuk menulis penjelasan ringkas tentang fungsi aplikasi dan cara menjalankannya.
