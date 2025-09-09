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

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda akan membahas pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan terkait untuk menerbitkan label. Kemudian, Anda akan melihat cara menerapkan label dan dampak label tersebut, dari sudut pandang pengguna.

**Perkiraan Waktu**: 45 menit

### Tugas 1

Dalam tugas ini, Anda akan mendapatkan pemahaman tentang apa yang dapat dilakukan label sensitivitas dengan melalui proses pembuatan label baru dan membuat kebijakan untuk menerbitkan label.

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **`https://admin.microsoft.com`**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Microsoft Purview**.  Halaman browser baru terbuka ke halaman selamat datang portal Microsoft Purview.

1. Di panel navigasi kiri, pilih **Solusi** lalu pilih **Perlindungan** informasi.  Anda berada di halaman gambaran umum. Gulir ke bawah untuk melihat informasi yang tersedia.

1. Dari panel navigasi kiri, pilih **Label** sensitivitas.
1. Anda akan melihat banner kuning yang menunjukkan bahwa organisasi Anda belum mengaktifkan kemampuan untuk memproses konten dalam file online Office yang menerapkan label sensitivitas terenkripsi dan disimpan di OneDrive dan SharePoint.  Pilih **Aktifkan sekarang**.

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
    1. Pengaturan default untuk rapat dan acara kalender: Tinjau opsi dan perhatikan opsi untuk menerapkan pewarisan antara rapat Teasm dan artefak. Jangan ubah pengaturan apa pun.  Pilih **Selanjutnya**.
    1. Pengaturan default untuk konten Fabric dan Power BI: Jangan ubah pengaturan apa pun.  Pilih **Selanjutnya**.
    1. Beri nama kebijakan Anda: Karena Anda mengedit kebijakan, bidang nama berwarna abu-abu.  Pilih **Berikutnya**.
    1. Tinjau dan selesai: Karena tidak ada yang diubah, pilih **Batalkan**.

1. Dari panel navigasi kiri, di bawah Perlindungan informasi, pilih **Kebijakan** pelabelan otomatis. Tinjau deskripsi. Perhatikan bahwa Anda membuat kebijakan pelabelan otomatis untuk menerapkan label sensitivitas secara otomatis ke pesan email atau file OneDrive dan SharePoint yang berisi info sensitif. Tidak ada kebijakan label otomatis yang telah dikonfigurasi sebelumnya di penyewa kita. Untuk membuat kebijakan label otomatis baru, pilih **Buat kebijakan label otomatis**.  Di sini Anda akan menelusuri langkah-langkah yang terlibat dalam membuat kebijakan baru.
    1. Anda mulai dengan memilih informasi yang Anda inginkan untuk diterapkan label ini.  Perhatikan opsi yang tersedia.  Pilih **Medis dan kesehatan** lalu pilih salah satu peraturan yang tersedia yang akan berfungsi sebagai templat.  Pilih **Selanjutnya**.
    1. Anda dapat memberi nama kebijakan label otomatis atau menggunakan nama default.  Pilih **Selanjutnya**.
    1. Selanjutnya Anda memilih label untuk diterapkan secara otomatis.  Pilih **+ Pilih label**.  Pilih label dari daftar, lalu pilih **Tambahkan**.
    1. Anda dapat menetapkan unit admin tempat kebijakan ini berlaku.  Biarkan pengaturan default pada seluruh direktori dan pilih **Berikutnya**.
    1. Pilih lokasi tempat Anda ingin menerapkan label.  Tinjau informasi yang disediakan dan lokasi yang tersedia yang dapat Anda pilih. Untuk latihan ini, pilih kotak di samping **Email** Exchange lalu pilih **Berikutnya**.
    1. Anda dapat menyiapkan aturan umum atau tingkat lanjut yang menentukan konten tempat label diterapkan.  Biarkan pengaturan default pada Aturan umum dan pilih **Berikutnya**.
    1. Anda dapat menentukan aturan untuk konten di semua lokasi.  Label akan diterapkan ke konten yang cocok dengan aturan yang ditentukan di laman ini.  Untuk templat yang Anda pilih, Anda akan melihat item baris. Bentangkan untuk melihat kondisi yang berlaku.  Biarkan pengaturan default dan pilih **Berikutnya**.
    1. Pengaturan tambahan dapat dikonfigurasi untuk email. Biarkan default dan pilih **Berikutnya**.
    1. Anda dapat memutuskan untuk menguji kebijakan sekarang atau nanti.  Pilih **Biarkan kebijakan dinonaktifkan**, lalu pilih **Berikutnya**.
    1. Tinjau pengaturan. Untuk tujuan latihan ini, Anda dapat membatalkan dengan membuat kebijakan. Pilih **Batalkan**.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke portal Microsoft Purview.

1. Biarkan laman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda akan melalui proses penerapan label sensitivitas ke dokumen Microsoft Word lalu menampilkan penandaan konten (footer) yang dihasilkan oleh label. CATATAN: Saat menggunakan Microsoft Word online, Anda mungkin mengalami penundaan sebelum opsi untuk memilih Label sensitivitas muncul di pita atas.  Sebaiiknya Anda menyelesaikan semua lab yang tersisa, lalu kembali ke tugas ini.

1. Anda masih harus berada di beranda untuk Portal Microsoft Purview. 
1. Dari portal Microsoft Purview, pilih **ikon** peluncur aplikasi, di samping tempatnya tertulis Microsoft Purview. Pilih **ikon Word**.  

1. Buat Pilih **Dokumen kosong**, lalu masukkan beberapa teks di laman tersebut.  Di bagian atas halaman, di samping ikon Word, pilih di mana katanya **Dokumen** dan ganti nama file menjadi **Test-label** lalu tekan **Enter** di keyboard Anda.

1. Di ujung kanan bilah menu atas (juga disebut sebagai pita) adalah panah bawah, pilih, lalu pilih **Pita Klasik**.  Ini akan mempermudah identitas ikon sensitivitas. Pilih **Sensitivitas**, yang terletak di samping ikon mikrofon. Dari menu drop-down, pilih **Sangat Rahasia** lalu pilih **Semua Karyawan**.  

1. Dari bilah menu atas, pilih **Tampilan**, lalu pilih **Tampilan baca**.

1. Perhatikan bagaimana dokumen menyertakan footer, "Diklasifikasikan sebagai Sangat Rahasia".  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word, tetapi tetap buka tab browser ke beranda Microsoft Purview.

### Tinjauan

Di lab ini, Anda mengeksplorasi kemampuan label sensitivitas.  Anda menjelajahi pengaturan untuk label sensitivitas yang ada dan kebijakan terkait untuk menerbitkan label.  Anda menerapkan label dan karena label menyertakan penandaan konten, Anda dapat melihat penandaan tersebut dalam dokumen tempat Anda menerapkan label.
