<!---
---
Demo: Judul: 'Label sensitivitas di Microsoft Purview' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview; Modul 2:Menjelaskan solusi keamanan data Microsoft Purview; Unit 4: Menjelaskan label dan kebijakan sensitivitas dalam Perlindungan Informasi Microsoft Purview'
---
--->

# Demo: Label sensitivitas di Microsoft Purview

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan solusi keamanan data Microsoft Purview
- Unit: Menjelaskan label dan kebijakan sensitivitas dalam Perlindungan Informasi Microsoft Purview

## Skenario demo

Dalam demo ini, Anda akan menunjukkan kemampuan label sensitivitas.  Anda akan membahas pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label.   Kemudian, Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.  **CATATAN**: Pertama kali Anda menggunakan Word online dengan penyewa Microsoft 365, diperlukan waktu 15 menit agar opsi Sensitivitas muncul pada pita.  Penyaji harus menjalankan demo bagian 2 sebelum kelas untuk memastikan waktu yang diperlukan hingga opsi muncul.

### Demo Bagian 1

Dalam demo ini, Anda menunjukkan pengaturan untuk label sensitivitas yang ada dan kebijakan terkait untuk menerbitkan label.

1. Buka tab browser Microsoft Edge baru. Di bilah alamat, masukkan **https://purview.microsoft.com**. Untuk mengakses portal Microsoft Purview baru, pilih kotak di samping tempat yang tertulis, **saya menyetujui ketentuan pengungkapan aliran data dan Pernyataan** Privasi, lalu pilih **Mulai**.  

1. Dari halaman arahan portal Microsoft Purview baru, pilih **petak Peta Tampilkan semua solusi** , lalu pilih **petak Peta Manajer** Informasi. Atau, Anda memilih **Solusi** dari panel navigasi kiri, lalu pilih **Perlindungan** Informasi.

1. Anda akan masuk ke halaman gambaran umum. Dari panel navigasi kiri, pilih **Label** sensitivitas.

1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk memudahkan Anda. Pilih label bernama **Confidential-Finance**.  Jendela terbuka yang menyediakan informasi tentang label ini.  Perhatikan pengaturan untuk label ini.  Pilih **Edit label** (mungkin juga ditampilkan sebagai ikon pensil) di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar. Jika Anda tidak melihat opsi ini, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau cakupan untuk label ini. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Label ini dikonfigurasi untuk mendukung penandaan konten. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
        1. Pada laman penandaan konten, catat kotak informasi di bagian atas laman.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Sekarang, Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas laman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis bagi kondisi tertentu. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Jendela ini menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Berikutnya** di bagian bawah laman.
    1. Jendela ini adalah fitur pratinjau untuk menerapkan label ini secara otomatis ke aset data skema di Microsoft Purview Data Map (seperti SQL, Synapse, dan lainnya) yang berisi jenis info sensitif yang Anda pilih.  Fitur ini tidak diaktifkan. Pilih **Batal** di bagian bawah laman untuk keluar dari wizard konfigurasi label dan kembali ke laman Perlindungan Informasi.

1. Dari panel navigasi kiri, pilih **Kebijakan** lalu pilih **Kebijakan** penerbitan.  Label sensitivitas dapat diterbitkan melalui kebijakan label.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kemudahan Anda.

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

1. Dari panel navigasi kiri, di bawah Perlindungan informasi, pilih Pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Jika ada kebijakan pelabelan otomatis yang dikonfigurasi, pilih salah satu dan tinjau informasi kebijakan di panel detail.  Jika tidak ada kebijakan yang tercantum, Anda dapat memilih untuk menelusuri langkah-langkah untuk membuatnya, jika waktu memungkinkan.

1. Dari panel navigasi kiri, pilih Beranda untuk kembali ke portal Microsoft Purview.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Pada langkah ini, Anda akan menunjukkan proses penerapan label dari sudut pandang pengguna (dalam hal ini, pengguna adalah admin).  Untuk melihat dampak penerapan label, Anda akan memilih label Rahasia - Keuangan karena label ini menerapkan tanda air.

1. Dari beranda portal kepatuhan Microsoft Purview, pilih **ikon** peluncur aplikasi, di samping tempat bertuliskan Microsoft Purview (di atas ikon beranda). Pilih **ikon Word**.  

1. Pilih **Dokumen** kosong, lalu masukkan beberapa teks di laman tersebut.  Pada bilah wartna biru di bagian atas laman, pilih panah arah bawah, di sebelah tulisan Dokumen - Tersimpan, dan di kotak Nama File masukkan, **Label-uji** lalu tekan tombol **Enter** pada keyboard Anda.

1. Di ujung kanan bilah menu atas (juga disebut sebagai pita) adalah panah bawah, pilih, lalu pilih **Pita Klasik**.  Ini akan mempermudah identitas ikon sensitivitas. Pilih **Sensitivitas**, yang terletak di samping ikon mikrofon. Dari menu drop-down, pilih **Confidential-Finance**.  

1. Dari bilah menu atas, pilih **Tampilan**, lalu pilih **Tampilan baca**.

1. Perhatikan bahwa dokumen menyertakan marka air.  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

1. Biarkan tab browser Microsoft Purview terbuka untuk demo berikutnya.

### Tinjauan

Dalam demo ini, Anda telah menunjukkan pengaturan yang dapat dikonfigurasi untuk label sensitivitas dan pengaturan kebijakan untuk menerbitkan label sensitivitas. Anda juga telah menunjukkan cara menerapkan label.
