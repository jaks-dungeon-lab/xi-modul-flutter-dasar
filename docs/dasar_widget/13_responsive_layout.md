# Responsive Layout (Tata Letak Adaptif)

Layar HP tidak memiliki ukuran yang sama persis. Ada layar tablet yang lebar, dan ada layar ponsel lawas yang kecil. Aplikasi yang bagus wajib beradaptasi dengan semua ukuran layar agar letaknya tidak menabrak batas, hancur, atau terpotong. Konsep ini disebut **Responsive Layout**.

**Analogi:** `Responsive Layout` itu meniru sifat **air**. Jika air dituangkan ke dalam mangkuk bundar, ia akan menyesuaikan diri melebar. Jika dituangkan ke dalam botol kurus memanjang, ia akan menyesuaikan diri meninggi.

## Alat Pencegah Tabrakan Teks: Expanded

*Widget* andalan saat menyusun posisi ke samping (`Row`) atau ke bawah (`Column`) adalah **`Expanded`**. 

Fungsi utama `Expanded` adalah mengambil alih sisa ruang kosong yang belum terpakai pada baris tersebut. 

Sebagai contoh pada desain daftar siswa kita sebelumnya, teks nama siswa bisa saja diinput sangat panjang (misal: "Budi Santoso Muhammad Firdaus Iskandar"). Jika dibiarkan di dalam `Row`, teks nama panjang ini akan memanjang lurus hingga menabrak tepi kanan layar dan menyebabkan *error display overflow* berupa garis kuning-hitam.

Solusinya, kita cukup membungkus *widget* *Column* tempat kumpulan teks tersebut dengan jaket `Expanded`:

```dart
Row(
  children: [
    Container(child: Image.asset('...')), // Pas foto di sebelah kiri
    const SizedBox(width: 16),
    
    // Kita bungkus Column teks dengan pelindung Expanded
    // Artinya: "Teks ini diizinkan mengembang secara wajar mengisi sisa layar sebelah kanan"
    Expanded(
      child: Column(
        crossAxisAlignment: CrossAxisAlignment.start,
        children: const [
          Text('Nama Panjang Yang Berpotensi Membentur Garis Batas Kanan Layar'),
        ],
      ),
    ),
  ],
)
```

Dengan `Expanded`, teks yang terlalu panjang akan secara otomatis dipotong atau didorong turun ke baris bawahnya sehingga tidak akan pernah menabrak tepi kanan layar.

## Alat Pemeriksa Lebar Layar: MediaQuery

Terkadang kita butuh mengetahui ukuran pasti layar fisik perangkat secara angka mutlak pada saat itu juga. Untuk melakukannya, kita menggunakan fitur sensor yang disebut `MediaQuery`.

```dart
// Mengambil data pasti lebar layar saat ini dalam satuan angka piksel
double lebarLayarAktif = MediaQuery.of(context).size.width;

if (lebarLayarAktif > 600) {
  print('Layar ini terdeteksi luas, kemungkinan besar ini adalah Tablet.');
} else {
  print('Layar ini berukuran normal seperti HP standar.');
}
```

Dengan menggabungkan pengetahuan `Expanded` dan `MediaQuery`, aplikasi buatanmu dijamin akan tampil rapi di semua merek HP mana pun.
