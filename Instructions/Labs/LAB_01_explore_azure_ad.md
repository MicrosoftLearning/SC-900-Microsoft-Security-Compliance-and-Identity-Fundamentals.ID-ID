---
lab:
  title: Mempelajari Azure Active Directory
  module: 'Module 2 Lesson 1: Describe the capabilities of Microsoft Identity and access management solutions: Explore the services and identity types of Azure AD'
ms.openlocfilehash: 075b7123b5d7e17b7e30dfcacf9f90ef97a67f83
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894020"
---
# <a name="lab-explore-azure-active-directory"></a>Lab: Mempelajari Azure Active Directory

## <a name="lab-scenario"></a>Skenario lab

Pada lab ini, Anda akan mengakses Azure Active Directory.  Selain itu, Anda akan membuat pengguna dan mengonfigurasi pengaturan yang berbeda, termasuk menambahkan lisensi.  



**Perkiraan Waktu**: 10-15 menit

#### <a name="task-1--as-a-subscriber-to-microsoft-365-you-are-already-using-azure-ad--in-this-task-you-will-walk-through-accessing-azure-ad-through-the-microsoft-365-admin-portal-and-through-the-azure-portal"></a>Tugas 1:  Sebagai pelanggan Microsoft 365, Anda sudah menggunakan Microsoft Azure AD.  Dalam tugas ini Anda akan mempelajari cara mengakses Microsoft Azure AD melalui portal Admin Microsoft 365 dan melalui portal Microsoft Azure.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **admin.microsoft.com** untuk mengakses pusat admin Microsoft 365.

3. Masuk dengan kredensial admin Anda. 
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

4. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

5. Di bagian Pusat admin, pilih **Azure Active Directory** (Anda mungkin perlu menggulir ke bawah).  Halaman browser baru membuka halaman Dasbor Saya di pusat admin Azure Active Directory. Dari jendela utama dasbor, Anda akan melihat beberapa ubin, termasuk ubin Identitas Organisasi (Contoso, penyewa dan edisi Microsoft Azure AD), ubin untuk pengguna dan grup, serta banyak lagi.

6. Dari panel navigasi sebelah kiri, di bagian favorit, pilih **Azure Active Directory**.  Di jendela utama, Anda akan melihat panel navigasi lain yang mencantumkan semua layanan yang tersedia di Microsoft Azure AD. Di sebelah kanan, Anda akan melihat informasi tentang penyewa Contoso dan tautan ke jenis identitas yang dapat Anda buat dan layanan unggulan.  

7. Sekarang buka jendela browser baru dan di bilah alamat, masukkan **portal.azure.com**.  Karena Anda sudah masuk sebagai admin@WWLxZZZZZZ.onmicrosoft.com dan awalnya menggunakan kredensial yang sama untuk menukarkan Azure pass, Anda harus masuk sebagai administrator saat mengakses portal Microsoft Azure.  Anda dapat memverifikasi hal ini dengan memeriksa email di sudut kanan atas halaman dan mengarahkan mouse ke atas ikon pengguna.

8. Halaman arahan portal Microsoft Azure menampilkan layanan Azure, termasuk Azure Active Directory, Komputer Virtual, akun penyimpanan, database, dan banyak lagi.  Pilih **Azure Active Directory**.  

9. Sekarang Anda melihat Azure Active Directory untuk penyewa Microsoft 365 Contoso.    Pendekatan apa pun yang Anda gunakan untuk mengakses layanan Azure Active Directory (portal admin Microsoft 365 atau portal Microsoft Azure) akan berakhir di tempat yang sama – Contoso Azure Active Directory tempat Anda dapat mengelola semua layanan Microsoft Azure AD.

10. Biarkan halaman browser ini terbuka untuk tugas berikutnya.


#### <a name="task-2--in-this-task-youll-learn-how-to-create-a-new-user-in-azure-active-directory-and-explore-some-of-services-that-can-be-managed-at-the-user-level"></a>Tugas 2:  Dalam tugas ini, Anda akan mempelajari cara membuat pengguna baru di Azure Active Directory dan menjelajahi beberapa layanan yang dapat dikelola di tingkat pengguna.

1. Buka tab Contoso – Microsoft Azure yang terbuka di browser Anda. Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan pilih Azure Active Directory.  Anda harus masuk sebagai admin di portal Microsoft Azure. Jika tidak, masuk kembali.

2. Dari panel navigasi sebelah kiri, pilih **Users**.  Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan pengguna.

3. Dari bagian atas halaman, pilih **+ New user**.

4. **Create User** semestinya sudah dipilih. Jika belum, pilihlah opsi itu.

5. Isi bidang **Identity** sebagai berikut:

    1. Nama pengguna: **sara**.

    2. Nama bidang: **Sara Perez**.

    3. Nama depan: **Sara**.

    4. Nama belakang: **Perez**.

6. Isi bidang **Password** sebagai berikut:

    1. Pilih **Izinkan saya membuat kata sandi**.

    1. Kata sandi awal: **Naja8996**. Ketika Sara masuk untuk pertama kalinya, dia akan diminta untuk mengubah kata sandinya.

7. Mengonfigurasi **Groups and roles**.

    1. Di samping Grup, pilih **0 groups selected**.  Hal ini menampilkan grup yang tersedia.  Perhatikan daftar grup yang tersedia.

    2. Pilih **Operations**, Anda mungkin perlu menggulir ke bawah, lalu tekan **Select**. Perhatikan bagaimana teks di sebelah grup telah diperbarui untuk menampilkan 1 grup yang telah dipilih.  

    3. Di samping Peran, pilih **User**. Daftar Peran direktori muncul.  Gulir ke bawah untuk melihat berbagai peran bawaan, untuk melihat berbagai peran, tetapi jangan ubah peran pengguna.  Tutup jendela ini dengan memilih **X** di sudut kanan atas halaman.

8. Konfigurasi **Settings**

    1. Blokir proses masuk:  **No** (gunakan pengaturan default).

    1. Lokasi penggunaan: **United States** (pilih menu tarik-turun, lalu gulir ke bawah untuk menemukan opsi ini).  Mengonfigurasi lokasi penggunaan diperlukan untuk menetapkan lisensi.

9. Dari bagian bawah halaman, pilih tombol **Create**.

10. Pastikan pengguna muncul di daftar pengguna (nama tercantum dalam urutan abjad).

11. Dari daftar pengguna, pilih pengguna yang baru saja Anda buat, **Sara Perez**.  Halaman profil terbuka.

12. Panel navigasi sebelah kiri menunjukkan berbagai opsi yang dapat dikonfigurasi untuk pengguna.  Pilih **Grup**.  Di sini Anda dapat melihat informasi tambahan tentang grup.  Pastikan grup Operasi tercantum (mungkin diperlukan beberapa menit agar tugas grup muncul).  Catatan: Anda juga akan melihat grup Contoso, meskipun kita hanya menetapkan satu grup saat kita membuat pengguna.  Hal ini adalah hasil dari kebijakan yang telah dikonfigurasi sebelumnya, terhadap penyewa, yang secara otomatis menetapkan pengguna baru pada grup Contoso.

13. Dari panel navigasi sebelah kiri, pilih **Licenses**.  Perhatikan bahwa tidak ada penetapan lisensi yang ditemukan untuk pengguna ini.  

14. Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.

15. Di bagian Pilih lisensi, pilih **Office 365 E3** dan **Windows 10 Enterprise E3**, lalu pilih tombol **Save** di bagian bawah layar. Pemberitahuan di sudut kanan atas layar akan menunjukkan bahwa penetapan lisensi berhasil.

16. Pilih **X** di kanan atas layar untuk menutup jendela Penugasan lisensi.

17. Pilih **ikon Refresh** di bagian atas halaman untuk mengonfirmasi penetapan lisensi.

18. Kembali ke halaman direktori Azure Active Gambaran Umum Contoso, dengan memilih **Contoso** di kiri atas layar (bread-crumb), di atas bagian yang tertulis Sara Perez | Lisensi.

19. Anda telah berhasil membuat dan mengonfigurasi pengguna di Azure Active Directory.

20. Keluar dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.

#### <a name="task-3--in-this-task-you-will-sign-in-as-sara-perez-for-the-first-time"></a>Tugas 3:  Dalam tugas ini, Anda akan masuk sebagai Sara Perez, untuk pertama kalinya.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **login.microsoft.com**.

3. Masuk sebagai **sara@WWLxZZZZZ.onmicrosoft.com** , (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda).

4. Masukkan kata sandi sementara **Naja8996**.

5. Sekarang Anda diminta untuk Memperbarui kata sandi Anda. Di bidang Kata sandi saat ini, masukkan **Naja8996**.

6. Di bidang Kata sandi baru, masukkan  **SC900-Lab**.  Pada bidang Konfirmasi kata sandi Anda masukkan SC900-Lab, lalu pilih Masuk.  Catatan: Untuk praktik terbaiknya, gunakanlah kata sandi yang lebih aman. Kata sandi ini dipilih untuk kelayakan dan hanya untuk tujuan lab ini.

7. Anda telah berhasil masuk ke Microsoft 365.

8. **Sign out** dari semua tab browser dengan mengklik ikon pengguna di samping alamat email di sudut kanan atas layar. Kemudian tutup semua jendela browser.



#### <a name="review"></a>Tinjau
Dalam lab ini, Anda telah memulai penjelajahan awal Microsoft Azure AD. Karena pelanggan Microsoft 365 secara otomatis menggunakan Microsoft Azure AD, maka Anda mengakses fitur dan layanan Microsoft Azure AD melalui portal admin Microsoft 365 atau melalui portal Microsoft Azure.  Anda dapat menggunakan pendekatan apa pun untuk mengerjakan suatu proses.  Anda juga telah mempelajari cara membuat pengguna baru dan pengaturan lainnya yang dapat dikonfigurasi, termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.


