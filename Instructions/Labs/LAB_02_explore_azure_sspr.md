<!---
---
Lab: Judul: 'Jelajahi Autentikasi Azure AD dengan pengaturan ulang kata sandi mandiri' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra; Modul 2: Menjelaskan kemampuan autentikasi Azure AD; Unit 4: Menjelaskan kata sandi layanan mandiri'
---
--->

# Lab: Microsoft Entra pengaturan ulang kata sandi mandiri

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan autentikasi ID Microsoft Entra
- Unit: Menjelaskan pengaturan ulang kata sandi mandiri

## Skenario lab

Di lab ini, Anda, sebagai admin, akan menelusuri proses penambahan pengguna ke grup keamanan SSPR, yang sudah disiapkan di penyewa Microsoft 365 Anda. Dengan mengaktifkan SSPR, Anda kemudian akan mengambil peran sebagai pengguna dan melalui proses pendaftaran SSPR dan juga mengatur ulang kata sandi.  Terakhir, Anda sebagai admin akan dapat melihat log audit serta data penggunaan & wawasan untuk SSPR.

**Perkiraan Waktu**: 15-20 menit

### Tugas 1

Dalam tugas ini, Anda, sebagai admin, akan menelusuri beberapa pengaturan konfigurasi yang tersedia untuk SSPR.

1. Buka browser Microsoft Edge. Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh ALH Anda) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Dari panel navigasi kiri, perluas opsi untuk **Perlindungan**, lalu pilih **Reset kata sandi**.  

1. Properti untuk pengaturan ulang kata sandi mandiri ditampilkan. Pilih ikon informasi di samping tempat kata sandi **Layanan mandiri diaktifkan** untuk melihat deskripsinya. Pastikan **bahwa Dipilih** disorot dengan warna biru. Sekarang letakkan kursor Anda di atas ikon informasi di samping tempat bertuliskan **Pilih grup** dan perhatikan bahwa tertulis, "Menentukan grup pengguna yang diizinkan untuk mengatur ulang kata sandi mereka sendiri." Anda harus menyertakan pengguna dalam grup, Anda tidak dapat memilih pengguna satu per satu. Perhatikan bahwa ada grup yang sudah tercantum - SSPRSecurityGroupUsers (grup ini telah dikonfigurasi sebelumnya sebagai bagian dari penyewa Microsoft 365 Anda). Terakhir, perhatikan kotak informasi berwarna biru, "Pengaturan ini hanya berlaku untuk pengguna akhir di organisasi Anda. Admin selalu mengaktifkan layanan pengaturan ulang kata sandi mandiri dan diharuskan menggunakan dua metode autentikasi untuk mengatur ulang kata sandi mereka.”

1. Dari panel navigasi sebelah kiri Pengaturan ulang kata sandi, pilih **Authentication Methods**.

1. Di bagian Jumlah metode yang diperlukan untuk diam, pilih **1**. Perhatikan kotak informasi di layar.

1. Perhatikan berbagai macam metode yang tersedia bagi pengguna.  **Email** dan **Mobile phone (SMS only)** harus sudah dicentang; pilihlah jika belum.

1. Dari panel navigasi sebelah kiri pengaturan ulang kata sandi, pilih **Registration**.  

1. Pastikan pengaturan Mewajibkan pengguna untuk mendaftar saat masuk ditetapkan ke **Yes**.  Biarkan Jumlah hari diatur ke default 180 sebelum pengguna diminta untuk mengonfirmasi ulang informasi autentikasi mereka.   Perhatikan kotak informasi di halaman itu.

1. Dari panel navigasi sebelah kiri Pengaturan ulang kata sandi, pilih **Notifications**.  

1. Pastikan pengaturan untuk Memberi tahu pengguna tentang pengaturan ulang sandi ditetapkan ke **Yes**.  Biarkan pengaturan untuk Memberi tahu semua admin ketika admin lain mengatur ulang kata sandi mereka ke Tidak.

1. Perhatikan bagaimana panel navigasi pengaturan ulang kata sandi juga menyertakan opsi untuk melihat log audit serta Penggunaan & wawasan.

1. Tutup jendela reset kata sandi dengan memilih **X** di sudut kanan atas jendela. Ini mengembalikan Anda ke pusat admin Microsoft Entra.

1. Biarkan jendela Microsoft Entra terbuka.

### Tugas 2

Dalam tugas ini, Anda, sebagai admin, akan menambahkan pengguna yang Anda buat di latihan lab sebelumnya ke grup keamanan SSPR.

1. Buka tab browser untuk halaman beranda **[entra.microsoft.com](https://entra.microsoft.com)** pusat Microsoft Entra Admin. Jika diperlukan, perluas **Identitas**.

1. Dari panel navigasi kiri, di bawah "Identitas", perluas **Grup** lalu pilih **Semua grup**.

1. Daftar grup yang ada akan ditampilkan. Di bidang Cari grup, masukkan **SSPR**, lalu dari hasil pencarian pilih **SSPRSecurityGroupUsers**.  Anda akan diarahkan ke opsi konfigurasi untuk grup ini.

1. Dari panel navigasi sebelah kiri, pilih **Members**.

1. Dari bagian atas halaman, pilih **+ Add members**.  

1. Di kotak Pencarian, masukkan **Sara Perez**.  Setelah pengguna, **Sara Perez**, muncul di bawah kotak pencarian, pilih lalu tekan **Pilih** dari bagian bawah halaman.  Anda akan dikembalikan ke halaman anggota.  Pilih **Refresh** dari bagian atas halaman. Anda sekarang akan melihat Sara Perez terdaftar sebagai anggota dalam kelompok keamanan SSPR.

1. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

### Tugas 3

Dalam tugas ini Anda, sebagai pengguna Sara Perez, akan melalui proses pendaftaran untuk pengaturan ulang kata sandi mandiri.  Tugas ini mengharuskan Anda memiliki akses ke perangkat seluler tempat Anda dapat menerima pesan teks atau akun email pribadi yang dapat Anda akses

1. Buka Microsoft Edge dan di bilah alamat masukkan **https://login.microsoft.com**.

1. Masuk sebagai Sara Perez.

1. Tampilan pop-up yang menunjukkan bahwa informasi lebih lanjut diperlukan.  Ini karena sebagai anggota grup SSPRSecurityGroupUsers, konfigurasi mengharuskan anggotanya untuk mendaftar saat mereka masuk.  Pilih tombol **Berikutnya**.  Catatan:  Alternatif untuk meminta pengguna melakukan pendaftaran sendiri, agar admin segera mengonfigurasi metode autentikasi saat mereka menambahkan pengguna. Hal ini mengharuskan administrator untuk mengetahui dan mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan pengaturan ulang kata sandi mandiri, dan mengatur ulang kata sandi pengguna.

1. Halaman "Amankan akun Anda" akan terbuka.  Jendela yang muncul yaitu untuk metode autentikasi Ponsel, jika Anda tidak memiliki perangkat seluler yang dapat menerima pesan teks, lewati ke langkah berikutnya.  Anda diminta memasukkan nomor telepon. Pastikan pilihan **Text me a code** diaktifkan.   Masukkan nomor ponsel tempat Anda dapat menerima kode teks dan pilih **tombol Next**.  Jendela baru terbuka menunjukkan kode telah dikirim ke ponsel yang Anda masukkan.  Masukkan kode yang Anda terima dan pilih **Next**. Jendela terbuka menunjukkan Berhasil dan menampilkan metode Masuk default Anda.  Pilih **Selesai**.  
    1. Atau, Anda dapat mengatur metode yang berbeda seperti yang ditunjukkan di bagian kiri bawah jendela.  Jika Anda memilih untuk menyiapkan metode yang berbeda, pilih **Saya ingin menyiapkan metode yang berbeda**, jendela pop-up muncul, menanyakan Metode mana yang ingin Anda gunakan?  Dari menu dropdown, pilih metode pilihan Anda, **Email**, lalu pilih tombol **Konfirmasi**.  Masukkan email yang ingin Anda gunakan, lalu pilih **Next**.  Jendela baru akan terbuka yang menunjukkan bahwa kode telah dikirim ke email yang Anda masukkan.  Akses email yang Anda masukkan untuk mendapatkan kode.  Masukkan kode yang Anda terima dan pilih **Next**. Jendela terbuka menunjukkan Berhasil dan menampilkan metode Masuk default Anda.  Pilih **Selesai**.

1. Sekarang Anda dapat menyelesaikan proses masuk. Jika Anda melihat bahwa waktu masuk Anda telah kedaluwarsa, cukup masukkan kembali kata sandi.

1. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

### Tugas 4 (Opsional)

Dalam tugas ini Anda, sebagai pengguna Sara Perez, akan melalui proses pengaturan ulang kata sandi Anda

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **https://login.microsoftonline.com**.

1. Masuk sebagai Sara Perez, dengan memasukkan email **sara@WWLxZZZZ.onmicrosoft.com** Anda (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab Anda)dan pilih tombol **Berikutnya** . Sebagai gantinya, Anda dapat melihat jendela Pilih akun yang terbuka, jika demikian, pilih akun untuk Sara Perez.

1. Dari jendela Masukkan kata sandi, pilih **Forgot my password**.

1. Kembali ke jendela akun Anda yang terbuka.   Verifikasi bahwa email untuk Sara Perez, sara@WWLxZZZZ.onmicrosoft.com, ditampilkan dalam kotak email atau nama pengguna.  Jika tidak, masukkan.  

1. Di kotak kosong, masukkan karakter yang ditampilkan dalam gambar atau kata-kata dari audio. Setelah Anda memasukkannya, pilih **Berikutnya**.

1. Layar menunjukkan Kembali ke akun Anda dan menunjukkan langkah Verifikasi 1 > pilih kata sandi baru. Biarkan pengaturan default **Text my mobile phone**.  Anda diminta untuk memasukkan nomor ponsel.  Setelah Anda memasukkannya, pilih tombol **Teks**.  Jika selama pendaftaran Anda memilih email, jendela Kembali ke akun Anda akan menunjukkan bahwa Anda akan menerima email yang berisi kode verifikasi di alamat email alternatif Anda.  Pilih **Email**.

1. Masukkan kode verifikasi lalu tekan **Next**.

1. Di layar berikutnya, Anda diminta memasukkan kata sandi baru dan mengonfirmasi kata sandi baru.  Masukkan kata sandi dan pilih tombol **Finish**.

1. Anda akan melihat pesan di layar bahwa kata sandi Anda telah diatur ulang.  Pilih **click here** untuk masuk dengan kata sandi baru Anda.

1. Dari kotak Pilih informasi akun, pilih **sara@WWLxZZZZZZ.onmicrosoft.com** , masukkan kata sandi baru Anda, lalu pilih tombol **Masuk**.  Jika Anda diminta untuk Tetap masuk. pilih **Tidak**.

1. Sekarang Anda ada di portal Office.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser

### Tugas 5 (Opsional)

Dalam tugas ini, Anda, sebagai administrator, akan secara singkat melihat log Audit serta data Penggunaan & wawasan yang terkait dengan pengaturan ulang kata sandi

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **https://entra.microsoft.com** dan masuk dengan kredensial admin Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.

1. Anda berada di pusat admin Microsoft Entra.  Dari panel navigasi kiri, perluas opsi untuk **Perlindungan**, lalu pilih **Reset kata sandi**.

1. Dari panel navigasi sebelah kiri, pilih **Audit logs**.  Perhatikan informasi dan filter yang tersedia.  Perhatikan juga bahwa Anda dapat mengunduh log.  

1. Pilih **Unduh**.  Perhatikan bahwa Anda dapat memformat unduhan sebagai CSV atau JSON.  Tutup jendela dengan memilih **X** di sudut kanan atas layar.

1. Dari panel navigasi sebelah kiri, pilih **Usage & insights**.

1. Perhatikan informasi tersedia yang berkaitan dengan Pendaftaran.  Perhatikan bahwa mungkin perlu waktu untuk menyegarkan data ini, bahkan setelah Anda melakukan penyegaran, sehingga mungkin pendaftaran atau data penggunaan dari tugas sebelumnya belum ditampilkan.

1. Dari bagian atas halaman, pilih **Usage** untuk melihat jumlah Pengaturan ulang kata sandi mandiri dan pembukaan akun berdasarkan metode.  Perhatikan bahwa mungkin perlu waktu untuk menyegarakan data ini, bahkan setelah Anda melakukan penyegaran, sehingga mungkin data penggunaan dari tugas sebelumnya belum ditampilkan.

1. Tutup tab browser yang terbuka.

### Tinjau

Di lab ini, Anda sebagai admin telah melalui proses mengaktifkan pengaturan ulang kata sandi mandiri. Dengan mengaktifkan SSPR, Anda kemudian akan berperan sebagai pengguna untuk menjalani proses pendaftaran SSPR dan juga mengatur ulang kata sandi Anda.  Terakhir, Anda sebagai admin telah mempelajari tempat mengakses log audit serta data penggunaan & wawasan untuk SSPR.
