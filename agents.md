# Aturan Proyek Kelas XI Flutter Roadmap

Ikuti panduan ini saat tambah/ubah materi web kursus.

## Struktur File

- Simpan file materi (*Markdown*) di dalam sub-folder spesifik di `docs/`.
- Simpan gambar/aset di `docs/assets/`. 
- Setiap penambahan halaman baru **wajib didaftarkan** pada bagian `nav` di `mkdocs.yml`.

## Format Penulisan

Gunakan bahasa Indonesia yang jelas, singkat, dan langsung ke inti (ditargetkan untuk siswa kelas XI SMK).

- **Tanpa Emoji**: Dilarang keras menggunakan ikon/emoji di dalam teks.
- **Wajib Analogi**: Untuk materi yang sulit dipahami, selalu sertakan penjelasan dengan tajuk **Analogi:** yang mengibaratkan konsep *coding* dengan kehidupan sehari-hari. 
- **Cetak Tebal**: Gunakan *bold* (`**teks**`) pada kata-kata kunci.
- **Format Bullet Point**: Wajib memberikan jarak satu baris kosong (*enter/newline*) sebelum memulai daftar *bullet list* (`- ` atau `1. `) agar ter-*render* benar di MkDocs.
- **Standar Kuis**: Pembuatan kuis harus menggunakan HTML *vanilla* (tanpa compiler eksternal) dan wajib mengatur warna UI dengan metode transparan (`rgba()` atau `inherit`) agar secara otomatis beradaptasi dengan *Light/Dark Mode* tema *Material*. Format dan sistem logika kuis **wajib** menggunakan sistem pengecekan per-soal (tombol cek di setiap soal) dengan objek `quizData` untuk memberikan balikan (*feedback*) penjelasan spesifik pada setiap opsi jawaban, persis seperti sistem pada materi Dart Dasar.

## Penamaan File dan Folder

Gunakan huruf kecil seluruhnya, dan pisahkan kata dengan garis bawah (**`snake_case`**).

**Sangat Penting:** Setiap file materi di dalam sebuah bab **WAJIB** diawali dengan dua digit angka urutan, dan penghitungan selalu mutlak **dimulai dari `00_`**.

- ✅ **Contoh Benar**: `00_pengenalan.md`, `01_variabel_tipe_data.md`
- ❌ **Contoh Salah**: `00-pengenalan.md` (*kebab-case*), `1_Pengenalan.md` (huruf besar), `variabel_tipe_data.md` (tanpa urutan angka)
