---
lab:
  title: Menjelajahi Pengaturan Pengguna ID Microsoft Entra
  module: Describe the function and identity types of Microsoft Entra ID
---

# Lab: Menjelajahi Pengaturan Pengguna ID Microsoft Entra

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan fungsi dan jenis identitas Microsoft Entra ID.
- Unit: Menjelaskan jenis identitas.

## Skenario lab

Di lab ini, Anda akan mengakses Microsoft Entra ID (sebelumnya disebut sebagai Azure Active Directory).  Selain itu, Anda akan membuat pengguna dan mengonfigurasi pengaturan yang berbeda, termasuk menambahkan lisensi.  

**Perkiraan Waktu**: 10-15 menit

### Tugas 1

Sebagai pelanggan Microsoft 365, Anda sudah menggunakan Microsoft Entra ID (sebelumnya disebut sebagai Microsoft Azure AD).  Dalam tugas ini, Anda akan mempelajari cara membuat pengguna baru di Microsoft Entra ID dan menjelajahi beberapa layanan yang dapat dikelola di tingkat pengguna.

1. Buka browser Microsoft Edge. Di bilah alamat, masukkan **[admin.microsoft.com](https://admin.microsoft.com)** dan masuk dengan kredensial Microsoft 365 yang disediakan oleh host lab resmi (ALH).
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Di Pusat admin, pilih **Identitas** (Anda mungkin perlu memilih **Tampilkan semua** dan menggulir ke bawah).  Laman browser baru membuka laman ikhtisar di pusat admin Microsoft Entra. Di sini, Anda akan melihat informasi dasar tentang penyewa Contoso Anda. Jika Anda menggulir ke bawah jendela utama, Anda juga akan melihat informasi tentang pemberitahuan, umpan saya, sorotan fitur, dan banyak lagi.

1. Dari panel navigasi kiri, bentangkan **Pengguna**, lalu pilih **Semua pengguna**. Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan beberapa pengguna.

1. Dari bagian atas laman, pilih **+ Pengguna baru**, lalu dari kotak menurun, pilih **Buat pengguna baru**.

1. Sekarang, Anda berada di tab **dasar-dasar** dari laman buat pengguna baru. Isi bidang-bidang sebagai berikut:
    1. Nama prinsipal pengguna: **sara**.

    1. Nama panggilan email: biarkan default, yang diatur ke berasal dari nama utama pengguna.

    1. Nama tampilan: **Sara Perez**.

    1. Kata sandi: hapus centang pada kotak yang mengatakan buat kata sandi secara otomatis dan masukkan kata sandi sementara yang mematuhi persyaratan kata sandi dan catatlah, karena Anda akan membutuhkannya untuk menyelesaikan tugas berikutnya.

    1. Akun diaktifkan: Biarkan tanda centang untuk memastikan akun diaktifkan.

    1. Di bagian bawah laman, pilih **Properti Berikutnya**.

1. Di sini, Anda akan mengonfigurasi beberapa bidang di tab **Properti** .

    1. Nama depan: Sara

    1. Nama belakang: Perez

    1. Jenis pengguna: Biarkan default ke **Anggota**, tetapi perhatikan bahwa dari menu menurun, Anda memiliki opsi untuk memilih tamu.

    1. Lokasi penggunaan: Pilih negara/wilayah tempat Anda berada.  Perhatikan bahwa untuk masuk ke bidang lokasi penggunaan, Anda harus menggulir ke bawah pada laman tersebut karena ini adalah bidang terakhir di laman.  **CATATAN**: jika Anda tidak melakukan ini, Anda tidak akan dapat menetapkan lisensi di langkah berikutnya.

    1. Pilih **Berikutnya: Penugasan**.

1. Sekarang, Anda berada di tab **Penugasan** tempat Anda menambahkan penetapan grup dan melihat opsi yang tersedia untuk menambahkan peran.

    1. Pilih **Tambahkan grup**.

    1. Jendela yang terbuka menampilkan semua grup yang tersedia.  

    1. Perhatikan daftar grup yang tersedia.  Dari daftar, pilih **Operaso**.  Di bagian bawah laman, pilih tombol **Pilih**.  Mungkin perlu beberapa detik, tetapi Anda akan melihat grup operasi muncul di laman penugasan.

    1. Dari bagian atas laman, pilih **Tambahkan peran**.  Jendela yang terbuka menampilkan semua peran direktori yang tersedia.  Lihat opsi yang tersedia, tetapi jangan tambahkan peran baru apa pun.  Tutup laman ini dengan memilih **X** di pojok kanan atas laman peran direktori.
    1. Di bagian bawah panel, pilih **Tinjau + buat**. Ringkasan pengaturan akan ditampilkan.  Di bagian bawah laman, pilih **Buat**.

1. Anda akan dikembalikan ke laman pengguna.  Setelah beberapa detik, Sara Perez akan terdaftar.  Anda mungkin perlu memilih ikon **refresh** di bagian atas laman.

1. Dari daftar pengguna, pilih pengguna yang Anda buat, **Sara Perez**.  Laman **Ikhtisar** akan terbuka.

1. Panel navigasi kiri memperlihatkan berbagai opsi yang dapat dikonfigurasi untuk pengguna. Lihat opsi yang tersedia.

1. Dari panel navigasi kiri, pilih **Lisensi**.  Perhatikan bahwa tidak ada penetapan lisensi yang ditemukan untuk pengguna ini.  CATATAN: Lisensi hanya dapat ditetapkan jika lokasi penggunaan dikonfigurasi. Jika Anda tidak mengatur lokasi penggunaan, kembali ke langkah tersebut di tugas sebelumnya.

    1. Untuk menambahkan lisensi pilih **+ Penugasan** dari bagian atas jendela utama.

    1. Di bagian Pilih lisensi, pilih **Office 365 E3** dan **Windows 10/11 Enterprise E3**, lalu pilih tombol **Simpan** di bagian bawah layar. Pemberitahuan di sudut kanan atas layar akan menunjukkan bahwa penetapan lisensi berhasil.

    1. Pilih **X** di kanan atas layar untuk menutup laman Penugasan lisensi.

    1. Pilih **ikon Refresh** di bagian atas laman untuk mengonfirmasi penetapan lisensi.

1. Kembali ke pusat admin Microsoft Entra dengan memilih **Beranda** dari panel navigasi kiri atau dari kiri atas layar (bilah), di atas tulisan Sara Perez | Lisensi.

1. Anda telah berhasil membuat dan mengonfigurasi pengguna di Microsoft Entra ID.

1. Keluar dari semua tab browser yang terbuka. Keluar dengan memilih ikon pengguna di sebelah alamat email di sudut kanan atas layar dan memilih **keluar.**. Kemudian tutup semua jendela browser.

### Tugas 2

Dalam tugas ini, Anda akan masuk sebagai Sara Perez, untuk pertama kalinya.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **https://login.microsoft.com**.

3. Masuk sebagai **sara@WWLxZZZZZ.onmicrosoft.com**, (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda).
4. Masukkan kata sandi sementara yang Anda catat dari tugas sebelumnya.

5. Sekarang Anda diminta Memperbarui kata sandi. Di bidang Kata sandi saat ini, masukkan kata sandi sementara dari tugas sebelumnya.

6. Di bidang Kata sandi baru, masukkan kata sandi baru, konfirmasi kata sandi, lalu pilih **Masuk**.  Catat kata sandi baru karena Anda akan membutuhkannya untuk latihan lab berikutnya di SSPR.

7. Sekarang, Anda berhasil masuk ke Microsoft 365.

8. Keluar dengan memilih ikon di sudut kanan atas jendela Microsoft 365 yang ditampilkan sebagai lingkaran dengan huruf SP (di sebelah ikon tanda tanya), lalu pilih **Keluar**, lalu tutup browser.

### Tinjauan

Di lab ini, Anda telah memulai eksplorasi awal Azure AD. Karena pelanggan Microsoft 365 secara otomatis menggunakan Azure AD, Anda menemukan bahwa Anda mengakses fitur dan layanan Azure AD melalui portal admin Microsoft 365 atau melalui portal Azure.  Silakan gunakan cara apa pun Anda sukai untuk sampai ke tempat yang sama.  Anda juga telah mempelajari proses pembuatan pengguna baru dan berbagai pengaturan yang dapat dikonfigurasi, termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
