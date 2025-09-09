---
lab:
  title: Menjelajahi eDiscovery
  module: Describe the data compliance solutions of Microsoft Purview
---

# Lab: Jelajahi eDiscovery

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan kemampuan solusi kepatuhan Microsoft Purview
- Unit: Menjelaskan eDiscovery

## Skenario lab

Di lab ini, Anda akan melalui langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, termasuk menyiapkan izin peran, membuat kasus eDiscovery, membuat penangguhan eDiscovery, dan membuat kueri pencarian.  Catatan: Lisensi untuk eDiscovery memerlukan langganan organisasi dan lisensi per pengguna yang sesuai. Jika Anda tidak yakin lisensi mana yang mendukung eDiscovery, kunjungi [Mulai menggunakan eDiscovery di Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Perkiraan Waktu**: 45 menit

### Tugas 1

Untuk mengakses eDiscovery atau ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Dalam tugas ini, Anda sebagai admin global, akan menambahkan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

1. Anda harus berada di beranda portal Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://purview.microsoft.com**.

1. Dari panel navigasi kiri, pilih **Pengaturan**, perluas **Peran dan cakupan**, lalu pilih **Grup peran**.

1. Di bidang pencarian, di bagian atas, kanan halaman, masukkan **eDiscovery** lalu tekan Enter di keyboard Anda.  Pilih **Manajer eDiscovery**.

1. Pilih **Edit**. Untuk tujuan lab ini, Anda akan menetapkan diri Anda sebagai administrator MOD sebagai Manajer eDiscovery dan administrator.  Dalam praktiknya, Anda akan menunjuk pengguna tertentu untuk peran tertentu.
    1. Laman "Kelola Manajer eDiscovery" memungkinkan Anda menambahkan pengguna ke peran manajer eDiscovery.
    1. Pilih **Pilih pengguna**. Cari dan pilih **Administrator** MOD lalu tekan **Pilih** di bagian bawah halaman, lalu pilih **Berikutnya**.
    1. Pada laman "Kelola Administrator eDiscovery", pilih **Pilih pengguna** . Cari dan pilih **Administrator** MOD lalu tekan **Pilih** di bagian bawah halaman, lalu pilih **Berikutnya** lalu **Simpan**.
    1. Pada laman "Anda berhasil memperbarui grup peran", pilih **Selesai**.

1. Kembali ke beranda Microsoft Purview dengan memilih **Beranda** dari panel navigasi kiri.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini Anda, sebagai Administrator eDiscovery (admin MOD adalah administrator eDiscovery), akan membuat kasus untuk mulai menggunakan eDiscovery.

1. Anda harus berada di beranda portal Microsoft Purview.

1. Dari panel navigasi kiri, di bawah Solusi, perluas **eDiscovery** lalu pilih Kasus.****

1. Dari halaman Kasus, pilih teks di bagian kiri kotak biru yang berbuah, **Buat huruf besar/kecil**.  Jika Anda memilih panah bawah, Anda akan membuka jendela untuk membuat pencarian dan dalam proses membuat pencarian akan membuat kasus.
    1. Di jendela Kasus baru, masukkan Nama kasus, **SC900 Test Case** lalu pilih Buat****.
    1. Sekarang, kasus akan muncul dalam daftar.
    1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  
    1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### Tugas 3

Dengan kasus yang dibuat, Anda dapat mulai bekerja dengan kasus tersebut. Ini termasuk membuat kueri pencarian untuk menemukan data dan konten yang relevan dengan kasus Anda, menerapkan kebijakan penangguhan, membuat kumpulan tinjauan, dan mengekspor data. Dalam tugas ini Anda akan menjelajahi beberapa opsi ini.

1. Buka tab Kasus Uji SC900 di browser Anda.

1. Dari halaman Kasus Pengujian SC900, pilih  **Buat pencarian**.

1. Di bidang nama, masukkan **pencarian** kasus SC900 lalu pilih **Buat**.

1. Pilih **Tambahkan sumber**. Perhatikan opsi filter dan pengaturan default. Dalam kotak pencarian, masukkan **`Pradeep`** lalu pilih **Cari.** Dari hasil pencarian pilih **Pradeep Gupta**, lalu pilih **Simpan dan tutup**. Penyusun Kondisi memungkinkan Anda membuat kueri pencarian berdasarkan Kata Kunci atau Kondisi tertentu yang terpenuhi, Dalam kotak kata kunci, masukkan **Penjualan**. Dari sini Anda bisa memilih untuk **Menjalankan kueri**, Dari jendela Pilih hasil pencarian. Untuk penyewa lab, hanya tampilan statistik hasil pencarian yang tersedia. Perhatikan opsi untuk mengatur menurut indikator atas. Pilih **Jalankan kueri**.  Proses ini mungkin memerlukan waktu beberapa menit.

1. Dengan hasil kueri yang dikembalikan dalam bentuk statistik, Anda dapat mengekspor hasil.  Pilih **Ekspor** untuk melakukan vew opsi yang tersedia, lalu pilih **Batalkan**.

1. Anda dapat menambahkan ke kumpulan ulasan untuk pemrosesan lebih lanjut.  Pilih **Tambahkan untuk meninjau set**. Masukkan nama untuk kumpulan tinjauan baru, **`SC900-review-set`**, biarkan pengaturan default, lalu pilih **Tambahkan untuk meninjau set.** Proses ini bisa memerlukan waktu beberapa menit. Setelah hasil kumpulan ulasan disajikan, Anda dapat menjelajahi berbagai opsi, yang mencakup Analitik, Kueri, Tindakan, File tag, dan Kelola.

1. Anda juga dapat membuat kebijakan penahanan untuk mempertahankan konten yang relevan dengan kasus Anda. Dari jendela Tinjau set, pilih tab Tangguhkan****.  Ini akan membawa Anda ke jendela Kebijakan penangguhkan. Pilih **Kebijakan baru**.  Masukkan Nama kebijakan, **`SC900-hold`**, dan pilih **Buat.**  Seperti dalam pencarian, Anda perlu menambahkan sumber data untuk penangguhkan dan Anda dapat menambahkan kata kunci dan kondisi yang akan digunakan dalam kebijakan penahanan, lalu Anda dapat memilih **Terapkan penangguhan**.  Tindakan yang dapat Anda ambil pada kebijakan penangguhan termasuk mencoba kembali, menonaktifkan kebijakan, dan menghapus kebijakan penangguhan.

1. Keluar dan tutup semua jendela browser yang terbuka.

### Tinjauan

Di lab ini, Anda melalui langkah-langkah yang diperlukan untuk memulai eDiscovery, termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dengan kasus ini, membuat Anda menjelajahi pengaturan untuk membuat pencarian dan mengekspor hasil, menambahkan ke kumpulan tinjauan, dan membuat penangguhan.
