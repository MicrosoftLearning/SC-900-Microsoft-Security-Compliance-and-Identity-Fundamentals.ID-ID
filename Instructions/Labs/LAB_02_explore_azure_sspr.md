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

**Perkiraan Waktu**: 15-20 menit

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

1. Perhatikan berbagai metode yang tersedia untuk pengguna.  **Email** dan **Ponsel (khusus SMS)** harus sudah dicentang. Jika belum, pilihlah.

1. Dari panel navigasi kiri Pengaturan ulang kata sandi, pilih **Pendaftaran**.  

1. Pastikan pengaturan Wajibkan pengguna mendaftar saat masuk diatur ke **Ya**.  Biarkan Jumlah hari sebelum pengguna diminta untuk mengonfirmasi ulang informasi autentikasi mereka diatur ke default 180.   Perhatikan kotak informasi laman tersebut.

1. Dari panel navigasi kiri Pengaturan ulang kata sandi, pilih **Pemberitahuan**.  

1. Pastikan pengaturan Wajibkan pengguna mendaftar saat masuk diatur ke **Ya**.  Biarkan pengaturan Beri tahu semua admin saat admin lain mengatur ulang kata sandi mereka diatur ke Ya.

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

Dalam tugas ini, Anda, sebagai pengguna Sara Perez, akan menjalani pendaftaran proses pengaturan ulang kata sandi ulang   Tugas ini mengharuskan Anda memiliki akses ke perangkat seluler tempat Anda dapat menerima pesan teks atau akun email pribadi yang dapat Anda akses

1. Buka Microsoft Edge dan di bilah alamat, masukkan **https://login.microsoft.com**.

1. Masuk sebagai Sara Perez.

1. Pop-up yang ditampilkan menunjukkan bahwa Informasi lebih lanjut diperlukan.  Ini karena sebagai anggota grup SSPRSecurityGroupUsers, konfigurasi mengharuskan anggotanya untuk mendaftar saat mereka masuk.  Pilih tombol **Berikutnya**.  Catatan: Alternatif untuk meminta pengguna melakukan pendaftaran, sendiri, adalah agar admin dapat langsung mengonfigurasi metode autentikasi saat mereka menambahkan pengguna. Hal ini mengharuskan administrator untuk mengetahui dan mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan pengaturan ulang kata sandi mandiri, dan mengatur ulang kata sandi pengguna.

1. Laman "Jaga keamanan akun Anda” akan terbuka.  Jendela yang muncul untuk metode autentikasi Telepon, jika Anda tidak memiliki perangkat seluler yang mampu menerima pesan teks, lewati ke langkah berikutnya.  Anda diminta memasukkan nomor telepon. Pastikan opsi **Kirim kode lewat SMS** diaktifkan.   Masukkan nomor telepon tempat Anda bisa menerima teks kode dan pilih tombol **Berikutnya**.  Jendela baru yang terbuka menunjukkan kode telah dikirim ke ponsel yang Anda masukkan.  Masukkan kode yang Anda terima dan pilih **Berikutnya**. Jendela yang terbuka menunjukkan Berhasil dan memperlihatkan Metode masuk default Anda.  Pilih **Selesai**.  
    1. Atau, Anda dapat mengatur metode yang berbeda seperti yang ditunjukkan di bagian kiri bawah jendela.  Jika Anda memilih untuk menyiapkan metode yang berbeda, pilih **Saya ingin menyiapkan metode yang berbeda**, jendela pop-up muncul, menanyakan Metode mana yang ingin Anda gunakan?  Dari menu menurun, pilih metode pilihan Anda, **Email**, lalu pilih tombol **Konfirmasi**.  Masukkan email yang ingin Anda gunakan, lalu pilih **Berikutnya**.  Jendela baru akan terbuka yang menunjukkan bahwa kode telah dikirim ke email yang Anda masukkan.  Akses email yang Anda masukkan untuk mendapatkan kode.  Masukkan kode yang Anda terima dan pilih **Berikutnya**. Jendela yang terbuka menunjukkan Berhasil dan memperlihatkan Metode masuk default Anda.  Pilih **Selesai**.

1. Sekarang Anda dapat menyelesaikan proses masuk. Jika Anda melihat bahwa waktu masuk telah kedaluwarsa, cukup masukkan kembali kata sandi.

1. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

### Tugas 4 (Opsional)

Dalam tugas ini, Anda, sebagai pengguna Sara Perez, akan menjalani proses pengaturan ulang kata sandi

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **https://login.microsoftonline.com**.

1. Masuk sebagai Sara Perez, dengan memasukkan email Anda **sara@WWLxZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik yang disediakan oleh penyedia host lab Anda) dan pilih tombol **Berikutnya**. Sebagai gantinya, Anda dapat melihat jendela Pilih akun yang terbuka. Jika demikian, pilih akun untuk Sara Perez.

1. Dari jendela Masukkan kata sandi, pilih **Lupa kata sandi saya**.

1. Jendela Kembali ke akun Anda akan terbuka.   Pastikan email untuk Sara Perez, sara@WWLxZZZZ.onmicrosoft.com ditampilkan di kotak email atau nama pengguna.  Jika tidak, masukkan.  

1. Dalam kotak kosong, masukkan karakter yang ditampilkan dalam gambar atau kata-kata dari audio. Setelah Anda memasukkannya, pilih **Berikutnya**.

1. Layar menunjukkan Kembali ke akun Anda dan menampilkan Langkah verifikasi 1 > memilih kata sandi baru. Biarkan pengaturan default **SMS ke ponsel saya**.  Anda diminta untuk memasukkan nomor ponsel.  Setelah Anda memasukkannya, pilih tombol **Teks**.  Jika selama pendaftaran Anda memilih email, jendela Kembali ke akun Anda akan menunjukkan bahwa Anda akan menerima email yang berisi kode verifikasi di alamat email alternatif Anda.  Pilih **Email**.

1. Masukkan kode verifikasi, lalu tekan **Berikutnya**.

1. Di layar berikutnya, Anda diminta memasukkan kata sandi baru dan mengonfirmasi kata sandi baru.  Masukkan sekarang dan pilih tombol **Selesai**.

1. Anda akan melihat pesan di layar bahwa kata sandi Anda telah diatur ulang.  Pilih **klik di sini** untuk masuk dengan kata sandi baru Anda.

1. Dari kotak Pilih informasi akun, pilih **sara@WWLxZZZZZZ.onmicrosoft.com**, masukkan kata sandi baru Anda, lalu pilih tombol **Masuk**.  Jika Anda diminta untuk Tetap masuk. pilih **Tidak**.

1. Sekarang Anda berada di portal Office.

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
