<!---
---
Lab: Judul: 'Jelajahi Microsoft Entra ID Pengaturan Pengguna' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 1: Menjelaskan jenis fungsi dan identitas ID Microsoft Entra; Unit 3: Menjelaskan jenis identitas Microsoft Entra'
---
--->

# Lab: Jelajahi ID Microsoft Entra

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan jenis fungsi dan identitas ID Microsoft Entra.
- Unit: Menjelaskan jenis identitas.

## Skenario lab

Di lab ini, Anda akan mengakses ID Microsoft Entra (sebelumnya disebut sebagai Azure Active Directory).  Selain itu, Anda akan membuat pengguna dan mengonfigurasi pengaturan yang berbeda, termasuk menambahkan lisensi.  

**Perkiraan Waktu**: 10-15 menit

### Tugas 1

Sebagai pelanggan Microsoft 365, Anda sudah menggunakan ID Microsoft Entra (sebelumnya disebut sebagai Azure AD).  Dalam tugas ini, Anda akan mempelajari cara membuat pengguna baru di ID Microsoft Entra dan menjelajahi beberapa layanan yang dapat dikelola di tingkat pengguna.

1. Buka browser Microsoft Edge. Di bilah alamat, masukkan **[admin.microsoft.com](https://admin.microsoft.com)** dan masuk dengan kredensial Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh ALH Anda) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Di bawah pusat Admin, pilih **Identitas** (Anda mungkin perlu memilih **Tampilkan semua** dan gulir ke bawah).  Halaman browser baru terbuka ke halaman gambaran umum pusat admin Microsoft Entra. Di sini Anda akan melihat informasi dasar tentang penyewa Contoso Anda. Jika Anda menggulir ke bawah jendela utama, Anda juga akan melihat informasi tentang pemberitahuan, umpan saya, sorotan fitur, dan banyak lagi.

1. Dari panel navigasi kiri, perluas **Pengguna** lalu pilih **Semua pengguna**. Perhatikan bahwa penyewa Anda sudah dikonfigurasi dengan pengguna.

1. Dari bagian atas halaman, pilih **+ Pengguna baru** lalu dari kotak dropdown, pilih **Buat pengguna baru**.

1. Anda sekarang berada di tab **dasar-dasar** halaman buat pengguna baru. Isi bidang sebagai berikut:
    1. Nama utama pengguna: **sara**.

    1. Nama panggilan email: biarkan default, yang diatur untuk berasal dari nama utama pengguna.

    1. Nama tampilan: **Sara Perez**.

    1. Kata sandi: hapus centang pada kotak yang bertuliskan buat kata sandi secara otomatis dan masukkan kata sandi sementara yang mematuhi persyaratan kata sandi dan catat, karena Anda akan membutuhkannya untuk menyelesaikan tugas berikutnya.

    1. Akun diaktifkan: Biarkan tanda centang untuk memastikan akun diaktifkan.

    1. Di bagian bawah halaman, pilih **Berikutnya: Properti**.

1. Di sini Anda akan mengonfigurasi beberapa bidang di tab **Properti** .

    1. Nama depan: Sara

    1. Nama belakang: Perez

    1. Jenis pengguna: Biarkan default ke **Anggota**, tetapi perhatikan bahwa dari menu drop-down Anda memiliki opsi untuk memilih tamu.

    1. Lokasi penggunaan: Pilih negara/wilayah tempat Anda berada.  Perhatikan bahwa untuk masuk ke bidang lokasi penggunaan, Anda harus menggulir ke bawah pada halaman karena ini adalah bidang terakhir di halaman.  **CATATAN**: jika Anda tidak melakukan ini, Anda tidak akan dapat menetapkan lisensi di langkah berikutnya.

    1. Pilih **Berikutnya: Penugasan**.

1. Anda sekarang berada di tab **Penugasan** tempat Anda menambahkan penetapan grup dan melihat opsi yang tersedia untuk menambahkan peran.

    1. Pilih **Tambahkan grup**.

    1. Jendela yang terbuka menampilkan semua grup yang tersedia.  

    1. Perhatikan daftar grup yang tersedia.  Dari daftar, pilih **Operasi**.  Dari bagian bawah halaman, pilih tombol **Pilih** .  Mungkin perlu beberapa detik tetapi Anda akan melihat grup operasi muncul di halaman penugasan.

    1. Dari bagian atas halaman, pilih **Tambahkan peran**.  Jendela terbuka yang menampilkan semua peran direktori yang tersedia.  Lihat opsi yang tersedia, tetapi jangan tambahkan peran baru apa pun.  Tutup halaman ini dengan memilih **X** di sudut kanan atas halaman peran direktori.
    1. Di bagian bawah panel, pilih **Tinjau + buat**. Ringkasan pengaturan akan ditampilkan.  Di bagian bawah halaman, pilih **Buat**.

1. Anda dikembalikan ke halaman pengguna.  Setelah beberapa detik, Sara Perez akan terdaftar.  Anda mungkin perlu memilih ikon **refresh** di bagian atas halaman.

1. Dari daftar pengguna, pilih pengguna yang Anda buat, **Sara Perez**.  Halaman **Gambaran Umum** terbuka.

1. Panel navigasi sebelah kiri menunjukkan berbagai opsi yang dapat dikonfigurasi untuk pengguna. Lihat opsi yang tersedia.

1. Dari panel navigasi sebelah kiri, pilih **Licenses**.  Perhatikan bahwa tidak ada penetapan lisensi yang ditemukan untuk pengguna ini.  CATATAN: Lisensi hanya dapat ditetapkan jika lokasi penggunaan dikonfigurasi. Jika Anda tidak mengatur lokasi penggunaan, kembali ke langkah tersebut di tugas sebelumnya.

    1. Untuk menambah lisensi, pilih **+ Assignments** dari bagian atas jendela utama.

    1. Di bagian Pilih lisensi, pilih **Office 365 E3** dan **Windows 10/11 Enterprise E3** lalu pilih tombol **Simpan** di bagian bawah layar. Pemberitahuan di sudut kanan atas layar akan menunjukkan bahwa penetapan lisensi berhasil.

    1. Pilih **X** di kanan atas layar untuk menutup jendela Penugasan lisensi.

    1. Pilih **ikon Refresh** di bagian atas halaman untuk mengonfirmasi penetapan lisensi.

1. Kembali ke pusat admin Microsoft Entra dengan memilih **Beranda** dari panel navigasi kiri atau dari kiri atas layar (remah roti), di atas yang bertuliskan Sara Perez | Lisensi.

1. Anda telah berhasil membuat dan mengonfigurasi pengguna dalam ID Microsoft Entra.

1. Keluar dari semua tab browser yang terbuka. Keluar dengan memilih ikon pengguna di samping alamat email di sudut kanan atas layar lalu pilih **Keluar**. Tutup semua jendela browser.

### Tugas 2

Dalam tugas ini, Anda akan masuk sebagai Sara Perez, untuk pertama kalinya.

1. Buka Microsoft Edge.

2. Di bilah alamat, masukkan **https://login.microsoft.com**.

3. Masuk sebagai **sara@WWLxZZZZZ.onmicrosoft.com**, (di mana ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh ALH Anda)
4. Masukkan kata sandi sementara yang Anda tetapkan di tugas sebelumnya.

5. Sekarang Anda diminta untuk Memperbarui kata sandi Anda. Di bidang Kata sandi saat ini, masukkan kata sandi sementara dari tugas sebelumnya.

6. Di bidang Kata sandi baru, masukkan kata sandi baru, konfirmasi kata sandi, lalu pilih **Masuk**.  Catat kata sandi baru Anda karena Anda akan membutuhkannya untuk latihan lab berikutnya pada SSPR.

7. Anda telah berhasil masuk ke Microsoft 365.

8. Keluar dengan memilih ikon di sudut kanan atas jendela Microsoft 365 yang ditampilkan sebagai lingkaran dengan huruf SP (di sebelah ikon tanda tanya), lalu pilih **Keluar**, lalu tutup browser.

### Tinjau

Dalam lab ini, Anda telah memulai penjelajahan awal Microsoft Azure AD. Karena pelanggan Microsoft 365 secara otomatis menggunakan Microsoft Azure AD, maka Anda mengakses fitur dan layanan Microsoft Azure AD melalui portal admin Microsoft 365 atau melalui portal Microsoft Azure.  Anda dapat menggunakan pendekatan apa pun untuk mengerjakan suatu proses.  Anda juga menjalani proses pembuatan pengguna baru dan berbagai pengaturan yang dapat dikonfigurasi, termasuk grup tempat pengguna dapat ditetapkan, ketersediaan peran, dan penetapan lisensi pengguna.
