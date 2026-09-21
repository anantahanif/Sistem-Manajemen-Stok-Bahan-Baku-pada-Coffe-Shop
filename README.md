# Sistem Manajemen Stok Coffee Shop

## 1. Identitas Mahasiswa
* **Nama:** Ananta Hanif Fidzya Pratama
* **NIM:** 2509116023
* **Kelas:** Sistem Informasi A 2025

---

## 2. Penjelasan Studi Kasus
Aplikasi ini merupakan program berbasis Command Line Interface (CLI) menggunakan bahasa pemrograman Java dengan menerapkan konsep Object-Oriented Programming (OOP). Sistem ini berfungsi mengelola persediaan operasional pada usaha **Coffee Shop** yang terdiri dari tiga entitas utama, yaitu:
* **Bahan Baku:** Mengelola data persediaan stok bahan baku (misal: Biji Kopi, Susu, Sirup).
* **Supplier:** Mengelola data vendor pemasok bahan baku.
* **Resep SOP:** Mengelola data takaran porsi pembuatan minuman standar bar.

Aplikasi ini menyediakan fitur manipulasi data CRUD (Create, Read, Update, Delete) tanpa adanya modul transaksi jual-beli.

---

## 3. Diagram Kelas & Hierarki Class

### Hierarki Class (Diagram Sederhana)
```text
               +-------------------+
               |   model.Entitas   |  <--- (Super-Class)
               +-------------------+
               | # id : int        |
               | # nama : String   |
               +-------------------+
                         ^
                         | (extends)
      +------------------+------------------+
      |                  |                  |
+--------------+  +--------------+  +--------------+
|  BahanBaku   |  |   Supplier   |  |    Resep     |  <--- (Sub-Classes)
+--------------+  +--------------+  +--------------+
| - stok       |  | - noTelepon  |  | - ukuranPorsi|
| - satuan     |  | - alamat     |  | - takaran    |
+--------------+  +--------------+  +--------------+
```
**Peran Masing-Masing Class**
* Entitas.java (Super-Class): Kelas induk di package model yang menampung atribut dasar (id dan nama).

* BahanBaku.java (Sub-Class): Turunan dari Entitas dengan atribut tambahan stok dan satuan.

* Supplier.java (Sub-Class): Turunan dari Entitas dengan atribut tambahan noTelepon dan alamat.

* Resep.java (Sub-Class): Turunan dari Entitas dengan atribut tambahan ukuranPorsi dan takaranBahan.

* Service.java (Logic Class): Mengelola daftar data (ArrayList) dan operasi logika CRUD.

* SistemManajemenStokBahanBaku.java (Main Class): Berisi menu interaktif while dan switch-case sebagai entry point program.
---
## 4. Penjelasan Penerapan Inheritance
**Penerapan konsep Inheritance (Pewarisan) pada program ini meliputi:**

* Penggunaan Keyword extends: Class BahanBaku, Supplier, dan Resep menggunakan sintaks extends Entitas untuk mewarisi atribut dari class Entitas.

* Access Modifier protected: Atribut id dan nama di kelas Entitas menggunakan modifier protected agar dapat diakses langsung oleh sub-class turunannya.

* Pemanggilan super() Constructor: Setiap sub-class memanggil super(id, nama) di baris pertama constructor-nya untuk meneruskan nilai ID dan Nama ke super-class Entitas.
---
## 5. Tangkapan Layar (Screenshot) Running Program
A. Tampilan Menu Utama & Tambah Data

<img width="484" height="284" alt="Screenshot 2026-09-21 222906" src="https://github.com/user-attachments/assets/48f1f7ba-d78d-4977-9d73-e80940263650" />
<img width="637" height="465" alt="Screenshot 2026-09-21 222959" src="https://github.com/user-attachments/assets/94e991d7-9bc8-4192-99e8-04efdf1437d3" />

B. Tampilkan Data

<img width="637" height="465" alt="Screenshot 2026-09-21 222959" src="https://github.com/user-attachments/assets/804a045f-5de5-4820-9891-682b0975413b" />

C. Update & Hapus Data

<img width="630" height="397" alt="Screenshot 2026-09-21 223152" src="https://github.com/user-attachments/assets/f88faa39-00ad-4b8d-9a08-79151142df4c" />
<img width="544" height="425" alt="Screenshot 2026-09-21 223127" src="https://github.com/user-attachments/assets/613e0242-5e61-46a4-8969-d1f9d9eccc2c" />
