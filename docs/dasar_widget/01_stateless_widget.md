# Stateless Widget

Di Flutter, *widget* terbagi menjadi dua kategori utama berdasarkan sifatnya. Yang pertama dan paling sederhana adalah **StatelessWidget**.

**Analogi:** `StatelessWidget` itu ibarat **sebuah poster**. Sekali poster tersebut dicetak dan ditempel di dinding, gambar dan tulisannya tidak akan pernah bisa berubah lagi secara otomatis. Ia diam dan statis.

## Karakteristik StatelessWidget

- **Tidak Bisa Berubah (Immutable)**: Setelah digambar (di-render) di layar, data atau penampilannya tidak bisa berubah sama sekali meskipun ada interaksi dari pengguna (kecuali *widget* induknya memaksa untuk merender ulang keseluruhan layar).
- **Digunakan Untuk Tampilan Statis**: Sangat cocok digunakan untuk elemen yang sekadar menampilkan informasi tetap, seperti judul aplikasi, teks statis, ikon dekorasi, atau gambar profil.

## Cara Menggunakannya

Berikut adalah contoh kerangka dasar pembuatan `StatelessWidget`:

```dart
import 'package:flutter/material.dart';

class TeksPeringatan extends StatelessWidget {
  const TeksPeringatan({super.key});

  @override
  Widget build(BuildContext context) {
    return const Text(
      'Dilarang merokok di area ini!',
      style: TextStyle(color: Colors.red, fontSize: 20),
    );
  }
}
```

- Kata kunci **`extends StatelessWidget`** wajib disertakan agar kelas tersebut dikenali sebagai *widget* statis.
- Kamu wajib menggunakan fungsi **`build`** untuk menggambar apa yang ingin ditampilkan ke layar (dalam contoh ini, *widget* `Text`).
