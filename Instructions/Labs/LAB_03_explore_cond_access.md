---
lab:
  title: Akses Bersyarat Microsoft Entra ID
  module: Describe the access management capabilities of Microsoft Entra
---

# Lab: Akses Bersyarat Microsoft Entra

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan manajemen akses Microsoft Entra ID
- Unit: Menjelaskan Akses Bersyarat

## Skenario lab

Di lab ini, Anda akan mempelajari MFA akses bersyarat, dari sudut pandang admin dan pengguna.  Sebagai admin, Anda akan membuat kebijakan yang mengharuskan pengguna melalui autentikasi multifaktor saat mengakses portal Microsoft Admin.  Dari perspektif pengguna, Anda akan melihat dampak kebijakan akses bersyarat, termasuk proses pendaftaran MFA.

**Perkiraan Waktu**: 45 menit

### Tugas 1

Dalam tugas ini Anda, sebagai admin, akan mengatur ulang kata sandi untuk pengguna Debra Berger.  Langkah ini diperlukan sehingga Anda awalnya dapat masuk sebagai pengguna dalam tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Tergantung pada hoster lab Anda dan jika ini adalah pertama kalinya Anda masuk ke penyewa, Anda mungkin diminta untuk menyelesaikan proses pendaftaran MFA. Jika demikian, ikuti perintah di layar untuk menyiapkan MFA.
    1. Setelah masuk, Anda akan dibawa ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri, di bagian “Identitas”, bentangkan **Identitas**, bentangkan **Pengguna**, lalu pilih **Semua pengguna**.

1. Pilih **Debra Berger** dari daftar pengguna.

1. Pilih **Atur ulang kata sandi** dari bagian atas laman. Karena sebelumnya Anda belum masuk sebagai Debra Berger, Anda tidak mengetahui kata sandinya, dan harus mengatur ulang kata sandinya.

1. Ketika jendela pengaturan kata sandi terbuka, pilih **Atur Ulang Kata Sandi**  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

1. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di pojok kanan atas laman, lalu tutup jendela Debra Berger dengan memilih **X** di pojok kanan atas laman.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke pusat admin Microsoft Entra.

1. Biarkan jendelanya tetap terbuka.

### Tugas 2

Dalam tugas ini, Anda akan menjalani proses pembuatan kebijakan akses bersyarat di Microsoft Entra ID.

1. Buka tab browser untuk beranda pusat admin Microsoft Entra.   Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan di bilah alamat, masukkan **`https://entra.microsoft.com`** dan masuk dengan kredensial admin Anda disediakan oleh host ALH.

1. Dari panel navigasi kiri, pastikan **ID** Entra diperluas, gulir ke bawah dan pilih **Akses** Bersyar.

1. Laman ikhtisar Akses bersyar ditampilkan. Saat Anda masuk ke halaman gambaran umum, tab **Memulai** dipilih (digarisbawahi). Pilih tab **Gambaran Umum** . Di sini Anda akan melihat petak peta memperlihatkan ringkasan Kebijakan dan pemberitahuan umum.

1. Dari panel navigasi kiri, pilih **Kebijakan**, lalu pilih **+ Kebijakan** baru.

1. Di bidang Nama, masukkan **Blokir portal** admin.

1. Di bagian Pengguna, pilih **0 pengguna dan grup dipilih**.

1. Sekarang, Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup.  Pastikan **Sertakan** dipilih (digarisbawahi).

1. Pilih opsi untuk **Pilih pengguna dan grup** dan pilih **Pengguna dan grup**.  Jendela Pilih Pengguna atau Grup akan terbuka.  

1. Di bilah pencarian, masukkan **Debra**.  Pilih **Debra Berger** dari bawah bilah pencarian, lalu tekan tombol **Pilih** di bagian bawah laman.  Perhatikan, praktik umumnya adalah menetapkan kebijakan kepada pengguna dalam grup.  Untuk tujuan kedaluwarsa dengan lab ini, kami akan menetapkan kebijakan ke pengguna tertentu.

1. Di bagian Sumber daya target, pilih **Tidak ada sumber daya target yang dipilih**.

1. Di bidang di bawah tulisan **Pilih apa kebijakan ini berlaku**, pilih panah bawah dan catat opsi yang tersedia.  Pertahankan pengaturan default, **Sumber Daya (sebelumnya aplikasi Cloud)**.  Pastikan tab **Sertakan** digarisbawahi.  Pilih **Pilih sumber daya**, lalu di bawah tempatnya tertulis **Pilih**, pilih **Tidak Ada**.  Jendela Pilih Aplikasi cloud akan terbuka.

1. Pilih **Portal** Admin Microsoft, lalu tekan **Pilih** di bagian bawah halaman.  Perhatikan peringatannya.  

1. Di bawah Jaringan, pilih **Jaringan atau lokasi** apa pun.  Tinjau opsi tetapi jangan pilih opsi apa pun.

1. Di bagian Kondisi, pilih **0 kondisi yang dipilih**.  Perhatikan berbagai opsi yang dapat Anda konfigurasi.  Melalui kebijakan, Anda dapat mengontrol akses pengguna berdasarkan sinyal dari kondisi termasuk: risiko pengguna, risiko masuk, platform perangkat, lokasi, aplikasi klien, atau filter untuk perangkat.  Jelajahi opsi yang dapat dikonfigurasi ini, tetapi jangan atur kondisi apa pun.

1. Sekarang Anda akan mengatur kontrol akses.  Di bagian Izinkan, pilih **0 kontrol yang dipilih**.

1. Jendela Izinkan terbuka.  Pilih **Blokir akses**. Tekan **Berikutnya** di bagian bawah laman.

1. Di bawah laman, Di bagian Aktifkan kebijakan, pilih **Aktif**, lalu pilih **Buat**.

1. Dari panel navigasi kiri, pilih **Kebijakan**. Kebijakan **Blokir portal admin yang baru saja Anda buat akan muncul dalam daftar kebijakan akses bersyarah** (jika diperlukan, pilih **ikon** Refresh di bilah perintah di bagian atas halaman).

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **Keluar**. Kemudian tutup semua jendela browser.

### Tugas 3

Dalam tugas ini, Anda akan melihat dampak dari kebijakan akses bersyarat, dari sudut pandang pengguna, Debra Berger. Pertama, Anda akan masuk ke aplikasi yang tidak disertakan dalam kebijakan akses bersyarat (portal Microsoft 365 di https://login.microsoftonline.com).  Kemudian Anda akan mengulangi proses di atas untuk aplikasi yang disertakan dalam kebijakan akses bersyarat (portal Microsoft Azure di https://portal.azure.com).  Ingat bahwa kebijakan memblokir akses ke salah satu Portal Admin Microsoft, termasuk portal Azure.  CATATAN: Untuk alasan keamanan, semua akun pengguna yang mengakses portal apa pun diperlukan untuk menggunakan MFA.  Persyaratan MFA tidak bergantung pada latihan lab ini.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://login.microsoftonline.com**.
    1. Masuk sebagai **DebraB@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi yang Anda catat dari tugas sebelumnya. Pilih **Masuk**.
    1. Karena kata sandi yang disediakan saat Anda, sebagai admin, atur ulang kata sandi bersifat sementara, Anda perlu memperbarui kata sandi Anda. Masukkan kata sandi saat ini, lalu masukkan kata sandi baru, lalu konfirmasi kata sandi baru.  Catat kata sandi baru karena Anda akan membutuhkannya untuk menyelesaikan tugas.
    1. Karena ini adalah pertama kalinya Anda masuk sebagai Debra Berger, Anda mungkin diminta untuk mengatur MFA. Ikuti perintah di layar untuk menyiapkan MFA.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.  Anda berhasil masuk ke akun Microsoft 365.

1. Sekarang Anda akan mencoba masuk ke aplikasi yang memenuhi kriteria kebijakan Akses Bersyarat. Buka tab browser baru dan masukkan **https://portal.azure.com**, yang merupakan portal admin untuk Azure.  Jendela pop-up muncul yang menunjukkan "Anda tidak memiliki akses ke ini."  Ini adalah hasil dari kebijakan akses bersyarah yang memblokir akses Anda ke semua portal admin Microsoft.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih keluar. Kemudian tutup semua jendela browser.

### Tinjauan

Di lab ini, Anda melalui proses pengaturan kebijakan akses bersyarkat yang memblokir akses ke portal admin Microsoft untuk semua pengguna yang disertakan dalam kebijakan.  Kemudian, sebagai pengguna, Anda mengalami dampak kebijakan akses bersyarah saat mengakses portal Azure.
