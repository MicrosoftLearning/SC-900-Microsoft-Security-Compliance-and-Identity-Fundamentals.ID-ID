---
lab:
  title: Menjelajahi label sensitivitas di Microsoft Purview
  module: Describe the data security solutions of Microsoft Purview
---

# Lab: Menjelajahi label sensitivitas di Microsoft Purview

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan solusi keamanan data Microsoft Purview
- Unit: Menjelaskan label dan kebijakan sensitivitas dalam Perlindungan Informasi Microsoft Purview

## Skenario lab

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda akan membahas pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian, Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.

**Perkiraan Waktu**: 45 menit

### Tugas 1

Dalam tugas ini, Anda akan mendapatkan pemahaman tentang apa yang dapat dilakukan label sensitivitas dengan melalui proses pembuatan label baru dan membuat kebijakan untuk menerbitkan label.

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **`https://admin.microsoft.com`**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Microsoft Purview**.  Halaman browser baru terbuka ke halaman selamat datang portal Microsoft Purview.

1. Di panel navigasi kiri, pilih **Solusi** lalu pilih **Perlindungan** informasi.  Anda berada di halaman gambaran umum. Gulir ke bawah untuk melihat informasi yang tersedia.

1. Dari panel navigasi kiri, pilih **Label** sensitivitas.
1. Anda akan melihat banner kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang menerapkan label sensitivitas terenkripsi dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.

1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk memudahkan Anda. Pilih label bernama **Confidential-Finance**.  Jendela terbuka yang menyediakan informasi tentang label ini.  Perhatikan pengaturan untuk label ini.  Pilih **Edit label** Jika Anda tidak melihat opsi ini, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan detail dasar untuk label.  Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau cakupan untuk label ini. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Label ini dikonfigurasi untuk mendukung penandaan konten. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
        1. Pada laman penandaan konten, catat kotak informasi di bagian atas laman.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Sekarang, Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas laman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis bagi kondisi tertentu. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Jendela ini menentukan pengaturan perlindungan untuk grup dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Berikutnya** di bagian bawah laman.
    1. Jendela terakhir ini adalah tempat Anda dapat meninjau pengaturan dan menyelesaikannya. Pilih **Batal** di bagian bawah laman untuk keluar dari wizard konfigurasi label dan kembali ke laman Perlindungan Informasi.

1. Dari panel navigasi kiri, perluas **Kebijakan** lalu pilih **Kebijakan** penerbitan label.  Label sensitivitas dapat diterbitkan melalui kebijakan label.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kemudahan Anda.

1. Pilih **Kebijakan Confidential-Finance**.  Jendela yang terbuka menyediakan informasi tentang pembuatan kebijakan. Pilih **Edit kebijakan** dari bagian atas laman.  Di sini, Anda akan membahas pengaturan tanpa mengubah apa pun.
    1. Tinjau deskripsi untuk "Pilih label sensitivitas untuk diterbitkan".  Perhatikan label yang tercantum.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Tetapkan unit admin". Unit Admin diatur ke direktori lengkap, jangan mengubah pengaturan apa pun. Pilih **Selanjutnya**.  
    1. Tinjau deskripsi untuk "Terbitkan ke pengguna dan grup".  Perhatikan bahwa label ini tersedia untuk semua pengguna.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau pengaturan kebijakan. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi, "Terapkan label default ke dokumen." Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default ke email" dan "Warisi label dari lampiran". Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default ke rapat dan peristiwa kalender." Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default untuk konten Fabric dan Power BI". Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Karena Anda sedang mengedit kebijakan, kolom nama berwarna abu-abu. Pilih **Berikutnya** di bagian bawah halaman.
    1. Tinjau pengaturan kebijakan. Pilih **Batal** untuk membuang perubahan apa pun dan kembali ke laman Kebijakan label.

1. Dari panel navigasi kiri, di bawah Perlindungan informasi, pilih **Kebijakan** pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Tidak ada kebijakan label otomatis yang telah dikonfigurasi sebelumnya di penyewa kita. Untuk membuat kebijakan label otomatis baru, pilih **Buat kebijakan label otomatis**.  Di sini, Anda akan mempelajari langkah-langkah untuk membuat kebijakan baru.
    1. Anda mulai dengan memilih informasi yang Anda inginkan untuk diterapkan label ini.  Perhatikan opsi yang tersedia.  Pilih **Medis dan kesehatan** lalu pilih salah satu peraturan yang tersedia yang akan berfungsi sebagai templat.  Pilih **Selanjutnya**.
    1. Anda dapat memberi nama kebijakan label otomatis atau menggunakan nama default.  Pilih **Selanjutnya**.
    1. Selanjutnya Anda memilih label untuk diterapkan secara otomatis.  Pilih **+ Pilih label**.  Pilih label dari daftar, lalu pilih **Tambahkan**.
    1. Anda dapat menetapkan unit admin tempat kebijakan ini berlaku.  Biarkan pengaturan default pada seluruh direktori dan pilih **Berikutnya**.
    1. Perhatikan lokasi yang tersedia tempat Anda ingin menerapkan label. Pilih kotak di samping **Email** Exchange dan pilih **Berikutnya**.
    1. Anda dapat menyiapkan aturan umum atau tingkat lanjut yang menentukan konten tempat label diterapkan.  Biarkan pengaturan default pada Aturan umum dan pilih **Berikutnya**.
    1. Anda dapat menentukan aturan untuk konten di semua lokasi.  Label akan diterapkan ke konten yang cocok dengan aturan yang ditentukan di laman ini.  Untuk templat yang Anda pilih, Anda akan melihat item baris. Bentangkan untuk melihat kondisi yang berlaku.  Biarkan pengaturan default dan pilih **Berikutnya**.
    1. Pengaturan tambahan dapat dikonfigurasi untuk email. Biarkan default dan pilih **Berikutnya**.
    1. Anda dapat memutuskan untuk menguji kebijakan sekarang atau nanti.  Pilih **Biarkan kebijakan dinonaktifkan**, lalu pilih **Berikutnya**.
    1. Tinjau pengaturan. Untuk tujuan latihan ini, Anda dapat membatalkan dengan membuat kebijakan. Pilih **Batalkan**.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke portal Microsoft Purview.

1. Biarkan laman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda akan melalui proses penerapan label sensitivitas ke dokumen Microsoft Word, lalu menampilkan penandaan konten (marka air) yang dihasilkan oleh label. CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Sebaiiknya Anda menyelesaikan semua lab yang tersisa, lalu kembali ke tugas ini.

1. Anda masih harus berada di beranda untuk Portal Microsoft Purview. 
1. Dari portal Microsoft Purview, pilih **ikon** peluncur aplikasi, di samping tempatnya tertulis Microsoft Purview. Pilih **ikon Word**.  

1. Buat Pilih **Dokumen kosong**, lalu masukkan beberapa teks di laman tersebut.  Di bagian atas halaman, di samping ikon Word, pilih di mana katanya **Dokumen** dan ganti nama file menjadi **Test-label** lalu tekan **Enter** di keyboard Anda.

1. Di ujung kanan bilah menu atas (juga disebut sebagai pita) adalah panah bawah, pilih, lalu pilih **Pita Klasik**.  Ini akan mempermudah identitas ikon sensitivitas. Pilih **Sensitivitas**, yang terletak di samping ikon mikrofon. Dari menu drop-down, pilih **Confidential-Finance**.  

1. Dari bilah menu atas, pilih **Tampilan**, lalu pilih **Tampilan baca**.

1. Perhatikan bahwa dokumen menyertakan marka air-Confidential FINANCIAL DATA..  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word, tetapi tetap buka tab browser ke beranda Microsoft Purview.

### Tinjauan

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda telah mempelajari pengaturan label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label.
