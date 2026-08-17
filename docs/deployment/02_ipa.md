# Build IPA (Aplikasi iOS)

Selain Android, Flutter juga sangat terkenal karena kemampuannya membuat aplikasi untuk iPhone (sistem operasi iOS) hanya dengan satu kode yang sama. 

Jika *file* mentah untuk Android bernama APK, maka *file* mentah aplikasi yang siap dipasang untuk iPhone disebut dengan **IPA** (*iOS App Store Package*).

**Analogi:** Bayangkan kamu adalah pembuat kunci gembok. Gembok Android itu universal dan bisa dibuat oleh siapa saja. Namun, gembok Apple itu sangat eksklusif; kamu hanya diizinkan mencetak kunci tersebut jika kamu menggunakan mesin cetak resmi buatan pabrik Apple.

## Syarat Wajib Pembuatan IPA

Di sinilah letak perbedaan terbesarnya. Sistem keamanan Apple sangat ketat. Kamu **tidak bisa** membuat *file* IPA menggunakan laptop Windows atau Linux. 

Untuk melakukan proses *build* iOS, kamu wajib memenuhi dua syarat mutlak:

1. **Memiliki Komputer Mac**: Entah itu MacBook atau iMac, kamu butuh sistem operasi macOS.
2. **Memasang Xcode**: Ini adalah aplikasi oven resmi buatan Apple (berukuran sangat besar) yang bertugas menerjemahkan kode menjadi bahasa mesin iPhone.

Jika di lab sekolahmu hanya terdapat PC Windows, jangan khawatir. Mengetahui bahwa Flutter *bisa* digunakan untuk iPhone saja sudah merupakan wawasan mendasar yang cukup bagi seorang teknisi tingkat pemula.

## Perintah Dasar

Jika suatu saat kamu sudah bekerja dan difasilitasi MacBook oleh perusahaanmu, perintah untuk membungkus kodemu menjadi *file* iPhone sangatlah mirip dengan Android:

```bash
flutter build ipa
```

Setelah proses tersebut selesai, *file* aplikasimu akan siap untuk didistribusikan ke dalam ekosistem eksklusif App Store milik Apple.
