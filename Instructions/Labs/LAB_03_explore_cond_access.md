---
lab:
  title: Akses Bersyarat Microsoft Entra ID
  module: Describe the access management capabilities of Microsoft Entra ID
---

# Lab: Akses Bersyarat Microsoft Entra

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan manajemen akses Microsoft Entra ID
- Unit: Menjelaskan Akses Bersyarat

## Skenario lab

Di lab ini, Anda akan mempelajari MFA akses bersyarat, dari sudut pandang admin dan pengguna.  Sebagai admin, Anda akan membuat kebijakan yang mengharuskan pengguna melalui autentikasi multifaktor saat mengakses portal Microsoft Admin.  Dari perspektif pengguna, Anda akan melihat dampak kebijakan akses bersyarat, termasuk proses pendaftaran MFA.

**Perkiraan Waktu:**: 30 menit

### Tugas 1

Dalam tugas ini Anda, sebagai admin, akan mengatur ulang kata sandi untuk pengguna Debra Berger.  Langkah ini diperlukan sehingga Anda awalnya dapat masuk sebagai pengguna dalam tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Dari panel navigasi sebelah kiri, di bagian “Identitas”, bentangkan **Identitas**, bentangkan **Pengguna**, lalu pilih **Semua pengguna**.

1. Pilih **Debra Berger** dari daftar pengguna.

1. Pilih **Atur ulang kata sandi** dari bagian atas laman. Karena sebelumnya Anda belum masuk sebagai Debra Berger, Anda tidak mengetahui kata sandinya, dan harus mengatur ulang kata sandinya.

1. Ketika jendela pengaturan kata sandi terbuka, pilih **Atur Ulang Kata Sandi**  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

1. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di pojok kanan atas laman, lalu tutup jendela Debra Berger dengan memilih **X** di pojok kanan atas laman.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke pusat admin Microsoft Entra.

1. Biarkan jendelanya tetap terbuka.

### Tugas 2

Dalam tugas ini, Anda akan menjalani proses pembuatan kebijakan akses bersyarat di Microsoft Entra ID.

1. Buka tab browser untuk beranda pusat admin Microsoft Entra.   Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Anda disediakan oleh host ALH.

1. Dari panel navigasi kiri, bentangkan **Perlindungan**, lalu pilih **Akses Bersyarat**.

1. Laman ikhtisar Akses bersyar ditampilkan.  Di sini, Anda akan melihat petak yang memperlihatkan ringkasan Kebijakan dan pemberitahuan umum.  Dari panel navigasi kiri, pilih **Kebijakan**.

1. Dari panel navigasi kiri, pilih **Kebijakan**. Kebijakan Akses Bersyarat yang ada tercantum di sini. Pilih **+ Kebijakan baru**.

1. Di bidang Nama, masukkan **Kebijakan Pengujian MFA**.

1. Di bagian Pengguna, pilih **0 pengguna dan grup dipilih**.

1. Sekarang, Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup.  Pastikan **Sertakan** dipilih (digarisbawahi).

1. Pilih opsi untuk **Pilih pengguna dan grup** dan pilih **Pengguna dan grup**.  Jendela Pilih Pengguna atau Grup akan terbuka.  

1. Di bilah pencarian, masukkan **Debra**.  Pilih **Debra Berger** dari bawah bilah pencarian, lalu tekan tombol **Pilih** di bagian bawah laman.  Perhatikan, praktik umumnya adalah menetapkan kebijakan kepada pengguna dalam grup.  Demi kepentingan lab ini, kami akan menetapkan kebijakan ke pengguna tertentu.

1. Di bagian Sumber daya target, pilih **Tidak ada sumber daya target yang dipilih**.

1. Di bidang di bawah tulisan **Pilih apa kebijakan ini berlaku**, pilih panah bawah dan catat opsi yang tersedia.  Biarkan pengaturan default, **Cloud apps**.  Pastikan tab **Sertakan** digarisbawahi.  Pilih **Pilih aplikasi**, lalu di bawah tulisan **Pilih**, pilih **Tidak Ada**.  Jendela Pilih Aplikasi cloud akan terbuka.

1. Di bilah pencarian, masukkan **Azure**.  Dari hasil pencarian yang muncul di bawah kotak pencarian, pilih **Portal  Admin Microsoft**, lalu tekan **Pilih** di bagian bawah laman.  Perhatikan peringatannya.  

1. Di bagian Kondisi, pilih **0 kondisi yang dipilih**.  Perhatikan berbagai opsi yang dapat Anda konfigurasi.  Melalui kebijakan, Anda dapat mengontrol akses pengguna berdasarkan sinyal dari kondisi termasuk: risiko pengguna, risiko masuk, platform perangkat, lokasi, aplikasi klien, atau filter untuk perangkat.  Jelajahi opsi yang dapat dikonfigurasi ini, tetapi jangan atur kondisi apa pun.

1. Sekarang Anda akan mengatur kontrol akses.  Di bagian Izinkan, pilih **0 kontrol yang dipilih**.

1. Jendela Izinkan terbuka.  Pastikan **Izinkan akses** dipilih, lalu pilih **Memerlukan autentikasi multifaktor**. Gulir ke bawah sedikit di jendela kanan dan di bawah bagian Untuk beberapa kontrol, biarkan default **Memerlukan semua kontrol yang dipilih**.  Tekan **Berikutnya** di bagian bawah laman.

1. Di bawah laman, Di bagian Aktifkan kebijakan, pilih **Aktif**, lalu pilih **Buat**.

1. Dari panel navigasi kiri, pilih **Kebijakan**. Kebijakan MFA Pilot akan muncul dalam daftar kebijakan akses bersyarat (jika diperlukan, pilih **ikon Refresh** di bilah perintah di bagian atas laman).

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **Keluar**. Kemudian tutup semua jendela browser.

### Tugas 3

Dalam tugas ini, Anda akan melihat dampak dari kebijakan akses bersyarat, dari sudut pandang pengguna, Debra Berger. Pertama, Anda akan masuk ke aplikasi yang tidak disertakan dalam kebijakan akses bersyarat (portal Microsoft 365 di https://login.microsoftonline.com).  Kemudian Anda akan mengulangi proses di atas untuk aplikasi yang disertakan dalam kebijakan akses bersyarat (portal Microsoft Azure di https://portal.azure.com).  Ingat bahwa kebijakan mengharuskan pengguna untuk melalui MFA saat mengakses salah satu Portal Admin Microsoft, termasuk portal Azure.  Untuk menggunakan MFA, pengguna harus terlebih dahulu mendaftarkan metode autentikasi yang akan digunakan untuk MFA, misalnya kode yang dikirim ke perangkat seluler atau aplikasi pengautentikasi.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://login.microsoftonline.com**.
    1. Masuk sebagai **DebraB@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi yang Anda catat dari tugas sebelumnya. Pilih **Masuk**.
    1. Karena kata sandi yang diberikan saat Anda, sebagai admin, mengatur ulang kata sandi bersifat sementara, Anda perlu memperbarui kata sandi (ini bukan bagian dari kebijakan MFA). Masukkan kata sandi saat ini, lalu masukkan kata sandi baru, lalu konfirmasi kata sandi baru.  Catat kata sandi baru karena Anda akan membutuhkannya untuk menyelesaikan tugas.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.  Anda berhasil masuk ke akun Microsoft 365. MFA tidak diperlukan untuk aplikasi ini karena bukan bagian dari kebijakan.

1. Sekarang Anda akan mencoba masuk ke aplikasi yang memenuhi kriteria untuk MFA. Buka tab browser baru masukkan **https://portal.azure.com**.

1. Anda akan melihat jendela yang menunjukkan, Informasi lebih lanjut diperlukan.  Pilih **Selanjutnya**.  Perlu diperhatikan, tindakan ini akan memulai proses pendaftaran MFA, karena ini pertama kalinya Anda mengakses aplikasi cloud yang diidentifikasi dalam kebijakan akses bersyarat.  Proses pendaftaran ini hanya diperlukan sekali.   Alternatif untuk meminta pengguna melalui proses pendaftaran adalah meminta admin mengonfigurasi metode autentikasi untuk digunakan.

1. Di jendela Jaga keamanan akun Anda, Anda memiliki opsi untuk memilih metode yang akan digunakan untuk MFA.  Microsoft Authenticator adalah salah satu opsi. Untuk kelayakan dalam latihan lab ini, Anda akan memilih metode yang berbeda.  Pilih **Saya ingin menyiapkan metode lain**  Dari jendela pop-up Pilih metode lain, pilih **panah menurun** dan pilih **Telepon**, lalu pilih **Konfirmasi**.

1. Di jendela yang terbuka, pastikan negara Anda dipilih lalu masukkan nomor ponsel yang ingin digunakan.  Pastikan bahwa **Kirimi saya kode** dipilih, lalu tekan **Berikutnya**.  Anda akan menerima pesan teks di ponsel dengan kode yang harus dimasukkan di tempat yang bertuliskan masukkan kode.  Masukkan kode yang Anda terima, lalu tekan **Berikutnya**.  Setelah dikonfirmasi, layar akan menampilkan, "SMS diverifikasi. Ponsel Anda berhasil didaftarkan".  Pilih **Selanjutnya**. lalu pilih **Selesai**.  ini menyelesaikan proses pendaftaran satu kali.

1. Anda akan dapat mengakses portal Azure.  Portal Azure adalah portal Microsoft Admin dan oleh karena itu memerlukan autentikasi multifaktor, sesuai kebijakan akses bersyarat yang dibuat.  
    1. Jika Anda mendapatkan pesan yang menunjukkan bahwa waktu masuk Anda habis, masukkan kata sandi dan pilih **Masuk**.
    1. Anda akan melihat jendela yang mengharuskan memverifikasi identitas.  Pilih tempat yang bertuliskan Teks =X XXXXXXX untuk menerima kode di ponsel Anda, masukkan kode dan pilih **Verifikasi**.
    1. Jika Anda diminta untuk tetap masuk, pilih **Tidak**.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih keluar. Kemudian tutup semua jendela browser.

### Tinjauan

Di lab ini, Anda telah mempelajari proses penyiapan kebijakan akses bersyarat yang mengharuskan pengguna melakukan MFA saat mengakses Portal Microsoft Admin.  Kemudian, sebagai pengguna, Anda telah mempelajari proses pendaftaran untuk MFA dan melihat dampak kebijakan akses bersyarat yang mengharuskan Anda menggunakan MFA saat mengakses portal Azure.
