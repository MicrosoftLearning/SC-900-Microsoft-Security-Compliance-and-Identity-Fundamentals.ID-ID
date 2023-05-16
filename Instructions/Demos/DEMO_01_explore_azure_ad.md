---
demo:
  title: 'Jelajahi Azure AD Pengaturan Pengguna'
  module: 'Modul 1: Menjelaskan layanan dasar dan jenis identitas Azure AD'
---


# <a name="demo-azure-ad-user-settings"></a>Demo: Pengaturan pengguna Azure AD

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Azure Active Directory (Azure AD), bagian dari Microsoft Entra
- Modul: Menjelaskan layanan dasar dan jenis identitas Azure AD
- Pelajaran: Menjelaskan jenis identitas Azure AD

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan mengakses Azure Active Directory dan menelusuri berbagai pengaturan untuk pengguna yang sudah ada.  CATATAN untuk penyaji:  Demo ini mengakses Azure Active Directory melalui penyewa Microsoft 365. Opsi alternatif untuk menampilkan peserta didik adalah dengan mengakses Azure Active Directory melalui portal Microsoft Azure. Tujuan melalui portal Microsoft 365 adalah untuk menunjukkan bahwa Microsoft 365 menyertakan akses ke Azure Active Directory.

1. Buka Microsoft Edge.

1. Di bilah alamat, masukkan **admin.microsoft.com** untuk mengakses pusat admin Microsoft 365.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian Pusat admin, pilih **Azure Active Directory** (Anda mungkin perlu menggulir ke bawah).  Halaman browser baru membuka halaman Dasbor Saya di pusat admin Azure Active Directory. Dari jendela utama dasbor, Anda akan melihat beberapa petak peta, termasuk petak peta Identitas Organisasi (Contoso, penyewa, dan edisi Azure Active Directory), petak peta untuk pengguna dan grup, dan lainnya.

1. Dari panel navigasi sebelah kiri, pilih **Users**. Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari daftar pengguna, pilih **Adele Vance**.

1. Perhatikan bahwa di panel navigasi kiri, **Profile** dipilih.  Tunjukkan/sebutkan informasi yang ditampilkan di halaman profil.

1. Dari panel navigasi kiri, pilih **Assigned roles**.  Pengguna ini tidak memiliki peran administratif yang ditetapkan.  Dari bagian atas halaman, pilih **+ Add assignments**, untuk menunjukkan jenis peran administratif yang tersedia.  Jangan menambahkan apa pun, tutuplah halaman dengan memilih **X** di kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih  **Groups**.  Katakan bahwa pengguna ini adalah anggota dari beberapa grup.  Di sini, Anda dapat berbicara dengan jenis grup.  Untuk menambahkan pengguna ini ke grup lain, pilih **+ Tambahkan keanggotaan**.  Jangan menambahkan grup baru apa pun, katakan saja betapa mudahnya menambahkan pengguna ke grup yang sudah ada. Tutup jendela grup dengan memilih **X** di pojok kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih **Licenses**. Perhatikan bahwa pengguna ini diberi lisensi Microsoft 365 E5 dan lisensi EMS.  Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.  Tampilkan lisensi untuk pengguna ini. JANGAN mengubah apa pun.  Tutup jendela ini dengan memilih **X** di sudut kanan atas halaman.

1. Dari panel navigasi kiri, pilih **Perangkat**.  Tidak ada yang muncul, tetapi Anda dapat mengatakan bahwa jika pengguna ini memiliki perangkat yang ditetapkan, ia akan muncul di sini.

1. Dari panel navigasi kiri, pilih **Azure role assignments**.  Katakan:
    1. Ini berbeda dari tab peran yang ditetapkan yang diperlihatkan sebelumnya di sana bahwa tab sebelumnya adalah untuk kontrol akses berbasis peran di Azure Active Directory (menekankan Active Directory).
    1. Di tab ini, Anda dapat melihat penetapan peran, yang ditetapkan ke pengguna, untuk sumber daya Azure. Misalnya, jika Anda membuat Grup Sumber Daya Azure, dan Anda menetapkan Adele dengan peran tertentu, seperti pemilik atau kontributor untuk grup sumber daya, Anda akan melihat peran tersebut tercantum di sini. Ini adalah bagian dari Kontrol Akses Berbasis Peran Azure (Azure RBAC). Penetapan peran tersebut dikelola sebagai bagian dari sumber daya tertentu.

1. Dari panel navigasi kiri, pilih **Authentication methods**.  Sebutkan deskripsi yang tertulis, “Di sini, Anda dapat mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan autentikasi multifaktor serta mengatur ulang sandi layanan mandiri dan sandi pengguna.” Jika pengguna dikonfigurasi untuk SSPR atau diharuskan menggunakan MFA, dan Anda, sebagai admin, mengisi ini, maka pengguna sudah terdaftar dan tidak perlu melalui langkah-langkah pendaftaran untuk SSPR atau MFA.  Biasanya pengguna akan mendaftar sendiri vs admin yang harus melakukan ini.

1. Dari panel navigasi kiri, pilih **Sign-ins**.  Di sini, Anda dapat melihat aktivitas masuk pengguna ini.  Anda mungkin tidak melihat apa pun untuk pengguna ini, karena dia belum masuk.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke daftar pengguna.  Sebelum menutup daftar pengguna, Anda dapat menyoroti bahwa MFA ditampilkan di bagian atas halaman.  Pilih **autentikasi multifaktor**.  Ini akan membuka jendela browser baru.  Di sini, Anda dapat memilih MFA secara massal untuk pengguna.  Ini adalah salah satu cara agar Anda dapat mengaktifkan MFA untuk pengguna.  Kami akan menunjukkan lebih banyak tentang MFA dalam konteks Akses bersyarat dan bagaimana MFA menyediakan kontrol MFA yang lebih terperinci.  Tutup tab browser untuk Autentikasi multifaktor.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke halaman utama untuk penyewa Contoso.

### <a name="review"></a>Tinjau

Dalam demo ini, Anda menunjukkan pengaturan pengguna yang ada termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
