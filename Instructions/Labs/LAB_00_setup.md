---
lab:
  title: Penyiapan lab
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# Lab: Penyiapan penyewa Microsoft 365

## Penyewa WWL - Ketentuan penggunaan
Jika Anda diberikan penyewa sebagai bagian dari penyajian pelatihan yang dipimpin instruktur, harap diperhatikan bahwa penyewa tersedia untuk mendukung lab praktik dalam pelatihan yang dipimpin instruktur.

Penyewa tidak boleh dibagikan atau digunakan untuk tujuan di luar lab praktik. Penyewa yang digunakan dalam kursus ini adalah penyewa uji coba dan tidak dapat digunakan atau diakses setelah kelas berakhir dan tidak memenuhi syarat perpanjangan.

Penyewa tidak boleh dikonversi ke langganan berbayar. Penyewa yang diperoleh sebagai bagian dari kursus ini tetap menjadi milik Microsoft Corporation dan kami berhak mendapatkan akses dan repositorinya kapan saja.

## Skenario lab

Lab penyiapan ini terdiri dari mengaktifkan Log Audit Microsoft dan kemampuan pemantauan file di penyewa Microsoft 365.

**Perkiraan Waktu:**: 5-10 menit

### Penyiapan - Mengaktifkan log audit Microsoft 365 dan pemantauan file

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan Log audit dan pemantauan file di Microsoft 365.  

1. Buka Microsoft Edge. Di bilah alamat, masukkan **https://admin.microsoft.com**.

1. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Keamanan**.  Halaman browser baru terbuka ke halaman selamat datang Pertahanan Microsoft.  

1. Dari panel navigasi sebelah kiri portal kepatuhan Microsoft Purview, pilih **Tampilkan semua**.

1. Di panel navigasi kiri, gulir ke bawah dan perluas **Sistem**.  Dari daftar yang diperluas, pilih **Audit**.  Catatan: fungsionalitas audit juga dapat diakses melalui portal Microsoft Purview.

1. Setelah Anda masuk ke halaman Audit, tunggu 1-2 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas laman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Mulai merekam aktivitas pengguna dan admin**.  Setelah audit diaktifkan, bilah biru menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.

1. Dari panel navigasi kiri, di bawah Sistem, pilih **Pengaturan**.

1. Dari halaman pengaturan, pilih **Aplikasi cloud**.   Gulir ke bawah, lalu di bawah Perlindungan Informasi pilih **File**.

1. Jika belum diaktifkan, pilih kotak di samping tempatnya berbunyi **Aktifkan pemantauan** file lalu pilih **Simpan**.  

1. Ini menyimpulkan penyiapan lab pada penyewa Microsoft 365.

### Tinjauan

Dalam penyiapan ini, Anda mengaktifkan kemampuan log audit dan pemantauan file di Microsoft 365.
