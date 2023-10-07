<!---
---
Lab: Judul: 'Jelajahi Privileged Identity Management. ' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 4: Modul: Menjelaskan kemampuan perlindungan identitas dan tata kelola Microsoft Entra; Unit 4: Menjelaskan kemampuan Privileged Identity Management'
---
--->

# Lab: Menjelajahi privileged Identity management

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan perlindungan identitas dan tata kelola Microsoft Entra
- Pelajaran: Menjelaskan kemampuan Privileged Identity Management

## Skenario lab

Di lab ini, Anda akan mempelajari beberapa fungsi dasar Privileged Identity Management (PIM). PIM memang memerlukan lisensi ID P2 Microsoft Entra.  Di lab ini, Anda, sebagai admin, akan mengonfigurasi salah satu pengguna Anda, Diego Siciliani, dengan peran administrator pengguna Microsoft Entra, melalui privileged ID management (PIM).   Dengan hak istimewa admin pengguna, Diego akan dapat membuat pengguna dan mengelola lisensi grup, dan banyak lagi.  Baik admin maupun pengguna, Diego, harus dikonfigurasi untuk lisensi ID P2 Microsoft Entra.

**Perkiraan Waktu**: 45-60 menit

### Tugas 1

Di tugas ini, Anda sebagai admin akan mengatur ulang kata sandi untuk pengguna Diego Siciliani. Langkah ini diperlukan agar Anda dapat masuk sebagai pengguna di tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://entra.microsoft.com**.

1. Masuk dengan kredensial admin Microsoft 365 yang disediakan oleh ALH Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh ALH Anda) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Dari panel navigasi kiri, perluas **Identitas**, perluas **Pengguna**, lalu pilih **Semua pengguna**.

1. Pilih **Diego Siciliani** dari daftar pengguna.

1. Pilih **Reset password** dari bagian atas halaman. Karena sebelumnya Anda belum masuk sebagai Diego, Anda tidak mengetahui kata sandinya, dan perlu mengatur ulang kata sandinya.

1. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

1. Dari panel navigasi kiri, pilih **Beranda** untuk mengembalikan halaman beranda untuk pusat admin Microsoft Entra.

1. Biarkan halaman browser tetap terbuka, karena Anda akan membutuhkannya di tugas berikutnya.

### Tugas 2

Di tugas ini, Anda sebagai admin akan menetapkan peran Microsoft Azure AD kepada Diego dalam Privileged Identity Management.

1. Buka tab browser untuk beranda pusat admin Microsoft Entra.

1. Dari panel navigasi kiri, di bawah "Identitas", perluas **Tata Kelola Identitas**, lalu pilih **Privileged Identity Management**.

1. Anda sekarang berada di halaman mulai cepat Privileged Identity Management. Tinjau informasi di halaman Memulai. Pilih **Kelola**.

1. Anda sekarang berada di halaman Peran Aswono.  Di bilah pencarian, di bagian atas halaman, masukkan **user**.  Dari hasil pencarian, pilih **User Administrator**.

1. Dari bagian atas halaman, pilih **+ Tambahkan penugasan**.

1. Di halaman Tambahkan tugas, pastikan **Membership** digarisbawahi.  Di sini Anda akan mengonfigurasi pengaturan keanggotaan untuk peran administrator pengguna di PIM.

1. Biarkan jenis Cakupan ke nilai default, yaitu Direktori.  

1. Di bawah Pilih anggota, pilih **Tidak ada anggota yang dipilih**. Hal ini akan membuka jendela untuk Memilih anggota.

1. Di bilah pencarian, masukkan **Diego**.  Dari hasil pencarian, pilih **Diego Siciliani**, lalu tekan **Select** di bagian bawah halaman.  

1. Di bagian Pilih anggota, Anda akan melihat 1 Anggota dipilih dan nama serta email anggota terpilih, Deigo Siciliani. Dari bagian bawah halaman Tambahkan tugas, pilih **Next**.  

1. Anda sekarang berada di halaman Pengaturan.  Biarkan jenis Tugas ke pengaturan default, Eligible.

1. Jika kotak memenuhi syarat secara permanen dicentang, pilih **Permanently eligible**, untuk menghapus tanda centang.

1. Di bidang Mulai tugas, pertahankan tanggal dan waktu default, yaitu hari dan waktu saat ini.

1. Di bidang Akhir tugas, ubah tanggal menjadi tanggal hari ini (perhatikan pengaturan default adalah tahun dari hari ini, jadi Anda perlu mengubah tahun). Untuk waktu, atur waktu menjadi dua jam dari waktu sekarang. Setelah Anda mengatur bidang waktu saat Tugas berakhir, tekan tombol tab pada keyboard dan pilih **Assign** di bagian bawah halaman.  

1. Hal ini membawa Anda kembali ke jendela Tugas.  Setelah beberapa detik, Anda akan melihat Diego Siciliani terdaftar di tabel Administrator Pengguna, bersama dengan detail tugas. Jika setelah beberapa detik Anda masih tidak melihat pembaruan, pilih **Refresh** dari bagian atas halaman.

1. Dari bagian atas halaman, pilih **Settings**.

1. Dalam detail pengaturan Peran untuk Administrator Pengguna, perhatikan pilihan yang berbeda.  Perhatikan bahwa pengaturan “Memerlukan pembenaran pada aktivasi” diatur ke ya, dan “Pada aktivasi, memerlukan Azure MFA” juga diatur ke ya.  Anda akan melihat keduanya di tugas berikutnya saat Diego mengaktifkan peran tersebut.  Perhatikan juga bahwa “Memerlukan persetujuan untuk mengaktifkan” diatur ke Tidak.  Biarkan semua pengaturan ke nilai default pengaturan.  Tutup halaman dengan memilih **X** di sudut kanan atas halaman.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser.

### Tugas 3

Dalam tugas ini Anda, sebagai Diego Siciliani, akan masuk ke pusat admin Microsoft Entra, untuk mengakses kemampuan Privileged Identity Management Microsoft Entra untuk mengaktifkan tugas Anda sebagai administrator Pengguna.  Setelah diaktifkan, Anda akan membuat beberapa perubahan konfigurasi pada pengguna yang sudah ada. Catatan: Untuk tugas ini, Anda memerlukan akses ke perangkat seluler yang dapat diakses langsung dan dapat menerima pesan teks.

1. Buka Microsoft Edge.  Di bilah alamat browser, masukkan **Entra.microsoft.com**.

1. Masuk sebagai Diego Siciliani.
    1. Di jendela Masuk, masukkan **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi sementara yang Anda catat dari tugas sebelumnya dan pilih **Masuk**.  Pilih **Masuk**.
    1. Karena kata sandi yang Anda masukkan hanyalah kata sandi sementara, Anda harus memperbaruinya sekarang. Masukkan kata sandi saat ini, masukkan kata sandi baru, lalu konfirmasi kata sandi baru.  Catat kata sandi baru ini karena Anda perlu menyelesaikan tugas.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Anda harus berhasil masuk ke pusat admin Microsoft Entra.
1. Dari panel navigasi kiri, perluas **Tata Kelola Identitas** lalu pilih **Privileged Identity Management**.
1. Dari panel navigasi sebelah kiri, pilih **My roles**.  Anda sekarang melihat informasi untuk penugasan yang memenuhi syarat.  Anda akan melihat bahwa Anda, Diego, diberi peran sebagai administrator Pengguna.  
1. Di kolom terakhir tabel, tindakan berlabel, pilih **Activate**.
1. Anda akan melihat ikon peringatan yang menunjukkan Diperlukan verifikasi tambahan.  Pilih **Click to continue**.  Perlu diperhatikan bahwa pengaturan PIM untuk peran Administrator pengguna memerlukan autentikasi multifaktor.  Selain itu, karena informasi kontak Diego yang digunakan dengan MFA (metode autentikasi) sebelumnya tidak dikonfigurasi, maka harus mendaftarkan informasinya untuk dapat menggunakan MFA.  Meskipun dia harus melakukan MFA kapan saja dia masuk sebagai admin pengguna, dalam periode penugasan, proses pendaftaran MFA hanya diperlukan sekali.
1. Anda diberi tahu bahwa informasi selengkapnya diperlukan, pilih **Berikutnya**.
1. Masukkan kata sandi Anda.
1. Dari kiri bawah jendela Microsoft Authenticator, pilih **I want to setup a different method**.
1. Anda diminta untuk Memilih metode yang berbeda.  Di sebelah aplikasi Authenticator, pilih tombol panah bawah.   Pilih **Phone**, lalu pilih **Confirm**.
1. Anda diminta untuk memasukkan nomor telepon yang ingin digunakan. Pastikan negaranya benar, untuk kode negara nomor ponsel Anda.  Masukkan nomor ponsel Anda, pastikan **Text me a code** dipilih, lalu pilih **Next**.
1. Masukkan kode 6 digit yang Anda terima di ponsel Anda dan pilih **Next**.
1. Anda akan melihat pemberitahuan bahwa ponsel Anda telah berhasil didaftarkan. Pilih **Next**, lalu pilih **Done**.
1. Anda ditanya apakah ingin tetap masuk.  Pilih **Ya**.
1. Jendela Aktifkan Administrator Pengguna muncul.  Anda harus memasukkan alasan aktivasi.  Pada kotak yang muncul, masukkan alasan yang Anda inginkan (maksimal 500 karakter), lalu pilih **Activate**.
1. Anda akan melihat status (3 tahap progres), saat aktivasi diproses.
1. Setelah aktivasi selesai, Anda kembali ke Peran saya | Halaman peran Azure Active Directory, tempat Anda akan melihat pemberitahuan yang menyatakan bahwa Anda telah mengaktifkan peran.  Pilih **Click here** untuk melihat peran aktif Anda.  Jika Anda melihat waktu berakhir yang berbeda dari yang semula dikonfigurasi, pilih tombol segarkan di bagian atas halaman (mungkin perlu beberapa menit untuk menyegarkan).
1. Kembali ke halaman beranda pusat admin Microsoft Entra dengan memilih **Beranda** dari panel navigasi kiri. 
1. Sebagai administrator pengguna Microsoft Azure AD, Anda dapat membuat pengguna dan grup, mengelola lisensi, dan banyak lagi. Dari panel navigasi kiri, kedaluwarsa **Identitas**, pilih **Pengguna**, lalu pilih **Semua pengguna**.
1. Dari daftar pengguna, pilih **Bianca Pisani**.
1. Dari panel navigasi sebelah kiri, pilih **Licenses**.
1. Perhatikan bahwa Bianca tidak memiliki lisensi yang ditetapkan.  Dari bagian atas halaman, pilih **+ Assignments**.
1. Dari daftar pilihan lisensi, pilih **Office 365 E3** dan **Windows 10 Enterprise E3**.
1. Dari bagian bawah halaman, pilih **Save**.  Anda akan melihat pemberitahuan singkat di kanan atas halaman yang menunjukkan bahwa lisensi berhasil ditetapkan.
1. Tutup halaman penetapan lisensi yang diperbarui, dengan memilih **X** di sudut kanan atas halaman.
1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser.
1. Durasi peran Administrator Pengguna terbatas pada waktu yang dikonfigurasi.

### Tinjau

Di lab ini; Anda, menjelajahi PIM.  Anda sebagai admin telah mengonfigurasi Diego dengan hak istimewa admin pengguna selama jangka waktu tertentu.  Kemudian Anda sebagai Diego telah mempelajari proses mengaktifkan hak istimewa admin pengguna dan mengonfigurasi pengaturan pengguna.  Ingatlah bahwa PIM memerlukan lisensi Microsoft Azure AD Premium P2.
