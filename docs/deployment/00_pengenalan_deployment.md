# Pengenalan Deployment

Setelah berhari-hari berjibaku dengan kode *Widget* untuk mendesain layar, menulis alur logika *Stateful*, hingga menghubungkannya dengan gambar dan fon interaktif, kini aplikasi buatanmu sudah memasuki batas akhir.

Proses tahap akhir penutup ini dinamakan **Deployment**.

## Kenapa Deployment Itu Penting?

Tanpa proses *deployment*, aplikasi sehebat apa pun buatanmu hanya akan hidup dan terkurung selamanya di dalam memori komputer milikmu atau di *emulator* sementara. Pengguna umum di luar sana tidak mungkin diwajibkan membuka laptopmu hanya untuk bisa memakai aplikasi tersebut.

Melalui *deployment*, kita membungkus kode mentah (Dart) tersebut ke dalam sebuah wadah tertutup yang sangat aman dan ringkas. Bentuk jadi inilah yang nantinya bisa dikirimkan secara bebas lewat internet (seperti melalui WhatsApp atau diunggah ke Google Play Store). 

## Multi-Platform: Keajaiban Flutter

Keunggulan utama Flutter yang tidak dimiliki oleh teknologi masa lalu adalah kemampuannya yang sangat hebat untuk mencetak **banyak jenis produk format berbeda hanya dari satu cetak biru yang sama**.

Melalui proses *deployment* di Flutter, satu kode aplikasi daftar siswa yang sama persis bisa dicetak wujudnya menjadi tiga produk yang berbeda alam:
1. Dicetak menjadi format **APK** (khusus untuk menjangkau pengguna *handphone* Android).
2. Dicetak menjadi format **IPA** (khusus untuk menembus batasan ekosistem pengguna iOS / iPhone).
3. Dicetak menjadi format **Web** (berupa situs peramban agar bisa dibuka langsung lewat Google Chrome).

Mari kita bahas cara kerja dan syarat pencetakan ketiga produk hebat ini di materi-materi selanjutnya!
