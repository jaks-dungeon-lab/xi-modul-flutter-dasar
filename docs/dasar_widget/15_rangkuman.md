# Rangkuman Dasar Widget

Selamat! Kamu telah menyelesaikan bab tentang fondasi paling penting di Flutter, yaitu tentang struktur tata letak *Widget*.

## Intisari Materi

Berikut adalah poin-poin utama yang perlu kamu ingat:

- **Everything is a Widget**: Hampir seluruh komponen pembangun layar visual di Flutter (mulai dari teks hingga ruang kosong) adalah balok *Widget*.
- **Stateless vs Stateful**: Gunakan `StatelessWidget` untuk halaman tampilan statis yang kaku (tidak perlu berubah). Gunakan `StatefulWidget` dipasangkan dengan `setState()` untuk halaman interaktif yang tampilannya berubah saat ada aktivitas.
- **Pembungkus Utama**: Gunakan `Scaffold` sebagai kanvas dasar yang berisi menu atap (`AppBar`). Gunakan `Container` dan `Padding` untuk memberi bingkai atau memosisikan anak objek secara tunggal.
- **Penyusun Baris**: Gunakan `Row` untuk menata anak-anak berjajar menyamping secara horizontal. Gunakan `Column` untuk menyusun anak-anak berderet ke bawah secara vertikal.
- **Daftar Gulir**: Jika kamu memiliki komponen berjumlah puluhan baris, gunakan *widget* cerdas `ListView.builder` agar halaman tidak patah dan memori perangkat selalu ringan.
- **Layout Fleksibel**: Selalu tambahkan jubah pengaman `Expanded` saat menyusun komponen rentan batas ke dalam baris `Row` atau tiang `Column`. Ini wajib dilakukan agar teks nama panjang secara otomatis pindah paragraf dan tidak menerobos batas layar sebelah kanan.
- **Gambar & Teks Modern**: Pakai `Image.asset` untuk menanam foto aslimu tanpa butuh internet, dan hiasi tulisan menggunakan pustaka `GoogleFonts`.
- **Interaksi Pengguna**: `TextField` adalah alat penangkap ketikan pengguna (seperti kolom pencarian), sedangkan `ElevatedButton` adalah saklar pemicu perintah.
- **Berpindah Layar**: Fungsi sakti `Navigator.push` bertugas menumpuk halaman baru ke atas layar, sementara `Navigator.pop` membuang layar saat ini untuk mundur.
