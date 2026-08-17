# Tugas Besar: Katalog Menu Kantin Sekolah

Selamat! Kamu telah mencapai akhir dari modul **Flutter Dasar**. Saatnya menguji seluruh ilmu yang telah kamu pelajari dengan merancang dan mengembangkan aplikasi utuh secara mandiri dari awal.

## Deskripsi Proyek

Tema tugas akhir kita adalah **"Aplikasi Katalog Menu Kantin Sekolah"**.

Kamu bertugas sebagai pengembang aplikasi yang disewa oleh pengurus kantin sekolah. Mereka menginginkan sebuah aplikasi di mana para siswa bisa melihat daftar makanan, mencari nama jajanan favorit mereka, dan mengklik makanan tersebut untuk masuk ke halaman detail yang menampilkan foto makanan, harga, dan tombol pemesanan.

## Syarat Kelulusan Dasar (Nilai Minimal 80)

Untuk mencapai nilai standar, aplikasimu **wajib** menggunakan komponen-komponen berikut:

- **StatefulWidget & TextField**: Aplikasi harus memiliki kolom pencarian di bagian atas layar. Saat huruf diketikkan, daftar makanan di bawahnya harus langsung tersaring.
- **ListView.builder & Expanded**: Menampilkan minimal 5 jenis makanan atau minuman kantin (seperti mi ayam, batagor, es teh manis) dalam wujud baris yang berderet ke bawah.
- **Image.asset**: Menggunakan gambar lokal yang disimpan di dalam *folder* proyek.
- **GoogleFonts**: Teks pada judul aplikasi dan nama makanan harus menggunakan gaya huruf dari paket `google_fonts`.
- **Navigator**: Terdapat dua halaman utama (Halaman Daftar Menu dan Halaman Detail Menu). Jika salah satu makanan diklik, aplikasi wajib berpindah ke halaman detail menggunakan `Navigator.push`.

## Tantangan Tambahan (Nilai Maksimal 100)

Jika kamu ingin mendapatkan nilai sempurna dan membuktikan kemampuanmu dengan standar industri, lengkapi aplikasimu dengan kriteria tambahan berikut:

- **Halaman Ekstra (Tambah 2 Halaman Baru)**: Buat dua halaman tambahan, misalnya halaman "Keranjang Belanja" dan halaman "Tentang Kantin".
- **Perhitungan Harga Otomatis**: Buat fitur di mana pengguna bisa menambah jumlah porsi pesanan di halaman detail, lalu aplikasi akan menghitung total harganya secara otomatis menggunakan variabel *State*.
- **Struktur Proyek Rapi (Refactoring)**: Pisahkan kode halaman pertama dan halaman kedua ke dalam *file* Dart yang berbeda (misalnya `home_page.dart` dan `detail_page.dart`), lalu simpan di dalam *folder* yang rapi.
- **Kode Bersih (Clean Code)**: Berikan jarak (*enter*) yang teratur antar baris fungsi, dan hapus semua *widget* pembungkus yang tidak terpakai agar kodemu mudah dibaca.

## Aturan Pengumpulan

Setelah kodemu berjalan lancar tanpa ada keluhan *error overflow* (garis batas kuning hitam di layar), cetak aplikasimu (*build*) untuk dikumpulkan.

Kirimkan tugas akhirmu kepada guru penilai di dalam **salah satu** format berikut:

- **File APK**: Menggunakan perintah `flutter build apk` (pastikan aplikasinya bisa dipasang di HP Android).

Jangan lupa, kumpulkan juga seluruh kode sumber aslimu (*source code*) melalui tautan repositori GitHub!

Selamat berkarya!
