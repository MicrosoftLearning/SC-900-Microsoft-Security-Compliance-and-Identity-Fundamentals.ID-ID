---
lab:
    title: 'Menjelajahi Autentikasi Microsoft Azure AD dengan pengaturan ulang kata sandi mandiri'
    module: 'Modul 2 Pelajaran 2: Menjelaskan kemampuan Microsoft Identity dan solusi manajemen akses: Menjelaskan metode autentikasi lain dari Microsoft Azure AD'
---

# Lab: Menjelajahi Autentikasi Microsoft Azure AD dengan pengaturan ulang kata sandi mandiri

## Skenario lab

Di lab ini, Anda sebagai admin akan menjalani proses pengaktifan pengaturan ulang kata sandi mandiri. Dengan mengaktifkan SSPR, Anda akan berperan sebagai pengguna dan menjalani proses pendaftaran SSPR dan juga mengatur ulang kata sandi Anda.  Terakhir, Anda sebagai admin akan dapat melihat log audit serta data penggunaan & wawasan untuk SSPR.

**Perkiraan Waktu**: 15-20 menit


#### Tugas 1:  Dalam tugas ini, Anda,sebagai admin akan menambahkan pengguna yang sudah ada, Adele Vance, ke dalam grup SSPRSecurityUsers.  Selain itu, Anda juga perlu melakukan pengaturan ulang kata sandi pengguna sehingga Anda dapat melakukan upaya masuk yang pertama kali sebagai pengguna dan mendaftar SSPR.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan**portal.azure.com** dan masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Pilih **Azure Active Directory**.  

4. Dari panel navigasi sebelah kiri, pilih  **Groups**.

5. Daftar grup yang ada akan ditampilkan. Di bidang Cari grup, masukkan **SSPR**, lalu dari hasil pencarian pilih **SSPRSecurityGroupUsers**.  Anda akan diarahkan ke opsi konfigurasi untuk grup ini.

6. Dari panel navigasi sebelah kiri, pilih **Members**.

7. Dari bagian atas halaman, pilih **+ Add members**.  

8. Di kotak Pencarian, masukkan **Adele**.  Ketika pengguna, **Adele Vance**, muncul di bawah kotak pencarian, pilih dan tekan **Select** dari bagian bawah halaman.

9. Tutup jendela SSPRSecurityUsers, pilih **X** di sudut kanan atas layar,

10. Kembali ke halaman Direktori Aktif, dengan memilih **Contoso** dari sudut kiri atas layar, tepat di atas tulisan Grup, untuk kembali ke halaman Contoso Azure Active Directory.

11. Dari panel navigasi sebelah kiri, pilih **Users**.

12. Pilih **Adele Vance** dari daftar pengguna.

13. Pilih **Reset password** dari bagian atas halaman. Karena Anda belum pernah masuk sebagai Adele Vance, Anda perlu mengatur ulang sandi

14. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda akan memerlukannya di tugas berikutnya untuk dapat masuk sebagai pengguna.

15. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di sudut kanan atas halaman.

16. Tutup jendela Adele Vance dengan memilih **X** di sudut kanan atas halaman.

17. Tutup jendela Pengguna dengan memilih **X**  di sudut kanan atas halaman.

18. Biarkan jendela Ringkasan Contoso tetap terbuka karena Anda akan menggunakannya dalam tugas berikutnya.

#### Tugas 2: Dalam tugas ini, Anda sebagai admin akan mempelajari cara mengonfigurasi pengaturan ulang Kata Sandi untuk pengguna, termasuk konfigurasi jenis metode autentikasi yang akan digunakan.

1. Buka tab Contoso – Microsoft Azure yang terbuka di browser Anda. Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan pilih Azure Active Directory.  Anda harus masuk sebagai admin di portal Microsoft Azure. Jika tidak, masuk kembali.

2. Dari panel navigasi sebelah kiri, pilih **Password reset**.  

3. Properti untuk pengaturan ulang kata sandi mandiri ditampilkan.  Pastikan bahwa **Self service reset** telah **dipilih** untuk grup yang terdaftar, **SSPRSecurityUsers**.  Arahkan kursor Anda di atas ikon informasi di samping tulisan “select group” dan perhatikan yang tercantum, “Menentukan grup pengguna yang diizinkan untuk mengatur ulang kata sandi milik mereka." Anda harus menyertakan pengguna dalam grup, Anda tidak dapat memilih pengguna satu per satu.  Selain itu, jika Anda mengubah grup, grup yang Anda pilih akan menggantikan grup yang sudah terdaftar.  Karena itu, sebaiknya Anda menambahkan pengguna ke grup SSPR.  Terakhir, perhatikan kotak informasi berwarna biru, "Pengaturan ini hanya berlaku untuk pengguna akhir di organisasi Anda. Admin selalu mengaktifkan layanan pengaturan ulang kata sandi mandiri dan diharuskan menggunakan dua metode autentikasi untuk mengatur ulang kata sandi mereka.”

5. Dari panel navigasi sebelah kiri Pengaturan ulang kata sandi, pilih **Authentication Methods**.

6. Di bagian Jumlah metode yang diperlukan untuk diam, pilih **1**. Perhatikan kotak informasi di layar.

7. Perhatikan berbagai macam metode yang tersedia bagi pengguna.  **Email** dan **Mobile phone (SMS only)** harus sudah dicentang; pilihlah jika belum.

8. Dari panel navigasi sebelah kiri pengaturan ulang kata sandi, pilih **Registration**.  

9. Pastikan pengaturan Mewajibkan pengguna untuk mendaftar saat masuk ditetapkan ke **Yes**.  Biarkan Jumlah hari sebelum pengguna diminta untuk mengonfirmasi ulang informasi autentikasi mereka ditetapkan ke nilai default 180.   Perhatikan kotak informasi di halaman itu.

10. Dari panel navigasi sebelah kiri Pengaturan ulang kata sandi, pilih **Notifications**.  

11. Pastikan pengaturan untuk Memberi tahu pengguna tentang pengaturan ulang sandi ditetapkan ke **Yes**.  Biarkan pengaturan untuk Memberi tahu semua admin ketika admin lain mengatur ulang kata sandi mereka ke Tidak.

12. Perhatikan bagaimana panel navigasi pengaturan ulang kata sandi juga menyertakan opsi untuk melihat log audit serta Penggunaan & wawasan.

13. **Sign out** dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.


#### Tugas 3:  Dalam tugas ini, Anda sebagai pengguna Adele Vance akan melalui proses pendaftaran untuk pengaturan ulang kata sandi mandiri.  Tugas ini mengharuskan Anda memiliki akses ke perangkat seluler tempat Anda dapat menerima pesan teks atau akun email pribadi yang dapat diakses.
 
1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **login.microsoftonline.com**.

3. Masuk sebagai Adele Vance,
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi yang Anda catat sebelumnya. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

4. Karena ini adalah pertama kalinya Anda masuk sebagai Adele Vance, Anda akan diminta untuk mengatur ulang kata sandi.  Masukkan kata sandi lama Anda.  Untuk kata sandi baru Anda, masukkan **SC900-Lab**. Masukkan **SC-900-Lab** di bidang konfirmasi kata sandi.  Pilih **Sign in**.  Catatan: kami menggunakan kata sandi ini hanya untuk kemudahan lab. Sebaiknya, Anda memasukkan kata sandi yang lebih aman.

5. Tampilan pop-up yang menunjukkan bahwa informasi lebih lanjut diperlukan.  Hal ini karena sebagai anggota grup SSPRSecurityUsers, konfigurasi mengharuskan anggotanya untuk mendaftar ketika mereka masuk. Pilih tombol **Next**.  Catatan:  Alternatif untuk meminta pengguna melakukan pendaftaran sendiri, agar admin segera mengonfigurasi metode autentikasi saat mereka menambahkan pengguna. Hal ini mengharuskan admin untuk mengetahui dan mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan pengaturan ulang kata sandi mandiri, dan mengatur ulang kata sandi pengguna.

6. Halaman "Amankan akun Anda" akan terbuka.  Jendela yang muncul yaitu untuk metode autentikasi Ponsel, jika Anda tidak memiliki perangkat seluler yang dapat menerima pesan teks, lewati ke langkah berikutnya.  Anda diminta untuk memasukkan nomor ponsel. Pastikan pilihan **Text me a code** diaktifkan.   Masukkan nomor ponsel tempat Anda dapat menerima kode teks dan pilih **tombol Next**.  Jendela baru terbuka menunjukkan kode baru saja dikirim ke ponsel yang Anda masukkan.  Masukkan kode yang Anda terima dan pilih **Next**. Jendela terbuka menunjukkan Berhasil dan menampilkan metode Masuk default Anda.  Pilih **Done**.  

7. Lewati langkah ini jika Anda dapat mengonfigurasi SSPR dengan nomor ponsel Anda.  Atau, Anda dapat mengatur metode yang berbeda seperti yang ditunjukkan di bagian kiri bawah jendela.  Jika Anda memilih untuk menyiapkan metode yang berbeda, pilih **I want to set up a different method**, jendela pop-up akan muncul, menanyakan Metode mana yang ingin Anda gunakan?  Dari menu tarik-turun, pilih metode yang Anda inginkan, **Email**, lalu pilih tombol **Confirm**.  Masukkan email yang ingin Anda gunakan, lalu pilih **Next**.  Jendela baru terbuka menunjukkan bahwa kode baru saja dikirim ke email yang Anda masukkan.  Akses email yang Anda masukkan untuk mendapatkan kode.  Masukkan kode yang Anda terima dan pilih **Next**. Jendela terbuka menunjukkan Berhasil dan menampilkan metode Masuk default Anda.  Pilih **Done**.

8. Sekarang Anda dapat menyelesaikan proses masuk. Anda akan diarahkan ke halaman arahan portal Microsoft Azure.  Jika Anda melihat waktu proses masuk Anda telah kedaluwarsa, cukup masukkan kembali kata sandi, SC900-Lab.

9. Keluar dari portal Microsoft Azure dan tutup jendela browser Anda. 

#### Tugas 4 (Opsional): Dalam tugas ini, Anda sebagai pengguna Adele Vance akan melalui proses pengaturan ulang kata sandi.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan login.microsoftonline.com.

3. Masuk sebagai Adele Vance, dengan memasukkan email Anda **AdeleV@WWLxZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab) dan pilih tombol **Next**. Sebagai gantinya, Anda mungkin melihat jendela Pilih akun terbuka, jika demikian, pilih akun untuk Adele Vance.

4. Dari jendela Masukkan kata sandi, pilih **Forgot my password**. 

5. Kembali ke jendela akun Anda yang terbuka.   Pastikan email untuk Adele Vance, AdeleV@WWLxZZZZ.onmicrosoft.com, ditampilkan di kotak email atau nama pengguna.  Jika tidak, masukkan.  

6. Di kotak kosong, masukkan karakter yang ditampilkan dalam gambar atau kata-kata dari audio. Setelah Anda memasukkannya, pilih **Next**.

7. Layar menunjukkan Kembali ke akun Anda dan menunjukkan langkah Verifikasi 1 > pilih kata sandi baru. Biarkan pengaturan default **Text my mobile phone**.  Anda diminta untuk memasukkan nomor ponsel Anda.  Setelah Anda memasukkannya, pilih **Text button**.  Jika selama pendaftaran Anda memilih email, jendela Kembali ke akun Anda akan menunjukkan bahwa Anda akan menerima email yang berisi kode verifikasi di alamat email alternatif Anda.  Pilih **Email**. 

8. Masukkan kode verifikasi lalu tekan **Next**.

9. Di layar berikutnya, Anda diminta memasukkan kata sandi baru dan mengonfirmasi kata sandi baru.  Masukkan kata sandi dan pilih tombol **Finish**.

10. Anda akan melihat pesan di layar bahwa kata sandi Anda telah diatur ulang.  Pilih **click here** untuk masuk dengan kata sandi baru Anda.

11. Dari kotak Pilih informasi akun, pilih **AdeleV@WWLxZZZZZZ.onmicrosoft.com**, masukkan kata sandi baru Anda, lalu pilih tombol **Sign in**.  Jika Anda diminta untuk Tetap masuk, pilih **No**.

12. Anda akan diarahkan ke portal Microsoft Azure.

13. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan pilih **Sign out**. Kemudian tutup semua jendela browser

#### Tugas 5 (Opsional):  Dalam tugas ini, Anda sebagai administrator, akan secara singkat melihat log Audit serta data Penggunaan & wawasan yang terkait dengan pengaturan ulang kata sandi.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **portal.azure.com** 

3. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

4. Pilih **Azure Active Directory**.  

5. Dari panel navigasi sebelah kiri, pilih **Password rest**.

6. Dari panel navigasi sebelah kiri, pilih **Audit logs**.  Perhatikan informasi dan filter yang tersedia.  Perhatikan juga bahwa Anda dapat mengunduh log.  

7. Pilih **Download**.  Perhatikan bahwa Anda dapat memformat unduhan sebagai CSV atau JSON.  Tutup jendela dengan memilih **X** di sudut kanan atas layar.

8. Dari panel navigasi sebelah kiri, pilih **Usage & insights**.

9. Perhatikan informasi tersedia yang berkaitan dengan Pendaftaran.  Perhatikan bahwa mungkin perlu waktu untuk menyegarkan data ini, bahkan setelah Anda melakukan penyegaran, sehingga mungkin pendaftaran atau data penggunaan dari tugas sebelumnya belum ditampilkan.

10. Dari bagian atas halaman, pilih **Usage** untuk melihat jumlah Pengaturan ulang kata sandi mandiri dan pembukaan akun berdasarkan metode.  Perhatikan bahwa mungkin perlu waktu untuk menyegarakan data ini, bahkan setelah Anda melakukan penyegaran, sehingga mungkin data penggunaan dari tugas sebelumnya belum ditampilkan.

11. Tutup tab browser yang terbuka.


#### Tinjauan
Di lab ini, Anda sebagai admin telah melalui proses mengaktifkan pengaturan ulang kata sandi mandiri. Dengan mengaktifkan SSPR, Anda diasumsikan sebagai pengguna yang harus menjalani proses pendaftaran SSPR dan juga mengatur ulang kata sandi.  Terakhir, Anda sebagai admin telah mempelajari tempat mengakses log audit serta data penggunaan & wawasan untuk SSPR.
