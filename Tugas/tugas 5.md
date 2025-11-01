## 🧩 **Tugas Praktik CRUD Menggunakan Query Builder**

### 🎯 **Tujuan**

Mahasiswa mampu menerapkan operasi **Create, Read, Update, dan Delete (CRUD)** menggunakan konsep **Query Builder** dalam PHP dengan koneksi **MySQL**.

---

### 📘 **Kasus: Manajemen Koleksi Film**

Anda diminta untuk membuat **aplikasi manajemen data film** sederhana menggunakan PHP dan Query Builder.
Aplikasi ini bertujuan untuk mengelola daftar film yang dimiliki oleh sebuah studio kecil.

---

### 🗂️ **Spesifikasi Tabel (MySQL)**

Buat database dengan nama `db_filmku` dan tabel `film` dengan struktur berikut:

| Nama Kolom  | Tipe Data    | Keterangan                                |
| ----------- | ------------ | ----------------------------------------- |
| id          | INT (11)     | Primary Key, Auto Increment               |
| judul       | VARCHAR(100) | Judul film                                |
| genre       | VARCHAR(50)  | Jenis film (misal: Drama, Action, Komedi) |
| tahun_rilis | YEAR         | Tahun rilis film                          |
| rating      | DECIMAL(2,1) | Nilai rating film (misal: 8.5)            |

---

### ⚙️ **Fungsi yang Harus Dibuat**

1. **Tambah Data Film**

   * Menyimpan data baru ke tabel `film` menggunakan Query Builder.

2. **Tampilkan Semua Film**

   * Menampilkan seluruh data film dalam bentuk tabel HTML.

3. **Edit Data Film**

   * Menampilkan form untuk mengedit data yang sudah ada.
   * Menyimpan perubahan data ke database menggunakan Query Builder.

4. **Hapus Data Film**

   * Menghapus data film berdasarkan `id`.

---

### 🧱 **Struktur Folder Disarankan**

```
project_film/
│
├── config/
│   └── database.php        → Koneksi ke MySQL
│
├── core/
│   └── QueryBuilder.php    → Class Query Builder (insert, update, delete, select)
│
├── model/
│   └── FilmModel.php       → Implementasi fungsi CRUD (gunakan QueryBuilder)
│
├── views/
│   ├── form_tambah.php
│   ├── form_edit.php
│   └── tampil_data.php
│
└── index.php               → Routing sederhana (navigasi antar fitur)
```

---

### 💡 **Petunjuk Teknis**

* Query Builder minimal memiliki fungsi:

  * `insert($table, $data)`
  * `update($table, $data, $where)`
  * `delete($table, $where)`
  * `select($table, $where = [])`
* Gunakan `PDO` untuk koneksi database.
* Gunakan prepared statements untuk keamanan (hindari SQL Injection).
* Tampilan boleh dibuat sederhana menggunakan HTML dan Bootstrap.

---

### 📄 **Output yang Diharapkan**

1. Tampilan tabel data semua film.
2. Form untuk menambah dan mengedit film.
3. Aksi hapus yang berjalan dengan benar.
4. Struktur kode rapi dengan pembagian file sesuai fungsinya.
