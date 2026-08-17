# Padding, Center, & Container

Untuk membuat tampilan aplikasi yang cantik, kita tidak bisa sekadar menumpuk teks dan gambar. Kita butuh pengatur tata letak visual (*layout*). Tiga *widget* dasar yang paling sering digunakan untuk merapikan *layout* adalah **Padding**, **Center**, dan **Container**.

## 1. Padding (Pemberi Jarak Bebas)

**Analogi:** Bayangkan sebuah bingkai foto. Tentu kamu tidak ingin fotonya menempel ketat dengan pinggiran kayu bingkainya. Kamu butuh sekat putih di antaranya. **Padding** adalah sekat ruang kosong tersebut.

`Padding` digunakan untuk memberikan jarak aman (ruang kosong) di sekeliling *widget* anaknya.

```dart
Padding(
  // EdgeInsets.all(16.0) artinya memberikan jarak 16 piksel di semua sisi (atas, bawah, kiri, kanan)
  padding: const EdgeInsets.all(16.0),
  child: const Text('Teks ini tidak akan menempel ke pinggir layar.'),
)
```

## 2. Center (Penengah Objek)

Sesuai namanya, **Center** adalah *widget* instan yang bertugas memposisikan *widget* anaknya persis di tengah-tengah ruang yang tersedia.

```dart
Center(
  child: const Text('Aku berada tepat di tengah layar!'),
)
```

## 3. Container (Kotak Serbaguna)

**Analogi:** `Container` itu ibarat **kardus sepatu**. Ia adalah sebuah kotak tempat kamu menyimpan barang (anak *widget*), yang bagian luarnya bisa kamu warnai, kamu beri bingkai (*border*), atau kamu buat melengkung ujungnya.

`Container` adalah *widget* pembungkus paling *powerful* karena menggabungkan fitur jarak (`padding`), ukuran panjang-lebar (`width` & `height`), hingga dekorasi visual.

```dart
Container(
  width: 200,
  height: 100,
  padding: const EdgeInsets.all(10), // Jarak ke dalam
  margin: const EdgeInsets.all(20), // Jarak ke luar (mendorong elemen lain)
  decoration: BoxDecoration(
    color: Colors.blue, // Warna latar belakang kardus
    borderRadius: BorderRadius.circular(8), // Membuat ujung kardus melengkung
  ),
  child: const Text('Ini di dalam kardus biru'),
)
```

Ketiga *widget* pembungkus di atas (Padding, Center, Container) hanya boleh memiliki **satu** *widget* anak (`child`). Jika kamu ingin membungkus banyak anak sekaligus, kamu harus mempelajari materi berikutnya: *Row* dan *Column*.
