---
lab:
  title: Menjelajahi manajemen risiko dari dalam di Microsoft Purview
  module: Describe the data security solutions of Microsoft Purview
---

# Lab: Menjelajahi manajemen risiko dari dalam di Microsoft Purview

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan Microsoft Priva dan Microsoft Purview
- Modul: Menjelaskan solusi keamanan data Microsoft Purview
- Unit: Menjelaskan manajemen risiko orang dalam di Microsoft Purview

## Skenario lab

Di lab ini, Anda akan mempelajari proses penyiapan kebijakan risiko dari dalam, beserta prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.  Catatan: lab ini hanya akan memberikan visibilitas tentang apa yang diperlukan untuk menyiapkan Manajemen risiko dari dalam dan opsi yang terkait dengan pembuatan kebijakan.  Lab ini tidak menyertakan tugas untuk memicu kebijakan, karena jumlah peristiwa yang perlu terjadi untuk memicu kebijakan dan waktu yang diperlukan berada di luar cakupan latihan ini.

**Perkiraan Waktu**: 60 menit

### Tugas 1

Dalam tugas ini, Anda sebagai administrator global akan mengaktifkan izin untuk Manajemen Risiko Dari Dalam.  Khususnya, Anda akan menambahkan pengguna ke grup peran Manajemen Risiko Dari Dalam untuk memastikan bahwa pengguna yang ditunjuk dapat mengakses dan mengelola fitur manajemen risiko dari dalam.  Mungkin perlu waktu hingga 30 menit agar izin grup peran berlaku untuk pengguna di seluruh organisasi.

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda. 

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**, lalu pilih **Kepatuhan**.  Halaman browser baru terbuka ke halaman selamat datang portal Microsoft Purview.  

1. Dari panel navigasi kiri, pilih **Pengaturan**, perluas **Peran & cakupan** lalu pilih **Grup peran**.

1. Di bidang pencarian, di kanan atas halaman, ketik **risiko** Insider lalu tekan Enter di keyboard Anda.  Perhatikan banyak peran yang muncul.  Masing-masing memiliki tingkat akses yang berbeda.  Pilih **Manajemen risiko dari dalam** dan tinjau deskripsinya.  Gulir ke bawah ke tempat yang menunjukkan anggota dan perhatikan bahwa MOD Administrator dan Megan Bowen terdaftar. Tutup jendela dengan memilih **X** di kanan atas jendela.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke halaman portal Microsoft Purview.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan kembali ke sana di tugas selanjutnya.

### Tugas 2

Dalam tugas ini, Anda akan mempelajari pengaturan yang terkait dengan solusi Manajemen Risiko Dari Dalam.  Pengaturan manajemen risiko dari dalam berlaku untuk semua kebijakan manajemen risiko dari dalam, terlepas dari templat yang Anda pilih saat membuat kebijakan.

1. Anda harus berada di beranda portal Microsoft Purview. Jika tidak, buka tab browser **Beranda-Kepatuhan Microsoft 365**.

1. Sebelum mulai menyiapkan kebijakan, ada beberapa pengaturan yang harus dipahami admin dan dikonfigurasi sesuai kebutuhan untuk organisasi mereka. Dari panel navigasi kiri, pilih **Pengaturan** lalu pilih **Manajemen** Risiko Insider.  Di sini Anda akan menjelajahi beberapa pengaturan yang tersedia.
    1. Pilih **Privasi**: bagi pengguna yang melakukan aktivitas yang cocok dengan kebijakan risiko orang dalam Anda, pengaturan ini akan menentukan apakah akan menampilkan nama sebenarnya atau menggunakan versi anonim untuk menutupi identitas mereka.  Untuk keperluan pembelajaran ini, Anda dapat membiarkan pengaturannya diatur ke default.
    1. Pilih **Indikator kebijakan**. Setelah peristiwa pemicu kebijakan terjadi, aktivitas yang memetakan ke indikator yang dipilih digunakan dalam menentukan skor risiko, untuk pengguna. Indikator kebijakan yang dipilih di sini menyertakan templat kebijakan risiko dari dalam.  Gulir untuk melihat semua indikator yang tersedia dan informasi terkait. 
    1. Pilih **Kerangka** waktu kebijakan. Jangka waktu yang Anda pilih di sini berlaku untuk pengguna ketika mereka memicu kecocokan untuk kebijakan risiko orang dalam.   Jendela Aktivasi menentukan berapa lama kebijakan akan secara aktif mendeteksi aktivitas untuk pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan. Deteksi aktivitas terdahulu Menentukan seberapa jauh kebijakan harus terdeteksi aktivitas pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan.  Biarkan nilai default.
    1. Pilih **Deteksi** cerdas. Tinjau opsi di sini.  Perhatikan pengaturan domain dan bagaimana pengaturan tersebut berhubungan dengan indikator.
    1. Jelajahi item lain yang tercantum dalam pengaturan dan perhatikan bahwa banyak item dalam pratinjau.

1. Dari panel navigasi kiri, pilih **Solusi**, lalu pilih **Manajemen** Risiko Insider.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 3

Dalam tugas ini, Anda akan mempelajari pengaturan untuk membuat kebijakan.  Tujuannya hanyalah untuk memahami berbagai opsi dan fleksibilitas yang terkait dengan pembuatan kebijakan.

1. Anda harus berada di halaman gambaran umum untuk manajemen risiko Insider.  Jika belum ada, pilih **Solusi** dari panel navigasi kiri, lalu pilih **Insider Risk Management** .

1. Dari laman ikhtisar manajemen risiko dari dalam, pilih tab **Kebijakan**, lalu pilih **+ Buat kebijakan**.  Konfigurasikan setiap tab kebijakan berikut.

    1. Templat kebijakan: Di bagian kategori Kebocoran data, pilih **Kebocoran data**.  Baca detail yang terkait dengan templat ini. Di bagian prasyarat, kebijakan DLP ditampilkan dengan tanda centang dalam lingkaran hijau untuk menunjukkan bahwa prasyarat telah terpenuhi.  Ada kebijakan DLP yang telah dikonfigurasikan sebelumnya untuk penyewa lab ini. Pilih **Selanjutnya**. 
    1. Nama dan deskripsi: masukkan nama, **SC900-InsiderRiskPolicy**, lalu pilih **Berikutnya**.
    1. Pengguna dan grup: Tinjau kotak informasi.  Biarkan pengaturan default, **Sertakan semua pengguna dan grup**.  Pilih **Selanjutnya**.
    1. Mengecualikan pengguna dan grup (opsional)(pratinjau): Di sini Anda dapat mencantumkan pengguna dan grup untuk dikecualikan. Jangan mengubah apapun. Pilih **Selanjutnya**.
    1. Konten yang akan diprioritaskan: Sesuai deskripsi, Skor risiko ditingkatkan untuk aktivitas apa pun yang berisi konten prioritas, yang pada gilirannya meningkatkan kemungkinan menghasilkan peringatan tingkat keparahan tinggi. Untuk memudahkan, pilih **Saya tidak ingin memprioritaskan konten saat ini**, lalu pilih **Berikutnya**.
    1. Pemicu: Peristiwa pemicu menentukan kapan suatu kebijakan akan mulai menetapkan skor risiko ke aktivitas pengguna.  Anda dapat memilih dari kebijakan DLP yang ada atau jika pengguna melakukan aktivitas eksfiltrasi. Pilih **Pengguna cocok dengan kebijakan pencegahan kehilangan data (DLP)** lalu dari menu menurun, pilih **Data Keuangan AS**. Pilih **Selanjutnya**.
    1. Indikator: Perhatikan indikator yang dipilih. Jangan mengubah apapun. Pilih **Selanjutnya**.
    1. Pada laman Opsi deteksi, biarkan semua pengaturan diatur ke default, tetapi baca deskripsi yang terkait dengan berbagai opsi dan arahkan kursor ke ikon informasi untuk mendapatkan informasi selengkapnya tentang pengaturan tertentu.  Pilih **Selanjutnya**.
    1. Pada halaman untuk Memutuskan apakah akan menggunakan ambang indikator default atau pelanggan, biarkan pengaturan default **Terapkan ambang yang disediakan oleh Microsoft**, lalu pilih **Berikutnya**.
    1. Selesai: tinjau pengaturan, pilih **Kirim**.
    1. Tinjau deskripsi tentang apa yang terjadi selanjutnya, lalu pilih **Selesai**.

1. Anda kembali ke tab Kebijakan di laman Manajemen risiko dari dalam.  Kebijakan yang Anda buat akan dicantumkan.  Jika Anda tidak melihatnya, pilih ikon **Refresh**.

1. Sebagai admin, Anda dapat segera mulai menetapkan skor risiko kepada pengguna berdasarkan aktivitas yang terdeteksi oleh kebijakan yang Anda pilih. Hal ini melewati persyaratan bahwa peristiwa pemicu (seperti kecocokan kebijakan DLP) terdeteksi terlebih dahulu.  Admin akan melakukannya dengan memilih kotak kosong di samping nama kebijakan untuk memilih kebijakan, lalu pilih **Mulai aktivitas penilaian untuk pengguna**, yang ditampilkan di atas tabel kebijakan.  Jendela baru terbuka yang mengharuskan admin mengisi bidang yang tersedia. Kosongkan bidang karena Anda tidak akan mengonfigurasi opsi ini, tetapi untuk informasi selengkapnya tentang mengapa admin ingin melakukan ini, pilih **Mengapa saya melakukan ini??**.  Keluar dari jendela dengan memilih **X** di kanan atas jendela.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke halaman arahan portal Microsoft Purview.

1. Tetap buka tab browser.

### Tinjauan

Di lab ini, Anda telah mempelajari proses penyiapan kebijakan risiko dari dalam, beserta prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.
