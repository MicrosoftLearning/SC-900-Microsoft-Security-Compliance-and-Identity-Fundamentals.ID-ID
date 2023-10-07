<!---
---
Lab: Jalur Pembelajaran: Modul 'Jelaskan kemampuan Microsoft Entra': 'Jelaskan kemampuan manajemen akses unit Microsoft Entra ID': 'Jelaskan Akses Bersyarkat'
---
--->

# Lab: Akses Bersyar Microsoft Entra

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan manajemen akses ID Microsoft Entra
- Unit: Menjelaskan Akses Bersyar

## Skenario lab

Di lab ini, Anda akan mempelajari MFA akses bersyarat, dari sudut pandang admin dan pengguna.  Sebagai admin, Anda akan membuat kebijakan yang mengharuskan pengguna melalui autentikasi multifaktor saat mengakses aplikasi Microsoft Azure Management berbasis cloud.  Dari perspektif pengguna, Anda akan melihat dampak kebijakan akses bersyarat, termasuk proses pendaftaran MFA.

**Perkiraan Waktu**: 30 menit

### Tugas 1

Di tugas ini Anda, sebagai admin akan mengatur ulang kata sandi untuk pengguna bernama Debra Berger.  Langkah ini diperlukan agar Anda dapat masuk sebagai pengguna di tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://entra.microsoft.com**, dan masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Dari panel navigasi kiri, perluas **Identitas**, perluas **Pengguna**, lalu pilih **Semua pengguna**.

1. Pilih **Debra Berger** dari daftar pengguna.

1. Pilih **Reset password** dari bagian atas halaman. Karena sebelumnya Anda belum masuk sebagai Debra Berger, Anda tidak mengetahui kata sandinya, dan harus mengatur ulang kata sandinya.

1. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

1. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di pojok kanan atas halaman, lalu tutup jendela Debra Berger dengan memilih **X** di pojok kanan atas halaman.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke pusat admin Microsoft Entra.

1. Biarkan jendela ini terbuka.

### Tugas 2

Dalam tugas ini, Anda akan menjalani proses pembuatan kebijakan akses bersyarat di Azure Active Directory.

1. Buka tab browser ke beranda pusat admin Microsoft Entra.   Jika sebelumnya Anda menutup tab browser, buka Microsoft Edge dan di bilah alamat masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Microsoft 365 yang disediakan oleh ALH.

1. Dari panel navigasi kiri, perluas **Perlindungan** lalu pilih **Akses Bersyar**.

1. Halaman Gambaran umum akses bersyar ditampilkan.  Di sini Anda akan melihat petak peta yang menampilkan ringkasan Kebijakan dan pemberitahuan umum.  Dari panel navigasi kiri, pilih **Kebijakan**.

1. Dari panel navigasi kiri, pilih **Kebijakan**. Semua Kebijakan Akses Bersyarat dicantumkan di sini. Pilih **+ Kebijakan baru**.

1. Pada Nama bidang, masukkan **MFA Test Policy**.

1. Di bawah Pengguna, pilih **0 pengguna dan grup yang dipilih**.

1. Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup.  Pastikan **Include** dipilih (digarisbawahi).

1. Pilih opsi untuk **Select users and groups**, lalu pilih **Users and groups**.  Jendela untuk Memilih pengguna dan grup akan terbuka.  

1. Di Bilah pencarian, masukkan **Debra**.  Pilih **Debra Berger** di bawah bilah pencarian, lalu klik tombol **Select** di bagian bawah halaman.  Perlu dicatat, menetapkan kebijakan untuk pengguna dalam grup adalah praktik yang umum.  Demi kepentingan lab ini, kami akan menetapkan kebijakan ke pengguna tertentu.

1. Di bawah Sumber daya target, pilih **Tidak ada sumber daya target yang dipilih**.

1. Di bidang di bawahnya di mana tertulis **Pilih apa kebijakan ini berlaku**, pilih panah bawah dan catat opsi yang tersedia.  Pertahankan pengaturan default, **aplikasi Cloud**.  Pastikan tab **Sertakan** digaris bawahi.  Pilih **Pilih aplikasi**, lalu di bawah tempatnya tertulis **Pilih**, pilih **Tidak Ada**.  Jendela untuk Memilih aplikasi Cloud akan terbuka.

1. Pada bilah pencarian, masukkan **Azure**.  Dari hasil pencarian yang muncul di bawah kotak pencarian, pilih **Microsoft Azure Management**, lalu klik **Select** di bagian bawah halaman.  Perhatikan peringatan.  

1. Pada Kondisi, pilih **0 conditions selected**.  Perhatikan berbagai opsi yang dapat Anda konfigurasikan.  Melalui kebijakan ini, Anda dapat mengontrol akses pengguna berdasarkan sinyal dari kondisi termasuk: risiko pengguna, risiko masuk, platform perangkat, lokasi, aplikasi klien, atau filter untuk perangkat.  Jelajahi opsi yang dapat dikonfigurasi ini, tetapi jangan tetapkan kondisi apa pun.

1. Sekarang Anda akan mengatur kontrol akses.  Pada Grant, pilih **0 controls selected**.

1. Jendela Grant akan terbuka.  Pastikan **Izinkan akses** dipilih, lalu pilih **Memerlukan autentikasi multifaktor**. Gulir ke bawah sedikit di jendela kanan dan di bawah bagian Untuk beberapa kontrol, biarkan default **Memerlukan semua kontrol yang dipilih**.  Klik **Select** di bagian bawah halaman.

1. Di bawah halaman, Di bagian Aktifkan kebijakan, pilih **Aktif**, lalu pilih **Buat**.

1. Dari panel navigasi kiri pilih **Kebijakan**. Kebijakan MFA Pilot akan muncul dalam daftar kebijakan akses bersyarah (jika diperlukan, pilih **ikon Refresh** di bilah perintah di bagian atas halaman).

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser

### Tugas 3

Dalam tugas ini Anda akan melihat dampak dari kebijakan akses bersyarat, dari sudut pandang pengguna, Debra Berger. Anda akan mulai terlebih dahulu dengan masuk ke aplikasi yang tidak disertakan dalam kebijakan akses bersyarat (portal Microsoft 365 di https://login.microsoftonline.com).  Kemudian Anda akan mengulangi proses untuk aplikasi yang disertakan dalam kebijakan akses bersyarkat (portal Azure di https://portal.azure.com).  Ingat kembali bahwa kebijakan mengharuskan pengguna untuk menggunakan MFA ketika mengakses aplikasi Manajemen Microsoft Azure.  Untuk menggunakan MFA, pengguna terlebih dahulu harus mendaftar ke metode autentikasi yang akan digunakan untuk MFA, misalnya kode yang dikirimkan ke perangkat seluler atau aplikasi autentikasi.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://login.microsoftonline.com**.
    1. Masuk sebagai **DebraB@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi yang Anda catat sebelumnya. Pilih **Masuk**.
    1. Karena kata sandi yang diberikan saat Anda, sebagai admin, mengatur ulang kata sandi bersifat sementara, Anda perlu memperbarui kata sandi (ini bukan bagian dari kebijakan MFA). Masukkan kata sandi saat ini, lalu masukkan kata sandi baru lalu konfirmasi kata sandi baru.  Catat kata sandi baru karena Anda akan membutuhkannya untuk menyelesaikan tugas.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.  Anda telah berhasil masuk ke akun Microsoft 365 Anda. MFA tidak diperlukan untuk aplikasi ini karena tidak menjadi bagian kebijakan.

1. Sekarang Anda akan mencoba masuk ke aplikasi yang memenuhi kriteria untuk MFA. Buka tab browser baru dan masukkan **https://portal.azure.com**.

1. Anda akan melihat jendela yang menunjukkan, Informasi lebih lanjut diperlukan.  Pilih **Selanjutnya**.  Perlu diperhatikan, tindakan ini akan memulai proses pendaftaran MFA, karena ini adalah pertama kalinya Anda mengakses aplikasi cloud yang diidentifikasi dalam kebijakan akses bersyarat.  Proses pendaftaran diperlukan sekali saja.   Cara untuk mendorong pengguna untuk melewati proses pendaftaran adalah dengan membuat admin mengonfigurasi metode autentikasi untuk digunakan.

1. Di jendela Amankan akun Anda, Anda memiliki opsi untuk memilih metode yang digunakan untuk MFA.  Salah satunya adalah Microsoft Authenticator. Untuk kelayakan dalam latihan lab ini, Anda akan memilih metode yang berbeda.  Pilih **I want to setup a different method**.  Dari jendela pop-up Pilih metode lain, klik **panah tarik-turun**, lalu pilih **Phone**, kemudian pilih **Confirm**.

1. Di jendela yang terbuka, pastikan negara Anda dipilih lalu masukkan nomor ponsel yang ingin digunakan.  Pastikan bahwa **Kirimi saya kode** dipilih, lalu tekan **Berikutnya**.  Anda akan menerima pesan teks di ponsel dengan kode yang harus dimasukkan di tempat yang bertuliskan masukkan kode.  Masukkan kode yang Anda terima, lalu tekan **Berikutnya**.  Setelah dikonfirmasi, layar akan menampilkan, "SMS diverifikasi. Ponsel Anda berhasil didaftarkan".  Pilih **Selanjutnya**. lalu pilih **Selesai**.  yang menyelesaikan proses pendaftaran satu kali.

1. Sekarang Anda dapat mengakses portal Azure.  Portal Azure adalah aplikasi Manajemen Microsoft Azure dan oleh sebab itu memerlukan autentikasi multifaktor, sesuai dengan kebijakan akses bersyarat yang sudah dibuat.  
    1. Jika Anda mendapatkan pesan yang menunjukkan bahwa waktu masuk Anda habis, masukkan kata sandi dan pilih **Masuk**.
    1. Anda akan melihat jendela yang mengharuskan memverifikasi identitas.  Pilih tempat yang bertuliskan Teks =X XXXXXXX untuk menerima kode di ponsel Anda, masukkan kode dan pilih **Verifikasi**.
    1. Jika Anda diminta untuk tetap masuk, pilih **Tidak**.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih keluar. Kemudian tutup semua jendela browser.

### Tinjau

Di lab ini, Anda menjalani proses penyiapan kebijakan akses bersyarat yang mengharuskan pengguna melalui MFA saat mengakses aplikasi cloud Microsoft Azure Management.  Kemudian, sebagai pengguna Anda telah memahami proses pendaftaran untuk MFA dan melihat hasil kebijakan akses bersyarat yang mengharuskan Anda untuk menggunakan MFA ketika mengakses portal Azure.
