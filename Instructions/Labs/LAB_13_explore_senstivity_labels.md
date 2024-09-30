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

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**, lalu pilih **Kepatuhan**.  Halaman browser baru terbuka ke halaman selamat datang portal Microsoft Purview.

1. Di panel navigasi kiri, pilih **Solusi** lalu pilih **Perlindungan** informasi.  Anda berada di halaman gambaran umum. Gulir ke bawah untuk melihat informasi yang tersedia.

1. Dari panel navigasi kiri, pilih **Label** sensitivitas.

1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk memudahkan Anda. Pilih label bernama **Confidential-Finance**.  Jendela terbuka yang menyediakan informasi tentang label ini.  Perhatikan pengaturan untuk label ini.  Pilih **Edit label** Jika Anda tidak melihat opsi ini, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan detail dasar untuk label.  Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau cakupan untuk label ini. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Label ini dikonfigurasi untuk mendukung penandaan konten. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
        1. Pada laman penandaan konten, catat kotak informasi di bagian atas laman.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Sekarang, Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas laman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis bagi kondisi tertentu. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Jendela ini menentukan pengaturan perlindungan untuk grup dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Berikutnya** di bagian bawah laman.
    1. Jendela ini adalah fitur pratinjau untuk menerapkan label ini secara otomatis ke aset data skema di Microsoft Purview Data Map (seperti SQL, Synapse, dan lainnya) yang berisi jenis info sensitif yang Anda pilih.  Fitur ini tidak diaktifkan. Pilih **Batal** di bagian bawah laman untuk keluar dari wizard konfigurasi label dan kembali ke laman Perlindungan Informasi.

1. Dari panel navigasi kiri, perluas **Kebijakan** lalu pilih  **Kebijakan** penerbitan.  Label sensitivitas dapat diterbitkan melalui kebijakan label.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kemudahan Anda.

1. Pilih **Kebijakan Confidential-Finance**.  Jendela yang terbuka menyediakan informasi tentang pembuatan kebijakan. Pilih **Edit kebijakan** dari bagian atas laman.  Di sini, Anda akan membahas pengaturan tanpa mengubah apa pun.
    1. Tinjau deskripsi untuk "Pilih label sensitivitas untuk diterbitkan".  Perhatikan label yang tercantum.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Tetapkan unit admin". Unit Admin diatur ke direktori lengkap, jangan mengubah pengaturan apa pun. Pilih **Selanjutnya**.  
    1. Tinjau deskripsi untuk "Terbitkan ke pengguna dan grup".  Perhatikan bahwa label ini tersedia untuk semua pengguna.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau pengaturan kebijakan. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi, "Terapkan label default ke dokumen." Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default ke email" dan "Warisi label dari lampiran". Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default ke rapat dan peristiwa kalender." Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau deskripsi untuk "Terapkan label default ke konten Power BI." Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Karena Anda sedang mengedit kebijakan, kolom nama berwarna abu-abu. Pilih **Berikutnya** di bagian bawah halaman.
    1. Tinjau pengaturan kebijakan. Pilih **Batal** untuk membuang perubahan apa pun dan kembali ke laman Kebijakan label.

1. Dari panel navigasi kiri, di bawah Perlindungan informasi, pilih Pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Tidak ada kebijakan label otomatis yang telah dikonfigurasi sebelumnya di penyewa kita. Untuk membuat kebijakan label otomatis baru, pilih **Buat kebijakan label otomatis**.  Di sini, Anda akan mempelajari langkah-langkah untuk membuat kebijakan baru.
    1. Anda mulai dengan memilih informasi yang Anda inginkan untuk diterapkan label ini.  Perhatikan opsi yang tersedia.  Pilih **Medis dan kesehatan**, lalu pilih salah satu templat yang tersedia.  Pilih **Selanjutnya**.
    1. Anda dapat memberi nama kebijakan label otomatis atau menggunakan nama default.  Pilih **Selanjutnya**.
    1. Anda dapat menetapkan unit admin tempat kebijakan ini berlaku.  Biarkan pengaturan default pada seluruh direktori dan pilih **Berikutnya**.
    1. Perhatikan lokasi yang tersedia tempat Anda ingin menerapkan label.  Biarkan default dan pilih **Berikutnya**.
    1. Anda dapat menyiapkan aturan umum atau tingkat lanjut yang menentukan konten tempat label diterapkan.  Biarkan pengaturan default pada Aturan umum dan pilih **Berikutnya**.
    1. Anda dapat menentukan aturan untuk konten di semua lokasi.  Label akan diterapkan ke konten yang cocok dengan aturan yang ditentukan di laman ini.  Untuk templat yang Anda pilih, Anda akan melihat item baris. Bentangkan untuk melihat kondisi yang berlaku.  Biarkan pengaturan default dan pilih **Berikutnya**.
    1. Pilih label untuk diterapkan secara otomatis dengan memilih **Pilih label**.  Pilih label, lalu pilih **Tambahkan**. Pilih **Selanjutnya**.
    1. Pengaturan tambahan dapat dikonfigurasi untuk email. Biarkan default dan pilih **Berikutnya**.
    1. Anda dapat memutuskan untuk menguji kebijakan sekarang atau nanti.  Pilih **Biarkan kebijakan dinonaktifkan**, lalu pilih **Berikutnya**.
    1. Tinjau pengaturan dan pilih **Buat kebijakan**, lalu pilih **Selesai**.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke portal kepatuhan Microsoft Purview.

1. Biarkan laman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda akan melalui proses penerapan label sensitivitas ke dokumen Microsoft Word, lalu menampilkan penandaan konten (marka air) yang dihasilkan oleh label. CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Sebaiiknya Anda menyelesaikan semua lab yang tersisa, lalu kembali ke tugas ini.

1. Dari laman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping tulisan Contoso Electronics. Pilih **ikon Word**.  

1. Buat Pilih **Dokumen kosong**, lalu masukkan beberapa teks di laman tersebut.  Di bagian atas laman, pilih panah arah bawah, di sebelah tulisan Dokumen - Tersimpan, dan di kotak Nama File masukkan **Test-label**, lalu tekan **Enter** pada papan ketik.

1. Di ujung kanan bilah menu atas (juga disebut sebagai pita) adalah panah bawah, pilih, lalu pilih **Pita Klasik**.  Ini akan mempermudah identitas ikon sensitivitas. Pilih **Sensitivitas**, yang terletak di samping ikon mikrofon. Dari menu drop-down, pilih **Confidential-Finance**.  

1. Dari bilah menu atas, pilih **Tampilan**, lalu pilih **Tampilan baca**.

1. Perhatikan bahwa dokumen menyertakan marka air-Confidential FINANCIAL DATA..  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word, tetapi tetap buka tab browser ke beranda Microsoft Purview.

### Tinjauan

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda telah mempelajari pengaturan label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label.
