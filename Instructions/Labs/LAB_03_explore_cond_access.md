<a name="---"></a><!---
---
Lab: Jalur Pembelajaran: 'Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari modul Microsoft Entra': 'Menjelaskan kemampuan manajemen akses pelajaran Azure AD': 'Menjelaskan Akses Bersyarat di Azure AD'
---
--->

# <a name="lab-explore-access-management-in-azure-ad-with-conditional-access"></a>Lab: Menjelajahi manajemen akses di Azure Active Directory dengan Akses Bersyarat

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra
- Modul: Menjelaskan kemampuan manajemen akses Azure AD
- Pelajaran: Menjelaskan akses bersyarat di Azure AD

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari MFA akses bersyarat, dari sudut pandang admin dan pengguna.  Sebagai admin, Anda akan membuat kebijakan yang mengharuskan pengguna melalui autentikasi multifaktor saat mengakses aplikasi Microsoft Azure Management berbasis cloud.  Dari perspektif pengguna, Anda akan melihat dampak kebijakan akses bersyarat, termasuk proses pendaftaran MFA.

**Perkiraan Waktu**: 30 menit

### <a name="task-1"></a>Tugas 1

Di tugas ini Anda, sebagai admin akan mengatur ulang kata sandi untuk pengguna bernama Debra Berger.  Langkah ini diperlukan agar Anda dapat masuk sebagai pengguna di tugas berikutnya.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **portal.azure.com**.

2. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Di sudut kiri atas layar, di sebelah pada bagian yang bertuliskan Microsoft Azure, pilih ikon menu Tampilkan portal (tiga garis horizontal juga disebut sebagai ikon hamburger) lalu dari panel navigasi kiri, di bawah Favorit, pilih Azure Active Directory. Jika tidak tercantum di bawah favorit, lalu di kotak pencarian, masukkan Azure Active Directory, lalu dari daftar hasil, pilih **Azure Active Directory**.

4. Dari panel navigasi sebelah kiri, pilih **Users**.

5. Pilih **Debra Berger** dari daftar pengguna.

6. Pilih **Reset password** dari bagian atas halaman. Karena sebelumnya Anda belum masuk sebagai Debra Berger, Anda tidak mengetahui kata sandinya, dan harus mengatur ulang kata sandinya.

7. Ketika jendela pengaturan ulang kata sandi terbuka, pilih **Reset Password**.  PENTING, catat kata sandi baru, karena Anda memerlukannya di tugas berikutnya, agar dapat masuk sebagai pengguna.

8. Tutup jendela pengaturan ulang kata sandi dengan memilih **X** di pojok kanan atas halaman, lalu tutup jendela Debra Berger dengan memilih **X** di pojok kanan atas halaman.

9. Tutup jendela Pengguna dengan mengeklik **X** di pojok kanan atas halaman.

10. Anda sekarang kembali ke halaman **Contoso | Ringkasan**.  Biarkan jendela ini terbuka.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda akan menjalani proses pembuatan kebijakan akses bersyarat di Azure Active Directory.

1. Buka tab browser, yang diberi label Contoso – Microsoft Azure.   Jika sebelumnya Anda menutup tab browser, buka Microsoft Edge, dan di bilah alamat masukkan portal.azure.com dan masuk dengan kredensial admin Anda, lalu pilih Azure Active Directory.  

2. Dari panel navigasi kiri, pilih **Security**.

3. Dari panel navigasi kiri, pilih **Conditional Access**.

4. Layar Kebijakan Akses Bersyarat akan ditampilkan. Semua Kebijakan Akses Bersyarat dicantumkan di sini. Pilih **+ Kebijakan baru**.

5. Pada Nama bidang, masukkan **MFA Test Policy**.

6. Di bagian Pengguna atau identitas beban kerja, pilih **0 pengguna atau identitas beban kerja dipilih**.

7. Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup.  Pastikan **Include** dipilih (digarisbawahi).

8. Pilih opsi untuk **Select users and groups**, lalu pilih **Users and groups**.  Jendela untuk Memilih pengguna dan grup akan terbuka.  

9. Di Bilah pencarian, masukkan **Debra**.  Pilih **Debra Berger** di bawah bilah pencarian, lalu klik tombol **Select** di bagian bawah halaman.  Perlu dicatat, menetapkan kebijakan untuk pengguna dalam grup adalah praktik yang umum.  Demi kepentingan lab ini, kami akan menetapkan kebijakan ke pengguna tertentu.

10. Di bagian Aplikasi atau tindakan cloud, pilih **Tidak ada aplikasi cloud, tindakan, atau konteks terautentikasi yang dipilih**.

11. Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan aplikasi cloud atau tindakan pengguna.  Pastikan **Aplikasi cloud** disertakan dalam bidang berlabel Pilih tujuan penerapan kebijakan ini.  Jika belum disertakan, pilih dari menu dropdown. Pastikan **Sertakan** dipilih (digarisbawahi), lalu pilih **Pilih aplikasi**, lalu di bawah tulisan Pilih, pilih **Tidak ada**.  Jendela untuk Memilih aplikasi Cloud akan terbuka.

12. Pada bilah pencarian, masukkan **Azure**.  Dari hasil pencarian yang muncul di bawah kotak pencarian, pilih **Microsoft Azure Management**, lalu klik **Select** di bagian bawah halaman.  Perhatikan peringatan.  

13. Pada Kondisi, pilih **0 conditions selected**.  Perhatikan berbagai opsi yang dapat Anda konfigurasikan.  Dengan kebijakan, Anda dapat mengontrol akses pengguna berdasarkan sinyal dari kondisi seperti risiko, platform perangkat, lokasi, aplikasi klien, atau keadaan perangkat.  Misalnya, Anda dapat mencantumkan kondisi untuk kebijakan agar diterapkan di lokasi mana saja kecuali yang dipilih atau lokasi yang tepercaya seperti jaringan pusat Anda.  Untuk kebijakan ini, jangan atur kondisi.

14. Sekarang Anda akan mengatur kontrol akses.  Pada Grant, pilih **0 controls selected**.

15. Jendela Grant akan terbuka.  Pastikan **Izinkan akses** dipilih, lalu pilih **Memerlukan autentikasi multifaktor**. Gulir ke bawah sedikit di jendela kanan dan di bawah bagian Untuk beberapa kontrol, biarkan default **Memerlukan semua kontrol yang dipilih**.  Klik **Select** di bagian bawah halaman.

16. Di bawah halaman, Di bagian Aktifkan kebijakan, pilih **Aktif**, lalu pilih **Buat**.

17. Beberapa detik kemudian, kebijakan Pertama MFA akan muncul di daftar kebijakan akses bersyarat (jika perlu, pilih **Refresh** di bagian atas halaman).

18. Keluar dari Azure, lalu tutup jendela browser Anda.

### <a name="task-3"></a>Tugas 3

Dalam tugas ini Anda akan melihat dampak dari kebijakan akses bersyarat, dari sudut pandang pengguna, Debra Berger. Anda akan mulai terlebih dahulu dengan masuk ke aplikasi yang tidak termasuk dalam kebijakan akses bersyarat.  Kemudian Anda akan mengulangi proses untuk aplikasi yang termasuk dalam kebijakan akses bersyarat.  Ingat kembali bahwa kebijakan mengharuskan pengguna untuk menggunakan MFA ketika mengakses aplikasi Manajemen Microsoft Azure.  Untuk menggunakan MFA, pengguna terlebih dahulu harus mendaftar ke metode autentikasi yang akan digunakan untuk MFA, misalnya kode yang dikirimkan ke perangkat seluler atau aplikasi autentikasi.

1. Masuk sebagai Debra Burger. 
    1. Di jendela Masuk, masukkan **DebraB@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi yang Anda catat sebelumnya. Pilih **Masuk**.
    1. Karena kata sandi yang diberikan saat Anda, sebagai admin, mengatur ulang kata sandi bersifat sementara, Anda perlu memperbarui kata sandi (ini bukan bagian dari kebijakan MFA). Masukkan kata sandi saat ini, lalu untuk kata sandi baru masukkan **SC900-Lab**, lalu masukkan lagi **SC900** untuk mengonfirmasi kata sandi.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.  Anda telah berhasil masuk ke akun Microsoft 365 Anda. MFA tidak diperlukan untuk aplikasi ini karena tidak menjadi bagian kebijakan.

1. Sekarang Anda akan mencoba masuk ke aplikasi yang memenuhi kriteria untuk MFA. Buka tab baru di portal.Microsoft Microsoft Edge dan di bilah alamat, masukkan **portal.azure.com**.

1. Anda akan melihat jendela yang menunjukkan, Informasi lebih lanjut diperlukan.  Pilih **Selanjutnya**.  Perlu diperhatikan, tindakan ini akan memulai proses pendaftaran MFA, karena ini adalah pertama kalinya Anda mengakses aplikasi cloud yang diidentifikasi dalam kebijakan akses bersyarat.  Proses pendaftaran diperlukan sekali saja.   Cara untuk mendorong pengguna untuk melewati proses pendaftaran adalah dengan membuat admin mengonfigurasi metode autentikasi untuk digunakan.

1. Di jendela Amankan akun Anda, Anda memiliki opsi untuk memilih metode yang digunakan untuk MFA.  Salah satunya adalah Microsoft Authenticator. Untuk kelayakan dalam latihan lab ini, Anda akan memilih metode yang berbeda.  Pilih **I want to setup a different method**.  Dari jendela pop-up Pilih metode lain, klik **panah tarik-turun**, lalu pilih **Phone**, kemudian pilih **Confirm**.

1. Di jendela yang terbuka, pastikan negara Anda dipilih lalu masukkan nomor ponsel yang ingin digunakan.  Pastikan bahwa **Kirimi saya kode** dipilih, lalu tekan **Berikutnya**.  Anda akan menerima pesan teks di ponsel dengan kode yang harus dimasukkan di tempat yang bertuliskan masukkan kode.  Masukkan kode yang Anda terima, lalu tekan **Berikutnya**.  Setelah dikonfirmasi, layar akan menampilkan, "SMS diverifikasi. Ponsel Anda berhasil didaftarkan".  Pilih **Selanjutnya**. lalu pilih **Selesai**.  yang menyelesaikan proses pendaftaran satu kali.

1. Sekarang Anda dapat mengakses portal Azure.  Portal Azure adalah aplikasi Manajemen Microsoft Azure dan oleh sebab itu memerlukan autentikasi multifaktor, sesuai dengan kebijakan akses bersyarat yang sudah dibuat.  
    1. Jika Anda mendapatkan pesan yang menunjukkan bahwa waktu masuk Anda habis, masukkan kata sandi **SC900-Lab** dan pilih **Masuk**. 
    1. Anda akan melihat jendela yang mengharuskan memverifikasi identitas.  Pilih tempat yang bertuliskan Teks =X XXXXXXX untuk menerima kode di ponsel Anda, masukkan kode dan pilih **Verifikasi**.
    1. Jika Anda diminta untuk tetap masuk, pilih **Tidak**.

1. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih keluar. Kemudian tutup semua jendela browser.

### <a name="review"></a>Tinjau

Di lab ini, Anda menjalani proses penyiapan kebijakan akses bersyarat yang mengharuskan pengguna melalui MFA saat mengakses aplikasi cloud Microsoft Azure Management.  Kemudian, sebagai pengguna Anda telah memahami proses pendaftaran untuk MFA dan melihat hasil kebijakan akses bersyarat yang mengharuskan Anda untuk menggunakan MFA ketika mengakses portal Azure.
