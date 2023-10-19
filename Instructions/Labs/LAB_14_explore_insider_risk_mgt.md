<!---
---
Lab: Judul: 'Jelajahi manajemen risiko insider di Microsoft Purview' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 4: Menjelaskan kemampuan risiko orang dalam di Microsoft Purview; Pelajaran 2: Menjelaskan manajemen risiko orang dalam'
---
--->

# Lab: Mempelajari manajemen risiko orang dalam di Microsoft Purview

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan kemampuan risiko dari dalam di Microsoft Purview
- Pelajaran: Menjelaskan Manajemen Risiko Dari Dalam

## Skenario lab

Di lab ini, Anda akan menjalani proses penyiapan kebijakan risiko dari dalam, beserta prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.  Catatan: lab ini hanya akan memberikan visibilitas tentang apa yang diperlukan untuk menyiapkan manajemen risiko Insider dan opsi yang terkait dengan pembuatan kebijakan.  Lab ini tidak menyertakan tugas untuk memicu kebijakan, karena jumlah peristiwa yang perlu terjadi untuk memicu kebijakan dan waktu yang diperlukan berada di luar cakupan latihan ini.

**Perkiraan Waktu**: 45-60 menit

### Tugas 1

Dalam tugas ini, Anda sebagai administrator global akan mengaktifkan izin untuk Manajemen Risiko Dari Dalam.  Khususnya, Anda akan menambahkan pengguna ke grup peran Manajemen Risiko Dari Dalam untuk memastikan bahwa pengguna yang ditunjuk dapat mengakses dan mengelola fitur manajemen risiko dari dalam.  Mungkin diperlukan waktu hingga 30 menit agar izin grup peran diterapkan ke pengguna di seluruh organisasi.

1. Buka tab browser untuk beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH). Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua** lalu pilih **Kepatuhan**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi kiri, perluas **Peran & cakupan** lalu pilih **Izin**.

1. Di bawah Solusi Microsoft Purview, pilih **Peran**.

1. Di bidang pencarian ketik **risiko Insider** lalu tekan Enter di keyboard Anda.  Perhatikan banyak peran yang muncul.  Masing-masing memiliki tingkat akses yang berbeda.  Pilih **Manajemen risiko dari dalam** dan tinjau deskripsinya.  Gulir ke bawah ke tempat yang menunjukkan anggota dan catat bahwa MOD Administrator dan Megan Bowen terdaftar. Tutup jendela dengan memilih di **X** di kanan atas jendela..

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke halaman portal kepatuhan Microsoft Purview.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan kembali ke sana di tugas selanjutnya.

### Tugas 2 (CATATAN: LEWATI Tugas 2 jika Anda melakukan tugas lab penyiapan untuk mengaktifkan log audit.)

Manajemen risiko dari dalam menggunakan log audit Microsoft 365 untuk wawasan dan aktivitas pengguna yang diidentifikasi dalam kebijakan dan wawasan analitik. Dalam tugas ini, Anda akan mengaktifkan kemampuan pencarian log Audit. Catatan:  Mungkin diperlukan waktu beberapa jam setelah mengaktifkan pencarian log audit sebelum Anda dapat mengembalikan hasil saat mencari log audit.  Meskipun perlu beberapa jam sebelum Anda dapat menelusuri log audit, hal itu tidak akan memengaruhi kemampuan untuk menyelesaikan tugas lain di lab ini.

1. Pilih tab browser berlabel, **Beranda-Kepatuhan Microsoft 365**.  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge, dan di bilah alamat masukkan **compliance.microsoft.com** dan masuk dengan kredensial admin Anda.

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.

1. Pastikan tab **Pencarian Baru** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas halaman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.

1. Kembali ke beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi sebelah kiri.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 3

Dalam tugas ini, Anda akan menelusuri pengaturan yang terkait dengan solusi Manajemen Risiko Dari Dalam.  Pengaturan manajemen risiko dari dalam berlaku untuk semua kebijakan manajemen risiko dari dalam, terlepas dari templat yang Anda pilih saat membuat kebijakan.

1. Anda akan diarahkan ke halaman beranda portal kepatuhan Microsoft Purview. Jika tidak, Buka tab browser **Home - Microsoft 365 compliance**.

1. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **Insider risk management**.

1. Sebelum mulai menyiapkan kebijakan, ada beberapa pengaturan yang harus dipahami dan dikonfigurasi oleh admin sesuai kebutuhan untuk organisasinya. Dari halaman Manajemen Risiko Dari Dalam, pilih **ikon roda gigi pengaturan** di pojok kanan atas jendela manajemen risiko Dari Dalam untuk mengakses pengaturan Risiko Dari Dalam.  
    1. Pastikan Anda berada di tab **Privasi**: untuk pengguna yang melakukan aktivitas yang cocok dengan kebijakan risiko insider Anda, pengaturan ini akan menentukan apakah akan menampilkan nama mereka yang sebenarnya atau menggunakan versi anonim untuk menutupi identitas mereka.  Untuk keperluan penelusuran ini, Anda dapat membiarkan pengaturannya diatur ke default.
    1. Pilih tab **Indikator kebijakan**. Setelah peristiwa pemicu kebijakan terjadi, aktivitas yang dipetakan ke indikator yang dipilih akan digunakan dalam menentukan skor risiko, bagi pengguna. Indikator kebijakan yang dipilih di sini termasuk templat kebijakan risiko Dari Dalam.  Gulir untuk melihat semua indikator yang tersedia dan informasi terkait lainnya. Di bagian **Indikator kantor**, pilih **Pilih semua**, lalu pilih **Simpan** di bagian bawah halaman (Anda harus menggulir ke bawah).
    1. Pilih tab **Policy timeframes**. Kerangka waktu yang Anda pilih di sini berlaku pada pengguna saat memicu kecocokan untuk kebijakan risiko dari dalam.   Jendela Aktivasi menentukan berapa lama kebijakan akan secara aktif mendeteksi aktivitas untuk pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan. Deteksi aktivitas sebelumnya Menentukan seberapa jauh ke belakang kebijakan untuk mendeteksi aktivitas pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan.  Biarkan nilai tetapi default.
    1. Pilih tab **Intelligent detections**. Tinjau opsi di sini.  Perhatikan pengaturan domain dan bagaimana hubungannya dengan indikator.
    1. Jelajahi item lain yang tercantum dalam pengaturan dan perhatikan bahwa banyak item dalam pratinjau.

1. Untuk kembali ke ringkasan Manajemen risiko dari dalam, pilih **Insider risk management** dari sudut kiri atas halaman, di atas teks Pengaturan.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 4

Dalam tugas ini, Anda akan mempelajari pengaturan untuk membuat kebijakan.  Tujuannya hanyalah untuk memahami berbagai opsi dan fleksibilitas yang terkait dengan pembuatan kebijakan.

1. Anda seyogianya berada di halaman Manajemen risiko dari dalam.  Jika belum ada, buka tab browser berlabel, **Insider risk management - Microsoft 365 compliance**.

1. Dari halaman gambaran umum manajemen risiko Insider, pilih tab **Kebijakan** lalu pilih **+ Buat kebijakan**.  Konfigurasikan setiap tab kebijakan berikut.

    1. Template kebijakan: Di bagian kategori Kebocoran data, pilih **Kebocoran data**.  Baca detail yang terkait dengan template ini. Di bagian prasyarat, kebijakan DLP ditampilkan dengan tanda centang dalam lingkaran hijau untuk menunjukkan bahwa prasyarat telah terpenuhi.  Ada kebijakan DLP yang telah dikonfigurasikan sebelumnya untuk penyewa lab ini. Pilih **Selanjutnya**. 
    1. Nama dan deskripsi: masukkan nama, **SC900-InsiderRiskPolicy**, lalu pilih **Berikutnya**.
    1. Pengguna dan grup:  Tinjau kotak informasi.  Biarkan pengaturan default, **Include all users and groups**.  Pilih **Selanjutnya**.
    1. Konten yang akan diprioritaskan: Sesuai deskripsi, Skor risiko ditingkatkan untuk aktivitas apa pun yang berisi konten prioritas, yang pada gilirannya meningkatkan kemungkinan menghasilkan peringatan tingkat keparahan tinggi. Untuk memudahkan, pilih **Saya tidak ingin memprioritaskan konten saat ini**, lalu pilih **Berikutnya**.
    1. Pemicu: Peristiwa pemicu menentukan kapan suatu kebijakan akan mulai menetapkan skor risiko ke aktivitas pengguna.  Anda dapat memilih dari kebijakan DLP yang ada atau jika pengguna melakukan aktivitas eksfiltrasi. Pilih **Pengguna cocok dengan kebijakan pencegahan kehilangan data (DLP)** lalu dari menu dropdown pilih **Data Keuangan AS**. Pilih **Selanjutnya**.
    1. Indikator: Perhatikan bahwa semua indikator kantor yang Anda pilih di tugas sebelumnya dipilih (Anda dapat melihat ini dengan memilih tombol panah arah bawah di sebelah indikator Kantor), lalu pilih **Berikutnya**.
    1. Pada halaman Opsi deteksi, biarkan semua pengaturan diatur ke default, tetapi baca deskripsi yang terkait dengan berbagai opsi dan arahkan kursor ke ikon informasi untuk mendapatkan informasi selengkapnya tentang pengaturan tertentu.  Pilih **Selanjutnya**.
    1. Pada halaman untuk Memutuskan apakah akan menggunakan ambang indikator default atau pelanggan, biarkan pengaturannya diatur ke default **Ambang default**, lalu pilih **Berikutnya**.
    1. Selesai: tinjau pengaturan, pilih **Kirim**.
    1. Tinjau deskripsi tentang apa yang terjadi selanjutnya lalu pilih **Selesai**.

1. Anda kembali ke tab Kebijakan di halaman manajemen risiko Insider.  Kebijakan yang Anda buat akan dicantumkan.  Jika Anda tidak melihatnya, pilih ikon **Refresh**.

1. Sebagai admin, Anda dapat segera mulai menetapkan skor risiko kepada pengguna berdasarkan aktivitas yang terdeteksi oleh kebijakan yang Anda pilih. Hal ini melewati persyaratan bahwa peristiwa pemicu (seperti kecocokan kebijakan DLP) terdeteksi terlebih dahulu.  Admin akan melakukannya dengan memilih kotak kosong di samping nama kebijakan untuk memilih kebijakan, lalu pilih **Mulai aktivitas penilaian untuk pengguna**, yang ditampilkan di atas tabel kebijakan.  Jendela baru terbuka yang mengharuskan admin mengisi bidang yang tersedia. Kosongkan bidang karena Anda tidak akan mengonfigurasi opsi ini, namun untuk informasi selengkapnya tentang mengapa admin ingin melakukan ini, pilih **Mengapa saya melakukan ini??** .  Keluar dari jendela dengan memilih **X** di kanan atas jendela.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke halaman arahan portal kepatuhan Microsoft Purview.

1. Tetap buka tab browser.

### Tinjau

Di lab ini, Anda telah mempelajari proses penyiapan kebijakan risiko dari dalam, bersama dengan prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.
