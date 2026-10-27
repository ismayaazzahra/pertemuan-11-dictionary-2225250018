# Pertemuan 11 Dictionary/Map Python

## Identitas

Nama: Ismaya Catur Dewi Azzahra
NIM: 2225250018
Kelas: 3A

## Tujuan

Tujuan dari tugas ini adalah mempelajari penggunaan dictionary pada Python untuk menyimpan data berbentuk pasangan key-value, mengakses data berdasarkan key, menambah, mengubah, dan menelusuri isi dictionary, serta mencegah `KeyError` ketika key tidak ditemukan.

## Cara Menjalankan Program

Program dijalankan melalui VS Code menggunakan Python.

Langkah-langkah:

1. Buka folder `pertemuan-11-dictionary-2225250018` di VS Code.
2. Buka terminal dan pastikan posisi terminal berada di folder utama proyek.
3. Jalankan program dengan perintah berikut.

```bash
python3 praktik/data_mahasiswa.py
```

4. Periksa hasil program berdasarkan test case yang diberikan.

## Struktur Data

Data mahasiswa disimpan dalam dictionary `data_mahasiswa`. NIM dipakai sebagai key karena nilainya unik untuk setiap mahasiswa, sedangkan value berupa dictionary yang berisi nama, kelas, dan nilai.

| Bagian | Contoh | Keterangan |
| --- | --- | --- |
| Key | `"A001"` | NIM mahasiswa |
| Value | `{"nama": "Ayu", "kelas": "A", "nilai": 85}` | Data mahasiswa |

## Algoritma Latihan 2

1. Siapkan dictionary `data_mahasiswa` yang berisi 5 mahasiswa.
2. Buat fungsi `cari_mahasiswa(data, nim)` yang menggunakan `get()`.
3. Buat fungsi `rata_rata_nilai(data)` untuk menghitung rata-rata nilai.
4. Cari NIM yang ada dan NIM yang tidak ada.
5. Jika data tidak ditemukan, tampilkan pesan `Data tidak ditemukan`.
6. Tambahkan mahasiswa baru dengan NIM `A006`.
7. Ubah nilai mahasiswa `A002` menjadi 82.
8. Tampilkan seluruh data menggunakan `items()`.
9. Hitung dan tampilkan rata-rata nilai kelas dengan dua angka di belakang koma.

## Pengujian

| Test Case | Input/Aksi | Hasil yang Diharapkan | Hasil Aktual | Status |
| --- | --- | --- | --- | --- |
| 1 | Cari `A003` | Data Citra ditampilkan | `{'nama': 'Citra', 'kelas': 'B', 'nilai': 92}` | PASS |
| 2 | Cari `A999` | Pesan `Data tidak ditemukan` | `Data tidak ditemukan` | PASS |
| 3 | Ubah nilai `A002` menjadi 82 | Nilai `A002` menjadi 82 | Nilai `A002` = 82 | PASS |
| 4 | Tambah `A006` | Key `A006` tersedia | `"A006" in data_mahasiswa` bernilai `True` | PASS |
| 5 | Rekap dengan `items()` | Semua NIM dan data tampil | `A001` sampai `A006` tampil | PASS |
| 6 | Rata-rata nilai | 83.50 | `Rata-rata = 83.50` | PASS |

## Refleksi

Salah satu kesalahan yang dapat terjadi pada dictionary adalah mengakses key yang tidak ada, misalnya `data_mahasiswa["A999"]`, sehingga program berhenti dengan `KeyError`. Kesalahan tersebut dapat diperbaiki dengan menggunakan `get()` atau memeriksa key terlebih dahulu dengan operator `in` sebelum datanya ditampilkan.