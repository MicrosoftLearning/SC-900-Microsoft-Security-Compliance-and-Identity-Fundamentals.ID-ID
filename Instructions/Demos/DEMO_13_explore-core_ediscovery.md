<!---
---
Demo: Judul: 'Jelajahi Jalur Pembelajaran/Modul/Unit eDiscovery': 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview; Modul 3: Menjelaskan solusi kepatuhan data Microsoft Purview; Unit 2: Menjelaskan eDiscovery'
---
--->

# Demo: Jelajahi eDiscovery (Standar)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan solusi kepatuhan data Microsoft Purview
- Unit: Menjelaskan eDiscovery

## Skenario demo

Di Demo ini, Anda akan mempelajari langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, termasuk menyiapkan izin peran, membuat kasus eDiscovery, membuat penangguhan eDiscovery, dan membuat kueri pencarian.  CATATAN: Di portal Microsoft Purview pembaruan untuk antarmuka pengguna diluncurkan, secara bertahap. Beberapa penyewa lab/demo mungkin belum menampilkan UI terbaru, sehingga semua langkah lab ditampilkan menggunakan UI eDiscovery Klasik.

### Demo Bagian 1

Untuk mengakses eDiscovery (Standar) atau agar ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Di bagian demo ini, Anda sebagai admin global, akan mempelajari proses penambahan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

1. Buka tab browser untuk **Microsoft Purview**. Jika sebelumnya Anda menutupnya, buka tab browser dan di bilah alamat, masukkan **https://purview.microsoft.com**. Untuk mengakses portal Microsoft Purview baru, pilih kotak di samping tempat yang tertulis, **saya menyetujui ketentuan pengungkapan aliran data dan Pernyataan** Privasi, lalu pilih **Mulai**.  
1. Dari panel navigasi kiri, pilih **Pengaturan**.
1. Dari panel navigasi yang terbuka, pilih **Peran dan cakupan** untuk memperluas opsi, lalu pilih **Grup** peran.
1. Di kotak pencarian di sisi kanan layar, cari pada istilah **eDiscovery**.  Pilih **Manajer eDiscovery**.
    1. Pilih **Edit**.
    1. Pilih **Pilih pengguna**.
    1. Cari Administrator MOD, pilih kotak di samping **Administrator** MOD lalu pilih tombol **Pilih** di bagian bawah halaman.
    1. Pilih **Berikutnya** lalu pilih **Simpan**, lalu akhirnya pilih **Selesai**.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Di bagian ini Anda akan membuat kasus untuk mulai menggunakan eDiscovery (Standar).

1. Dari panel navigasi kiri, pilih **Solusi**, pilih **eDiscovery** lalu pilih **Kasus** standar.

1. Dari bagian atas laman eDiscovery (Standar), pilih **+ Buat kasus**.

1. Di jendela Kasus baru, masukkan Nama kasus, **SC900 Test Case**, lalu pilih **Simpan** di bagian bawah laman.

1. Sekarang, kasus akan muncul dalam daftar.

1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  

1. Tetap buka tab browser ini.

### Demo Bagian 3

Sekarang, setelah Anda membuat kasus eDiscovery (Standar), Anda dapat mulai bekerja dengan kasus tersebut.  Dalam bagian ini, Anda akan membuat penangguhan eDiscovery untuk kasus yang Anda buat.  Khususnya, Anda akan membuat penangguhan untuk kotak surat exchange milik Adele Vance.

1. Dari laman eDiscovery (Standar), pilih kasus yang Anda buat - **Kasus Pengujian SC900**.

1. Dari laman Beranda kasus, pilih tab **Penangguhan**, lalu pilih **+Buat**.

1. Di kolom nama, masukkan **Penangguhan pengujian**, lalu pilih **Berikutnya**.

1. Di laman Pilih lokasi, pilih tombol pengalih di samping **kotak surat Exchange** untuk mengatur status ke **Aktif**.  

1. Sekarang pilih **Pilih pengguna, grup, atau tim**.  Di Kotak pencarian, masukkan **Adele**, lalu tekan Enter di keyboard Anda. Dari hasil pencarian, pilih **Adele Vance**, lalu pilih **Selesai**.

1. Dari laman Pilih Lokasi, pilih **Berikutnya**.  Untuk kecocokan dengan Demo, tidak ada lokasi lain yang akan disertakan dalam penangguhan ini.

1. Laman Syarat kueri memungkinkan Anda membuat penangguhan, berdasarkan Kata Kunci atau Ketentuan tertentu yang dipenuhi, pilih **+ Tambahkan syarat** untuk melihat opsi yang tersedia.  Pilih **Selanjutnya**. Tanpa syarat apa pun, penangguhan akan mempertahankan semua konten di lokasi yang ditentukan.

1. Tinjau pengaturan Anda dan pilih **Kirim**, mungkin perlu waktu satu menit, lalu pilih **Selesai**.  Penangguhan pengujian akan muncul dalam daftar.  Jika Anda tidak segera melihatnya, pilih **Refresh**

1. Tetap buka tab browser ini.

### Demo Bagian 4

Setelah memasukkan penangguhan, Anda akan membuat kueri pencarian.  Setelah pencarian Anda selesai, eDiscovery mendukung tindakan, seperti mengekspor dan mengunduh hasil untuk penyelidikan di masa mendatang.   Catatan: Pencarian yang terkait dengan kasus eDiscovery (Standar) tidak terdaftar di laman pencarian konten di portal kepatuhan Microsoft Purview. Pencarian ini hanya terdaftar di laman Pencarian dari kasus eDiscovery (Standar) terkait.

1. Dari laman Kasus Uji SC900, pilih **Pencarian**.

1. Dari halaman Pencarian, pilih **+ Pencarian Baru**.

1. Di bidang Nama, masukkan **Penangguhan Pengujian – Pencarian Penjualan**, lalu pilih **Berikutnya** dari bagian bawah laman.

1. Di halaman Pilih lokasi, pilih **lokasi yang ditangguhkan** dan batal pilih **Tambahkan Konten Aplikasi untuk pengguna** Lokal, karena lingkungan lab Anda tidak memiliki pengguna lokal, lalu pilih **Berikutnya**.

1. Laman Syarat kueri memungkinkan Anda membuat penangguhan, berdasarkan Kata Kunci atau Syarat tertentu yang dipenuhi. Pada bidang kata kunci, masukkan **Penjualan**, pilih **Berikutnya**.

1. Tinjau pengaturan Anda dan pilih **Kirim**, mungkin perlu waktu satu menit, lalu pilih **Selesai**.  Pencarian akan muncul dalam daftar.  Jika Anda tidak segera melihatnya, pilih **Refresh**

1. Dari jendela Pencarian, pilih pencarian yang Anda buat, **Penangguhan pengujian - Pencarian Penjualan**.  Jendela akan terbuka dengan tab Ringkasan yang dipilih.  Setelah pencarian selesai, status akan menunjukkan bahwa pencarian selesai.  Anda akan melihat tab Statistik pencarian (jika Anda tidak melihat tab Statistik pencarian, pencarian mungkin masih berjalan dan mungkin perlu waktu beberapa menit hingga selesai).  Pilih tab **Statistik pencarian** dan pilih panah menurun di samping Cari konten.  Anda juga dapat melihat informasi selengkapnya untuk Laporan syarat dan Lokasi teratas.  

1. Di bagian bawah laman, pilih **Tindakan**.  Perhatikan opsi yang tersedia yang menyertakan opsi ekspor. Pilih **Tutup.**

1. Tutup semua tab browser yang terbuka.

### Tinjauan

Di demo ini, Anda telah mempelajari langkah-langkah yang diperlukan untuk memulai eDiscovery (Standar), termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dari kasus yang dibuat, Anda telah mempelajari elemen alur kerja eDiscovery (Standar) dengan membuat penangguhan eDiscovery dan membuat kueri pencarian.
