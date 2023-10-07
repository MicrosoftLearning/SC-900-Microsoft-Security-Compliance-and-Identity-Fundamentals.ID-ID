<!---
---
Demo: Judul: 'Jelajahi Microsoft Entra ID Pengaturan Pengguna' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 1: Menjelaskan jenis fungsi dan identitas ID Microsoft Entra; Unit 3: Menjelaskan jenis identitas Microsoft Entra'
---
--->

# Demo: Microsoft Entra pengaturan pengguna ID

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan jenis fungsi dan identitas ID Microsoft Entra.
- Unit: Menjelaskan jenis identitas.

## Skenario demo

Dalam demo ini, Anda akan mengakses ID Microsoft Entra dan menelusuri berbagai pengaturan untuk pengguna yang sudah ada.

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **admin.microsoft.com** untuk mengakses pusat admin Microsoft 365.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bawah pusat Admin, pilih **Identitas** (Anda mungkin perlu menggulir ke bawah).  Halaman browser baru terbuka ke halaman gambaran umum pusat admin Microsoft Entra. Di sini Anda akan melihat informasi dasar tentang penyewa Contoso Anda. Jika Anda menggulir ke bawah jendela utama, Anda juga akan melihat informasi tentang pemberitahuan, umpan saya, sorotan fitur, dan banyak lagi.  
    1. Catatan untuk penyaji/instruktur: Anda juga dapat mengakses pusat Microsoft Entra Admin secara langsung dengan **[membuka entra.microsoft.com](https://entra.microsoft.com)**.

1. Dari panel navigasi kiri, perluas **Pengguna** lalu pilih **Semua pengguna**.  Pada halaman pengguna Anda bisa melihat opsi navigasi tambahan dan daftar pengguna. Penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari daftar pengguna, pilih **Adele Vance**.

1. Perhatikan bahwa di panel navigasi kiri, **Gambaran Umum** disorot dalam abu-abu muda.  Perlihatkan/ucapkan ke informasi yang diperlihatkan di halaman gambaran umum.  Pilih tab **Pemantauan** di bagian atas halaman yang memperlihatkan rincian masuk pengguna (tidak ada rincian masuk yang akan ditampilkan, kecuali Anda sebelumnya masuk sebagai Adele Vance).  Lalu Pilih **Properti** untuk melihat semua properti untuk objek pengguna Adele Vance.

1. Dari panel navigasi kiri, pilih **Assigned roles**.  Pengguna ini tidak memiliki peran administratif yang ditetapkan.  Dari bagian atas halaman, pilih **+ Tambahkan tugas**, lalu dari halaman tambahkan tugas, perluas bidang Peran pencarian di bawah Pilih peran untuk melihat daftar jenis peran administratif yang tersedia.  Jangan menambahkan apa pun, tutuplah halaman dengan memilih **X** di kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih  **Groups**.  Katakan bahwa pengguna ini adalah anggota dari beberapa grup.  Di sini, Anda dapat berbicara dengan jenis grup.  Untuk menambahkan pengguna ini ke grup lain, pilih **+ Tambahkan keanggotaan**.  Jangan menambahkan grup baru apa pun, katakan saja betapa mudahnya menambahkan pengguna ke grup yang sudah ada. Tutup dari jendela Pilih grup dengan memilih **X** di sudut kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih **Licenses**. Perhatikan bahwa pengguna ini diberi lisensi Microsoft 365 E5 dan lisensi EMS.  Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.  Tampilkan lisensi untuk pengguna ini. JANGAN mengubah apa pun.  Tutup jendela ini dengan memilih **X** di sudut kanan atas halaman.

1. Dari panel navigasi kiri, pilih **Perangkat**.  Tidak ada yang muncul, tetapi Anda dapat mengatakan bahwa jika pengguna ini memiliki perangkat yang ditetapkan, ia akan muncul di sini.

1. Dari panel navigasi kiri, pilih **Azure role assignments**.  Katakan:
    1. Ini berbeda dari tab peran yang ditetapkan yang ditampilkan sebelumnya di tab sebelumnya adalah untuk kontrol akses berbasis peran di Microsoft Entra.
    1. Meskipun tidak ada yang tercantum di sini, ini adalah tab di mana Anda akan dapat melihat penetapan peran, yang ditetapkan ke Adele, untuk sumber daya Azure. Misalnya, jika Anda membuat Grup Sumber Daya Azure, dan Anda menetapkan Adele dengan peran tertentu, seperti pemilik atau kontributor untuk grup sumber daya, Anda akan melihat peran tersebut tercantum di sini. Ini adalah bagian dari Kontrol Akses Berbasis Peran Azure (Azure RBAC). Penetapan peran tersebut ditambahkan dan dikelola sebagai bagian dari sumber daya tertentu tersebut.

1. Dari panel navigasi kiri, pilih **Authentication methods**.  Sebutkan deskripsi yang tertulis, “Di sini, Anda dapat mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan autentikasi multifaktor serta mengatur ulang sandi layanan mandiri dan sandi pengguna.” Jika pengguna dikonfigurasi untuk SSPR atau diharuskan menggunakan MFA, dan Anda, sebagai admin, mengisi ini, maka pengguna sudah terdaftar dan tidak perlu melalui langkah-langkah pendaftaran untuk SSPR atau MFA.  Biasanya pengguna akan mendaftar sendiri vs admin yang harus melakukan ini.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke daftar pengguna.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke halaman utama untuk pusat admin Microsoft Entra.

1. Tetap buka tab browser ini karena Anda akan menggunakannya untuk demo berikutnya.

### Tinjau

Dalam demo ini, Anda menunjukkan pengaturan pengguna yang ada termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
