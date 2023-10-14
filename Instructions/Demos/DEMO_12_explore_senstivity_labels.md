<!---
---
Demo: Judul: 'Label sensitivitas di Microsoft Purview' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 3:Menjelaskan perlindungan informasi, manajemen siklus hidup data, dan kemampuan tata kelola data di Microsoft Purview; Unit 4: Menjelaskan label sensitivitas'
---
--->

# Demo: Label sensitivitas di Microsoft Purview

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan perlindungan informasi, manajemen siklus hidup data, dan kemampuan tata kelola data di Microsoft Purview
- Pelajaran: Menjelaskan label sensitivitas

## Skenario demo

Dalam demo ini, Anda akan menunjukkan kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.  **CATATAN**: Pertama kali Anda menggunakan Word online dengan penyewa Microsoft 365, diperlukan waktu 15 menit agar opsi Sensitivitas muncul pada pita.  Penyaji harus menjalankan demo bagian 2 sebelum kelas untuk memastikan waktu yang diperlukan hingga opsi muncul cukup.

### Demo Bagian 1

Dalam demo ini, Anda menunjukkan pengaturan untuk label sensitivitas yang ada dan kebijakan terkait untuk menerbitkan label.

1. Buka tab browser untuk beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH). Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Kepatuhan**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Di panel navigasi kiri, di bawah solusi, perluas **Perlindungan informasi** lalu pilih **Gambaran Umum**.  Halaman gambaran umum mencakup informasi tentang label sensitivitas teratas yang diterapkan ke konten, aktivitas teratas yang terdeteksi, lokasi di mana label sensitivitas diterapkan dan banyak lagi.  
    1. Pada halaman gambaran umum, Anda mungkin melihat kotak informasi kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.  Setelah Anda melakukan ini, mungkin akan ada penundaan pada pengaturan untuk menyebar melalui sistem.

1. Dari panel navigasi kiri, pilih **Label**.

1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk kenyamanan Anda. Perluas label bernama **Sangat Rahasia** dengan memilih **>**, lalu pilih **Semua Karyawan**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih **ikon pensil** di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar. Jika Anda tidak melihat ikon pensil, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Perhatikan cakupan untuk label ini.  Cakupan diatur ke File & email.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Perhatikan bahwa label ini dikonfigurasi untuk mendukung enkripsi dan penandaan konten. Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
        1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi. Tinjau pengaturan saat ini, tetapi jangan ubah apa pun. Perhatikan bagaimana akses pengguna ke konten diatur untuk tidak pernah kedaluwarsa.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Tim keuangan juga terdaftar dan mereka memiliki izin penulis bersama.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
        1. Pada halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya header dan footer yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Penandaan konten yang dikaitkan dengan label ini adalah marka air.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Sekarang Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Jendela berikutnya menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Next** di bagian bawah halaman.
    1. Jendela berikutnya adalah fitur pratinjau untuk menerapkan label ini secara otomatis ke aset data skema di Peta Data Microsoft Purview (seperti SQL, Synapse, dan banyak lagi) yang berisi jenis info sensitif yang Anda pilih.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Proteksi Informasi.

1. Dari panel navigasi kiri, pilih **Kebijakan label**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kenyamanan Anda.

1. Dalam hal ini, Pilih **Kebijakan label sensitivitas global**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Perhatikan deskripsinya, kebijakan label ini telah disiapkan untuk berfungsi sebagai kebijakan label sensitivitas default untuk semua pengguna dan grup. Kebijakan ini berfungsi untuk menerbitkan sebagian besar label yang telah dikonfigurasikan sebelumnya untuk penyewa lab Microsoft 365 ini dan dicantumkan di tab label.

1. Pilih **Edit kebijakan** dari bagian atas jendela.
    1. Baca deskripsi di bagian “Pilih label sensitivitas yang akan diterbitkan”.  Perhatikan label yang tercantum.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Halaman berikutnya adalah pratinjau untuk Menetapkan unit admin. Pilih **Selanjutnya**.
    1. Baca deskripsi di bagian “Terbitkan ke pengguna dan grup”.  Perhatikan bahwa label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Meninjau pengaturan kebijakan.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian, "Menerapkan label default ke dokumen." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah, "Terapkan label default ke email." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah, "Pengaturan default untuk rapat dan acara kalender." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bagian, "Terapkan label default ke konten Power BI." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Karena Anda sedang mengedit kebijakan, kolom nama berwarna abu-abu. Pilih **Berikutnya** di bagian bawah halaman.
    1. Meninjau pengaturan kebijakan. Karena tidak ada yang diubah pilih **Batal** untuk kembali ke halaman Kebijakan label.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Jika ada kebijakan pelabelan otomatis yang dikonfigurasi, pilih salah satu dan tinjau informasi kebijakan di panel detail.  Jika tidak ada kebijakan yang tercantum, Anda dapat memilih untuk menelusuri langkah-langkah untuk membuatnya, jika waktu memungkinkan.

1. Dari panel navigasi sebelah kiri, pilih Beranda untuk kembali ke portal kepatuhan Microsoft Purview.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Pada langkah ini, Anda akan menunjukkan proses penerapan label dari sudut pandang pengguna (dalam hal ini pengguna adalah admin).  Untuk melihat dampak penerapan label, Anda akan memilih label Rahasia - Keuangan karena label ini menerapkan tanda air.

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Word**.  

1. Pilih **Dokumen kosong**, lalu masukkan beberapa teks di halaman.  Pada bilah wartna biru di bagian atas halaman, pilih panah arah bawah, di sebelah tulisan Dokumen - Tersimpan, dan di kotak Nama File masukkan, **Label-uji** lalu tekan tombol **Enter** pada keyboard Anda.

1. Dari bilah menu atas, pilih **Ikon Sensitivitas** (ikon di sebelah kanan ikon mikrofon), jika Anda tidak segera melihat opsi ini, refresh halaman. Dari menu dropdown, pilih **Rahasia - Keuangan**.   CATATAN: jika Anda tidak segera melihat opsi Sensitivitas, refresh halaman, tetapi karena ini adalah lingkungan penyewa lab, Anda mungkin mengalami penundaan yang lebih lama dari penundaan normal (10-15 menit).
1. 
1. Dari bilah menu atas, pilih **View**, lalu pilih **Reading view**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

1. Biarkan tab browser Microsoft Purview tetap terbuka untuk demo berikutnya.

### Demo Bagian 3 (opsional)

Ingatlah dari bagian pertama demo, bahwa label Rahasia - Keuangan disiapkan untuk enkripsi. Per izin yang dikonfigurasi dengan label ini, pengguna di penyewa Contoso memiliki izin penampil untuk setiap dokumen/email dengan label yang diterapkan.  Di bagian ini Anda akan mengirim dokumen yang sebelumnya Anda buat, yang menyertakan label Rahasia - Keuangan, ke alamat email yang dapat Anda akses (alamat email pribadi atau email Microsoft Anda) dan itu BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com.  

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Outlook**

1. Pilih **Email baru** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Dari pita atas, pilih ikon klip kertas, lalu dari daftar drop-down, di bawah file yang disarankan, pilih dokumen yang Anda buat di langkah sebelumnya, **Test-label** untuk melampirkannya ke email.

1. Tekan **Kirim** untuk mengirim email.

1. Periksa email yang Anda kirimi dokumen.  Perhatian, email mungkin diarahkan ke folder sampah Anda.  Email berhasil terkirim, tetapi saat Anda mencoba membuka file word terlampir, yang awalnya diberi label sebagai rahasia - Keuangan, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen tersebut.

1. Tutup Outlook.

1. Biarkan tab browser Microsoft Purview tetap terbuka untuk demo berikutnya.


### Tinjau

Dalam demo ini, Anda menunjukkan pengaturan yang dapat dikonfigurasi untuk label sensitivitas dan pengaturan kebijakan untuk menerbitkan label sensitivitas. Anda juga menunjukkan cara menerapkan label dan dampak label tersebut, dari perspektif pengguna.

