---
Demo:
    title: 'Pengaturan ulang kata sandi mandiri Azure Active Directory'
    module: 'Modul 2 Pelajaran 2: Menjelaskan kemampuan Microsoft Identity dan solusi manajemen akses: Menjelaskan metode autentikasi lain dari Microsoft Azure AD'
---

# Demo: Pengaturan ulang kata sandi mandiri Azure Active Directory (SSPR)

### Skenario demo

Dalam demo ini, Anda akan mempelajari berbagai pengaturan yang terkait dengan pengaktifan pengaturan ulang kata sandi mandiri.

1. Buka tab Contoso – Microsoft Azure yang terbuka di browser Anda. Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan pilih Azure Active Directory. Anda harus masuk sebagai admin di portal Microsoft Azure, jika tidak, masuk kembali.

1. Dari panel navigasi kiri, pilih Atur ulang kata sandi.

1. Tab properti disorot.  Di jendela Properti, perhatikan bahwa SSPR dapat diaktifkan ke Tidak ada, Pilih, atau Semua.
    1. Letakkan kursor Anda di atas ikon informasi di sebelah tulisan “Pengaturan ulang kata sandi mandiri diaktifkan," dan jelaskan bahwa Anda dapat memilih "Dipilih" untuk membatasi pengaturan ulang kata sandi ke sekelompok pengguna terbatas, daripada, memilih Tidak Ada atau semua.
    1. Letakkan kursor Anda di atas ikon informasi di sebelah tulisan "pilih grup" dan jelaskan bahwa ini adalah tempat Anda mengidentifikasi grup pengguna yang diizinkan untuk mengatur ulang kata sandi mereka.   Anda harus menyertakan pengguna dalam grup, Anda tidak dapat memilih pengguna satu per satu.  Selain itu, jika Anda mengubah grup, grup yang Anda pilih akan menggantikan grup yang sudah terdaftar.  Karena itu, sebaiknya Anda menambahkan pengguna ke grup SSPR.
    1. Perhatikan kotak informasi berwarna biru muda dan jelaskan kepada siswa - Setelan ini hanya berlaku untuk pengguna akhir di organisasi Anda. Admin selalu diaktifkan untuk mengatur ulang sandi secara mandiri dan diharuskan menggunakan dua metode autentikasi untuk mengatur ulang sandi mereka.

1. Dari panel navigasi kiri Atur ulang kata sandi, pilih Metode Autentikasi.
    1. Letakkan kursor Anda di atas ikon informasi di sebelah tulisan “Jumlah metode yang diperlukan untuk mengatur ulang”.  Jelaskan bahwa ini menetapkan jumlah metode identifikasi alternatif yang harus dimiliki pengguna dalam direktori ini untuk mengatur ulang kata sandi mereka.   Jangan mengubah pengaturan.
    1. Jelaskan “metode yang tersedia untuk pengguna” yang berbeda-beda, termasuk poin bahwa SSPR mendukung pertanyaan keamanan. Pilih Pertanyaan keamanan untuk menampilkan opsi penggunaan pertanyaan keamanan. Setelah Anda selesai menyampaikan tentang opsi, kembali dan pilih Pertanyaan keamanan, untuk menghapus tanda centang.

1. Dari panel navigasi kiri Atur ulang kata sandi, pilih Registrasi.
    1. Arahkan mouse ke ikon informasi di sebelahnya yang tertulis, “Wajibkan pengguna untuk mendaftar saat masuk”.   Jelaskan ini kepada pengguna.  
    1. Arahkan mouse ke ikon informasi di sebelah tulisan, “Jumlah hari sebelum pengguna diminta mengonfirmasi ulang informasi autentikasi”.   Jelaskan ini kepada pengguna.  

1. Dari panel navigasi kiri Atur ulang kata sandi, pilih Notifikasi.  Jelaskan dua pengaturan tersebut – arahkan mouse ke ikon informasi untuk melihat deskripsi.

1. Perhatikan bagaimana Panel navigasi atur ulang kata sandi juga menyertakan opsi untuk melihat log audit dan Penggunaan & wawasan.

1. Pilih X di sudut kanan atas halaman. Ini mengembalikan Anda ke halaman utama untuk penyewa Contoso.

1. Biarkan halaman browser ini terbuka untuk demo berikutnya.

#### Tinjauan

Dalam demo ini, Anda menunjukkan pengaturan yang terkait dengan pengaturan ulang kata sandi mandiri. 

