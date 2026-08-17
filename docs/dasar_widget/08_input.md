# Input (Kolom Isian)

Jika tombol adalah cara aplikasi mendengarkan ketukan darimu, maka kolom isian adalah cara aplikasi mendengarkan kata-kata darimu. Di Flutter, untuk membuat tempat pengetikan teks, kita menggunakan *widget* **TextField**.

## Penggunaan Dasar TextField

Untuk menampilkan kolom isian yang sangat sederhana, kamu cukup memanggil kode ini:

```dart
TextField()
```

Namun, kolom kosong berbentuk garis bawah saja tentu akan membingungkan pengguna. Kita butuh dekorasi (`decoration`) agar pengguna mengerti apa fungsi kolom tersebut (misalnya untuk pencarian).

## Memberi Dekorasi dan Label

Kita bisa mempercantik kolom isian dengan menambahkan garis tepi yang melengkung, ikon kaca pembesar, dan teks petunjuk samar yang disebut *hint text*:

```dart
TextField(
  decoration: InputDecoration(
    prefixIcon: const Icon(Icons.search), // Ikon di sebelah kiri dalam kotak
    hintText: 'Cari nama siswa...', // Teks bantuan yang samar
    border: OutlineInputBorder(
      borderRadius: BorderRadius.circular(10), // Pinggiran kotak membulat
    ),
  ),
)
```

Nantinya, dalam pembuatan aplikasi tingkat lanjut, *widget* `TextField` ini wajib dipasangkan dengan `TextEditingController`. Pengontrol tersebut berfungsi menangkap dan menyimpan kata yang diketik pengguna agar bisa diproses lebih lanjut oleh logika program (misalnya untuk menyaring daftar absen).
