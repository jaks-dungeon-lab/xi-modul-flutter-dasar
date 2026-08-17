# Rangkuman Dasar-Dasar Flutter

Selamat! Kamu sudah menyelesaikan bab pengenalan tentang dasar pengembangan aplikasi menggunakan Flutter.

## Intisari Materi

Berikut adalah poin-poin utama yang harus kamu ingat:

- **Struktur Projek**: `lib/` adalah tempat menulis kode utama, sedangkan `.dart_tool/`, `build/`, `.gitignore`, dan direktori spesifik *platform* (`android/`, `ios/`, `web/`) biasanya tidak perlu diubah manual.
- **`main.dart`**: Aplikasi selalu diawali dengan mengeksekusi fungsi **`main()`** dan `runApp()`.
- **Widget Utama**: Tampilan statis menggunakan **StatelessWidget**, sementara tampilan dinamis (bisa berubah saat interaksi) wajib menggunakan **StatefulWidget** dipadukan dengan fungsi `setState()`.
- **`Scaffold`**: *Widget* yang menyediakan kerangka layar standar (seperti `AppBar`, `body`, dan `FloatingActionButton`).
- **`pubspec.yaml`**: Jantung pengaturan proyek. Tempat kamu mengatur versi aplikasi dan menambahkan *package* dari pihak ketiga.
- **Perintah Terminal**: Gunakan `flutter pub get` untuk mengunduh *package* ke komputer, dan `flutter pub add` untuk menambahkan sekaligus mengunduhnya.
- **Sumber Package**: Kamu bisa mencari pustaka dan inspirasi tambahan melalui **Pub.dev**, **Flutter Gems**, dan **Flutter Awesome**.
