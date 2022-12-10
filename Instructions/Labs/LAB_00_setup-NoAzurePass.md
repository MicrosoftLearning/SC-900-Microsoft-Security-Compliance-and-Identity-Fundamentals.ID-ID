<a name="---"></a><!---
---
Lab: Judul: 'Penyiapan'
---
--->

# <a name="lab-setup"></a>Lab: Pengaturan

## <a name="lab-scenario"></a>Skenario lab

Lab penyiapan ini terdiri dari mengaktifkan Log Audit Microsoft.

**Perkiraan Waktu**: 5-10 menit

### <a name="setup---enable-microsoft-365-audit-log"></a>Penyiapan - Mengaktifkan log audit Microsoft 365

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan log Audit di Microsoft 365.  Meskipun dokumentasi menunjukkan bahwa log audit diaktifkan secara default, sebagian besar penyewa lab tidak mengaktifkan fitur ini dan mungkin perlu beberapa jam untuk menerapkannya.  Mengaktifkan fitur ini bermanfaat karena Microsoft 365 menggunakan log audit untuk wawasan pengguna dan aktivitas yang diidentifikasi dalam kebijakan dan wawasan analitik.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.  Catatan: fungsi audit juga dapat diakses melalui halaman beranda Pertahanan Microsoft 365 (sebelumnya disebut sebagai pusat keamanan Microsoft 365).

1. Pastikan bahwa tab **Search** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah berwarna biru di bagian atas halaman yang mengatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Jika diminta untuk mengonfirmasi bahwa pengaturan organisasi perlu diperbarui, pilih **Ya**. Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak ada tindakan lebih lanjut yang diperlukan.  Cara lain untuk memeriksa apakah audit diaktifkan adalah melalui PowerShell, tetapi itu di luar cakupan kursus ini.

1. Kembali ke halaman beranda pusat kepatuhan Microsoft 365 dengan memilih **Home** dari panel navigasi sebelah kiri.

### <a name="review"></a>Tinjau

Dalam penyiapan ini, Anda telah mengaktifkan kemampuan log audit di Microsoft 365.
