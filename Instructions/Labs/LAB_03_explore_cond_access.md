---
lab:
    title: 'Menjelajahi manajemen akses di Azure AD dengan Bersyarat'
    module: 'Modul 2 Pelajaran 3: Menjelaskan kemampuan Microsoft Identity dan solusi manajemen akses: Mempelajari kemampuan manajemen akses Microsoft Azure AD'
---


# Lab: Menjelajahi manajemen akses di Azure AD dengan Bersyarat

## Skenario lab
Di lab ini, Anda akan menjelajahi MFA akses bersyarat, dari perspektif admin dan pengguna.  Sebagai admin, Anda akan membuat kebijakan yang mengharuskan pengguna untuk menggunakan autentikasi multifaktor ketika mengakses aplikasi Manajemen Microsoft Azure berbasis cloud.  Dari perspektif pengguna, Anda akan melihat hasil dari kebijakan akses bersyarat, termasuk proses mendaftar ke MFA.

**Perkiraan Waktu**: 10-15 menit

#### Tugas 1: Di tugas ini Anda, sebagai admin akan mengatur ulang kata sandi untuk pengguna bernama Debra Berger.  Tahap ini diperlukan agar Anda dapat mulai masuk sebagai pengguna dalam tugas berikutnya.

1. Buka Microsoft Edge.  DI bilah alamat, masukkan **portal.azure.com**.

2. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Pilih **Azure Active Directory**.  

4. Dari panel navigasi sebelah kiri, pilih **Users**.

5. Pilih **Debra Berger** dari daftar pengguna.

6. Pilih **Atur ulang kata sandi** di bagian atas halaman. Karena belum pernah masuk sebagai Debra Berger sebelumnya, Anda tidak mengetahui kata sandinya dan perlu mengatur ulang kata sandi.

7. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda akan memerlukannya pada tugas berikutnya, yaitu untuk bisa masuk sebagai pengguna.

8. Tutup jendela atur ulang kata sandi dengan mengeklik **X** di bagian pojok kanan atas halaman.

9. Tutup jendela Pengguna dengan mengeklik **X** di pojok kanan atas halaman.

10. Biarkan jendela ini terbuka.


#### Tugas 2:  Di tugas ini, Anda akan memahami proses membuat kebijakan akses bersyarat di Azure AD.

1. Buka tab browser, yang diberi label Contoso – Microsoft Azure.   Jika sebelumnya Anda menutup tab browser, buka Microsoft Edge dan di bilah alamat masukkan portal.azure.com dan masuk menggunakan kredensial admin Anda, kemudian pilih Azure Active Directory.  

2. Dari panel navigasi kiri, pilih **Security**.

3. Dari panel navigasi kiri, pilih **Conditional Access**.

4. Layar Kebijakan Akses Bersyarat akan ditampilkan. Semua Kebijakan Akses Bersyarat dicantumkan di sini. Pilih **New Policy**.

5. Pada Nama bidang, masukkan **MFA Test Policy**.

6. Pada Pengguna dan grup, pilih **0 users and groups selected**.

7. Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup.  Pastikan **Include** dipilih (digarisbawahi).

8. Pilih opsi untuk **Select users and groups**, lalu pilih **Users and groups**.  Jendela untuk Memilih pengguna dan grup akan terbuka.  

9. Di Bilah pencarian, masukkan **Debra**.  Pilih **Debra Berger** di bawah bilah pencarian, lalu klik tombol **Select** di bagian bawah halaman.  Perlu dicatat, menetapkan kebijakan untuk pengguna dalam grup adalah praktik yang umum.  Untuk kelayakan tujuan menggunakan lab ini, kita akan menetapkan kebijakan untuk pengguna tertentu. 

10. Pada tindakan atau aplikasi Cloud, pilih **No cloud apps or actions selected**.

11. Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan tindakan pengguna atau aplikasi cloud.  Pastikan **Cloud apps** disorot dan **Include** dipilih (digarisbawahi), lalu pilih **Select apps**.  Jendela untuk Memilih aplikasi Cloud akan terbuka.

12. Pada bilah pencarian, masukkan **Azure**.  Dari hasil pencarian yang muncul di bawah kotak pencarian, pilih **Microsoft Azure Management**, lalu klik **Select** di bagian bawah halaman.  Perhatikan peringatan.  

13. Pada Kondisi, pilih **0 conditions selected**.  Perhatikan berbagai opsi yang dapat Anda konfigurasikan.  Dengan kebijakan, Anda dapat mengontrol akses pengguna berdasarkan sinyal dari kondisi seperti risiko, platform perangkat, lokasi, aplikasi klien, atau keadaan perangkat.  Misalnya, Anda dapat mencantumkan kondisi untuk kebijakan agar diterapkan di lokasi mana saja kecuali yang dipilih atau lokasi yang tepercaya seperti jaringan pusat Anda.  Untuk kebijakan ini, jangan atur kondisi.

14. Sekarang Anda akan mengatur kontrol akses.  Pada Grant, pilih **0 controls selected**.

15. Jendela Grant akan terbuka.  Pastikan **Grant access** dipilih, kemudian pilih **Require multi-factor authentication**.  Pada bagian Untuk beberapa kontrol, biarkan default **Require all the selected controls**.  Klik **Select** di bagian bawah halaman.

16. DI bagian bawah halaman, di Aktifkan kebijakan, pilih **On**, lalu klik **Create button**.

17. Beberapa detik kemudian, kebijakan Pertama MFA akan muncul di daftar kebijakan akses bersyarat (jika perlu, pilih **Refresh** di bagian atas halaman).

18. Keluar dari Azure, lalu tutup jendela browser Anda.

#### Tugas 3: Pada tugas ini, Anda akan menliaht hasil dari kebijakan akses bersyarat, dari persperktif pengguna yaitu Debra Berger. Anda akan mulai pertama kali dengan masuk ke aplikasi yang tidak disertakan dalam kebijakan akses bersyarat.  Lalu Anda akan mengulang proses kembali untuk aplikasi yang disertakan dalam kebijakan akses bersyarat.  Ingat kembali bahwa kebijakan mengharuskan pengguna untuk menggunakan MFA ketika mengakses aplikasi Manajemen Microsoft Azure.  Untuk menggunakan MFA, pengguna terlebih dahulu harus mendaftar ke metode autentikasi yang akan digunakan untuk MFA, misalnya kode yang dikirimkan ke perangkat seluler atau aplikasi autentikasi.

1. Buka Microsoft Edge.  Pada bilah halaman browser, masukkan **https://login.microsoftonline.com/**.

1. Masuk sebagai Debra Burger,
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi yang Anda catat sebelumnya. Pilih **Sign in**.
    1. Karena kata sandi yang tersedia ketika Anda menjadi admin mengatur ulang kata sandi secara sementara, Anda perlu memperbarui kata sandi Anda (ini bukan bagian dari MFA).  Masukkan kata sandi saat ini, lalu untuk kata sandi baru dan bidang konfirmasi kata sandi masukkan **SC900-Lab**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**

1. Anda telah berhasil masuk ke akun Microsoft 365 Anda.  MFA tidak diperlukan untuk aplikasi ini karena tidak menjadi bagian kebijakan.

1. Sekarang Anda akan berupaya untuk masuk ke aplikasi yang sesuai dengan kriteria MFA.  Buka Microsoft Edge dan di bilah alamat, masukkan https://portal.azure.com.

1. Anda akan melihat jendela yang menunjukkan, Perlu informasi selengkapnya.  Klik **Next**.  Perlu diperhatikan, upaya ini akan memulai proses pendaftaran MFA, karena ini adalah upaya pertama kali untuk mengakses aplikasi cloud yang diidentifikasi dalam kebijakan akses bersyarat.  Proses pendaftaran diperlukan sekali saja.   Cara untuk mendorong pengguna untuk melewati proses pendaftaran adalah dengan membuat admin mengonfigurasi metode autentikasi untuk digunakan.

1. Di jendela Amankan akun Anda, Anda memiliki opsi untuk memilih metode yang digunakan untuk MFA.  Salah satunya adalah Microsoft Authenticator. Untuk kelayakan pada latihan lab ini, Anda akan memilih metode lain.  Pilih **I want to setup a different method**.  Dari jendela pop-up Pilih metode lain, klik **panah tarik-turun**, lalu pilih **Phone**, kemudian pilih **Confirm**.

1. Di jendela yang terbuka, pastikan negara Anda sudah dipilih lalu masukkan nomor ponsel yang ingin Anda gunakan lalu pilih, pastikan **Text me a code** sudah dipilih, lalu tekan **Next**.  Layar akan menampilkan, "SMS terverifikasi. Ponsel Anda berhasil terdaftar".  Klik **Next**. Lalu pilih **Done**.  yang menyelesaikan proses pendaftaran satu kali.

1. Anda mungkin akan mendapatkan pesan yang menunjukkan bahwa waktu proses masuk Anda habis.  Cukup masukkan kata sandi **SC900-Lab**, lalu tekan **Sign in**.

1. Anda akan melihat jendela yang meminta Anda untuk memasukkan kode yang dikirimkan ke ponsel Anda.  Masukan kode dan klik **Next**.  Pengalaman inilah yang akan Anda rasakan sebagai Gerhart kapan saja ketika Anda mengakses aplikasi cloud Manajemen Microsoft Azure, seperti Azure Portal yang sesuai dengan kebijakan MFA.

1. Anda akan melihat jendela yang meminta Anda untuk memasukkan kode yang dikirimkan ke ponsel Anda.  Masukkan kode dan klik tombol **Verify** .  Ketika diminta untuk tetap masuk, pilih **No**.

1. Sekarang Anda dapat mengakses portal Azure.  Portal Azure adalah aplikasi Manajemen Microsoft Azure dan oleh sebab itu memerlukan autentikasi multifaktor, sesuai dengan kebijakan akses bersyarat yang sudah dibuat.  

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di pojok kanan atas layar dan mengeklik Keluar. Kemudian tutup semua jendela browser.

#### Tinjauan
Di lab ini, Anda telah memahami proses menyiapkan kebijakan akses bersyarat yang mengharuskan pengguna untuk melalui MFA ketika mereka mengakses aplikasi cloud Manajemen Microsoft Azure.  Kemudian, sebagai pengguna Anda telah memahami proses pendaftaran untuk MFA dan melihat hasil kebijakan akses bersyarat yang mengharuskan Anda untuk menggunakan MFA ketika mengakses portal Azure.
