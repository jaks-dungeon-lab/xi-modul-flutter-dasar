# Kelas XI - Flutter Dasar

[![Flutter](https://img.shields.io/badge/Flutter-Framework-02569B.svg)](https://flutter.dev/)

Repositori ini berisi modul pembelajaran interaktif berbasis web untuk siswa Kelas XI SMK bidang Rekayasa Perangkat Lunak (RPL). *Course* ini dirancang khusus dengan pendekatan berbasis proyek (*Project-Based Learning*) untuk membimbing siswa dari konsep awal desain *layout* hingga sanggup merancang dan merilis aplikasi *mobile* modern menggunakan *framework* **Flutter**.

## Fitur Utama Modul

- **Pendekatan Analogi:** Konsep antarmuka teknis (*Widget*, *State*, dan *Layout*) selalu diibaratkan dengan hal fisik seperti menyusun balok Lego.
- **Project-Based Learning:** Setiap teori yang dipelajari langsung diterapkan dan digabungkan menjadi sebuah aplikasi nyata yang dapat dilihat hasilnya (contoh: Aplikasi Daftar Siswa).
- **Kuis Interaktif Vanilla:** Dilengkapi dengan kuis mandiri di setiap akhir materi untuk menguji pemahaman teori siswa secara instan.
- **Adaptif Dark Mode:** Menggunakan tema *MkDocs Material* yang indah dengan pergantian mode terang/gelap otomatis.
- **Tugas Akhir Mandiri:** Dilengkapi dengan instruksi dan standar kelulusan yang jelas di akhir bab untuk merancang proyek mandiri berskala besar.

## Struktur Kurikulum

Materi disusun secara sistematis (*step-by-step*):
1. **Dasar-dasar Flutter:** Pengenalan Arsitektur, Instalasi *Tools*, dan Anatomi Direktori Proyek.
2. **Dasar Widget (Stateless):** Scaffold, Padding, Center, Container, Row & Column, Button, Text, dan Image.
3. **Dasar Widget (Stateful):** Pemahaman *State*, Input (TextField), dan Reaktivitas Layar.
4. **List & Navigation:** Menampilkan data berulang (`ListView.builder`) dan perpindahan antar layar (`Navigator`).
5. **Deployment:** Pembuatan paket aplikasi (*Build*) menjadi format rilis Android (APK), iOS (IPA), dan Web.

## Cara Menjalankan Secara Lokal (*Local Development*)

Untuk menjalankan *website course* ini di komputermu sendiri:

1. Pastikan kamu sudah menginstal [Python](https://www.python.org/downloads/) dan `pip`.
2. Instal MkDocs dan Tema Material melalui terminal:
   ```bash
   pip install mkdocs mkdocs-material
   ```
3. *Clone* repositori ini:
   ```bash
   git clone <url-repo-github>
   cd kelas_xi_flutter_dasar
   ```
4. Jalankan server lokal:
   ```bash
   mkdocs serve
   ```
5. Buka browser dan akses `http://127.0.0.1:8000`.
