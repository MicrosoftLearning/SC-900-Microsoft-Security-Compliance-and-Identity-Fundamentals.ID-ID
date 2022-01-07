---
lab:
    title: 'Menjelajahi tata kelola identitas di Microsoft Azure AD dengan Privileged Identity management.'
    module: 'Modul 2 Pelajaran 4: Menjelaskan kemampuan perlindungan dan tata kelola identitas di Azure AD. Penjelasan Perlindungan Identitas Microsoft Azure.'
---


# Lab: Menjelajahi tata kelola identitas di Microsoft Azure AD dengan Privileged Identity management.

## Skenario lab
Di lab ini, Anda akan mempelajari beberapa fungsi dasar Privileged Identity Management (PIM). PIM membutuhkan Microsoft Azure AD Premium P2.  Di lab ini, Anda sebagai admin akan mengonfigurasi salah satu pengguna, yaitu Diego Siciliani, dengan peran administrator pengguna Microsoft Azure AD, melalui Privileged ID management (PIM).   Dengan hak istimewa admin pengguna, Diego akan dapat membuat pengguna dan mengelola lisensi grup, dan banyak lagi.  Baik sebagai admin maupun pengguna, Diego harus mengonfigurasi untuk lisensi Microsoft Azure AD Premium P2.

**Perkiraan Waktu**: 30-45 menit

#### Tugas 1: Di tugas ini, Anda sebagai admin akan mengatur ulang kata sandi untuk pengguna Diego Siciliani. Langkah ini diperlukan agar Anda dapat masuk sebagai pengguna di tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **portal.azure.com**.

2. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Pilih **Azure Active Directory**.  

4. Dari panel navigasi sebelah kiri, pilih **Users**.

5. Pilih **Diego Siciliani** dari daftar pengguna.

6. Pilih **Reset password** dari bagian atas halaman. Karena Anda belum pernah masuk sebagai Diego, Anda tidak mengetahui kata sandinya dan perlu mengatur ulang kata sandi.

7. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda akan memerlukannya di tugas berikutnya untuk dapat masuk sebagai pengguna.

8. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di sudut kanan atas halaman.

9. Tutup jendela profil Diego dengan memilih **X** di sudut kanan atas halaman.

10. Tutup jendela Semua pengguna dengan memilih **X** di sudut kanan atas halaman. Kini Anda seyogianya berada di halaman Contoso Azure Active Directory.

11. Biarkan halaman browser tetap terbuka, seperti yang akan Anda lakukan di tugas-tugas berikutnya.


#### Tugas 2: Di tugas ini, Anda sebagai admin akan menetapkan peran Microsoft Azure AD kepada Diego dalam Privileged Identity Management.

1. Buka tab browser, yang berlabel Contoso – Microsoft Azure.   Jika sebelumnya Anda menutup tab browser, buka Microsoft Edge, dan di bilah alamat masukkan portal.azure.com dan masuk dengan kredensial admin Anda, lalu pilih Azure Active Directory.  

2. Dari panel navigasi sebelah kiri, pilih **Identity Governance**.

3. Dari jendela utama, pastikan **Getting started** digarisbawahi, lalu pilih **Manage role assignments** di bagian tengah kanan layar.  Atau, dari panel navigasi sebelah kiri, di bagian Privileged Identity Management, pilih **Azure AD roles**.

4. Sekarang Anda berada di jendela Mulai Cepat Privileged Identity Management.  Pilih **Manage Access**.

5. Sekarang Anda berada di halaman Peran Contoso.  Di bilah pencarian, di bagian atas halaman, masukkan **user**.  Dari hasil pencarian, pilih **User Administrator**.

6. Dari bagian atas halaman, pilih **+ Assignments**.

7. Di halaman Tambahkan tugas, pastikan **Membership** digarisbawahi.  Di sini, Anda akan mengonfigurasi pengaturan keanggotaan untuk peran administrator pengguna di PIM.

8. Biarkan jenis Cakupan ke nilai default, yaitu Direktori.  

9. Di bagian Pilih anggota, pilih **No members selected**. Hal ini akan membuka jendela untuk Memilih anggota. 

10. Di bilah pencarian, masukkan **Diego**.  Dari hasil pencarian, pilih **Diego Siciliani**, lalu tekan **Select** di bagian bawah halaman.  

11. Di bagian Pilih anggota, Anda akan melihat 1 Anggota yang telah dipilih serta nama dan email anggota yang dipilih, Deigo Siciliani. Dari bagian bawah halaman Tambahkan tugas, pilih **Next**.  

12. Anda sekarang berada di halaman Pengaturan.  Biarkan jenis Tugas ke pengaturan default, Eligible.

13. Jika kotak memenuhi syarat secara permanen dicentang, pilih **Permanently eligible**, untuk menghapus tanda centang.

14. Di bidang Mulai tugas, pertahankan tanggal dan waktu default, yaitu hari dan waktu saat ini.

15. Di bidang Akhir tugas, ubah tanggal menjadi tanggal hari ini (perhatikan pengaturan default adalah tahun dari hari ini, jadi Anda perlu mengubah tahun). Untuk waktu, atur waktu menjadi dua jam dari waktu sekarang.  Setelah Anda mengatur bidang waktu saat Tugas berakhir, tekan tombol tab pada keyboard dan pilih **Assign** di bagian bawah halaman.  

16. Hal ini membawa Anda kembali ke jendela Tugas.  Setelah beberapa detik, Anda akan melihat Diego Siciliani terdaftar di tabel Administrator Pengguna, bersama dengan detail tugas.  Jika setelah beberapa detik Anda masih tidak melihat pembaruan, pilih **Refresh** dari bagian atas halaman.

17. Dari bagian atas halaman, pilih **Settings**.

18. Dalam detail pengaturan Peran untuk Administrator Pengguna, perhatikan pilihan yang berbeda.  Perhatikan bahwa pengaturan “Memerlukan pembenaran pada aktivasi” diatur ke ya, dan “Pada aktivasi, memerlukan Azure MFA” juga diatur ke ya.  Anda akan melihat keduanya di tugas berikutnya ketika Diego mengaktifkan peran.  Perhatikan juga bahwa “Memerlukan persetujuan untuk mengaktifkan” diatur ke Tidak. Biarkan semua pengaturan ke nilai defaultnya.  Tutup halaman dengan memilih **X** di sudut kanan atas halaman.

19. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser.


#### Tugas 3: Tugas 3:  Dalam tugas ini, Anda sebagai Diego Siciliani akan masuk ke Portal Azure untuk mengakses kemampuan Privileged Identity Management dari Azure Active Directory untuk mengaktifkan tugas Anda sebagai administrator Pengguna.  Setelah diaktifkan, Anda akan membuat beberapa perubahan konfigurasi pada pengguna yang sudah ada. Catatan: Untuk tugas ini, Anda memerlukan akses ke perangkat seluler yang dapat Anda akses langsung dan dapat menerima pesan teks.

1. Buka Microsoft Edge.  Di bilah alamat browser, masukkan **portal.azure.com**.

1. Masuk sebagai Diego Siciliani.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi sementara yang Anda catat dari tugas sebelumnya dan pilih **Sign in**.  Pilih **Sign in**.
    1. Karena kata sandi yang Anda masukkan hanyalah kata sandi sementara, Anda perlu memperbaruinya sekarang. Masukkan kata sandi saat ini.  Untuk kata sandi baru dan kolom konfirmasi kata sandi, masukkan **SC900-Lab**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Anda seyogianya berhasil masuk ke Azure Portal.
1. Dari halaman Selamat datang utama, di bagian layanan Azure, pilih **Azure Active Directory**.
1. Dari panel navigasi sebelah kiri, pilih **Identity Governance**.
1. Dari panel navigasi sebelah kiri, di bagian Privileged Identity Management, pilih **Azure AD roles**.
1. Dari panel navigasi sebelah kiri, pilih **My roles**.  Sekarang Anda melihat informasi untuk peran Microsoft Azure AD Anda.  Anda akan melihat bahwa Anda, sebagai Diego, diberi peran Administrator pengguna.  
1. Di kolom terakhir tabel, tindakan berlabel, pilih **Activate**.
1. Anda akan melihat ikon peringatan yang menunjukkan verifikasi tambahan diperlukan.  Pilih **Click to continue**.  Ingatlah bahwa pengaturan PIM untuk peran Administrator pengguna memerlukan autentikasi multifaktor.  Selain itu, karena informasi kontak Diego yang digunakan dengan MFA (metode autentikasi) sebelumnya tidak dikonfigurasi, maka harus mendaftarkan informasinya untuk dapat menggunakan MFA.  Meskipun dia harus melakukan MFA kapan saja dia masuk sebagai admin pengguna, dalam periode penugasan, proses pendaftaran MFA hanya diperlukan sekali.
1. Anda akan diberi tahu bahwa informasi lebih lanjut diperlukan, pilih **Next**.
1. Masukkan kata sandi Anda, **SC900-Lab**.
1. Dari kiri bawah jendela Microsoft Authenticator, pilih **I want to setup a different method**.
1. Anda diminta untuk Memilih metode yang berbeda.  Di sebelah aplikasi Authenticator, pilih tombol panah bawah.   Pilih **Phone**, lalu pilih **Confirm**.
1. Anda diminta untuk memasukkan nomor ponsel yang ingin Anda gunakan. Pastikan negaranya benar, untuk kode negara nomor ponsel Anda.  Masukkan nomor ponsel Anda, pastikan **Text me a code** dipilih, lalu pilih **Next**.
1. Masukkan kode 6 digit yang Anda terima di ponsel Anda dan pilih **Next**. 
1. Anda akan melihat pemberitahuan bahwa ponsel Anda berhasil didaftarkan. Pilih **Next**, lalu pilih **Done**.
1. Anda akan ditanya apakah Anda ingin tetap masuk. Pilih **Yes**.
1. Jendela Aktifkan Administrator Pengguna muncul.  Anda diminta untuk memasukkan alasan aktivasi.Anda diminta untuk memasukkan alasan aktivasi.  Pada kotak yang muncul, masukkan alasan yang Anda inginkan (maksimal 500 karakter), lalu pilih **Activate**.
1. Anda akan melihat status (3 tahap progres), saat aktivasi diproses.
1. Setelah aktivasi selesai, Anda kembali ke peran Saya | Halaman peran Microsoft Azure AD, tempat Anda akan melihat pemberitahuan yang menyatakan bahwa Anda baru saja mengaktifkan peran.  Pilih **Click here** untuk melihat peran aktif Anda.  Jika Anda melihat waktu berakhir yang berbeda dari yang semula dikonfigurasi, pilih tombol segarkan di bagian atas halaman (mungkin perlu beberapa menit untuk menyegarkan). 
1. Tutup halaman dengan memilih **X** di sudut kanan atas halaman.
1. Tutup jendela Mulai cepat | Privileged Identity Management dengan memilih **X** di sudut kanan atas halaman.
1. Tutup jendela Tata Kelola Identitas dengan memilih **X** di sudut kanan atas halaman.
1. Sekarang Anda kembali ke halaman Contoso Azure Active Directory.  Sebagai administrator pengguna Microsoft Azure AD, Anda dapat membuat pengguna dan grup, mengelola lisensi, dan banyak lagi.   Dari panel navigasi sebelah kiri, pilih **Users**.
1. Dari daftar pengguna, pilih **Bianca Pisani**.
1. Dari panel navigasi sebelah kiri, pilih **Licenses**.
1. Perhatikan bahwa Bianca tidak memiliki lisensi yang ditetapkan.  Dari bagian atas halaman, pilih **+ Assignments**. 
1. Dari daftar pilihan lisensi, pilih **Office 365 E3** dan **Windows 10 Enterprise E3**.
1. Dari bagian bawah halaman, pilih **Save**.  Anda akan melihat pemberitahuan singkat di kanan atas halaman yang menunjukkan bahwa lisensi berhasil ditetapkan.
1. Tutup halaman penetapan lisensi yang diperbarui, dengan memilih **X** di sudut kanan atas halaman.
1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser.
1. Durasi peran admin pengguna terbatas pada waktu yang dikonfigurasi.

#### Tinjauan
Di lab ini; Anda telah menjelajahi PIM.  Anda sebagai admin telah mengonfigurasi Diego dengan hak istimewa admin pengguna selama jangka waktu tertentu.  Kemudian Anda sebagai Diego telah mempelajari proses mengaktifkan hak istimewa admin pengguna dan mengonfigurasi pengaturan pengguna.  Ingatlah bahwa PIM memerlukan lisensi Microsoft Azure AD Premium P2.
