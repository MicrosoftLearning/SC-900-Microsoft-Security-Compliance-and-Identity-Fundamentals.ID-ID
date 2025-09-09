<!---
---
Demo: Judul: 'Jelajahi Jalur Pembelajaran/Modul/Unit eDiscovery': 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview; Modul 3: Menjelaskan solusi kepatuhan data Microsoft Purview; Unit 2: Menjelaskan eDiscovery'
---
--->

# Demo: Jelajahi eDiscovery (Standar)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan kemampuan solusi kepatuhan Microsoft Purview
- Unit: Menjelaskan eDiscovery

## Skenario demo

Di Demo ini, Anda akan mempelajari langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, termasuk menyiapkan izin peran, membuat kasus eDiscovery, membuat penangguhan eDiscovery, dan membuat kueri pencarian.  CATATAN: Di portal Microsoft Purview pembaruan untuk antarmuka pengguna diluncurkan, secara bertahap. Beberapa penyewa lab/demo mungkin belum menampilkan UI terbaru, sehingga semua langkah lab ditampilkan menggunakan UI eDiscovery Klasik.

### Demo Bagian 1

Untuk mengakses eDiscovery atau ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Di bagian demo ini, Anda sebagai admin global, akan mempelajari proses penambahan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

1. Buka tab browser untuk **Microsoft Purview**. Jika sebelumnya Anda menutupnya, buka tab browser dan di bilah alamat, masukkan **https://purview.microsoft.com** lalu pilih **Mulai.**  
1. Dari panel navigasi kiri, pilih **Pengaturan**.
1. Dari panel navigasi yang terbuka, pilih **Peran dan cakupan** untuk memperluas opsi, lalu pilih **Grup** peran.
1. Di kotak pencarian di sisi kanan layar, cari pada istilah **eDiscovery**.  Pilih **Manajer eDiscovery**.
    1. Pilih **Edit**.
    1. Pilih **Pilih pengguna**.
    1. Cari Administrator MOD, pilih kotak di samping **Administrator** MOD lalu pilih tombol **Pilih** di bagian bawah halaman.
    1. Pilih **Berikutnya** lalu pilih **Simpan**, lalu akhirnya pilih **Selesai**.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Di bagian ini Anda, sebagai Administrator eDiscovery (admin MOD adalah administrator eDiscovery), akan membuat kasus untuk mulai menggunakan eDiscovery.

1. Anda harus berada di beranda portal Microsoft Purview.

1. Dari panel navigasi kiri, di bawah Solusi, perluas **eDiscovery** lalu pilih Kasus.****

1. Dari halaman Kasus, pilih **Buat kasus**.

1. Di jendela Kasus baru, masukkan Nama kasus, **SC900 Test Case** lalu pilih Buat****.

1. Sekarang, kasus akan muncul dalam daftar.

1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### Demo Bagian 3

Dengan kasus yang dibuat, Anda dapat mulai bekerja dengan kasus tersebut. Ini termasuk membuat kueri pencarian untuk menemukan data dan konten yang relevan dengan kasus Anda, menerapkan kebijakan penangguhan, membuat kumpulan tinjauan, dan mengekspor data. Dalam tugas ini Anda akan menjelajahi beberapa opsi ini. CATATAN: Disarankan agar Anda melalui pembuatan pencarian dan tinjauan yang ditetapkan sebelum pengiriman sehingga hasil set pencarian dan tinjauan tersedia selama demo, karena tindakan ini dapat memakan waktu beberapa menit untuk diselesaikan.  

1. Buka tab Kasus Uji SC900 di browser Anda.

1. Dari halaman Kasus Pengujian SC900, pilih  **Buat pencarian**.

1. Di bidang nama, masukkan **pencarian** kasus SC900 lalu pilih **Buat**.

1. Pilih **Tambahkan sumber**. Perhatikan opsi filter dan pengaturan default. Dalam kotak pencarian, masukkan **`Pradeep`** lalu pilih **Cari.** Dari hasil pencarian pilih **Pradeep Gupta**, lalu pilih **Simpan dan tutup**. Penyusun Kondisi memungkinkan Anda membuat kueri pencarian berdasarkan Kata Kunci atau Kondisi tertentu yang terpenuhi, Dalam kotak kata kunci, masukkan **Penjualan**. Dari sini Anda bisa memilih untuk **Menjalankan kueri**, Dari jendela Pilih hasil pencarian. Untuk penyewa lab, hanya tampilan statistik hasil pencarian yang tersedia. Perhatikan opsi untuk mengatur menurut indikator atas. Pilih **Jalankan kueri**.  Proses ini mungkin memerlukan waktu beberapa menit.

1. Dengan hasil kueri yang dikembalikan dalam bentuk statistik, Anda dapat mengekspor hasil.  Dari kanan atas layar (di samping tempat tertulis Tambahkan untuk meninjau set), pilih **Ekspor** ke opsi vew yang tersedia lalu pilih **Batal**.

1. Anda dapat menambahkan ke kumpulan ulasan untuk pemrosesan lebih lanjut.  Pilih **Tambahkan untuk meninjau set**. Masukkan nama untuk kumpulan tinjauan baru, **`SC900-review-set`**, biarkan pengaturan default, lalu pilih **Tambahkan untuk meninjau set.** Proses ini bisa memerlukan waktu beberapa menit. Setelah hasil kumpulan ulasan disajikan, Anda dapat menjelajahi berbagai opsi, yang mencakup Analitik, Kueri, Tindakan, File tag, dan Kelola.

1. Anda juga dapat membuat kebijakan penahanan untuk mempertahankan konten yang relevan dengan kasus Anda. Dari jendela Tinjau set, pilih tab Tangguhkan****.  Ini akan membawa Anda ke jendela Kebijakan penangguhkan. Pilih **Kebijakan baru**.  Masukkan Nama kebijakan, **`SC900-hold`**, dan pilih **Buat.**  Seperti dalam pencarian, Anda perlu menambahkan sumber data untuk penangguhkan dan Anda dapat menambahkan kata kunci dan kondisi yang akan digunakan dalam kebijakan penahanan, lalu Anda dapat memilih **Terapkan penangguhan**.  Tindakan yang dapat Anda ambil pada kebijakan penangguhan termasuk mencoba kembali, menonaktifkan kebijakan, dan menghapus kebijakan penangguhan.

1. Keluar dan tutup semua jendela browser yang terbuka.

### Tinjauan

Dalam demo ini, Anda melalui langkah-langkah yang diperlukan untuk mulai menggunakan eDiscovery, termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dengan kasus ini, membuat Anda menjelajahi pengaturan untuk membuat pencarian dan mengekspor hasil, menambahkan ke kumpulan tinjauan, dan membuat penangguhan.
