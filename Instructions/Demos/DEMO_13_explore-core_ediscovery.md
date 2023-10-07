<!---
---
Demo: Judul: 'Jelajahi alur kerja eDiscovery (Standar) ' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 5: Menjelaskan kemampuan eDiscovery dan audit Microsoft Purview; Unit 2: Menjelaskan solusi eDiscovery di Microsoft 365'
---
--->

# Demo: Menjelajahi alur kerja eDiscovery (Standar)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan eDiscovery dan kemampuan audit Microsoft Purview
- Unit: Menjelaskan solusi eDiscovery di Microsoft Purview

## Skenario demo

Dalam demo ini Anda akan melakukan panduan langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, termasuk menyiapkan izin peran, membuat kasus eDiscovery, membuat penangguhan eDiscovery, dan membuat kueri pencarian.  Catatan:  Lisensi untuk eDiscovery (Standar) memerlukan langganan organisasi yang sesuai dan lisensi per pengguna. Jika Anda tidak yakin lisensi mana yang mendukung eDiscovery (Standar), kunjungi [Memulai eDiscovery (Standar) di Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

### Demo Bagian 1

Untuk mengakses eDiscovery (Standar) atau agar ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Di bagian demo ini, Anda sebagai admin global, akan berjalan melalui proses penambahan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

1. Buka tab browser untuk beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH). Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Kepatuhan**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi kiri, perluas (pilih panah bawah) **Peran & Cakupan** lalu pilih **Izin**.

1. Di bawah Solusi Microsoft Purview, pilih **Peran**.

1. Di bidang pencarian, masukkan **eDiscovery** lalu pilih ikon pencarian (kaca pembesar).  Pilih **eDiscovery Manager**.  Perhatikan peran dalam grup peran.

1. Pilih **Edit**.  Perhatikan bagaimana ada dua subgrup, Manajer eDiscovery dan Administrator eDiscovery.  
    1. Halaman "Kelola Manajer eDiscovery" memungkinkan Anda menambahkan pengguna ke peran manajer eDiscovery. Untuk demo ini, kami akan menambahkan anggota ke subgrup Administrator eDiscovery jadi pilih **Berikutnya**.
    1. Pada halaman "Kelola Administrator eDiscovery", pilih **Pilih pengguna** . Cari dan pilih **Administrator MOD** dan **Megan Bowen** lalu tekan **Pilih** di bagian bawah halaman, lalu pilih **Berikutnya** lalu **Simpan**.
    1. Pada halaman "Anda berhasil memperbarui grup peran", pilih **Selesai**.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Di bagian ini Anda, sebagai Administrator eDiscovery (admin MOD adalah administrator eDiscovery), akan membuat kasus untuk mulai menggunakan eDiscovery (Standar).

1. Anda harus tetap berada di halaman peran portal kepatuhan. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **eDiscovery** lalu pilih **Standar**.

1. Dari bagian atas halaman eDiscovery (Standar), pilih **+ Buat kasus**.

1. Di jendela Kasus baru, masukkan nama Kasus, **SC900 Test Case**, lalu pilih **Save** di bagian bawah halaman.

1. Kasus ini sekarang akan muncul dalam daftar.

1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  

1. Tetap buka tab browser ini.

### Demo Bagian 3

Sekarang setelah Anda membuat kasus eDiscovery (Standar), Anda dapat mulai bekerja dengan kasus tersebut.  Di bagian ini, Anda akan membuat penangguhan eDiscovery untuk kasus yang Anda buat.  Khususnya, Anda akan membuat penangguhan untuk kotak surat pertukaran milik Adele Vance.

1. Dari halaman eDiscovery (Standar) , pilih kasus yang Anda buat - **Kasus Pengujian SC900**.

1. Dari halaman Beranda kasus, pilih tab **Hold**, lalu pilih **+Create**.

1. Di kolom nama, masukkan **Penangguhan pengujian** lalu pilih **Berikutnya**.

1. Di halaman Pilih lokasi, pilih tombol pengalih di samping **kotak surat Exchange** untuk mengatur status ke **Aktif**.  

1. Sekarang pilih **Pilih pengguna, grup, atau tim**.  Di kotak pencarian, masukkan **Adele**, lalu tekan enter di keyboard. Dari hasil pencarian pilih **Adele Vance**, lalu pilih **Selesai**.

1. Dari halaman Pilih lokasi, pilih **Next**.  Untuk kedaluwarsa dengan demo, tidak ada lokasi lain yang akan disertakan dalam penangguhan ini.

1. Halaman Ketentuan kueri memungkinkan Anda membuat penangguhan, berdasarkan Kata Kunci atau Ketentuan tertentu yang dipenuhi, pilih **+ Tambahkan ketentuan** untuk melihat opsi yang tersedia.  Pilih **Selanjutnya**. Tanpa kondisi apa pun, penangguhan akan mempertahankan semua konten di lokasi yang ditentukan.

1. Tinjau pengaturan Anda dan pilih **Submit**, mungkin perlu satu menit, lalu pilih **Done**.  Penangguhan Test akan muncul di daftar.  Jika Anda tidak langsung melihatnya, pilih **Refresh**

1. Tetap buka tab browser ini.

### Demo Bagian 4

Dengan penangguhan, Anda akan membuat kueri pencarian.  Setelah pencarian Anda selesai, eDiscovery mendukung tindakan, seperti mengekspor dan mengunduh hasil untuk penyelidikan di masa mendatang.   Catatan:  Pencarian yang terkait dengan kasus eDiscovery (Standar) tidak terdaftar di halaman pencarian konten di portal kepatuhan Microsoft Purview. Pencarian ini hanya terdaftar di halaman Pencarian dari kasus eDiscovery (Standar) terkait.

1. Dari halaman Kasus Uji SC900, pilih **Pencarian**.

1. Dari halaman Pencarian, pilih **+ New Search**.

1. Di bidang Nama, masukkan **Test Hold – Sales Search**, lalu pilih **Next** dari bagian bawah halaman.

1. Di halaman Pilih lokasi, pilih **lokasi yang ditangguhkan** dan batalkan pilihan **Tambahkan Konten Aplikasi untuk pengguna Lokal**, karena lingkungan lab Anda tidak memiliki pengguna lokal, lalu pilih **Berikutnya** .

1. Halaman kondisi kueri memungkinkan Anda membuat pencarian, berdasarkan Kata Kunci atau Ketentuan tertentu yang dipenuhi. Di bidang kata kunci masukkan **Sales**, pilih **Next**.

1. Tinjau pengaturan Anda dan pilih **Submit**, mungkin perlu satu menit, lalu pilih **Done**.  Pencarian akan muncul di daftar.  Jika Anda tidak langsung melihatnya, pilih **Refresh**

1. Dari jendela Pencarian, pilih pencarian yang Anda buat, **Penangguhan pengujian - Pencarian Penjualan**.  Jendela yang terbuka dengan tab Ringkasan dipilih.  Setelah pencarian selesai, status akan menunjukkan bahwa pencarian selesai.  Anda akan melihat tab Statistik pencarian (jika Anda tidak melihat tab Statistik pencarian, pencarian mungkin masih berjalan dan mungkin perlu waktu beberapa menit hingga selesai).  Pilih tab **Statistik pencarian** dan pilih panah bawah di samping Cari konten.  Anda juga dapat melihat informasi selengkapnya untuk laporan Kondisi dan Lokasi teratas.  

1. Dari bagian bawah halaman, pilih **Actions**.  Perhatikan opsi yang tersedia yang menyertakan opsi ekspor. Pilih **Tutup**.

1. Tutup semua tab browser yang terbuka.

### Tinjau

Dalam demo ini, Anda melalui langkah-langkah yang diperlukan untuk memulai eDiscovery (Standar), termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dengan kasus yang dibuat, Anda menelusuri elemen alur kerja eDiscovery (Standar) dengan membuat penangguhan eDiscovery dan membuat kueri pencarian.
