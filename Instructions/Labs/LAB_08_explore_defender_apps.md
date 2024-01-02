<!---
---
Lab: Judul: 'Menjelajahi Microsoft Defender untuk Cloud Apps' Modul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 4: Menjelaskan kemampuan perlindungan terhadap ancaman di Microsoft 365; Unit 5: Menjelaskan Microsoft Defender untuk Cloud Apps'
---
--->

# Lab: Menjelajahi Microsoft Defender untuk Cloud Apps

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan perlindungan terhadap ancaman di Microsoft 365
- Pelajaran: Menjelaskan Microsoft Defender untuk Cloud Apps

## Skenario laboratorium

Di lab ini, Anda akan mempelajari kemampuan Microsoft Defender untuk Cloud Apps.  Anda akan mempelajari informasi yang tersedia di dasbor Cloud Discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan, dan cara mengontrol dampak terhadap organisasi Anda melalui kebijakan. Catatan: Organisasi harus memiliki lisensi untuk menggunakan Microsoft Defender untuk Cloud Apps yang merupakan layanan langganan berbasis pengguna.

**Perkiraan Waktu**: 15-20 menit

### Tugas 1 - Menjelajahi Cloud discovery

Menjelajahi Cloud Discovery.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda untuk penyewa Microsoft 365.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab Anda) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**. Ini akan membawa Anda ke laman pusat admin Microsoft 365.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Keamanan**.  Laman browser baru membuka laman selamat datang di portal Pertahanan Microsoft 365.  

1. Jika ini pertama kalinya Anda mengunjungi portal Pertahanan Microsoft 365, Anda mungkin mendapatkan jendela pop-up untuk mengikuti tur cepat.  Tutup ini.

1. Dari panel navigasi kiri, pilih **Cloud apps** untuk meluaskan daftar, lalu pilih **Cloud Discovery**. Tindakan ini akan membawa Anda ke tampilan Dasbor.  Catat informasi yang tersedia di dasbor. Dari tampilan dasbor, Anda dapat memilih berbagai tab dari bagian atas halaman.  

1. Pilih **Aplikasi yang ditemukan**. Jendela aplikasi yang ditemukan menyediakan tampilan aplikasi yang ditemukan lebih terperinci, termasuk skor risiko, lalu lintas, jumlah pengguna, dan banyak lagi.
    1. Dari item apa pun dalam daftar, pilih **elipsis** di kolom tindakan tabel.  Perhatikan berbagai opsi yang tersedia, termasuk kemampuan untuk menandai aplikasi sebagai disetujui atau tidak disanksi.  Pilih **elipsis**, sekali lagi, untuk menutup kotak tindakan.
    1. Memilih item baris tertentu akan membuka laman detail untuk aplikasi tertentu.  Pilih item dari daftar dan tinjau informasi yang tersedia di laman ikhtisar.  Untuk item yang dipilih, pilih tab **Penggunaan aplikasi cloud** untuk melihat informasi selengkapnya, termasuk **Penggunaan**, **Pengguna, IP**, **Alamat**, dan **Peringatan**. Setelah selesai menjelajahi laman detail, kembali ke laman aplikasi yang ditemukan, dengan memilih **Cloud Discovery** dari bilah di bagian atas laman.  Jika memilih Cloud discovery dari panel navigasi kiri, Anda akan dibawa kembali ke tampilan dasbor.
    1. Dari bagian atas halaman, pilih tab **Alamat IP**. Di sini, Anda akan menemukan data termasuk jumlah transaksi, jumlah lalu lintas, dan jumlah unggahan berdasarkan alamat IP.  Perhatikan bahwa Anda juga dapat memfilter menurut alamat IP tertentu atau mengekspor data untuk analisis lebih lanjut.
    1. Dari bagian atas halaman, pilih **Pengguna**.  Ini adalah jenis informasi yang sama yang diberikan saat Anda memilih alamat IP, tetapi terdaftar untuk masing-masing pengguna.  Di sini juga, Anda memfilter menurut pengguna tertentu dan mengekspor data untuk analisis lebih lanjut.

1. Informasi yang diberikan di laman Cloud Discovery dan tab terkait didasarkan pada laporan cuplikan dari log lalu lintas yang Anda unggah secara manual dari firewall dan proksi atau laporan berkelanjutan yang menganalisis semua log yang diteruskan dari jaringan Anda menggunakan Cloud App Security.  Untuk melihat tempat informasi ini disiapkan, pilih **Tindakan** di pojok kanan atas laman.
    1. Pilih opsi pertama, **Buat laporan snapshot Cloud Discovery**, lalu pilih **Berikutnya**. Di sini, Anda akan mengisi detail yang diminta dan mengunggah log lalu lintas untuk membuat dan mengunggah laporan.  Pilih **Keluar** dan jika diminta dengan Apakah Anda yakin, pilih **Keluar** lagi.  Data yang ditampilkan untuk penyewa lab Anda berasal dari laporan Snapshot, Anda dapat melihat informasi ini di bagian atas jendela Cloud Discovery.
    1. Untuk melihat opsi laporan berkelanjutan, pilih **Tindakan** di pojok kanan atas laman dan dari menu menurun, pilih **Konfigurasikan unggahan otomatis**.  Tidak ada sumber data yang tersambung, tetapi di sinilah Anda akan menambahkan sumber data. Pilih **Tambahkan sumber data**, lalu pilih panah menu dropdown di bidang **Pilih alat** untuk melihat jenis alat yang dapat Anda sambungkan sebagai sumber data.  Pilih **Batal** untuk keluar,
    1. Dari panel navigasi kiri, pilih **Cloud discovery** untuk kembali ke laman Cloud discovery.

1. Anda dapat terhubung ke aplikasi secara langsung dengan menyiapkan konektor aplikasi yang akan memberi visibilitas dan kontrol lebih besar atas aplikasi cloud Anda. Dari pojok kanan atas layar, pilih **Tindakan**, lalu pilih **Pengaturan Cloud Discovery**.  Dari sisi kiri layar, di bagian Aplikasi yang terhubung, pilih **Konektor aplikasi**.  

    1. Pada laman Aplikasi yang terhubung, pilih **Office 365** dari daftar untuk menampilkan informasi terperinci yang tersedia, lalu pilih elipsis vertikal di sisi kanan layar dan pilih **Tampilkan pengaturan Konektor aplikasi** untuk kembali ke laman Konektor aplikasi. Jika Office 365 menampilkan kesalahan koneksi, kemungkinan besar karena Audit tidak diaktifkan.  Jika audit diaktifkan, buka elipsis vertikal di sisi kanan item baris, lalu pilih **Edit pengaturan**.  Untuk menghubungkan kembali, pilih **Hubungkan Office 365** di bagian bawah laman. Laman seharusnya sekarang menunjukkan bahwa Office 365 terhubung. Pilih **Selesai**.  Sekarang status akan ditampilkan dengan tanda peringatan kuning, menunjukkan tidak ada status terbaru.  Perlu beberapa waktu untuk memperbarui status karena periode waktu pemindaian retroaktif berbeda untuk setiap aplikasi dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya.

    1. Sekarang Anda akan menyiapkan konektor aplikasi baru. Pilih **+Hubungkan aplikasi** dan dari daftar menurun, pilih **Microsoft Azure**.  Dari jendela pop-up Microsoft Azure, pilih **Hubungkan Microsoft Azure**, lalu pilih **Selesai**.  Anda akan melihat status terhubung (jika tidak melihatnya, refresh browser). Pilih **Microsoft Azure** untuk melihat informasi terperinci tentang memindai pengguna, data, dan aktivitas.  Kembali ke dasbor Cloud Discovery dengan memilih **Cloud Discovery** di bagian Cloud Apps dari panel navigasi paling kiri.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2 - Menjelajahi katalog aplikasi Cloud

Cloud Discovery menganalisis log lalu lintas Anda berdasarkan katalog aplikasi cloud Microsoft Defender untuk Cloud Apps yang berisi lebih dari 31.000 aplikasi cloud. Aplikasi diberi peringkat dan skor berdasarkan lebih dari 80 faktor risiko untuk memberi Anda visibilitas berkelanjutan ke penggunaan cloud, Shadow IT, dan risiko yang ditimbulkan Shadow IT bagi organisasi Anda.  Dalam tugas ini, Anda akan mempelajari kemampuan katalog aplikasi Cloud.

1. Dari panel navigasi kiri, pilih **Katalog aplikasi cloud**.

1. Katalog aplikasi Cloud memungkinkan Anda memilih aplikasi yang sesuai dengan persyaratan keamanan organisasi Anda. Admin dapat melakukan pemfilteran dasar pada aplikasi seperti yang ditampilkan di bagian atas laman, yang mencakup apakah aplikasi diberi sanksi, tidak diberi sanksi, atau tidak memiliki tag, skor risiko, faktor risiko Kepatuhan, dan faktor risiko keamanan.  Misalnya, pemfilteran berdasarkan faktor risiko kepatuhan memungkinkan Anda menelusuri standar, sertifikasi, dan kepatuhan tertentu yang mungkin dipatuhi oleh aplikasi. Contohnya termasuk HIPAA, ISO 27001, SOC 2, dan PCI-DSS. Pilih **Faktor risiko kepatuhan** untuk melihat opsi yang tersedia.  Anda dapat memfilter lebih lanjut berdasarkan skor risiko, dengan menggerakkan penggeser pada skor risiko di bagian atas laman. Jika Anda memindahkan slide, pastikan sudah mengaturnya sehingga rentangnya diatur dari 0 hingga 10.

1. Admin juga dapat mencari aplikasi berdasarkan kategori.  Misalnya, pada kolom pencarian kategori, masukkan **Jejaring sosial**, lalu pilih **Jejaring sosial**.  Pilih item apa pun dari daftar untuk tampilan terperinci.  Mengarahkan mouse Anda ke topik apa pun untuk kategori tertentu akan menampilkan ikon informasi yang dapat Anda pilih untuk mendapatkan informasi lebih lanjut tentang topik tersebut.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 3 - Menjelajahi log Aktivitas dan File

Menjelajahi cara-cara menyelidiki aktivitas yang direkam dengan log aktivitas dan file.

1. Dari panel navigasi kiri, pilih **Log Aktivitas**. Di sini, Anda mendapatkan visibilitas ke semua aktivitas dari aplikasi yang terhubung. Anda mungkin tidak melihat data apa pun yang tercantum karena memerlukan waktu beberapa jam untuk melakukan pemindaian retroaktif setelah audit diaktifkan dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya. Perhatikan opsi filter yang tersedia dan opsi untuk membuat kebijakan baru dari pencarian.

1. Untuk memberikan perlindungan data, Microsoft Defender untuk Cloud Apps memberi Anda visibilitas ke semua file dari aplikasi yang terhubung, misalnya, semua file yang disimpan di SharePoint dan Salesforce. Dari panel navigasi kiri, pilih dan jelajahi opsi **File**.
    1. Kemampuan untuk memindai file harus diaktifkan sebagai bagian dari Pengaturan perlindungan informasi aplikasi Microsoft 365 Cloud.  Pilih **Aktifkan pemantauan file** dan pilih kotak di samping tempat yang bertuliskan **Aktifkan pemantauan file**, lalu pilih **Simpan**.  
    1. Kembali ke file dengan memilih **File**, tercantum di bagian aplikasi cloud, dari panel navigasi kiri. Seperti yang disebutkan, perlu beberapa hari agar file ditampilkan, setelah pemantauan file diaktifkan, perlu dicatat bahwa setelah file dicantumkan, Anda dapat memfilter data menurut aplikasi, pemilik, tingkat akses, jenis file, dan kebijakan yang cocok. Juga, Anda membuat kebijakan baru dari penelusuran dan ekspor data.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 4 - Menjelajahi Kebijakan

Dalam tugas ini, Anda akan mempelajari kebijakan di Microsoft Defender untuk Cloud Apps.

1. Dari panel navigasi kiri, pilih **Kebijakan** lalu pilih **Manajemen kebijakan**.  Kebijakan yang tercantum memberikan informasi tentang jumlah pemberitahuan yang dihasilkan oleh kebijakan, tingkat keparahan, dll. Memilih item baris apa pun memberikan informasi lebih terperinci tentang kebijakan tersebut.
    1. Perhatikan bahwa Anda juga dapat membuat kebijakan. Pilih **+ Buat kebijakan** untuk melihat jenis kebijakan yang dapat Anda buat.  Pilih **Kebijakan aktivitas** untuk melihat berbagai opsi yang tersedia untuk membuat kebijakan.  Pilih **Batalkan** untuk keluar dari jendela konfigurasi.
    1. Perhatikan bahwa Anda juga dapat memiliki opsi untuk mengekspor informasi kebijakan.

1. Dari panel navigasi kiri, pilih **Template kebijakan**. Untuk membuat kebijakan dari salah satu template yang tersedia, pilih **+** di sebelah kiri item baris template.  Lihat berbagai opsi konfigurasi untuk kebijakan.  Pilih **Batalkan** untuk keluar dari laman.

1. Tutup jendela browser.

### Tinjauan

Di lab ini, Anda telah mempelajari kemampuan Microsoft Defender untuk Cloud Apps.  Anda telah mempelajari informasi yang tersedia di dasbor Cloud Discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan, dan cara mengontrol dampak terhadap organisasi Anda melalui kebijakan.
