<!---
---
Demo: Judul: 'Jelajahi Microsoft Entra ID Pengaturan Pengguna' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 2: Menjelaskan kemampuan autentikasi ID Microsoft Entra; Unit 3: Menjelaskan metode autentikasi dan Unit 4: Menjelaskan autentikasi multifaktor'
---
--->

# Demo: Metode autentikasi dan MFA

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan kemampuan autentikasi ID Microsoft Entra.
- Unit: Menjelaskan metode autentikasi dan Menjelaskan autentikasi multifaktor.

## Skenario demo

Dalam demo ini, Anda akan menjelajahi berbagai pengaturan yang tersedia untuk autentikasi di Microsoft Entra.

1. Kembali ke tab browser terbuka berjudul "Pusat admin home-Microsoft Entra."  Jika sebelumnya Anda menutup tab browser tersebut, buka Microsoft Edge dan masuk ke **[entra.microsoft.com](https://entra.microsoft.com)** dengan kredensial admin Microsoft 365 Anda.

1. Dari panel navigasi kiri, perluas **Perlindungan** lalu pilih **Metode autentikasi**.

1. Memilih metode autentikasi menampilkan halaman kebijakan.  Di sini Anda akan melihat metode autentikasi yang tersedia dan jika diaktifkan.  Kita akan melalui beberapa metode ini: .  
    1. Pilih **SMS**.  Baca deskripsi di bagian atas halaman, "Metode autentikasi ini mengirimkan kode satu kali melalui SMS ke ponsel pengguna, dan pengguna kemudian memasukkan kode tersebut untuk masuk. SMS dapat digunakan untuk autentikasi multifaktor dan Self-Service Reset Kata Sandi; itu juga dapat dikonfigurasi untuk digunakan sebagai faktor pertama."
        1. Poin yang perlu dipanggil di sini adalah bahwa beberapa metode autentikasi dapat digunakan untuk MFA dan/atau SSPR.  Beberapa hanya dapat digunakan sebagai bentuk utama autentikasi sementara yang lain hanya dapat digunakan sebagai bentuk autentikasi sekunder.
        1. Untuk mengonfigurasi metode autentikasi tertentu, Anda perlu mengaktifkannya lalu menargetkan pengguna dan/atau grup mana yang akan disertakan.  Anda juga dapat memilih grup mana yang akan dikecualikan.
        1. Jangan ubah pengaturan apa pun.  Tutup dari halaman pengaturan SMS dengan memilih **X** di kanan atas halaman.  
    1. Mari kita lihat pengaturan panggilan suara.  Pilih **Panggilan suara**, dari deskripsi Anda dapat melihat perbedaan penting.  Panggilan suara tidak dapat digunakan sebagai metode autentikasi faktor pertama.
    1. Sekarang pilih **Microsoft Authenticator**.  Ini adalah metode autentikasi unggulan.  
        1. Di sini Anda mengaktifkan fitur dan menargetkan siapa yang harus disertakan.  Anda dapat melakukan ini untuk semua pengguna atau grup. Setelah mengidentifikasi pengguna/grup mana yang akan disertakan, Anda dapat mengidentifikasi grup tertentu untuk dikecualikan.  
        1. Pada tab **Konfigurasi,** Anda dapat memilih apakah fitur tertentu dikelola oleh Microsoft. Pengaturan ini adalah cara mudah bagi organisasi untuk memungkinkan Microsoft mengaktifkan atau menonaktifkan fitur secara default. Ini dapat membantu organisasi meningkatkan postur keamanan mereka.
        1. Jangan ubah pengaturan apa pun. Tutup dari halaman, dengan memilih **X** di sudut kanan atas halaman.
 
1. Sekarang mari kita lihat perlindungan kata sandi. Pilih **Perlindungan Kata Sandi**.  Perhatikan berbagai parameter konfigurasi yang tersedia.  
    1. Pilih ikon informasi di samping **Ambang penguncian** untuk melihat arti parameter ini.  Saat ini diatur ke 10, yang berarti bahwa mungkin ada hingga 10 proses masuk yang gagal sebelum akun dikunci.  Tampaknya sedikit tinggi, sehingga Anda dapat mengatur ke nilai yang berbeda.
    1. Pilih ikon informasi untuk setiap parameter yang berbeda dan bicarakan dengannya, secara singkat.  Anda terutama ingin memanggil daftar kata sandi terlarang kustom.

1. Kekuatan autentikasi adalah kontrol Akses Bersyarkat yang memungkinkan administrator menentukan kombinasi metode autentikasi mana yang dapat digunakan untuk mengakses sumber daya. Anda akan melihat ini di Akses bersyarah.

1. Dari panel navigasi kiri untuk metode Autentikasi, pilih **Aktivitas**.
    1. **Pendaftaran** ditampilkan dengan garis bawah biru.  Di sini Anda dapat melihat aktivitas pendaftaran untuk metode autentikasi yang berbeda.
    1. Pilih **Penggunaan** untuk melihat detail penggunaan dan perhatikan bahwa Anda bisa menambahkan filter yang berbeda.

1. Dalam modul ini Anda juga berbicara tentang autentikasi multifaktor. Anda akan membahas lebih lanjut tentang MFA dalam demo pada akses bersyarah, tetapi Anda mungkin ingin mengambil satu menit untuk menampilkan beberapa pengaturan dasar.  Dari Microsoft Entra panel navigasi pusat admin, pilih **Autentikasi multifaktor**.  Anda mungkin perlu memilih **Perlihatkan selengkapnya** di bawah bagian tentang Perlindungan, di panel navigasi kiri.
    1. Pada halaman **Memulai** , ini menunjukkan bahwa cara terbaik untuk menerapkannya kepada pengguna adalah melalui akses bersyarah, tetapi ada beberapa pengaturan khusus yang Anda konfigurasi di sini.
    1. Pilih **Penguncian akun** dan panggil parameter penguncian yang dapat dikonfigurasi.
    1. Pilih **Blokir/buka blokir pengguna**, panggil bahwa di sini adalah tempat admin dapat memblokir/membuka blokir pengguna secara manual.  Perhatikan bahwa pengguna yang diblokir akan tetap diblokir selama 90 hari kecuali secara manual tidak diblokir.
    1. Pilih **Pemberitahuan penipuan**.  Ini memungkinkan admin untuk memungkinkan pengguna melaporkan penipuan jika mereka menerima permintaan verifikasi dua langkah yang tidak mereka mulai.
    1. Pilih **Pemberitahuan**.  Anda dapat mengonfigurasi Microsoft Entra untuk mengirim pemberitahuan email saat pengguna melaporkan pemberitahuan penipuan. Pemberitahuan ini biasanya dikirim ke administrator identitas, karena kredensial akun pengguna kemungkinan disusupi.
    1. Tutup dari halaman dengan memilih **X** di sudut kanan atas jendela.  Kemudian ulangi langkah ini untuk kembali ke pusat admin Microsoft Entra.

1. Tetap buka tab browser karena Anda akan kembali ke pusat admin Microsoft Entra untuk demo berikutnya.

### Tinjau

Dalam demo ini, Anda menunjukkan metode autentikasi yang tersedia di Microsoft Entra.  Anda juga menunjukkan beberapa parameter yang dapat dikonfigurasi yang terkait dengan autentikasi multifaktor.
