<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi Jalur Pembelajaran/Modul/Pelajaran Azure Active Directory': 'Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra; Modul 1: Menjelaskan layanan dasar dan jenis identitas Azure AD; Pelajaran 4: Menjelaskan jenis identitas Azure AD'
---
--->

# <a name="lab-explore-azure-active-directory"></a>Lab: Mempelajari Azure Active Directory

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra
- Modul: Menjelaskan layanan dasar dan jenis identitas Azure AD
- Pelajaran: Menjelaskan jenis identitas Azure AD

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mengakses Azure Active Directory.  Selain itu, Anda akan membuat pengguna dan mengonfigurasi pengaturan yang berbeda, termasuk menambahkan lisensi.  

**Perkiraan Waktu**: 10-15 menit

### <a name="task-1"></a>Tugas 1

Sebagai pelanggan Microsoft 365, Anda sudah menggunakan Azure Active Directory.  Dalam tugas ini, Anda akan menelusuri cara mengakses Azure Active Directory melalui portal Admin Microsoft 365 dan melalui portal Microsoft Azure.

1. Dari browser Microsoft Edge, pilih tab berlabel Beranda - pusat admin Microsoft 365.

1. Jika sebelumnya Anda menutup tab browser tersebut, ikuti langkah-langkah di bawah ini:
    1. di bilah alamat, masukkan **admin.microsoft.com** dan masuk dengan kredensial admin Anda sebagai berikut:
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.
    1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian Pusat admin, pilih **Azure Active Directory** (Anda mungkin perlu menggulir ke bawah).  Halaman browser baru membuka halaman Dasbor Saya di pusat admin Azure Active Directory. Dari jendela utama dasbor, Anda akan melihat beberapa petak peta, termasuk petak peta Identitas Organisasi (Contoso, penyewa, dan edisi Azure Active Directory), petak peta untuk pengguna dan grup, dan lainnya.

1. Dari panel navigasi sebelah kiri, di bagian favorit, pilih **Azure Active Directory**.  Di jendela utama, Anda akan melihat panel navigasi lain yang mencantumkan semua layanan yang tersedia di Azure Active Directory. Di sebelah kanan, Anda akan melihat informasi tentang penyewa Contoso dan tautan ke jenis identitas yang dapat Anda buat dan layanan unggulan.  

1. Sekarang buka jendela browser baru dan di bilah alamat, masukkan **portal.azure.com**.  Karena Anda sudah masuk sebagai admin@WWLxZZZZZZ.onmicrosoft.com dan awalnya menggunakan kredensial yang sama untuk menukarkan kartu Azure, Anda harus masuk sebagai admin saat mengakses portal Microsoft Azure.  Anda dapat memverifikasi hal ini dengan memeriksa email di sudut kanan atas halaman dan mengarahkan mouse ke atas ikon pengguna.

1. Halaman arahan portal Microsoft Azure menampilkan layanan Azure, termasuk Azure Active Directory, Komputer Virtual, akun penyimpanan, database, dan banyak lagi.  Pilih **Layanan Lainnya**, lalu pilih **Azure Active Directory**. Jika Anda tidak langsung melihatnya, Anda dapat memasukkan Azure Active Directory di bilah pencarian warna biru dan memilihnya dari sana.  

1. Anda kini melihat Azure Active Directory untuk penyewa Microsoft 365 Contoso.    Pendekatan apa pun yang Anda gunakan untuk mengakses layanan Azure Active Directory (portal admin Microsoft 365 atau portal Microsoft Azure) akan berakhir di tempat yang sama – Contoso Azure Active Directory tempat Anda dapat mengelola semua layanan Microsoft Azure AD.

1. Biarkan halaman browser ini terbuka untuk tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda akan mempelajari cara membuat pengguna baru di Azure Active Directory dan menjelajahi beberapa layanan yang dapat dikelola di tingkat pengguna.

1. Buka tab Contoso – Microsoft Azure yang terbuka di browser Anda. Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan pilih Azure Active Directory.  Anda harus masuk sebagai admin di portal Microsoft Azure. Jika tidak, masuk kembali.

1. Dari panel navigasi sebelah kiri, pilih **Users**.  Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari bagian atas halaman, pilih **+ Pengguna baru** lalu dari kotak dropdown, pilih **Buat pengguna baru**.

1. **Buat pengguna baru** harus sudah dipilih, jika tidak pilih opsi tersebut.

1. Isi bidang **Identity** sebagai berikut:

    1. Nama pengguna: **sara**.

    1. Nama bidang: **Sara Perez**.

    1. Nama depan: **Sara**.

    1. Nama belakang: **Perez**.

1. Isi bidang **Password** sebagai berikut:

    1. Pilih **Izinkan saya membuat kata sandi**.

    1. Kata sandi awal: **Naja8996**. Saat Sara masuk untuk pertama kalinya, dia akan diminta untuk mengubah kata sandinya.

1. Mengonfigurasi **Groups and roles**.

    1. Di samping Grup, pilih **0 groups selected**.  Hal ini menampilkan grup yang tersedia.  Perhatikan daftar grup yang tersedia.

    1. Pilih **Operations**, Anda mungkin perlu menggulir ke bawah, lalu tekan **Select**. Perhatikan bagaimana teks di sebelah grup telah diperbarui untuk menampilkan 1 grup yang telah dipilih.  

    1. Di samping Peran, pilih **User**. Daftar Peran direktori muncul.  Gulir ke bawah untuk melihat berbagai peran bawaan, untuk melihat berbagai peran, tetapi jangan ubah peran pengguna.  Tutup jendela ini dengan memilih **X** di sudut kanan atas halaman.

1. Konfigurasi **Settings**

    1. Blokir proses masuk:  **No** (gunakan pengaturan default).

    1. Lokasi penggunaan: pilih menu dropdown, lalu pilih **Amerika Serikat** (gulir ke bawah untuk menemukan opsi ini) atau negara tempat Anda berada.  Mengonfigurasi lokasi penggunaan diperlukan untuk menetapkan lisensi.

1. Dari bagian bawah halaman, pilih tombol **Create**.

1. Pastikan pengguna muncul di daftar pengguna (nama dicantumkan dalam urutan abjad), Anda mungkin perlu merefresh halaman browser.

1. Dari daftar pengguna, pilih pengguna yang Anda buat, **Sara Perez**.  Halaman profil terbuka.

1. Panel navigasi sebelah kiri menunjukkan berbagai opsi yang dapat dikonfigurasi untuk pengguna.  Pilih **Grup**.  Di sini Anda dapat melihat informasi tambahan tentang grup.  Pastikan grup Operasi tercantum (mungkin diperlukan beberapa menit agar tugas grup muncul).  Catatan: Anda juga akan melihat grup Contoso, meskipun kami hanya menetapkan satu grup saat membuat pengguna.  Hal ini adalah hasil dari kebijakan yang telah dikonfigurasi sebelumnya, terhadap penyewa, yang secara otomatis menetapkan pengguna baru pada grup Contoso.

1. Dari panel navigasi sebelah kiri, pilih **Licenses**.  Perhatikan bahwa tidak ada penetapan lisensi yang ditemukan untuk pengguna ini.  

1. Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.

1. Di bagian Pilih lisensi, pilih **Office 365 E3** dan **Windows 10/11 Enterprise E3** lalu pilih tombol **Simpan** di bagian bawah layar. Pemberitahuan di sudut kanan atas layar akan menunjukkan bahwa penetapan lisensi berhasil.

1. Pilih **X** di kanan atas layar untuk menutup jendela Penugasan lisensi.

1. Pilih **ikon Refresh** di bagian atas halaman untuk mengonfirmasi penetapan lisensi.

1. Kembali ke halaman direktori Azure Active Gambaran Umum Contoso, dengan memilih **Contoso** di kiri atas layar (bread-crumb), di atas bagian yang tertulis Sara Perez | Lisensi.

1. Anda telah berhasil membuat dan mengonfigurasi pengguna di Azure Active Directory.

1. Keluar dari semua tab browser yang terbuka.  Di portal Microsoft Azure, keluar dengan memilih ikon pengguna di samping alamat email di pojok kanan atas layar, lalu pilih **Keluar**. Di Microsoft 365, keluar dengan memilih ikon di sudut kanan atas jendela Microsoft 365 yang ditampilkan sebagai lingkaran dengan huruf SP (di sebelah ikon tanda tanya), lalu pilih **Keluar**. Tutup semua jendela browser.

### <a name="task-3"></a>Tugas 3

Dalam tugas ini, Anda akan masuk sebagai Sara Perez, untuk pertama kalinya.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **login.microsoft.com**.

3. Masuk sebagai **sara@WWLxZZZZZ.onmicrosoft.com** , (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda).

4. Masukkan kata sandi sementara **Naja8996**.

5. Sekarang Anda diminta untuk Memperbarui kata sandi Anda. Di bidang Kata sandi saat ini, masukkan **Naja8996**.

6. Di bidang Kata sandi baru, masukkan  **SC900-Lab**.  Pada bidang Konfirmasi kata sandi Anda masukkan SC900-Lab, lalu pilih Masuk.  Catatan: Untuk praktik terbaiknya, gunakanlah kata sandi yang lebih aman. Kata sandi ini dipilih untuk kelayakan dan hanya untuk tujuan lab ini.

7. Anda telah berhasil masuk ke Microsoft 365.

8. Keluar dengan memilih ikon di sudut kanan atas jendela Microsoft 365 yang ditampilkan sebagai lingkaran dengan huruf SP (di sebelah ikon tanda tanya), lalu pilih **Keluar**, lalu tutup browser.

### <a name="review"></a>Tinjau

Dalam lab ini, Anda telah memulai penjelajahan awal Microsoft Azure AD. Karena pelanggan Microsoft 365 secara otomatis menggunakan Microsoft Azure AD, maka Anda mengakses fitur dan layanan Microsoft Azure AD melalui portal admin Microsoft 365 atau melalui portal Microsoft Azure.  Anda dapat menggunakan pendekatan apa pun untuk mengerjakan suatu proses.  Anda juga menjalani proses pembuatan pengguna baru dan berbagai pengaturan yang dapat dikonfigurasi, termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
