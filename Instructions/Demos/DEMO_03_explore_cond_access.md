<!---
---
Demo: Judul: ‘Akses Bersyarat Azure AD’ Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra; Modul 3: Menjelaskan kemampuan manajemen akses Microsoft Entra; Unit 2: Menjelaskan Akses Bersyarat'
---
--->

# Demo: Akses Bersyarat Microsoft Entra

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Entra
- Modul: Menjelaskan kemampuan manajemen akses Microsoft Entra ID
- Unit: Menjelaskan Akses Bersyarat

## Skenario demo

Dalam demo ini, Anda akan menelusuri berbagai opsi yang tersedia untuk kebijakan akses bersyarat.

1. Kembali ke tab browser terbuka yang berjudul "Pusat admin Beranda-Microsoft Entra."  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan masuk ke **[entra.microsoft.com](https://entra.microsoft.com)** dengan kredensial admin Microsoft 365 Anda.

1. Dari panel navigasi kiri, bentangkan **Perlindungan**, lalu pilih **Akses Bersyarat**.

1. Laman ikhtisar Akses bersyar ditampilkan.  Di sini, Anda akan melihat petak yang memperlihatkan ringkasan Kebijakan dan pemberitahuan umum.  Dari panel navigasi kiri, pilih **Kebijakan**.

1. Laman ikhtisar Akses bersyar ditampilkan. Kebijakan Akses Bersyarat yang ada tercantum di sini. Untuk menampilkan pengaturan yang terkait dengan akses bersyarkat, pilih **+ kebijakan** baru.

1. Di bidang **Nama**, Anda akan memasukkan nama untuk kebijakan tersebut.

1. Perhatikan bahwa Anda memiliki beberapa opsi di bagian **Penugasan**.  Karena kebijakan akses bersyarat seperti pernyataan if/then, pengaturan penugasan seperti pernyataan "if".
    1. **Pengguna** - arahkan kursor ke ikon informasi di sebelah “Pengguna” dan sebutkan bahwa ini adalah tempat Anda memilih identitas di direktori tempat kebijakan diterapkan, termasuk pengguna, grup, dan prinsip layanan. Pilih **0 pengguna dan grup dipilih**.  Sekarang, Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup. Pilih dan sampaikan pengaturan yang tersedia untuk tab **Sertakan**, lalu pilih dan sampaikan pengaturan yang tersedia untuk tab **Kecualikan** .
    1. **Sumber daya target** - Pilih **Sumber daya target**.  Di sini, Anda mengontrol akses berdasarkan semua atau sekelumit lalu lintas akses jaringan, aplikasi cloud, atau tindakan.  Bentangkan bidang di bawah tempat tertulis pilih kebijakan ini berlaku untuk apa.  Di sini, Anda dapat memilih apakah kebijakan berlaku untuk aplikasi cloud, tindakan pengguna, atau konteks autentikasi.  
        1. Pilih **Aplikasi cloud**, lalu di bagian tab Sertakan, pilih opsi **Pilih aplikasi**, lalu di bawah tempat tulisan **Pilih**, pilih **Tidak Ada**, jendela akan terbuka untuk memilih satu atau beberapa aplikasi yang kebijakannya akan diterapkan.
        1. Tutup jendela Pilih aplikasi cloud dengan memilih **X** di pojok kanan atas jendela.
        1. Saat waktu memungkinkan, Anda dapat memilih melalui opsi lain (tindakan pengguna dan konteks autentikasi) untuk melihat opsi konfigurasi untuk masing-masing opsi.
    1. **Syarat** - arahkan mouse ke ikon informasi di sebelah ikon yang bertuliskan “Syarat” dan sebutkan bahwa hal ini menetapkan syarat mana yang mendefinisikan kapan kebijakan akan berlaku. Misalnya, ‘lokasi. Pilih **0 syarat dipilih**. Sampaikan berbagai "sinyal" yang tercantum.   Pilih beberapa opsi dengan terlebih dahulu memilih ikon informasi untuk menentukan apa itu, kemudian memilih **Tidak dikonfigurasi** pada item tertentu untuk menampilkan berbagai opsi.
        1. **Risiko pengguna** - Risiko pengguna menunjukkan peluang identitas atau akun tertentu disusupi. Risiko ini dapat dihitung offline menggunakan sumber inteligensi ancaman internal dan eksternal Microsoft.
        1. **Risiko masuk** - Risiko masuk menunjukkan peluang bahwa permintaan autentikasi yang diberikan tidak diotorisasi oleh pemilik identitas. Contohnya mungkin meliputi perincian masuk yang berasal dari alamat IP anonim atau perjalanan tidak biasa, dll.
        1. **Platform Perangkat** - Platform tempat pengguna masuk. Misalnya, 'iOS’.
        1. **Lokasi** - Lokasi (ditentukan menggunakan rentang alamat IP) tempat pengguna masuk
        1. **Aplikasi klien** - Perangkat lunak yang digunakan pengguna untuk mengakses aplikasi cloud. Misalnya, 'Browser'
        1. **Filter untuk perangkat** - Saat membuat kebijakan Akses Bersyarat, administrator dapat menargetkan atau mengecualikan perangkat tertentu di lingkungannya. Admin dapat menargetkan perangkat tertentu menggunakan operator dan properti yang didukung untuk filter perangkat dan kondisi penetapan lain yang tersedia dalam kebijakan Akses Bersyarat Anda.

1. **Kontrol Akses** – kembali ke analogi bahwa kebijakan akses bersyarat seperti pernyataan if/then, kontrol akses dianalogikan dengan pernyataan "then".
    1. **Izinkan** - Arahkan mouse Anda ke ikon informasi di sebelah bagian yang bertuliskan “Izinkan” untuk deskripsi.  Pilih **0 kontrol yang dipilih** untuk menampilkan berbagai opsi.  Sampaikan beberapa hal ini.  Secara khusus sampaikan opsi untuk **Mewajibkan autentikasi multifaktor**, di bagian Izinkan Akses dan bagaimana ini dapat digunakan untuk memberikan kontrol terperinci tentang kapan harus meminta MFA.   Sampaikan juga bahwa Anda dapat mengatur beberapa kontrol dan memerlukan semua atau hanya salah satu kontrol yang dipilih.
    1. **Sesi** - Arahkan mouse ke ikon informasi di sebelah ikon yang bertuliskan “Sesi” untuk deskripsi.  Sampaikan bahwa Kontrol sesi memungkinkan pengalaman terbatas dalam aplikasi cloud.  Misalnya, pengguna mungkin dapat mengakses aplikasi cloud, tetapi akan diblokir dari mengunduh konten atau mencetak apa pun, sebagai contoh.  Ini adalah topik yang lebih kompleks sehingga usahakan tetap sederhana.

1. Setelah kebijakan dikonfigurasi, Anda dapat mengaktifkan kebijakan dengan memilih **Aktif**, lalu tekan tombol **Buat** untuk membuat kebijakan.

1. Pilih **X** di pojok kanan atas laman untuk menutup kebijakan.

1. Tutup tab browser yang terbuka.

### Tinjauan

Dalam demo ini, Anda telah mempelajari berbagai opsi yang tersedia untuk kebijakan akses bersyarat.
