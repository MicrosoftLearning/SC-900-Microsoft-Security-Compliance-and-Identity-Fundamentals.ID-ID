<!---
---
Demo: Judul: 'Menjelajahi Pengaturan Pengguna Microsoft Entra ID' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 2: Menjelaskan kemampuan autentikasi Microsoft Entra ID; Unit 3: Menjelaskan metode autentikasi dan Unit 4: Menjelaskan autentikasi multifaktor’
---
--->

# Demo: Metode autentikasi dan MFA

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra.
- Modul: Menjelaskan kemampuan autentikasi Microsoft Entra ID.
- Unit: Menjelaskan metode autentikasi dan Menjelaskan autentikasi multifaktor.

## Skenario demo

Dalam demo ini, Anda akan menjelajahi berbagai pengaturan yang tersedia untuk autentikasi di Microsoft Entra.

1. Kembali ke tab browser terbuka yang berjudul "Pusat admin Beranda-Microsoft Entra."  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan masuk ke **[entra.microsoft.com](https://entra.microsoft.com)** dengan kredensial admin Microsoft 365 Anda.

1. Dari panel navigasi kiri, bentangkan **Perlindungan**, lalu pilih **Metode autentikasi**.

1. Memilih metode autentikasi menampilkan laman kebijakan.  Di sini, Anda akan melihat metode autentikasi yang tersedia dan apakah itu diaktifkan.  Kita akan mempelajari beberapa metode ini:.  
    1. Pilih **SMS**.  Baca deskripsi di bagian atas laman, "Metode autentikasi ini memberikan kode sekali pakai melalui SMS ke ponsel pengguna, kemudian pengguna memasukkan kode tersebut untuk masuk. SMS dapat digunakan untuk autentikasi multifaktor dan Pengaturan Ulang Kata Sandi Mandiri; itu juga dapat dikonfigurasi untuk digunakan sebagai faktor pertama."
        1. Poin yang perlu ditekankan di sini adalah beberapa metode autentikasi dapat digunakan untuk MFA dan/atau SSPR.  Beberapa hanya dapat digunakan sebagai bentuk utama autentikasi, sementara yang lain hanya dapat digunakan sebagai bentuk autentikasi sekunder.
        1. Untuk mengonfigurasi metode autentikasi tertentu, Anda perlu mengaktifkannya, lalu menargetkan pengguna dan/atau grup yang akan disertakan.  Anda juga dapat memilih grup mana yang akan dikecualikan.
        1. Jangan ubah pengaturan apa pun.  Tutup laman pengaturan SMS dengan memilih **X** di kanan atas laman.  
    1. Mari kita lihat pengaturan panggilan suara.  Pilih **Panggilan suara**, dari deskripsinya, Anda dapat melihat perbedaan penting.  Panggilan suara tidak dapat digunakan sebagai metode autentikasi faktor pertama.
    1. Sekarang pilih **Microsoft Authenticator**.  Ini adalah metode autentikasi unggulan.  
        1. Di sini, Anda mengaktifkan fitur dan menargetkan siapa yang akan disertakan.  Anda dapat melakukan ini untuk semua pengguna atau grup. Setelah mengidentifikasi pengguna/grup yang akan disertakan, Anda dapat mengidentifikasi grup tertentu untuk dikecualikan.  
        1. Pada tab **Konfigurasi**, Anda dapat memilih fitur tertentu untuk dikelola oleh Microsoft. Pengaturan adalah cara yang tepat bagi organisasi untuk memungkinkan Microsoft mengaktifkan atau menonaktifkan fitur secara default. Ini dapat membantu organisasi meningkatkan postur keamanan mereka.
        1. Jangan ubah pengaturan apa pun. Tutup laman dengan memilih **X** di pojok kanan atas laman.
 
1. Sekarang, mari kita lihat perlindungan kata sandi. Pilih **Perlindungan Kata Sandi**.  Perhatikan berbagai parameter konfigurasi yang tersedia.  
    1. Pilih ikon informasi di samping **Ambang penguncian** untuk melihat arti parameter ini.  Saat ini diatur ke 10, yang berarti bahwa mungkin ada hingga 10 proses masuk yang gagal sebelum akun dikunci.  Tampaknya sedikit tinggi, sehingga Anda dapat mengatur ke nilai yang berbeda.
    1. Pilih ikon informasi untuk setiap parameter yang berbeda dan sampaikan, secara singkat.  Terutama, Anda ingin menyampaikan daftar kata sandi terlarang kustom.

1. Kekuatan autentikasi adalah kontrol Akses Bersyarat yang memungkinkan administrator menentukan kombinasi metode autentikasi mana yang dapat digunakan untuk mengakses sumber daya. Anda akan melihat ini di Akses bersyarat.

1. Dari panel navigasi kiri untuk metode Autentikasi, pilih **Aktivitas**.
    1. **Pendaftaran** ditampilkan dengan garis bawah biru.  Di sini, Anda dapat melihat aktivitas pendaftaran untuk metode autentikasi yang berbeda.
    1. Pilih **Penggunaan** untuk melihat detail penggunaan dan perhatikan bahwa Anda dapat menambahkan filter yang berbeda.

1. Dalam modul ini, Anda juga berbicara tentang autentikasi multifaktor. Anda akan membahas lebih lanjut tentang MFA dalam demo pada akses bersyarat, tetapi Anda mungkin ingin mengambil waktu satu menit untuk menampilkan beberapa pengaturan dasar.  Dari panel navigasi pusat admin Microsoft Entra, pilih **Autentikasi multifaktor**.  Anda mungkin perlu memilih **Tampilkan lainnya** pada bagian perlindungan, di panel navigasi kiri.
    1. Pada laman **Memulai**, ini menunjukkan bahwa cara terbaik untuk menerapkannya kepada pengguna melalui akses bersyarat, tetapi ada beberapa pengaturan tertentu yang Anda konfigurasi di sini.
    1. Pilih **Penguncian akun** dan panggil parameter penguncian yang dapat dikonfigurasi.
    1. Pilih **Blokir/buka blokir pengguna**, sampaikan bahwa di sinilah admin dapat memblokir/membuka blokir pengguna secara manual.  Perhatikan bahwa pengguna yang diblokir akan tetap diblokir selama 90 hari kecuali dibuka blokirnya secara manual.
    1. Pilih **Pemberitahuan penipuan**.  Ini memungkinkan admin untuk mengizinkan pengguna melaporkan penipuan jika mereka menerima permintaan verifikasi dua langkah yang tidak mereka mulai.
    1. Pilih **Pemberitahuan**.  Anda dapat mengonfigurasi Microsoft Entra untuk mengirim pemberitahuan email saat pengguna melaporkan peringatan penipuan. Pemberitahuan ini biasanya dikirim ke administrator identitas, karena kredensial akun pengguna kemungkinan disusupi.
    1. Tutup laman dengan memilih **X** di pojok kanan atas jendela.  Kemudian ulangi langkah ini untuk kembali ke pusat admin Microsoft Entra.

1. Buka tab browser karena Anda akan kembali ke pusat admin Microsoft Entra untuk demo berikutnya.

### Tinjauan

Dalam demo ini, Anda telah melihat metode autentikasi yang tersedia di Microsoft Entra.  Anda juga telah melihat beberapa parameter yang dapat dikonfigurasi yang terkait dengan autentikasi multifaktor.
