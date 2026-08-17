# Button (Tombol)

Agar aplikasi daftar siswamu (dan aplikasi secara umum) menjadi interaktif, pengguna harus bisa mengeklik sesuatu. Flutter menyediakan banyak *widget* khusus untuk membuat tombol. 

## 3 Jenis Tombol Utama

Flutter *Material Design* memiliki tiga gaya tombol utama:

1. **`ElevatedButton` (Tombol Menonjol)**
   Tombol ini memiliki bayangan dan latar belakang yang solid. Sangat cocok digunakan untuk aksi utama yang paling penting, seperti tombol "Kirim" atau "Simpan".
   
   ```dart
   ElevatedButton(
     onPressed: () {
       print('Tombol ditekan!');
     },
     child: const Text('Simpan Data'),
   )
   ```

2. **`TextButton` (Tombol Teks Datar)**
   Tombol ini tidak memiliki batas atau latar belakang, hanya teks biasa (atau ikon) yang berubah warna saat ditekan. Sangat cocok untuk aksi sekunder seperti tombol "Batal" atau "Lewati".

   ```dart
   TextButton(
     onPressed: () {
       // Aksi pembatalan
     },
     child: const Text('Batal'),
   )
   ```

3. **`OutlinedButton` (Tombol Bergaris Tepi)**
   Tombol dengan latar belakang transparan namun memiliki garis tepi (*border*). Tombol ini memiliki tingkat kepentingan menengah, cocok untuk tombol "Lihat Profil" di studi kasus daftar siswa.

   ```dart
   OutlinedButton(
     onPressed: () {
       // Aksi menengah
     },
     child: const Text('Lihat Detail'),
   )
   ```

## Properti Wajib pada Tombol

Setiap tombol **wajib** memiliki dua parameter utama:

- **`onPressed`**: Ini adalah mesin fungsi di mana kamu menuliskan perintah apa yang akan terjadi saat tombol ditekan (menggunakan kurung kurawal `{}`). Jika kamu mengisinya dengan `null`, tombol tersebut otomatis akan mati (berubah warna menjadi abu-abu dan tidak bisa ditekan).
- **`child`**: Isi atau wajah dari tombol tersebut, biasanya berupa *widget* `Text` atau `Icon`.
