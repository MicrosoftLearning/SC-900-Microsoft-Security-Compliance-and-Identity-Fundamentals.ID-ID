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

Di lab ini, Anda akan melalui langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, termasuk menyiapkan izin peran, membuat kasus eDiscovery, membuat penangguhan eDiscovery, dan membuat kueri pencarian.  Catatan: Lisensi untuk eDiscovery (Standar) memerlukan langganan organisasi yang sesuai dan lisensi per pengguna. Jika Anda tidak yakin lisensi mana yang mendukung eDiscovery (Standar), kunjungi [Memulai eDiscovery (Standar) di Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Perkiraan Waktu**: 45 menit

### Tugas 1

Untuk mengakses eDiscovery (Standar) atau agar ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Dalam tugas ini, Anda sebagai admin global, akan menambahkan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**, lalu pilih **Kepatuhan**.  Halaman browser baru terbuka ke halaman selamat datang portal Microsoft Purview.  

1. Dari panel navigasi kiri, pilih **Pengaturan**, perluas **Peran dan cakupan**, lalu pilih **Grup peran**.

1. Di bidang pencarian, di bagian atas, kanan halaman, masukkan **eDiscovery** lalu tekan Enter di keyboard Anda.  Pilih **Manajer eDiscovery**.

1. Pilih **Edit**. Untuk tujuan lab ini, Anda akan menetapkan diri Anda sebagai administrator MOD sebagai Manajer eDiscovery dan administrator.  Dalam praktiknya, Anda akan menunjuk pengguna tertentu untuk peran tertentu.
    1. Laman "Kelola Manajer eDiscovery" memungkinkan Anda menambahkan pengguna ke peran manajer eDiscovery.
    1. Pilih **Pilih pengguna**. Cari dan pilih **Administrator** MOD lalu tekan **Pilih** di bagian bawah halaman, lalu pilih **Berikutnya**.
    1. Pada laman "Kelola Administrator eDiscovery", pilih **Pilih pengguna** . Cari dan pilih **Administrator** MOD lalu tekan **Pilih** di bagian bawah halaman, lalu pilih **Berikutnya** lalu **Simpan**.
    1. Pada laman "Anda berhasil memperbarui grup peran", pilih **Selesai**.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda sebagai Administrator eDiscovery (admin MOD adalah administrator eDiscovery) akan membuat kasus untuk mulai menggunakan eDiscovery (Standar).

1. Anda harus tetap berada di laman peran portal kepatuhan. Jika Anda menutup tab browser dari tugas sebelumnya, buka tab browser baru dan masukkan **compliance.microsoft.com** untuk masuk ke portal Microsoft Purview.

1. Dari panel navigasi kiri, di bawah Solusi, perluas **eDiscovery** lalu pilih **Kasus** Standar.

1. Dari bagian atas laman eDiscovery (Standar), pilih **+ Buat kasus**.

1. Di jendela Kasus baru, masukkan Nama kasus, **SC900 Test Case**, lalu pilih **Simpan** di bagian bawah laman.

1. Sekarang, kasus akan muncul dalam daftar.

1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### Tugas 3

Sekarang, setelah Anda membuat kasus eDiscovery (Standar), Anda dapat mulai bekerja dengan kasus tersebut.  Dalam tugas ini, Anda akan membuat penangguhan eDiscovery untuk kasus yang Anda buat.  Khususnya, Anda akan membuat penangguhan untuk kotak surat exchange milik Adele Vance.

1. Buka tab eDiscovery (Standar) di browser Anda.

1. Dari halaman eDiscovery (Standar), pilih kasus yang Anda buat di tab sebelumnya, **Kasus Pengujian SC900**.

1. Dari laman Beranda kasus, pilih tab **Penangguhan**, lalu pilih **+Buat**.

1. Di kolom nama, masukkan **Penangguhan pengujian**, lalu pilih **Berikutnya**.

1. Di laman Pilih lokasi, pilih tombol pengalih di samping **kotak surat Exchange** untuk mengatur status ke **Aktif**.  

1. Sekarang pilih **Pilih pengguna, grup, atau tim**.  Di Kotak pencarian, masukkan **Adele**, lalu tekan Enter di keyboard Anda. Dari hasil pencarian, pilih **Adele Vance**, lalu pilih **Selesai**.

1. Pada halaman Pilih Lokasi, pilih **Berikutnya**.  Untuk kecocokan dengan lab, tidak ada lokasi lain yang akan disertakan dalam penangguhan ini.

1. Halaman Kondisi kueri memungkinkan Anda membuat penangguhan untuk item berdasarkan kueri yang bisa Anda buat.  Anda bisa memilih untuk menggunakan penyusun Kueri untuk membuat kueri atau untuk pengguna tingkat lanjut lainnya, Anda bisa menggunakan editor KQL. Untuk latihan ini, Anda ingin penangguhkan mempertahankan semua konten di lokasi yang ditentukan untuk pengguna yang ditentukan, sehingga Anda tidak akan membuat kueri.

1. Tinjau pengaturan Anda dan pilih **Kirim**, mungkin perlu waktu satu menit, lalu pilih **Selesai**.  Penangguhan pengujian akan muncul dalam daftar.  Jika Anda tidak segera melihatnya, pilih **Refresh**

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### Tugas 4

Setelah memasukkan penangguhan, Anda akan membuat kueri pencarian.  Setelah pencarian Anda selesai, eDiscovery mendukung tindakan, seperti mengekspor dan mengunduh hasil untuk penyelidikan di masa mendatang.   Catatan: Pencarian yang terkait dengan kasus eDiscovery (Standar) tidak tercantum di halaman Pencarian konten di portal Microsoft Purview. Pencarian ini hanya terdaftar di laman Pencarian dari kasus eDiscovery (Standar) terkait.

1. Buka tab Kasus Uji SC900 di browser Anda.

1. Dari laman Kasus Uji SC900, pilih **Pencarian**.

1. Dari halaman Pencarian, pilih **+ Pencarian Baru**.

1. Di bidang Nama, masukkan **Penangguhan Pengujian – Pencarian Penjualan**, lalu pilih **Berikutnya** dari bagian bawah laman.

1. Di laman Pilih lokasi, pilih **lokasi yang ditangguhkan** dan batalkan pilihan **Tambahkan Konten Aplikasi untuk pengguna Lokal**, karena lingkungan lab Anda tidak memiliki pengguna lokal, maka pilih **Berikutnya **.

1. Laman Syarat kueri memungkinkan Anda membuat penangguhan, berdasarkan Kata Kunci atau Syarat tertentu yang dipenuhi. Pada bidang kata kunci, masukkan **Penjualan**, pilih **Berikutnya**.

1. Tinjau pengaturan Anda dan pilih **Kirim**, mungkin perlu waktu satu menit, lalu pilih **Selesai**.  Pencarian akan muncul dalam daftar.  Jika Anda tidak segera melihatnya, pilih **Refresh**

1. Dari jendela Pencarian, pilih pencarian yang Anda buat, **Penangguhan pengujian - Pencarian Penjualan**.  Jendela akan terbuka dengan tab Ringkasan yang dipilih.  Setelah pencarian selesai, status akan menunjukkan bahwa pencarian selesai.  Anda akan melihat tab Statistik pencarian (jika Anda tidak melihat tab Statistik pencarian, pencarian mungkin masih berjalan dan mungkin perlu waktu beberapa menit hingga selesai).  Pilih tab **Statistik pencarian** dan pilih menu Menurun di samping Cari konten.  Anda juga dapat melihat informasi selengkapnya untuk Laporan syarat dan Lokasi teratas.  

1. Di bagian bawah halaman, pilih **Tindakan**.  Perhatikan opsi tersedia yang menyertakan opsi ekspor (opsi ekspor tidak dapat dipilih dari dalam platform lab yang disediakan oleh host lab resmi, tetapi tersedia di lingkungan produksi dan dianggap sebagai bagian dari alur kerja standar). Pilih **Tutup.**

1. Keluar dan tutup semua jendela browser yang terbuka.

### Tinjauan

Di lab ini, Anda telah melakukan langkah-langkah yang diperlukan untuk memulai eDiscovery (Standar), termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dengan kasus itu, Anda telah menelusuri elemen alur kerja eDiscovery (Standar) dengan membuat penangguhan eDiscovery dan membuat kueri pencarian.
