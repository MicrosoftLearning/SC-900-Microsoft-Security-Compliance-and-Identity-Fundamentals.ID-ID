---
lab:
  title: Penyiapan lab
  module: Setup your Microsoft 365 lab tenant (not associated with a Learn module)
---

# Lab: Penyiapan

## Penyewa WWL - Ketentuan penggunaan
Jika Anda diberikan penyewa sebagai bagian dari penyajian pelatihan yang dipimpin instruktur, harap diperhatikan bahwa penyewa tersedia untuk mendukung lab praktik dalam pelatihan yang dipimpin instruktur.

Penyewa tidak boleh dibagikan atau digunakan untuk tujuan di luar lab praktik. Penyewa yang digunakan dalam kursus ini adalah penyewa uji coba dan tidak dapat digunakan atau diakses setelah kelas berakhir dan tidak memenuhi syarat perpanjangan.

Penyewa tidak boleh dikonversi ke langganan berbayar. Penyewa yang diperoleh sebagai bagian dari kursus ini tetap menjadi milik Microsoft Corporation dan kami berhak mendapatkan akses dan repositorinya kapan saja.

## Skenario lab

Lab penyiapan ini terdiri dari mengaktifkan Log Audit Microsoft.

**Perkiraan Waktu:**: 5-10 menit

### Penyiapan - Mengaktifkan log audit Microsoft 365

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan log Audit di Microsoft 365.  Meskipun dokumentasi menunjukkan bahwa log audit diaktifkan secara default, sebagian besar penyewa lab tidak mengaktifkan fitur ini, dan perlu waktu beberapa jam untuk menerapkannya.  Mengaktifkan fitur ini bermanfaat, karena Microsoft 365 menggunakan log audit untuk wawasan pengguna dan aktivitas yang diidentifikasi dalam kebijakan dan wawasan analitik.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk menggunakan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**. Ini akan membawa Anda ke laman pusat admin Microsoft 365.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Kepatuhan**.  Laman browser baru membuka laman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi kiri, di bagian solusi, pilih **Audit**.  Catatan: fungsionalitas audit juga dapat diakses melalui beranda Microsoft 365 Defender (sebelumnya disebut sebagai pusat keamanan Microsoft 365).

1. Pastikan tab **Pencarian Baru** dipilih (digarisbawahi).

1. Setelah Anda masuk ke laman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas laman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Mulai merekam aktivitas pengguna dan admin**.  Jika diminta untuk mengonfirmasi bahwa pengaturan organisasi perlu diperbarui, pilih **Ya**. Setelah audit diaktifkan, bilah biru menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.  Cara lain untuk memeriksa apakah audit diaktifkan adalah melalui PowerShell, tetapi itu berada di luar cakupan kursus ini.

1. Kembali ke laman beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi kiri untuk keluar dari Microsoft 365. Keluar dengan memilih ikon di sudut kanan atas jendela Microsoft 365 yang ditampilkan sebagai lingkaran dengan huruf MA (di sebelah ikon tanda tanya), lalu pilih **Keluar**. Tutup browser.

### Tinjauan

Dalam penyiapan ini, Anda telah mengaktifkan kemampuan log audit di Microsoft 365.
