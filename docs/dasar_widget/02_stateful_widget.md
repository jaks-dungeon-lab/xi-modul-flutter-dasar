# Stateful Widget

Kategori *widget* kedua yang sangat sering digunakan adalah **StatefulWidget**. 

**Analogi:** Jika *StatelessWidget* adalah poster statis, maka `StatefulWidget` ibarat **papan skor digital di stadion**. Papan skor ini memiliki memori (ingatan) tentang skor saat ini, dan ketika terjadi gol, papan skor tersebut akan diperbarui secara mandiri (*update*) untuk menampilkan angka baru.

## Karakteristik StatefulWidget

- **Bisa Berubah (Mutable)**: Tampilan layar dapat berubah kapan saja selama aplikasi berjalan.
- **Memiliki State (Memori/Data)**: *Widget* ini menyimpan data (*state*). Jika ada perubahan data, ia akan memicu perubahan pada tampilan.
- **Digunakan Untuk Tampilan Interaktif**: Sangat cocok untuk *form* input, tombol *like* yang warnanya berubah, atau angka penghitung (*counter*).

## Cara Menggunakan setState()

Rahasia utama dari `StatefulWidget` terletak pada perintah ajaib bernama **`setState()`**. Setiap kali kamu memanggil fungsi ini, Flutter akan tahu bahwa ada data yang berubah dan langsung menggambar ulang (*re-build*) tampilan layar.

Berikut adalah kerangka dasarnya:

```dart
import 'package:flutter/material.dart';

class TombolLike extends StatefulWidget {
  const TombolLike({super.key});

  @override
  State<TombolLike> createState() => _TombolLikeState();
}

class _TombolLikeState extends State<TombolLike> {
  // Ini adalah State (Data yang bisa berubah)
  int jumlahLike = 0;

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Jumlah Like: $jumlahLike'),
        ElevatedButton(
          onPressed: () {
            // Memanggil setState agar layar diperbarui
            setState(() {
              jumlahLike = jumlahLike + 1;
            });
          },
          child: const Text('Like!'),
        ),
      ],
    );
  }
}
```

Perbedaan mencoloknya adalah `StatefulWidget` selalu membutuhkan dua buah *class* (satu untuk pendaftaran *widget*, dan satu lagi untuk mengatur *State*/datanya).
