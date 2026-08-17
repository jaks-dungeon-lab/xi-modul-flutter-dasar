# Navigation (Perpindahan Halaman)

Sebuah aplikasi dalam dunia nyata umumnya memiliki lebih dari satu halaman. Misalnya, jika pengguna menekan nama siswa, mereka seharusnya berpindah ke layar baru yang menampilkan detail lengkap siswa tersebut.

Di dalam Flutter, mekanisme berpindah layar ini disebut **Navigation** atau **Routing**.

## 1. Berpindah ke Halaman Baru (Push)

Untuk membuka dan menumpuk halaman baru, kita menggunakan perintah **`Navigator.push`**.

```dart
ElevatedButton(
  onPressed: () {
    Navigator.push(
      context,
      MaterialPageRoute(
        builder: (context) => const HalamanDetailProfilSiswa(),
      ),
    );
  },
  child: const Text('Buka Lembar Detail Siswa'),
)
```
- `MaterialPageRoute` berfungsi memberikan animasi perpindahan layar otomatis yang halus (seperti bergeser dari samping atau memudar terang).

## 2. Kembali ke Halaman Sebelumnya (Pop)

Untuk menutup halaman saat ini dan kembali mundur ke layar sebelumnya, kita menggunakan perintah **`Navigator.pop`**.

```dart
TextButton(
  onPressed: () {
    Navigator.pop(context); // Menutup layar ini
  },
  child: const Text('Kembali ke Halaman Sebelumnya'),
)
```

**Catatan:** Saat kamu menggunakan `Scaffold` yang memiliki `AppBar`, Flutter secara otomatis akan menampilkan ikon tombol panah "*Back*" di ujung kiri atas layar jika halaman tersebut baru saja dibuka lewat metode *push*. Jadi, kamu jarang perlu menuliskan kode `Navigator.pop` secara manual kecuali jika membuat tombol kustom sendiri.
