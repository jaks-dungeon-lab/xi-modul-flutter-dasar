# Scaffold

Setelah memahami dasar *Stateless* dan *Stateful*, saatnya kita membangun struktur halaman aplikasi yang sebenarnya. Di sinilah **Scaffold** berperan penting.

**Analogi:** `Scaffold` itu seperti **pondasi dan kerangka besi sebuah rumah**. Ia sudah menyediakan tempat-tempat khusus yang pas untuk menaruh atap (AppBar), badan rumah (Body), dan bel pintu di luar (FloatingActionButton).

## Mengenal Scaffold

`Scaffold` adalah *widget* standar dari *Material Design* yang memberikan struktur visual dasar bagi sebuah halaman. Tanpa `Scaffold`, aplikasimu hanya akan berupa layar hitam kosong.

Beberapa bagian penting dari `Scaffold`:

- **`appBar`**: Bilah navigasi yang letaknya selalu menempel di bagian paling atas layar.
- **`body`**: Area kanvas utama yang paling luas, tempat kamu akan menggambar seluruh isi aplikasimu.
- **`floatingActionButton`**: Tombol melayang yang biasanya berada di pojok kanan bawah layar.

## Contoh Penggunaan

```dart
import 'package:flutter/material.dart';

class HalamanUtama extends StatelessWidget {
  const HalamanUtama({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Aplikasi Pertamaku'),
        backgroundColor: Colors.blue, // Mengubah warna atap aplikasi
      ),
      body: const Text('Halo, ini adalah bagian isi badan aplikasi!'),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          // Aksi ketika tombol ditekan
        },
        child: const Icon(Icons.add),
      ),
    );
  }
}
```

Dengan menggunakan `Scaffold`, aplikasi kamu secara otomatis memiliki warna latar belakang (*background*) putih standar dan tata letak teks yang wajar, tidak lagi menabrak area sinyal atau baterai HP di bagian atas (*status bar*).
