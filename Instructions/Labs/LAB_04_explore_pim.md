---
lab:
  title: Jelajahi Privileged Identity management
  module: Describe the identity protection and governance capabilities of Microsoft Entra
---

# Lab: Menjelajahi Privileged Identity management

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan perlindungan identitas dan kemampuan tata kelola Microsoft Entra
- Unit: Menjelaskan kemampuan Privileged Identity Management

## Skenario lab

Di lab ini, Anda akan mempelajari beberapa fungsi dasar Privileged Identity Management (PIM). PIM memang memerlukan lisensi Microsoft Entra ID P2.  Di lab ini, Anda, sebagai admin, akan mengonfigurasi salah satu pengguna Anda, Diego Siciliani, dengan peran administrator pengguna Microsoft Entra, melalui privileged ID management (PIM).   Dengan hak istimewa admin pengguna, Diego akan dapat membuat pengguna dan grup mengelola lisensi, dan banyak lagi.  Baik admin maupun pengguna, Diego, harus dikonfigurasi untuk lisensi Microsoft Entra ID P2.

**Perkiraan Waktu**: 60 menit

### Tugas 1

Dalam tugas ini Anda, sebagai admin, akan mengatur ulang kata sandi untuk pengguna Diego Siciliani. Langkah ini diperlukan sehingga Anda awalnya dapat masuk sebagai pengguna dalam tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://entra.microsoft.com**.

1. Masuk dengan kredensial admin Microsoft 365 yang disediakan oleh ALH Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika sebelumnya Anda telah masuk sebagai admin, Anda mungkin diminta untuk menyelesaikan autentikasi sekunder, sebagai bagian dari MFA. JIKA sebelumnya Anda belum masuk sebagai admin, Anda mungkin diminta untuk menyelesaikan proses pendaftaran MFA. Ikuti perintah di layar untuk menyiapkan MFA.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Dari panel navigasi sebelah kiri, bentangkan **Identitas**, bentangkan **Pengguna**, lalu pilih **Semua pengguna**.

1. Pilih **Diego Siciliani** dari daftar pengguna.

1. Pilih **Atur ulang kata sandi** dari bagian atas laman. Karena sebelumnya Anda belum masuk sebagai Diego, Anda tidak mengetahui kata sandinya, dan perlu mengatur ulang kata sandinya.

1. Ketika jendela pengaturan kata sandi terbuka, pilih **Atur Ulang Kata Sandi**  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke beranda pusat admin Microsoft Entra.

1. Biarkan laman browser tetap terbuka, karena Anda akan membutuhkannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda, sebagai admin, akan menetapkan peran ID Microsoft Entra di Privileged Identity Management.

1. Buka tab browser untuk beranda pusat admin Microsoft Entra.

1. Dari panel navigasi sebelah kiri, di bagian “Identitas”, bentangkan **Tata Kelola Identitas**, lalu pilih **Privileged Identity Management**.

1. Sekarang, Anda berada di laman mulai cepat Privileged Identity Management. Tinjau informasi di laman Memulai. Di jendela utama, di mana tertulis Kelola akses, pilih **Kelola**.

1. Sekarang, Anda berada di laman Peran Contoso.  Di bilah pencarian, di bagian atas laman, masukkan **pengguna**.  Dari hasil pencarian, pilih **Administrator Pengguna**.

1. Dari bagian atas laman, pilih **+ Tambahkan penetapan**.

1. Di laman Tambahkan penugasan, pastikan **Keanggotaan** digarisbawaahkan.  Di sini, Anda akan mengonfigurasi pengaturan keanggotaan untuk peran administrator pengguna di PIM.

1. Biarkan jenis Cakupan ke nilai defaultnya, Direktori.  

1. Pada bagian Pilih anggota, pilih **Tidak ada anggota yang dipilih**. Ini membuka jendela Pilih anggota.

1. Di bilah pencarian, masukkan **Diego**.  Dari hasil pencarian, pilih **Diego Siciliani**, lalu tekan **Pilih** di bagian bawah laman.  

1. Di bagian Pilih anggota, Anda akan melihat 1 Anggota dipilih dan nama serta email anggota terpilih, Deigo Siciliani. Dari bagian bawah laman Tambah penugasan, pilih **Berikutnya**.  

1. Sekarang, Anda berada di laman Pengaturan.  Biarkan Jenis penugasan ke pengaturan defaultnya, Memenuhi Syarat.

1. Jika kotak Memenuhi syarat secara permanen dicentang, pilih **Memenuhi syarat secara permanen**, untuk menghapus tanda centang.

1. Di bidang Mulai penugasan, biarkan tanggal dan waktu default, yaitu hari ini dan waktu saat ini.

1. Di bidang Akhir penugasan, ubah tanggal menjadi tanggal hari ini (perhatikan pengaturan default adalah satu tahun dari hari ini, jadi Anda perlu mengubah tahun). Untuk waktu tersebut, atur waktu menjadi dua jam dari waktu saat ini. Setelah Anda mengatur bidang waktu saat Akhir penugasan, tekan tombol tab di keyboard Anda dan pilih **Tetapkan** di bagian bawah laman.  

1. Ini akan membawa Anda kembali ke jendela Penugasan.  Setelah beberapa detik, Anda akan melihat Diego Siciliani tercantum dalam tabel Administrator Pengguna, bersama dengan detail penugasan. Jika setelah beberapa detik Anda masih tidak melihat pembaruan, pilih **Refresh** dari bagian atas laman.

1. Dari bagian atas laman, pilih **Pengaturan**.

1. Di detail Pengaturan peran untuk Administrator Pengguna, perhatikan berbagai opsi.  Perhatikan bahwa pengaturan ke "Memerlukan pembenaran pada aktivasi" diatur ke ya, dan "Saat aktivasi, perlu Azure MFA" juga diatur ke ya.  Anda akan melihat keduanya di tugas berikutnya saat Diego mengaktifkan peran tersebut.  Perhatikan juga bahwa “Memerlukan persetujuan untuk mengaktifkan” diatur ke Tidak.  Biarkan semua pengaturan ke nilai default pengaturan.  Tutup laman dengan memilih **X** di pojok kanan atas jendela.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **Keluar**. Kemudian tutup semua jendela browser..

### Tugas 3

Dalam tugas ini, Anda sebagai Diego Siciliani akan masuk ke pusat admin Microsoft Entra, untuk mengakses kemampuan Privileged Identity Management di Microsoft Entra guna mengaktifkan tugas Anda sebagai Administrator pengguna.  Setelah diaktifkan, Anda akan membuat beberapa perubahan konfigurasi pada pengguna yang sudah ada. Catatan: Untuk tugas ini, Anda memerlukan akses ke perangkat seluler untuk digunakan dengan aplikasi Microsoft Authenticator.

1. Buka Microsoft Edge.  Di bilah alamat browser, masukkan **Entra.microsoft.com/**.

1. Masuk sebagai Diego Siciliani.
    1. Di jendela Masuk, masukkan **DiegoS@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi sementara yang Anda catat dari tugas sebelumnya dan pilih **Masuk**.  Pilih **Masuk**.
    1. Karena kata sandi yang Anda masukkan hanyalah kata sandi sementara, Anda harus memperbaruinya sekarang. Masukkan kata sandi saat ini, lalu masukkan kata sandi baru, lalu konfirmasi kata sandi baru.  Catat kata sandi baru karena Anda akan membutuhkannya untuk menyelesaikan tugas.
    1. Karena ini adalah pertama kalinya Anda masuk sebagai Diego, Anda mungkin diminta untuk mengatur MFA. Ikuti perintah di layar untuk menyiapkan MFA.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Anda berhasil masuk ke pusat admin Microsoft Entra.
1. Dari panel navigasi sebelah kiri,bentangkan **Tata Kelola Identitas**, lalu pilih **Privileged Identity Management**.
1. Dari panel navigasi kiri, pilih **Peran yang saya**.  Sekarang, Anda melihat informasi untuk penugasan yang memenuhi syarat.  Anda akan melihat bahwa Anda, Diego, diberi peran sebagai Administrator pengguna.  
1. Di kolom terakhir tabel, tindakan berlabel, pilih **Aktifkan**.
1. Anda akan melihat ikon peringatan yang menunjukkan Diperlukan verifikasi tambahan.  Pilih **Klik untuk melanjutkan**.  Perlu diperhatikan bahwa pengaturan PIM untuk peran Administrator pengguna memerlukan autentikasi multifaktor.  Selain itu, karena informasi kontak Diego yang digunakan dengan MFA (metode autentikasi) sebelumnya tidak dikonfigurasi, ia harus mendaftarkan informasinya, untuk dapat menggunakan MFA.  Meskipun dia harus melakukan MFA kapan saja dia masuk sebagai admin pengguna, dalam periode penugasan, proses pendaftaran MFA hanya diperlukan sekali.
1. Jendela yang muncul dan langkah-langkah berikut adalah untuk metode aplikasi Microsoft Authenticator. .
    1. Jika Anda sudah menginstal aplikasi Microsoft Authenticator di perangkat seluler, pilih **Berikutnya**. Jika tidak, pilih **Unduh sekarang** dan ikuti langkah-langkahnya.
    1. Anda akan mulai menyiapkan akun Anda.  Pilih **Selanjutnya**.
    1. Menggunakan aplikasi Microsoft Authenticator di perangkat seluler Anda, pilih **+** untuk menambahkan akun dan pilih **Akun** kantor atau sekolah.
    1. Pilih opsi untuk **Memindai kode** QR, lalu menggunakan perangkat seluler Anda, pindai kode QR di layar PC Anda.
    1. Menggunakan aplikasi Microsoft Authenticator di perangkat seluler Anda, pindai kode QR.
    1. Ikuti langkah-langkah di PC dan perangkat seluler Anda, lalu pilih **Berikutnya**.
    1. Setelah menyiapkan info keamanan, Anda akan melihat jendela Berhasil.  Pilih **Selesai**.

1. Setelah Anda menyelesaikan proses pendaftaran MFA, Anda dikembalikan ke halaman Administrator Pengguna Aktif PIM.
1. Jendela Aktifkan Administrator Pengguna muncul.  Anda harus memasukkan alasan aktivasi.  Dalam kotak yang muncul, masukkan alasan apa pun yang Anda inginkan (maksimal 500 karakter), lalu pilih **Aktifkan**.
1. Anda akan melihat status (3 tahap progres), saat aktivasi diproses.
1. Setelah aktivasi selesai, Anda dikembalikan ke Peran saya | Halaman peran ID Microsoft Entra, tempat Anda akan melihat pemberitahuan yang menyatakan bahwa Anda telah mengaktifkan peran.  Pilih **Klik di sini** untuk melihat peran aktif Anda.  Jika Anda melihat waktu akhir berbeda dari yang awalnya dikonfigurasi, pilih tombol refresh di bagian atas laman (mungkin perlu beberapa menit untuk melakukan penyegaran).
1. Kembali ke beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi sebelah kiri. 
1. Sebagai administrator pengguna ID Microsoft Entra, Anda dapat membuat pengguna dan grup, mengelola lisensi, dan banyak lagi. Dari panel navigasi kiri, perluas **Identitas**, pilih **Pengguna**.
1. Dari daftar pengguna, pilih **Bianca Pisani**.
1. Dari panel navigasi kiri, pilih **Grup**.
1. Perhatikan grup tempat Bianca sudah ditetapkan. Dari bagian atas halaman, pilih **+ Keanggotaan**.
1. Dari daftar grup, pilih **Mark 8 Project Team**.
1. Dari bagian bawah halaman, pilih **Pilih**.
1. Pada halaman Grup, perhatikan bahwa grup Tim Proyek Mark 8 telah ditambahkan ke daftar (jika Anda tidak segera melihatnya tercantum, pilih tombol **Refresh** ).
1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **Keluar**. Kemudian tutup semua jendela browser..
1. Durasi peran Administrator Pengguna terbatas pada waktu yang dikonfigurasi.

### Tinjauan

Di lab ini; Anda telah menjelajahi PIM.  Sebagai admin, Anda telah mengonfigurasi Diego dengan hak istimewa admin pengguna selama jumlah waktu yang ditentukan.  Kemudian Anda, sebagai Diego, berjalan melalui proses mengaktifkan hak istimewa admin pengguna dan pengguna ke grup.  Ingat bahwa PIM memerlukan lisensi Microsoft Entra ID Premium P2.
