---
Demo:
    title: 'Label sensitivitas di Microsoft 365'
    module: 'Modul 4 Pelajaran 2: Menjelaskan kemampuan solusi kepatuhan Microsoft: Menjelaskan proteksi informasi dan kemampuan tata kelola Microsoft 365'
---


# Demo: Label sensitivitas di Microsoft 365

### Skenario demo
Dalam demo ini, Anda akan menunjukkan kemampuan label sensitivitas.  Anda akan menelusuri pengaturan label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.


#### Demo Bagian 1: Dalam demo ini, Anda menunjukkan pengaturan label sensitivitas yang ada dan kebijakan yang sesuai untuk menerbitkan label.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Hal ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri pada pusat kepatuhan Microsoft 365, pilih **Show all**.

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Information protection**.

1. Dalam kotak informasi berwarna kuning, yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten di file Office online dengan label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint.  Pilih Turn on now.  Setelah Anda melakukan ini, mungkin akan ada penundaan pada pengaturan untuk menyebar melalui sistem.

1. Pastikan bahwa tab **Labels** di bagian atas halaman dipilih (digarisbawahi).

1. Di tengah halaman, perhatikan bagaimana ada tiga label yang sudah dibuat.  Pilih **Confidential - Finance**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih **Edit Label** di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar.

    1. Konfigurasi dimulai dengan memberikan nama dan deskripsi label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Perhatikan ruang lingkup untuk label ini.  Cakupan diatur ke File & email tempat Anda dapat mengonfigurasi Enkripsi dan pengaturan penandaan konten untuk melindungi email berlabel dan file kantor.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Untuk cakupan yang dipilih, File & email, Anda dapat mengonfigurasi untuk mengenkripsi dan/atau menandai konten.  Perhatikan bagaimana pengaturan perlindungan file dan email diatur untuk enkripsi dan penandaan konten file.  Tinjau definisi masing-masing.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi.  Jangan mengubah apa pun.  Tinjau kotak informasi di bagian Konfigurasi pengaturan enkripsi dan tinjau pengaturan yang dikonfigurasi. Perhatikan bagaimana akses pengguna ke konten diatur untuk tidak pernah kedaluwarsa.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Tim keuangan juga terdaftar dan mereka memiliki izin penulis bersama.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Di halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya judul dan catatan kaki yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Penandaan konten yang dikaitkan dengan label ini adalah marka air.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Sekarang Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Jendela berikutnya menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Hal ini tidak diaktifkan, pilih **Next** di bagian bawah halaman. 

    1. Jendela berikutnya adalah fitur pratinjau untuk menerapkan label ini ke kolom database Azure (seperti SQL, Synapse, dan lainnya) yang berisi tipe info sensitif yang Anda pilih secara otomatis.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Perlindungan Informasi. 

1. Dari bagian atas halaman Perlindungan Informasi, pilih **Label policies**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  

1. Pilih **Confidential-Finance Policy**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Kebijakan ini berfungsi untuk menerbitkan label Kebijakan Keuangan Rahasia dan melindungi data yang berisi data keuangan untuk Contoso.  Perhatikan juga bagaimana kebijakan ini diterbitkan kepada semua orang.  

1. Pilih **Edit** kebijakan dari bagian atas jendela.

    1. Baca deskripsi di bagian “Choose sensitivity labels to publish”.  Perhatikan label yang tertera.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Baca deskripsi di bagian “Publish to users and groups”.  Perhatikan label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Tinjau pengaturan kebijakan.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Jangan mengubah pengaturan apa pun.  Pilih **Cancel** di bagian bawah halaman untuk keluar dari konfigurasi kebijakan dan kembali ke halaman Perlindungan informasi.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis.  Perhatikan bahwa tidak ada kebijakan pelabelan otomatis yang dikonfigurasi.  Jangan mengubah pengaturan apa pun.  Jika Anda bertanya-tanya mengapa tidak ada kebijakan di sini, mengingat konfigurasi label diatur ke pelabelan otomatis untuk file dan email, kembali ke langkah-langkah saat Anda dipandu melalui pengaturan konfigurasi label dan meninjau deskripsi dan kotak informasi terkait pelabelan otomatis untuk file dan email.  Petunjuk:  Di tab pelabelan otomatis untuk lab sensitivitas, tertulis  “Untuk menerapkan label ini ke file yang sudah disimpan secara otomatis (di SharePoint dan OneDrive) atau email yang sudah diproses oleh Exchange, Anda harus membuat kebijakan pelabelan otomatis."

1. Dari panel navigasi sebelah kiri, pilih Beranda untuk kembali ke pusat kepatuhan Microsoft 365.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.


#### Demo Bagian 2:  Pada langkah ini, Anda akan menunjukkan proses penerapan label dari perspektif pengguna (dalam hal ini pengguna adalah admin) dan melihat penandaan konten yang dihasilkan oleh label.

1. Dari halaman beranda pusat kepatuhan Microsoft 365, pilih **ikon peluncur aplikasi**, di sebelah tulisan Contoso Electronics. **klik kanan di ikon Word** dan pilih **Open in new tab**.  

1. Pilih **+ New blank document**, kemudian masukkan beberapa teks di halaman.  Di bilah berwarna biru di bagian atas halaman, pilih panah bawah, di sebelahnya tertulis DocumenXX - Saved, dan di kotak Nama File masukkan, **Test-label**.

1. Dari bilah menu atas, pilih **Sensitivity**, jika Anda tidak langsung melihat opsi ini, segarkan halaman. Dari menu tarik-turun pilih **Confidential - Finance**. 

1. Dari bilah menu atas, pilih **View**, lalu pilih **Reading view**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

#### Demo Bagian 3 (opsional): Selain penandaan konten, pengaturan perlindungan label juga diatur untuk enkripsi. Sesuai izin yang dikonfigurasi dengan label ini, anggota grup keuangan dapat menulis bersama dokumen dengan label yang diterapkan ini dan pengguna di penyewa Contoso dapat melihat (atau dokumen/email apa pun dengan label yang diterapkan).  Di bagian ini, Anda akan mengirim dokumen ke alamat email yang dapat Anda akses (yaitu, alamat email pribadi atau email Microsoft Anda) dan ini BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com dan lihat apa yang terjadi ketika Anda mencoba untuk membuka lampiran.  

1. Dari halaman beranda pusat kepatuhan Microsoft 365, pilih **ikon peluncur aplikasi**, di sebelah tulisan Contoso Electronics. **klik kanan di ikon Outlook** dan pilih **Open in new tab**.

1. Pilih **New message** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Attach**.

1. Pilih **Browse cloud locations**.

1. Dari daftar yang muncul, pilih dokumen yang Anda buat dan beri label **Test-label**. Pilih **Next** dan pilih **Attach as a copy**.  Tekan **Send**.

1. Periksa email yang Anda kirimi dokumen.  Catatan, email mungkin diarahkan ke folder sampah Anda.  Saat mencoba membuka file word terlampir, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen.

1. Tutup tab browser yang terbuka.


#### Tinjauan
Dalam demo ini, Anda telah menunjukkan label sensitivitas.  Anda telah menunjukkan pengaturan label sensitivitas yang sudah ada yang telah dibuat dan kebijakan terkait untuk memublikasikan label. Kemudian Anda telah menunjukkan cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.
