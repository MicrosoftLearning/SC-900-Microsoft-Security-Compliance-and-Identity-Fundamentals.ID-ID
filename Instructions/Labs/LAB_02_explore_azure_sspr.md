---
lab:
  title: Pengaturan ulang kata sandi layanan mandiri Microsoft Entra
  module: Describe the authentication capabilities of Microsoft Entra ID
---

<!---
---
Lab: Judul: 'Menjelajahi autentikasi Azure AD dengan pengaturan ulang kata sandi mandiri' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra; Modul 2: Menjelaskan kemampuan autentikasi Azure AD; Unit 4: Menjelaskan kata sandi mandiri'
---
--->

# Lab: Pengaturan ulang kata sandi mandiri di Microsoft Entra

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan autentikasi Microsoft Entra ID
- Unit: Menjelaskan pengaturan ulang kata sandi mandiri

## Skenario lab

Di lab ini, Anda, sebagai admin, akan menelusuri proses penambahan pengguna ke grup keamanan SSPR, yang sudah disiapkan di penyewa Microsoft 365 Anda. Dengan mengaktifkan SSPR, Anda akan mengambil peran sebagai pengguna dan menjalani proses pendaftaran SSPR dan juga mengatur ulang kata sandi.  Terakhir, Anda sebagai admin, akan dapat melihat log audit dan data penggunaan & wawasan untuk SSPR.

**Perkiraan Waktu:**: 30 menit

### Tugas 1

Dalam tugas ini, Anda, sebagai admin, akan menelusuri beberapa pengaturan konfigurasi yang tersedia untuk SSPR.

1. Buka browser Microsoft Edge. Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan admin kredensial Microsoft 365 yang disediakan oleh host lab resmi (ALH).
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Dari panel navigasi kiri, bentangkan opsi untuk **Perlindungan**, lalu pilih **Atur ulang kata sandi**.  

1. Properti untuk pengaturan ulang kata sandi mandiri ditampilkan. Pilih ikon informasi di samping tulisan **Pengaturan ulang kata sandi mandiri diaktifkan** untuk melihat deskripsinya. Pastikan bahwa **Dipilih** disorot dengan warna biru. Arahkan kursor Anda di atas ikon informasi di sebelah yang bertuliskan **Pilih grup** dan perhatikan bahwa tertulis, "Menentukan grup pengguna yang diizinkan untuk mengatur ulang kata sandi sendiri." Anda harus menyertakan pengguna dalam grup, Anda tidak dapat memilih pengguna satu per satu. Perhatikan bahwa ada grup yang sudah tercantum - SSPRSecurityGroupUsers (grup ini telah dikonfigurasi sebelumnya sebagai bagian dari penyewa Microsoft 365 Anda). Terakhir, perhatikan kotak informasi biru, "Pengaturan ini hanya berlaku untuk pengguna akhir di organisasi Anda. Admin selalu diaktifkan untuk pengaturan ulang kata sandi mandiri dan diperlukan untuk menggunakan dua metode autentikasi guna mengatur ulang kata sandi mereka.”

1. Dari panel navigasi kiri Pengaturan ulang kata sandi, pilih **Metode Autentikasi**.

1. Dalam Jumlah metode yang diperlukan untuk beristirahat, pilih **1**. Catat informasi yang kotak di layar.

1. Perhatikan berbagai metode yang tersedia untuk pengguna.  **Email** dan **Ponsel** harus sudah diperiksa; jika tidak, pilih.

1. Dari panel navigasi kiri Pengaturan ulang kata sandi, pilih **Pendaftaran**.  

1. Pastikan pengaturan Wajibkan pengguna mendaftar saat masuk diatur ke **Ya**.  Biarkan Jumlah hari sebelum pengguna diminta untuk mengkonfirmasi ulang informasi autentikasi mereka, ke default **180**.   Perhatikan kotak informasi laman tersebut.

1. Dari panel navigasi kiri Pengaturan ulang kata sandi, pilih **Pemberitahuan**.  

1. Pastikan pengaturan Wajibkan pengguna mendaftar saat masuk diatur ke **Ya**.  Biarkan pengaturan untuk Memberi tahu semua admin saat admin lain mengatur ulang kata sandi mereka ke **Tidak**.

1. Perhatikan bahwa panel navigasi Pengaturan ulang kata sandi juga menyertakan opsi untuk melihat log audit dan Penggunaan & wawasan.

1. Tutup jendela atur ulang kata sandi dengan memilih **X** di pojok kanan atas jendela. Ini mengembalikan Anda ke pusat admin Microsoft Entra.

1. Tetap buka jendela Microsoft Entra.

### Tugas 2

Dalam tugas ini, Anda, sebagai admin, akan menambahkan pengguna yang Anda buat di latihan lab sebelumnya ke grup keamanan SSPR.

1. Buka tab browser untuk beranda pusat Admin Microsoft Entra **[entra.microsoft.com](https://entra.microsoft.com)**. Jika diperlukan, bentangkan **Identitas**.

1. Dari panel navigasi sebelah kiri, di bagian “Identitas”, bentangkan **Grup**, lalu pilih **Semua grup**.

1. Daftar grup yang ada akan ditampilkan. Di bidang Grup pencarian, masukkan **SSPR**, lalu dari hasil pencarian pilih **SSPRSecurityGroupUsers**.  Ini akan membawa Anda ke opsi konfigurasi untuk grup ini.

1. Dari panel navigasi kiri, pilih **Anggota**.

1. Dari bagian atas laman, pilih **+ Tambahkan anggota**.  

1. Di kotak pencarian, masukkan **Sara Perez**.  Setelah pengguna **Sara Perez**, muncul di bawah kotak pencarian, pilih, lalu tekan **Pilih** dari bagian bawah laman.  Anda akan dikembalikan ke laman anggota.  Pilih **Refresh** dari bagian atas laman. Sekarang, Anda akan melihat Sara Perez terdaftar sebagai anggota dalam grup keamanan SSPR.

1. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

### Tugas 3

Dalam tugas ini, Anda, sebagai pengguna Sara Perez, akan menjalani pendaftaran proses pengaturan ulang kata sandi ulang 

1. Buka Microsoft Edge dan di bilah alamat, masukkan **https://login.microsoft.com**.

1. Masuk sebagai Sara Perez.

1. Pop-up yang ditampilkan menunjukkan bahwa Informasi lebih lanjut diperlukan.  Ini karena sebagai anggota grup SSPRSecurityGroupUsers, konfigurasi mengharuskan anggotanya untuk mendaftar saat mereka masuk.  Pilih tombol **Berikutnya**.  Catatan: Alternatif untuk meminta pengguna melakukan pendaftaran, sendiri, adalah agar admin dapat langsung mengonfigurasi metode autentikasi saat mereka menambahkan pengguna. Hal ini mengharuskan administrator untuk mengetahui dan mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan pengaturan ulang kata sandi mandiri, dan mengatur ulang kata sandi pengguna.

1. Laman "Jaga keamanan akun Anda” akan terbuka.  Jendela yang muncul dan langkah-langkah berikut adalah untuk metode aplikasi Microsoft Authenticator. Jika Anda ingin menggunakan email, pilih **Saya ingin menyiapkan metode** lain dan ikuti langkah-langkahnya.
    1. Jika Anda sudah menginstal aplikasi Microsoft Authenticator di perangkat seluler, pilih **Berikutnya**. Jika tidak, pilih **Unduh sekarang** dan ikuti langkah-langkahnya.
    1. Anda akan mulai menyiapkan akun Anda.  Pilih **Selanjutnya**.
    1. Menggunakan aplikasi Microsoft Authenticator di perangkat seluler Anda, pilih **+** untuk menambahkan akun dan pilih **Akun** kantor atau sekolah.
    1. Pilih opsi untuk **Memindai kode** QR, lalu menggunakan perangkat seluler Anda, pindai kode QR di layar PC Anda.
    1. Ikuti langkah-langkah di PC dan perangkat seluler Anda, lalu pilih **Berikutnya**.
    1. Setelah menyiapkan info keamanan, Anda akan melihat jendela Berhasil.  Pilih **Selesai**.

1. Sekarang Anda dapat menyelesaikan proses masuk. Jika Anda melihat bahwa waktu masuk telah kedaluwarsa, cukup masukkan kembali kata sandi.

1. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

### Tugas 4 (Opsional)

Dalam tugas ini, Anda, sebagai pengguna Sara Perez, akan menjalani proses pengaturan ulang kata sandi

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **https://login.microsoft.com**.

1. Masuk sebagai Sara Perez, dengan memasukkan email Anda **sara@WWLxZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik yang disediakan oleh penyedia host lab Anda) dan pilih tombol **Berikutnya**. Sebagai gantinya, Anda dapat melihat jendela Pilih akun yang terbuka. Jika demikian, pilih akun untuk Sara Perez.

1. Dari jendela Masukkan kata sandi, pilih **Lupa kata sandi saya**.

1. Jendela Kembali ke akun Anda akan terbuka.   Pastikan email untuk Sara Perez, sara@WWLxZZZZ.onmicrosoft.com ditampilkan di kotak email atau nama pengguna.  Jika tidak, masukkan.  

1. Dalam kotak kosong, masukkan karakter yang ditampilkan dalam gambar atau kata-kata dari audio. Setelah Anda memasukkannya, pilih **Berikutnya**.

1. Layar menunjukkan Kembali ke akun Anda dan menampilkan Langkah verifikasi 1 > memilih kata sandi baru. Pilih opsi **Setujui pemberitahuan di aplikasi** pengautentikasi saya, lalu pilih **Kirim Pemberitahuan**.

1. Perhatikan nomor di PC Anda dan ikuti instruksi untuk menyetujui masuk menggunakan aplikasi Microsoft Authenticator di perangkat seluler Anda.

1. Di layar berikutnya, Anda diminta memasukkan kata sandi baru dan mengonfirmasi kata sandi baru.  Masukkan sekarang dan pilih tombol **Selesai**.

1. Anda akan melihat pesan di layar bahwa kata sandi Anda telah diatur ulang.  Pilih **klik di sini** untuk masuk dengan kata sandi baru Anda.

1. Dari kotak Pilih informasi akun, pilih **sara@WWLxZZZZZZ.onmicrosoft.com**, masukkan kata sandi baru Anda, lalu pilih tombol **Masuk**.  Jika Anda diminta untuk Tetap masuk. pilih **Tidak**.

1. Anda sekarang harus masuk ke akun Microsoft Sara.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **Keluar**. Kemudian tutup semua jendela browser.

### Tugas 5 (Opsional)

Dalam tugas ini, Anda, sebagai administrator, akan secara singkat melihat log Audit serta data Penggunaan & wawasan yang terkait dengan pengaturan ulang kata sandi

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan admin kredensial Microsoft 365 yang disediakan oleh host lab resmi (ALH).

1. Pusat admin Microsoft Entra  Dari panel navigasi kiri, bentangkan opsi untuk **Perlindungan**, lalu pilih **Atur ulang kata sandi**.

1. Dari panel navigasi kiri, pilih **Log audit**.  Perhatikan informasi dan filter yang tersedia.  Perhatikan bahwa Anda juga dapat mengunduh log.  

1. Pilih **Unduh**.  Perhatikan bahwa Anda dapat memformat unduhan sebagai CSV atau JSON.  Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari panel navigasi kiri, pilih **Penggunaan & wawasan**.

1. Perhatikan informasi tersedia yang berkaitan dengan Pendaftaran.  Perhatikan bahwa mungkin perlu waktu untuk menyegarkan data ini, bahkan setelah Anda melakukan refresh, sehingga mungkin belum mencerminkan data pendaftaran atau penggunaan dari tugas sebelumnya.

1. Dari bagian atas laman, pilih **Penggunaan** untuk melihat jumlah Pengaturan ulang kata sandi mandiri dan membuka kunci akun menurut metode.  Perhatikan bahwa mungkin perlu waktu untuk menyegarkan data ini, bahkan setelah Anda melakukan refresh, sehingga mungkin belum mencerminkan data penggunaan dari tugas sebelumnya.

1. Tutup tab browser yang terbuka.

### Tinjauan

Di lab ini, Anda, sebagai admin, telah menjalani proses mengaktifkan pengaturan ulang kata sandi mandiri. Dengan mengaktifkan SSPR, Anda akan berperan sebagai pengguna untuk menjalani proses pendaftaran SSPR dan juga mengatur ulang kata sandi Anda.  Terakhir, Anda sebagai admin, mempelajari akses log audit dan penggunaan & wawasan data untuk SSPR.
