<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi label sensitivitas di Microsoft Purview' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 3: Menjelaskan perlindungan informasi dan manajemen siklus hidup data di Microsoft Purview; Pelajaran 4: Menjelaskan label sensitivitas'
---
--->

# <a name="lab-explore-sensitivity-labels-in-microsoft-purview"></a>Lab: Mempelajari label sensitivitas di Microsoft Purview

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan perlindungan informasi dan manajemen siklus hidup data di Microsoft Purview
- Pelajaran: Menjelaskan label sensitivitas

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.

**Perkiraan Waktu**: 20-25 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini, Anda akan mendapatkan pemahaman tentang apa yang dapat dilakukan label sensitivitas dengan mempelajari pengaturan untuk label sensitivitas yang ada yang telah dibuat dan kebijakan terkait untuk menerbitkan label.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia hosting lab) lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Information protection**.

1. Dari halaman ringkasan, perhatikan bahwa kotak informasi berwarna kuning menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten di file Office online yang menerapkan label sensitivitas terenkripsi dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.  Setelah Anda melakukan ini, mungkin akan ada penundaan pada pengaturan untuk menyebar melalui sistem.  Tinjau juga informasi yang tersedia di halaman ringkasan ini.

1. Pilih tab **Label** dari bagian atas halaman.

1. Di tengah halaman, perhatikan bahwa ada label yang sudah dibuat.  Pilih **Confidential - Finance**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih **Edit Label** di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar.  Saat Anda menelusuri dan melihat berbagai pengaturan, JANGAN mengubah apa pun.

1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Perhatikan cakupan untuk label ini.  Cakupan diatur ke **Item**.  Baca deskripsi tetapi jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Untuk cakupan yang dipilih, item, Anda dapat mengonfigurasi untuk mengenkripsi dan/atau menandai konten.  Perhatikan bagaimana pengaturan perlindungan untuk file dan email diatur untuk enkripsi dan penandaan konten file.  Tinjau definisi masing-masing.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi.  Jangan mengubah apa pun.  Tinjau kotak informasi di bagian Konfigurasi pengaturan enkripsi dan tinjau pengaturan yang dikonfigurasi. Perhatikan bagaimana akses pengguna ke konten diatur untuk tidak pernah kedaluwarsa.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Tim keuangan juga terdaftar dan mereka memiliki izin penulis bersama.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Pada halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya header dan footer yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Penandaan konten yang terkait dengan label ini adalah marka air yang bertuliskan, SANGAT RAHASIA.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Anda sekarang berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela berikutnya menentukan pengaturan perlindungan untuk grup dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Next** di bagian bawah halaman.

1. Jendela berikutnya adalah fitur pratinjau Pelabelan otomatis untuk aset data yang dibuat skema. Baca deskripsinya.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Proteksi Informasi.

1. Dari bagian atas halaman Perlindungan Informasi, pilih **Label policies**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  

1. Dalam hal ini, Pilih **Kebijakan label sensitivitas global**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Perhatikan deskripsinya, ini adalah kebijakan label sensitivitas default untuk semua pengguna dan grup. Kebijakan ini berfungsi untuk menerbitkan sebagian besar label yang telah dikonfigurasikan sebelumnya untuk penyewa lab Microsoft 365 ini dan dicantumkan di tab label.  

1. Pilih **Edit** kebijakan dari bagian atas jendela.
    1. Baca deskripsi di bagian “Pilih label sensitivitas yang akan diterbitkan”.  Perhatikan label yang tertera.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian “Terbitkan ke pengguna dan grup”.  Perhatikan bahwa label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Meninjau pengaturan kebijakan.  Pilih **Wajibkan pengguna untuk menerapkan label ke email dan dokumen mereka**. Tinjau deskripsi yang diberikan. Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian, "Menerapkan label default ke dokumen." Di kolom Default label, pilih panah arah bawah lalu pilih **Umum/Semua karyawan (tidak dibatasi)** .  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian, Terapkan label default ke email." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian, "Terapkan label default ke konten Power BI." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Karena Anda sedang mengedit kebijakan, kolom nama berwarna abu-abu. Pilih **Berikutnya** di bagian bawah halaman.
    1. Tinjau pengaturan kebijakan lalu pilih **Kirim**, lalu pilih **Selesai** untuk kembali ke halaman Perlindungan informasi.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis.  Perhatikan bahwa tidak ada kebijakan pelabelan otomatis yang dikonfigurasi.  Jangan mengubah pengaturan apa pun.  Jika Anda bertanya-tanya mengapa tidak ada kebijakan di sini, karena konfigurasi label diatur ke pelabelan otomatis untuk file dan email, kembali ke langkah-langkah di mana Anda menelusuri pengaturan konfigurasi label dan tinjau kotak deskripsi dan informasi yang terkait dengan Pelabelan otomatis untuk file dan email.  Petunjuk:  Di tab pelabelan otomatis untuk lab sensitivitas, tertulis  “Untuk menerapkan label ini ke file yang sudah disimpan secara otomatis (di SharePoint dan OneDrive) atau email yang sudah diproses oleh Exchange, Anda harus membuat kebijakan pelabelan otomatis."

1. Dari panel navigasi sebelah kiri, pilih Beranda untuk kembali ke portal kepatuhan Microsoft Purview.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda akan melakukan proses penerapan label dari sudut pandang pengguna (dalam hal ini pengguna adalah admin) dan melihat penandaan konten yang dibuat oleh label.

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Word**.  

1. Di bawah Buat baru, pilih **Dokumen kosong**, lalu masukkan beberapa teks di halaman.  Di bagian atas halaman, pilih panah arah bawah, di sebelah tulisan Dokumen - Tersimpan, dan di kotak Nama File masukkan, **Label-uji** lalu tekan **Masuk** pada papan ketik.

1. Dari bilah menu atas, pilih **ikon Sensitivitas**, ikon di sebelah kanan ikon mikrofon (tergantung pada ukuran layar, Anda mungkin perlu memilih elipsis lalu memilih sensitivitas). Dari menu dropdown, pilih **Rahasia - Keuangan**.  CATATAN: jika Anda tidak segera melihat opsi Sensitivitas, refresh halaman, tetapi karena ini adalah lingkungan penyewa lab, Anda mungkin mengalami penundaan yang lebih lama dari penundaan normal (10-15 menit).

1. Dari bilah menu atas, pilih **View**, lalu pilih **Reading view**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

### <a name="task-3-optional"></a>Tugas 3 (opsional)

Ingatlah dari bagian pertama demo, bahwa label Rahasia - Keuangan disiapkan untuk enkripsi. Per izin yang dikonfigurasi dengan label ini, pengguna di penyewa Contoso memiliki izin penampil untuk setiap dokumen/email dengan label yang diterapkan.  Di bagian ini Anda akan mengirim dokumen yang Anda buat sebelumnya, yang menyertakan label Rahasia - Keuangan, ke alamat email yang dapat Anda akses (mis., alamat email pribadi atau email Microsoft Anda) dan itu BUKAN bagian dari WWLxZZZZ Domain.OnMicrosoft.com.  

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Outlook**.

1. Pilih **Email baru** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Lampirkan** (ikon penclip kertas).

1. Pilih **OneDrive**.

1. Pastikan tab **Terbaru** di panel navigasi kiri dipilih.  Dari daftar yang muncul, pilih dokumen yang Anda buat dan beri label **Test-label**. Pilih **Next** dan pilih **Attach as a copy**.  Tekan **Kirim**.

1. Periksa email yang Anda kirimi dokumen.  Perhatian, email mungkin diarahkan ke folder sampah Anda.  Email berhasil terkirim, tetapi saat Anda mencoba membuka file word terlampir, yang awalnya diberi label sebagai rahasia - Keuangan, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen tersebut.

1. Tutup tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda akan mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang sudah ada yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.
