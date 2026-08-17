# ListView (Daftar Gulir)

Bagaimana jika kita memiliki daftar 50 data siswa yang ingin ditampilkan ke bawah? Jika kita hanya menumpuknya menggunakan `Column`, aplikasi akan mengalami *error* layar peringatan kuning-hitam di bagian bawah. Ini disebut dengan masalah *Overflow*.

Penyebabnya adalah karena layar HP memiliki batas panjang, sedangkan `Column` sifatnya kaku dan tidak bisa digulir (*scroll*).

Solusinya adalah mengganti `Column` menjadi *widget* **ListView**.

**Analogi:** Menggunakan `Column` itu seperti menulis menggunakan kapur di **papan tulis**. Jika papannya penuh, tulisanmu akan menabrak pinggiran dan tidak bisa dilanjutkan. Menggunakan `ListView` itu ibarat menulis pada **kertas gulung panjang**; seberapa panjang pun daftarnya, kamu akan selalu bisa menggulungnya ke bawah.

## 1. ListView Biasa

Cara ini digunakan jika jumlah elemennya hanya sedikit (misalnya daftar 5 menu utama aplikasi).

```dart
ListView(
  children: const [
    Text('Pilihan Menu 1'),
    Text('Pilihan Menu 2'),
    Text('Pilihan Menu 3'),
  ],
)
```

## 2. ListView.builder (Mesin Cetak Otomatis)

Jika kamu ingin menampilkan ratusan daftar siswa, jangan gunakan `ListView` biasa karena akan membuat HP kepanasan (*lag*) akibat memaksa memuat semua data sekaligus.

Gunakan **`ListView.builder`**. Mesin ini cerdas karena hanya akan menggambar baris daftar yang saat itu sedang terlihat di layar saja. Jika data siswa ke-100 belum digulir ke atas layar, baris tersebut tidak akan diproses, sehingga aplikasi menjadi sangat ringan.

```dart
// Daftar memori sementara yang berisi 100 data teks kosong
final List<String> daftarSiswa = List.generate(100, (index) => 'Data Siswa ke-$index');

ListView.builder(
  itemCount: daftarSiswa.length, // Beri tahu mesin berapa total panjang datanya
  itemBuilder: (context, index) {
    // Mesin ini akan dipanggil otomatis untuk mencetak setiap baris
    return Text(daftarSiswa[index]);
  },
)
```

Fungsi `ListView.builder` ini akan sangat sering kamu gunakan, terutama ketika kita mengerjakan materi Studi Kasus akhir pembuatan daftar siswa.
