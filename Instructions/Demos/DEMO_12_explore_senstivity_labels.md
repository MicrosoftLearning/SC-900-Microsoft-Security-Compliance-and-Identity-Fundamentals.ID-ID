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

1. Anda masih harus berada di halaman beranda portal Microsoft Purview. Jika tidak, buka tab browser Microsoft Edge baru. Di bilah alamat, masukkan **https://purview.microsoft.com** lalu pilih **Mulai.**  

1. Dari halaman arahan portal Microsoft Purview baru, pilih **petak Peta Tampilkan semua solusi** , lalu pilih **petak Perlindungan** Informasi. Atau, Anda memilih **Solusi** dari panel navigasi kiri, lalu pilih **Perlindungan** Informasi.

1. Anda akan masuk ke halaman gambaran umum. Dari panel navigasi kiri, pilih **Label** sensitivitas. Jika Anda melihat banner kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**

1. Beberapa label telah dikonfigurasi sebelumnya di penyewa lab Microsoft 365 Anda, untuk memudahkan Anda. Perluas label bernama **Sangat Rahasia**, lalu pilih **Semua Karyawan**.  Jendela terbuka yang menyediakan informasi tentang label ini.  Perhatikan pengaturan untuk label ini.  Pilih **Edit label** Jika Anda tidak melihat opsi ini, pilih elipsis.
    1. Konfigurasi dimulai dengan memberikan detail dasar untuk label.  Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau cakupan untuk label ini. Jangan mengubah apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Layar berikutnya adalah tempat Anda dapat memilih pengaturan perlindungan untuk item berlabel. Label ini mengontrol siapa yang dapat mengakses dan melihat item berlabel dan juga menerapkan penandaan konten.  Pilih **Berikutnya** untuk melihat detailnya.
        1. Kontrol akses: Tinjau pengaturan, tetapi jangan ubah apa pun.  Pilih **Selanjutnya**.
        1. Penandaan konten: Perhatikan bahwa label menerapkan footer.  lalu, pilih **Berikutnya**.
        1. Pelabelan otomatis untuk file dan email: Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis saat nomor kartu kredit terdeteksi. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tentukan pengaturan perlindungan untuk grup dan situs: Tinjau opsi untuk pengaturan perlindungan dan terapkan pengaturan otomatis.  Tidak ada yang telah dikonfigurasi di jendela ini.  Jangan mengubah apapun. Pilih **Berikutnya** di bagian bawah laman.
    1. Tinjau pengaturan Anda dan selesai: Tinjau pengaturan Anda.  Karena tidak ada yang diubah, pilih **Batalkan**.

1. Dari panel navigasi kiri, perluas **Kebijakan** lalu pilih **Kebijakan** penerbitan label.  Label sensitivitas dapat diterbitkan melalui kebijakan label.  Penyewa Microsoft 365 telah dikonfigurasi dengan beberapa kebijakan label, demi kemudahan Anda. Pilih **Kebijakan** Sangat Rahasia.  Jendela yang terbuka menyediakan informasi tentang pembuatan kebijakan. Pilih **Edit kebijakan** dari bagian atas laman.  Di sini, Anda akan membahas pengaturan tanpa mengubah apa pun.
    1. Pilih label sensitivitas untuk diterbitkan: Perhatikan label yang tercantum.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Tetapkan unit admin: Unit Admin diatur ke direktori lengkap, jangan ubah pengaturan apa pun. Pilih **Selanjutnya**.  
    1. Terbitkan ke pengguna dan grup: Perhatikan label ini tersedia untuk semua pengguna.  Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Pengaturan kebijakan: Perhatikan opsi yang tersedia. Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Pengaturan default untuk dokumen: Jangan ubah pengaturan apa pun.  Pilih **Berikutnya** di bagian bawah laman.
    1. Pengaturan default untuk email: Tinjau opsi dan perhatikan bahwa email dapat mewarisi label dari lampiran dengan prioritas yang lebih tinggi, jika dikonfigurasi ke dalamnya. Pilih **Selanjutnya**.
    1. Pengaturan default untuk rapat dan acara kalender: Tinjau opsi dan perhatikan opsi untuk menerapkan pewarisan antara rapat Tim dan artefak. Jangan ubah pengaturan apa pun.  Pilih **Selanjutnya**.
    1. Pengaturan default untuk konten Fabric dan Power BI: Jangan ubah pengaturan apa pun.  Pilih **Selanjutnya**.
    1. Beri nama kebijakan Anda: Karena Anda mengedit kebijakan, bidang nama berwarna abu-abu.  Pilih **Berikutnya**.
    1. Tinjau dan selesai: Karena tidak ada yang diubah, pilih **Batalkan**.

1. Dari panel navigasi kiri, di bawah Perlindungan informasi, pilih Pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Jika ada kebijakan pelabelan otomatis yang dikonfigurasi, pilih salah satu dan tinjau informasi kebijakan di panel detail.  Jika tidak ada kebijakan yang tercantum, Anda dapat memilih untuk menelusuri langkah-langkah untuk membuatnya, jika waktu memungkinkan.

1. Dari panel navigasi kiri, pilih Beranda untuk kembali ke portal Microsoft Purview.

1. Tetap buka tab browser ini.

### Demo Bagian 2

Dalam langkah ini, Anda akan melalui proses penerapan label sensitivitas ke dokumen Microsoft Word lalu menampilkan penandaan konten (footer) yang dihasilkan oleh label. CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Sebaiiknya Anda menyelesaikan semua lab yang tersisa, lalu kembali ke tugas ini.

1. Anda masih harus berada di beranda untuk Portal Microsoft Purview. 
1. Dari portal Microsoft Purview, pilih **ikon** peluncur aplikasi, di samping tempatnya tertulis Microsoft Purview. Pilih **ikon Word**.  

1. Buat Pilih **Dokumen kosong**, lalu masukkan beberapa teks di laman tersebut.  Di bagian atas halaman, di samping ikon Word, pilih di mana katanya **Dokumen** dan ganti nama file menjadi **Test-label** lalu tekan **Enter** di keyboard Anda.

1. Di ujung kanan bilah menu atas (juga disebut sebagai pita) adalah panah bawah, pilih, lalu pilih **Pita Klasik**.  Ini akan mempermudah identitas ikon sensitivitas. Pilih **Sensitivitas**, yang terletak di samping ikon mikrofon. Dari menu drop-down, pilih **Sangat Rahasia** lalu pilih **Semua Karyawan**.  

1. Dari bilah menu atas, pilih **Tampilan**, lalu pilih **Tampilan baca**.

1. Perhatikan bagaimana dokumen menyertakan footer, "Diklasifikasikan sebagai Sangat Rahasia".  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word, tetapi tetap buka tab browser ke beranda Microsoft Purview.

### Tinjauan

Dalam demo ini, Anda telah menunjukkan pengaturan yang dapat dikonfigurasi untuk label sensitivitas dan pengaturan kebijakan untuk menerbitkan label sensitivitas. Anda juga telah menunjukkan cara menerapkan label.
