---
Demo:
    title: 'Pengaturan pengguna Azure Active Directory'
    module: 'Modul 2 Pelajaran 1: Menjelaskan kemampuan Microsoft Identity dan solusi manajemen akses: Menjelajahi jenis layanan dan identitas Microsoft Azure AD'
---

# Demo: Pengaturan pengguna Azure Active Directory

### Skenario demo

Dalam demo ini, Anda akan mengakses Azure Active Directory dan mempelajari berbagai pengaturan bagi pengguna yang ada.

1. Buka tab **Home – Microsoft Azure** yang terbuka di browser Anda.  Jika sebelumnya Anda menutup tab, buka Microsoft Edge dan di bilah alamat masukkan portal.azure.com, lalu masuk dengan kredensial admin yang sama dengan penyewa Microsoft 365 Anda.

1. Halaman arahan portal Azure menunjukkan layanan Azure, pilih **Azure Active Directory**. Jika tidak segera terlihat, dari kotak pencarian di sebelah tulisan Microsoft Azure, masukkan Azure Active Directory.  Anda mungkin juga ingin menunjukkan cara mengakses melalui ikon menu portal yang muncul (tiga garis horizontal juga disebut sebagai ikon hamburger, di bilah biru di bagian atas halaman) di sebelah kiri tulisan Microsoft Azure.

1. Dari panel navigasi sebelah kiri, pilih **Users**. Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari daftar pengguna, pilih **Adele Vance**.

1. Perhatikan bahwa di panel navigasi kiri, **Profile** dipilih.  Tunjukkan/sebutkan informasi yang ditampilkan di halaman profil.

1. Dari panel navigasi kiri, pilih **Assigned roles**.  Pengguna ini tidak memiliki peran administratif yang ditetapkan.  Dari bagian atas halaman, pilih **+ Add assignments**, untuk menunjukkan jenis peran administratif yang tersedia.  Jangan menambahkan apa pun, tutuplah halaman dengan memilih **X** di kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih  **Groups**.  Katakan bahwa pengguna ini adalah anggota dari beberapa grup.  Di sini, Anda dapat berbicara dengan jenis grup.  Untuk menambahkan pengguna ini ke grup lain, Anda cukup memilih **+ Add memberships**.  Jangan menambahkan grup baru, katakan saja betapa mudahnya menambahkan pengguna ke grup yang ada. Tutup jendela grup dengan memilih **X** di pojok kanan atas halaman.

1. Dari panel navigasi sebelah kiri, pilih **Licenses**. Perhatikan bahwa pengguna ini diberi lisensi Microsoft 365 E5 dan lisensi EMS.  Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.  Tampilkan lisensi untuk pengguna ini. JANGAN mengubah apa pun.  Tutup jendela ini dengan memilih **X** di sudut kanan atas halaman.

1. Dari panel navigasi kiri pilih **Devices**.  Tidak ada yang muncul, tetapi Anda dapat mengatakan bahwa jika pengguna ini memiliki perangkat yang ditetapkan, ia akan muncul di sini.

1. Dari panel navigasi kiri, pilih **Azure role assignments**.  Katakan:
    1. Ini berbeda dari tab peran yang ditetapkan yang diperlihatkan sebelumnya di sana bahwa tab sebelumnya adalah untuk kontrol akses berbasis peran di Azure Active Directory (menekankan Active Directory).
    1. Di tab ini, Anda dapat melihat penetapan peran, yang ditetapkan ke pengguna, untuk sumber daya Azure. Misalnya, jika Anda membuat Grup Sumber Daya Azure, dan Anda menetapkan Adele dengan peran tertentu, seperti pemilik atau kontributor untuk grup sumber daya, Anda akan melihat peran tersebut tercantum di sini. Ini adalah bagian dari Kontrol Akses Berbasis Peran Azure (Azure RBAC). Penetapan peran tersebut dikelola sebagai bagian dari sumber daya tertentu.

1. Dari panel navigasi kiri, pilih **Authentication methods**.  Sebutkan deskripsi yang tertulis, “Di sini, Anda dapat mengatur nomor telepon dan alamat email yang digunakan pengguna untuk melakukan autentikasi multifaktor serta mengatur ulang sandi layanan mandiri dan sandi pengguna.” Jika pengguna dikonfigurasi untuk SSPR atau diharuskan menggunakan MFA, dan Anda sebagai admin, mengisi ini, mereka sudah terdaftar dan tidak perlu melalui langkah-langkah pendaftaran untuk SSPR atau MFA.  Umumnya, pengguna akan mendaftar sendiri alih-alih admin yang melakukan hal ini.

1. Dari panel navigasi kiri, pilih **Sign-ins**.  Di sini, Anda dapat melihat aktivitas masuk pengguna ini.  Anda mungkin tidak melihat apa pun untuk pengguna ini, karena dia belum masuk.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke daftar pengguna.  Sebelum menutup daftar pengguna, Anda dapat menyoroti bahwa MFA ditampilkan di bagian atas halaman.  Pilih **Multi-Factor Authentication**.  Ini membuka jendela browser baru.  Di sini, Anda dapat memilih MFA secara massal untuk pengguna.  Ini adalah salah satu cara agar Anda dapat mengaktifkan MFA untuk pengguna.  Sebenarnya, kami akan menunjukkan lebih banyak tentang MFA dalam konteks Akses bersyarat yang menyediakan kontrol MFA yang lebih terperinci.  Tutup tab browser untuk Autentikasi multifaktor.

1. Pilih **X** di pojok kanan atas halaman. Ini mengembalikan Anda ke halaman utama untuk penyewa Contoso.

### Tinjauan

Dalam demo ini, Anda telah menelusuri panduan pengaturan pengguna yang ada termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
