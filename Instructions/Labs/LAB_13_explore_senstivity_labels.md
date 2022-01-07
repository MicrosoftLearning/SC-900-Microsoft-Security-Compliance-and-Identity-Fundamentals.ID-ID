---
lab:
    title: 'Mempelajari label sensitivitas di Microsoft 365'
    module: 'Modul 4 Pelajaran 2: Menjelaskan kemampuan solusi kepatuhan Microsoft: Menjelaskan perlindungan informasi dan kemampuan tata kelola Microsoft 365'
---


# Lab: Mempelajari label sensitivitas di Microsoft 365

## Skenario lab
Di lab ini, Anda akan mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.


**Perkiraan Waktu**: 20-25 menit

#### Tugas 1: Dalam tugas ini, Anda akan memperoleh pemahaman tentang hal yang dapat dilakukan oleh label sensitivitas dengan menelusuri pengaturan untuk label sensitivitas yang sudah ada, yang telah dibuat dan kebijakan terkait untuk menerbitkan label.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Hal ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Information protection**.

1. Pilih tab **Label** dari bagian atas halaman.

1. Muncullah kotak informasi berwarna kuning yang menunjukkan, “Organisasi Anda belum mengaktifkan kemampuan untuk memproses konten di file Office online dengan label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint...”  Pilih Turn on now.  Setelah Anda melakukan ini, mungkin akan ada penundaan pada pengaturan untuk menyebar melalui sistem.


1. Di tengah halaman, perhatikan bahwa ada tiga label yang sudah dibuat.  Pilih **Confidential - Finance**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih Edit Label di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar.

1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Perhatikan cakupan untuk label ini.  Cakupan diatur ke File & email tempat Anda dapat mengonfigurasi Enkripsi dan pengaturan penandaan konten untuk melindungi email berlabel dan file kantor.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Untuk cakupan yang dipilih, File & email, Anda dapat mengonfigurasi untuk mengenkripsi dan/atau menandai konten.  Perhatikan bagaimana pengaturan perlindungan file dan email diatur untuk enkripsi dan penandaan konten file.  Tinjau definisi masing-masing.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi.  Jangan mengubah apa pun.  Tinjau kotak informasi di bagian Konfigurasi pengaturan enkripsi dan tinjau pengaturan yang dikonfigurasi. Perhatikan bagaimana akses pengguna ke konten diatur untuk tidak pernah kedaluwarsa.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Tim keuangan juga terdaftar dan mereka memiliki izin penulis bersama.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Pada halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya header dan footer yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Penandaan konten yang dikaitkan dengan label ini adalah marka air yang bermakna, SANGAT RAHASIA.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Sekarang Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela berikutnya menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Next** di bagian bawah halaman. 

1. Jendela berikutnya adalah fitur pratinjau untuk menerapkan label ini ke kolom database Azure (seperti SQL, Synapse, dan lainnya) yang berisi tipe info sensitif yang Anda pilih secara otomatis.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Proteksi Informasi. 

1. Dari bagian atas halaman Perlindungan Informasi, pilih **Label policies**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  

1. Pilih **Confidential-Finance Policy**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Kebijakan ini berfungsi untuk menerbitkan label Kebijakan Keuangan Rahasia dan melindungi data yang berisi data keuangan untuk Contoso.  Perhatikan juga bagaimana kebijakan ini diterbitkan kepada semua orang.  

1. Pilih **Edit** kebijakan dari bagian atas jendela.

1. Baca deskripsi di bagian “Pilih label sensitivitas yang akan diterbitkan”.  Perhatikan label yang tertera.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Baca deskripsi di bagian “Terbitkan ke pengguna dan grup”.  Perhatikan label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Meninjau pengaturan kebijakan.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah "the Apply a default label to documents."  Perhatikan bahwa tidak ada label default. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah “the Apply a default label to emails."  Pilih panah menu tarik-turun di kotak input untuk melihat opsi yang tersedia. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah “the Apply a default label to Power BI content."  Perhatikan bahwa tidak ada label default. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Jangan mengubah pengaturan apa pun.  Pilih **Cancel** di bagian bawah halaman untuk keluar dari konfigurasi kebijakan dan kembali ke halaman Proteksi informasi.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis.  Perhatikan bahwa tidak ada kebijakan pelabelan otomatis yang dikonfigurasi.  Jangan mengubah pengaturan apa pun.  Jika Anda bertanya-tanya mengapa tidak ada kebijakan di sini, mengingat konfigurasi label diatur ke pelabelan otomatis untuk file dan email, kembali ke langkah-langkah di mana Anda dipandu melalui pengaturan konfigurasi label dan meninjau deskripsi dan kotak informasi terkait pelabelan otomatis untuk file dan email.  Petunjuk:  Di tab pelabelan otomatis untuk lab sensitivitas, tertulis  “Untuk menerapkan label ini ke file yang sudah disimpan secara otomatis (di SharePoint dan OneDrive) atau email yang sudah diproses oleh Exchange, Anda harus membuat kebijakan pelabelan otomatis."

1. Dari panel navigasi sebelah kiri, pilih Home untuk kembali ke pusat kepatuhan Microsoft 365.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.


#### Tugas 2:  Dalam tugas ini, Anda akan melalui proses penerapan label dari sudut pandang pengguna (dalam hal ini, pengguna adalah admin) dan melihat penandaan konten yang dihasilkan oleh label.

1. Pertama, pastikan Anda telah membuka penyiapan Office di komputer virtual (VM) lab.  Untuk melakukannya, pilih lab **Microsoft 365 admin center** yang akan membuka browser.  Jika tab telah Anda tutup, buka tab browser baru dan ketikkan **admin.microsoft.com**.
    1. Dari panel navigasi, pilih **Billing** untuk melihat semua opsi, lalu pilih **Your products**.
    1. Dari halaman produk Anda, pilih **Microsoft 365 E5 Trial**
    1. Dari halaman Microsoft 365 E5 Trial, pilih **Download and install software** lalu ikuti instruksi yang ada di halaman itu.

1. Dari pojok kiri bawah VM lab, pilih ikon Windows, lalu pilih **Word** dan pilih **Dokumen kosong**.  Ini akan membuka dokumen word yang baru menggunakan versi desktop dari Word.

1. Dari bilah menu bagian atas, pilih **Sensitivity**. Dari menu tarik-turun, pilih **Confidential - Finance**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  Marka air akan muncul pada teks kecil berwarna abu-abu muda yang ditampilkan secara vertikal di halaman itu. 

1. Simpan file Word.

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

#### Tugas 3 (opsional): Selain penandaan konten, setelan proteksi label juga disetel untuk enkripsi. Sesuai izin yang dikonfigurasi dengan label ini, anggota grup keuangan dapat mengedit bersama dokumen dengan menerapkan label ini dan pengguna di penyewa Contoso dapat melihat.  Dalam tugas ini, Anda akan mengirim dokumen ini ke alamat email yang dapat Anda akses (yaitu, alamat email pribadi) dan itu BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com dan lihat apa yang terjadi saat Anda mencoba membuka lampiran.  

1. Dari halaman beranda pusat kepatuhan Microsoft 365, pilih **ikon peluncur aplikasi**, di sebelah tulisan Contoso Electronics. **right click on the Outlook icon** dan pilih **Open in new tab**.

1. Pilih **New message** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Attach**.

1. Pilih **Browse cloud locations**.

1. Dari daftar yang muncul, pilih dokumen yang Anda buat dan beri label **Test-label**. Pilih **Next** dan pilih **Attach as a copy**.  Tekan **Send**.

1. Menggunakan browser web di VM lab, masuk ke akun email yang menjadi tujuan pengiriman dokumen.  Perhatian, email mungkin diarahkan ke folder sampah Anda.  Saat Anda mencoba membuka file kata terlampir, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen.

1. Tutup tab browser yang terbuka.


#### Tinjauan
Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda telah mempelajari pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.