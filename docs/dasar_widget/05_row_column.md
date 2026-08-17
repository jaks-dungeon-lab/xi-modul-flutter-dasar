# Row & Column

*Container* dan *Padding* hebat, tapi mereka hanya bisa menampung **satu** anak (*single child*). Bagaimana jika kita ingin menampilkan 3 tombol secara berdampingan? Di sinilah kita butuh *widget* yang menerima daftar banyak anak (`children`). Dua yang terpenting adalah **Row** dan **Column**.

## 1. Column (Kolom Vertikal)

**Analogi:** `Column` itu seperti **tumpukan buku**. Kamu menumpuk buku pertama di bawah, lalu buku kedua di atasnya, terus menjulang ke atas.

`Column` menyusun elemen-elemen anaknya secara vertikal, dari atas ke bawah.

```dart
Column(
  // MainAxis untuk Column adalah vertikal (atas-bawah)
  mainAxisAlignment: MainAxisAlignment.center, 
  children: const [
    Text('Baris Pertama (Paling Atas)'),
    Text('Baris Kedua (Tengah)'),
    Text('Baris Ketiga (Paling Bawah)'),
  ],
)
```

## 2. Row (Baris Horizontal)

**Analogi:** `Row` itu seperti **buku-buku yang berjejer rapi di rak perpustakaan**. Buku pertama di kiri, buku kedua di sebelahnya, menyamping ke arah kanan.

`Row` menyusun elemen-elemen anaknya secara horizontal, dari kiri ke kanan.

```dart
Row(
  // MainAxis untuk Row adalah horizontal (kiri-kanan)
  mainAxisAlignment: MainAxisAlignment.spaceBetween, // Jaraknya direnggangkan maksimal
  children: const [
    Icon(Icons.home),
    Icon(Icons.search),
    Icon(Icons.settings),
  ],
)
```

## Sumbu Utama (MainAxis) dan Sumbu Silang (CrossAxis)

Kunci untuk menguasai tata letak `Row` dan `Column` adalah memahami cara merapikan perataannya (*alignment*):

- **`mainAxisAlignment`**: Merapikan posisi searah dengan sumbunya. Pada `Row` artinya mengatur rata kiri/tengah/kanan. Pada `Column` artinya mengatur rata atas/tengah/bawah.
- **`crossAxisAlignment`**: Merapikan posisi berlawanan dengan sumbunya. Pada `Row` artinya mengatur rata atas/bawah. Pada `Column` artinya mengatur rata kiri/kanan.

Dengan menggabungkan `Row` di dalam `Column` (atau sebaliknya), kamu bisa membangun tampilan aplikasi sekaya apa pun yang kamu mau!
