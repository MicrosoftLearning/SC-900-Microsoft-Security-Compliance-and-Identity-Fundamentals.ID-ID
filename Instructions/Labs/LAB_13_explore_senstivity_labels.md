<!---
---
Lab: Judul: 'Jelajahi label sensitivitas di Microsoft Purview' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 3: Menjelaskan perlindungan informasi dan manajemen siklus hidup data di Microsoft Purview; Pelajaran 4: Menjelaskan label sensitivitas'
---
--->

# Lab: Mempelajari label sensitivitas di Microsoft Purview

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan perlindungan informasi dan manajemen siklus hidup data di Microsoft Purview
- Pelajaran: Menjelaskan label sensitivitas

## Skenario lab

Di lab ini, Anda akan mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.

**Perkiraan Waktu**: 20-25 menit

### Tugas 1

Dalam tugas ini, Anda akan mendapatkan pemahaman tentang apa yang dapat dilakukan label sensitivitas dengan mempelajari pengaturan untuk label sensitivitas yang ada yang telah dibuat dan kebijakan terkait untuk menerbitkan label.

1. Buka tab browser untuk beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH). Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Kepatuhan**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.   

1. Di panel navigasi kiri, di bawah solusi, perluas **Perlindungan informasi** lalu pilih **Gambaran Umum**. Perhatikan peringatan di bagian atas halaman dan gulir ke bawah untuk melihat informasi yang tersedia.
   1. Pada halaman Gambaran Umum, Anda mungkin melihat kotak informasi kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.  Setelah Anda melakukan ini, mungkin ada penundaan agar pengaturan disebarluaskan melalui sistem dan ada langkah tambahan yang harus diselesaikan untuk melindungi Teams, situs SharePoint, dan Grup Microsoft 365.

1. Dari panel navigasi kiri, pilih **Label**.
   1. Pada halaman Label, Anda mungkin melihat kotak informasi kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.  Setelah Anda melakukan ini, mungkin ada penundaan agar pengaturan disebarluaskan melalui sistem dan ada langkah tambahan yang harus diselesaikan untuk melindungi Teams, situs SharePoint, dan Grup Microsoft 365.
1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk kenyamanan Anda. Perluas label bernama **Sangat Rahasia** dengan memilih **>**, lalu pilih **Semua Karyawan**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih **ikon pensil** di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar. Jika Anda tidak melihat ikon pensil, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Perhatikan cakupan untuk label ini.  Cakupan diatur ke File & Email.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Perhatikan bahwa label ini dikonfigurasi untuk mendukung enkripsi dan penandaan konten. Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.
        1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi. Tinjau pengaturan saat ini, tetapi jangan ubah apa pun. Perhatikan bagaimana akses pengguna ke konten diatur ke tidak pernah kedaluwarsa dan selalu mengizinkan akses offline.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
        1. Pada halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya header dan footer yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Tanda isi yang terkait dengan label ini adalah footer.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Sekarang Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Jendela berikutnya menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Next** di bagian bawah halaman.
    1. Jendela berikutnya adalah fitur pratinjau untuk menerapkan label ini secara otomatis ke aset data skema di Peta Data Microsoft Purview (seperti SQL, Synapse, dan banyak lagi) yang berisi jenis info sensitif yang Anda pilih.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Proteksi Informasi.

1. Dari panel navigasi kiri, pilih **Kebijakan label**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kenyamanan Anda.

1. Dalam hal ini, Pilih **Kebijakan label sensitivitas global**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Perhatikan deskripsinya, kebijakan label ini telah disiapkan untuk berfungsi sebagai kebijakan label sensitivitas default untuk semua pengguna dan grup. Kebijakan ini berfungsi untuk menerbitkan sebagian besar label yang telah dikonfigurasikan sebelumnya untuk penyewa lab Microsoft 365 ini dan dicantumkan di tab label.  

1. Pilih **Edit kebijakan** dari bagian atas jendela.
    1. Tinjau deskripsi untuk "Pilih label sensitivitas untuk diterbitkan".  Perhatikan label yang tercantum.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Tinjau deskripsi untuk "Tetapkan unit admin". Unit Admin diatur ke direktori lengkap, jangan ubah pengaturan apa pun. Pilih **Selanjutnya**.  
    1. Tinjau deskripsi untuk "Terbitkan ke pengguna dan grup".  Perhatikan bahwa label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Meninjau pengaturan kebijakan. Pilih **Wajibkan pengguna menerapkan label ke email dan dokumen mereka dan** tinjau deskripsi yang disediakan. Pilih **Next** di bagian bawah halaman.
    1. Tinjau deskripsi untuk "Terapkan label default ke dokumen." Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Tinjau deskripsi untuk "Terapkan label default ke email" dan "Warisi label dari lampiran". Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Tinjau deskripsi untuk "Terapkan label default ke rapat dan acara kalender". Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Tinjau deskripsi untuk "Terapkan label default ke konten Power BI". Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Karena Anda sedang mengedit kebijakan, kolom nama berwarna abu-abu. Pilih **Berikutnya** di bagian bawah halaman.
    1. Meninjau pengaturan kebijakan. Pilih **Batal** untuk membuang perubahan apa pun dan kembali ke halaman Kebijakan label.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Tidak ada kebijakan label otomatis yang telah dikonfigurasi sebelumnya di penyewa kami. Untuk membuat kebijakan label otomatis baru, pilih **Buat kebijakan label otomatis**.  Di sini Anda akan menelusuri langkah-langkah untuk membuat kebijakan baru.
    1. Anda mulai dengan memilih informasi yang Anda inginkan untuk menerapkan label ini.  Perhatikan opsi yang tersedia.  Pilih **Medis dan kesehatan** lalu pilih salah satu templat yang tersedia.  Pilih **Selanjutnya**.
    1. Anda dapat memberi nama kebijakan label otomatis atau menggunakan nama default.  Pilih **Selanjutnya**.
    1. Anda dapat menetapkan unit admin tempat kebijakan ini berlaku.  Biarkan default diatur ke direktori penuh dan pilih **Berikutnya**.
    1. Perhatikan lokasi yang tersedia tempat Anda ingin menerapkan label.  Biarkan pengaturan default, lalu klik **Next**.
    1. Anda dapat menyiapkan aturan umum atau tingkat lanjut yang menentukan konten tempat label diterapkan.  Biarkan default diatur ke Aturan umum dan pilih **Berikutnya**.
    1. Anda dapat menentukan aturan untuk konten di semua lokasi.  Label akan diterapkan ke isi yang cocok dengan aturan yang ditentukan pada halaman ini.  Untuk templat yang Anda pilih, Anda akan melihat item baris. Perluas untuk melihat kondisi yang berlaku.  Biarkan semua pengaturan default dan pilih **Berikutnya**.
    1. Pilih label untuk diterapkan secara otomatis dengan memilih **Pilih label**.  Pilih label lalu pilih **Tambahkan**. Pilih **Selanjutnya**.
    1. Pengaturan tambahan dapat dikonfigurasi untuk email. Biarkan pengaturan default, lalu klik **Next**.
    1. Anda dapat memutuskan untuk menguji kebijakan sekarang atau nanti.  Pilih **Biarkan kebijakan dinonaktifkan** lalu pilih **Berikutnya**.
    1. Tinjau pengaturan dan pilih **Buat kebijakan** lalu pilih **Selesai**.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke portal kepatuhan Microsoft Purview.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda akan melalui proses penerapan label sensitivitas ke dokumen Microsoft Word lalu menampilkan penandaan konten (marka air) yang dihasilkan oleh label. CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Disarankan agar Anda menyelesaikan semua lab yang tersisa dan kemudian kembali ke tugas ini.

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Word**.  

1. Di bawah Buat baru, pilih **Dokumen kosong**, lalu masukkan beberapa teks di halaman.  Di bagian atas halaman, pilih panah arah bawah, di sebelah tulisan Dokumen - Tersimpan, dan di kotak Nama File masukkan, **Label-uji** lalu tekan **Masuk** pada papan ketik.

1. Dari bilah menu atas, pilih **ikon Sensitivitas**, ikon di sebelah kanan ikon mikrofon (tergantung pada ukuran layar Anda, Anda mungkin perlu memilih elipsis lalu pilih sensitivitas). Dari menu drop-down, pilih **Sangat Rahasia** lalu pilih **Semua Karyawan**.  CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Disarankan agar Anda menyelesaikan semua lab yang tersisa dan kemudian kembali ke tugas ini.

1. Dari bilah menu atas, pilih **View**, lalu pilih **Reading view**.

1. Perhatikan bagaimana dokumen menyertakan footer "Diklasifikasikan sebagai Sangat Rahasia".  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

### Tugas 3 (opsional)

Ingat dari bagian pertama demo bahwa label Sangat Rahasia - Semua Karyawan disiapkan untuk enkripsi. Per izin yang dikonfigurasi dengan label ini, pengguna di penyewa Contoso memiliki izin penampil untuk setiap dokumen/email dengan label yang diterapkan.  Di bagian ini Anda akan mengirim dokumen yang sebelumnya Anda buat, yang menyertakan label Sangat Rahasia - Semua Karyawan, ke alamat email yang dapat Anda akses (alamat email pribadi atau email Microsoft Anda) dan itu BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com.  

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. Pilih **ikon Outlook**.

1. Pilih **Email baru** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Lampirkan** (ikon penklip kertas).

1. Pilih **OneDrive**.

1. Pastikan tab **Terbaru** di panel navigasi kiri dipilih.  Dari daftar yang muncul, pilih dokumen **Test-label.docx** yang Anda buat dan yang Anda terapkan label Sangat Rahasia - Semua Karyawan. Pilih panah drop-down **Bagikan tautan** dan pilih **Lampirkan**.  Tekan **Kirim**.

1. Periksa email yang Anda kirimi dokumen.  Catatan: email dapat diarahkan ke folder sampah Anda.  Email berhasil dikirim tetapi ketika Anda mencoba membuka file kata terlampir, yang awalnya dilabeli sebagai Sangat Rahasia - Semua Karyawan, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen.

1. Tutup Outlook, tetapi tetap buka tab browser ke beranda Microsoft Purview.

### Tinjau

Di lab ini, Anda akan mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang sudah ada yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.
