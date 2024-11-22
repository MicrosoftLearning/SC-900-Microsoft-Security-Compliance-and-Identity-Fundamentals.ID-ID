<!---
---
Demo: Judul: 'Menjelajahi Pengaturan Pengguna Microsoft Entra ID' Jalur/Modul/Unit Pembelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 1: Menjelaskan fungsi dan jenis identitas Microsoft Entra ID; Unit 3: Menjelaskan jenis identitas Microsoft Entra'
---
--->

# Demo: Pengaturan pengguna Microsoft Entra ID

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan fungsi dan jenis identitas Microsoft Entra ID.
- Unit: Menjelaskan jenis identitas.

## Demo skenario

Dalam demo ini, Anda akan mengakses Microsoft Entra ID dan menelusuri berbagai pengaturan untuk pengguna yang sudah ada.

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **admin.microsoft.com** untuk mengakses pusat admin Microsoft 365.

1. Masuk menggunakan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Identitas** (Anda mungkin perlu menggulir ke bawah).  Laman browser baru membuka laman ikhtisar di pusat admin Microsoft Entra. Di sini, Anda akan melihat informasi dasar tentang penyewa Contoso Anda. Jika Anda menggulir ke bawah jendela utama, Anda juga akan melihat informasi tentang pemberitahuan, umpan saya, sorotan fitur, dan banyak lagi.  
    1. Catatan untuk penyaji/instruktur: Anda juga dapat mengakses Pusat admin Microsoft Entra secara langsung dengan membuka **[entra.microsoft.com](https://entra.microsoft.com)**.

1. Dari panel navigasi kiri, bentangkan **Pengguna**, lalu pilih **Semua pengguna**.  Pada laman pengguna, Anda dapat melihat opsi navigasi tambahan dan daftar pengguna. Penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari daftar pengguna, pilih **Adele Vance**.

1. Perhatikan bahwa di panel navigasi kiri, **Ikhtisar** disorot warna abu-abu muda.  Perlihatkan/sebutkan informasi yang ditampilkan di laman ikhtisar.  Pilih tab **Pemantauan** di bagian atas laman yang memperlihatkan info masuk pengguna (tidak ada info masuk yang akan ditampilkan, kecuali Anda sebelumnya masuk sebagai Adele Vance).  Lalu Pilih **Properti** untuk melihat semua properti objek pengguna Adele Vance.

1. Dari panel navigasi kiri, pilih **Peran yang ditugaskan**.  Pengguna ini tidak memiliki peran administratif yang ditetapkan.  Dari bagian atas laman, pilih **+ Tambahkan tugas**, lalu dari laman tambahkan tugas, bentangkan bidang Cari peran pada Pilih peran untuk melihat daftar jenis peran administratif yang tersedia.  Jangan tambahkan apa pun, cukup tutup laman dengan memilih **X** di kanan atas laman.

1. Dari panel navigasi kiri, pilih **Grup**.  Sebutkan fakta bahwa pengguna ini adalah anggota dari beberapa grup.  Di sini, Anda dapat menyebutkan beberapa jenis grup.  Untuk menambahkan pengguna ini ke grup lain, pilih **+ Tambahkan keanggotaan**.  Jangan menambahkan grup baru apa pun, katakan saja betapa mudahnya menambahkan pengguna ke grup yang sudah ada. Tutup jendela Pilih grup dengan memilih **X** di pojok kanan atas laman.

1. Dari panel navigasi kiri, pilih **Lisensi**. Perhatikan bahwa pengguna ini diberi lisensi Microsoft 365 E5 dan lisensi EMS.  Untuk menambahkan lisensi, pilih **+ Penugasan** dari bagian atas jendela utama.  Perlihatkan lisensi untuk pengguna ini. JANGAN mengubah apa pun.  Tutup jendela Pilih grup dengan memilih **X** di pojok kanan atas laman.

1. Dari panel navigasi kiri, pilih **Perangkat**.  Tidak ada yang muncul, tetapi Anda dapat mengatakan bahwa jika pengguna ini memiliki perangkat yang ditetapkan, di sinilah perangkat akan muncul.

1. Dari panel navigasi kiri, pilih **Peran Azure yang ditugaskan**.  Katakan:
    1. Ini berbeda dari tab peran yang ditetapkan yang ditunjukkan sebelumnya, di tab sebelumnya untuk kontrol akses berbasis peran di Microsoft Entra.
    1. Meskipun tidak ada yang tercantum di sini, ini tab tempat Anda akan dapat melihat penetapan peran, yang ditetapkan ke Adele, untuk sumber daya Azure. Misalnya, jika Anda membuat Grup Sumber Daya Azure dan menetapkan peran tertentu kepada Adele, seperti pemilik atau kontributor untuk grup sumber daya, Anda akan melihat peran tersebut tercantum di sini. Apa itu Kontrol Akses Berbasis Peran Azure (Azure RBAC). Penetapan peran tersebut ditambahkan dan dikelola sebagai bagian dari sumber daya tersebut.

1. Pilih **X** di pojok kanan atas laman. Ini mengembalikan Anda ke daftar pengguna.

1. Pilih **X** di pojok kanan atas laman. Ini mengembalikan Anda ke laman utama untuk pusat admin Microsoft Entra.

1. Biarkan tab browser ini tetap terbuka karena Anda akan menggunakannya di Demo berikutnya.

### Tinjauan

Dalam demo ini, Anda menunjukkan pengaturan pengguna yang ada termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
