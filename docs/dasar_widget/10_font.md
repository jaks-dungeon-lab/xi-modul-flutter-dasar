# Font (Jenis Huruf)

Aplikasi daftar siswa kita sudah memiliki gambar foto asli, tetapi jika kamu perhatikan, jenis hurufnya masih sangat kaku, membosankan, dan standar. Untuk memberikan kesan aplikasi kelas atas (*premium*) atau desain yang lebih modern, hal yang paling mudah dilakukan adalah mengganti jenis hurufnya.

## Menggunakan Google Fonts

Cara yang paling disukai pengembang Flutter masa kini untuk mengubah huruf dengan cepat adalah memanfaatkan *package* gratis dari mesin Google bernama **google_fonts**.

### Langkah 1: Pasang Package

Buka terminal komputermu dan jalankan perintah khusus penambahan pustaka pub.dev:
```bash
flutter pub add google_fonts
```

### Langkah 2: Impor ke dalam File

Di baris kode paling atas pada *file* `main.dart` kamu, wajib tambahkan perintah ini agar kode dikenali:
```dart
import 'package:google_fonts/google_fonts.dart';
```

### Langkah 3: Menerapkan ke Studi Kasus Daftar Siswa

Sekarang mari kita tingkatkan gaya jenis huruf untuk nama siswa menjadi jenis 'Poppins' (salah satu jenis huruf paling populer untuk aplikasi ponsel masa kini). Temukan *widget* teks nama di kodemu, lalu rombak total bagian `style`-nya.

```dart
// KODE LAMA STANDAR:
Text(
  'Budi Santoso',
  style: TextStyle(
    fontSize: 20,
    fontWeight: FontWeight.bold,
  ),
),

// KODE BARU DENGAN GOOGLE FONTS:
Text(
  'Budi Santoso',
  style: GoogleFonts.poppins(
    textStyle: const TextStyle(
      fontSize: 20,
      fontWeight: FontWeight.bold,
    ),
  ),
),
```

Cobalah *run* atau muat ulang (*hot reload*) kodemu.
