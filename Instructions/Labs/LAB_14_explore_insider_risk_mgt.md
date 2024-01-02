<!---
---
Lab: Judul: 'Menjelajahi manajemen risiko dari dalam di Microsoft Purview' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 4: Menjelaskan kemampuan risiko dari dalam di Microsoft Purview; Unit 2: Menjelaskan manajemen risiko dari dalam'
---
--->

# Lab: Menjelajahi manajemen risiko dari dalam di Microsoft Purview

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan kemampuan risiko dari dalam di Microsoft Purview
- Unit: Menjelaskan Manajemen Risiko Dari Dalam

## Skenario laboratorium

Di lab ini, Anda akan mempelajari proses penyiapan kebijakan risiko dari dalam, beserta prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.  Catatan: lab ini hanya akan memberikan visibilitas tentang apa yang diperlukan untuk menyiapkan Manajemen risiko dari dalam dan opsi yang terkait dengan pembuatan kebijakan.  Lab ini tidak menyertakan tugas untuk memicu kebijakan, karena jumlah peristiwa yang perlu terjadi untuk memicu kebijakan dan waktu yang diperlukan berada di luar cakupan latihan ini.

**Perkiraan Waktu**: 45-60 menit

### Tugas 1

Dalam tugas ini, Anda sebagai administrator global akan mengaktifkan izin untuk Manajemen Risiko Dari Dalam.  Khususnya, Anda akan menambahkan pengguna ke grup peran Manajemen Risiko Dari Dalam untuk memastikan bahwa pengguna yang ditunjuk dapat mengakses dan mengelola fitur manajemen risiko dari dalam.  Mungkin perlu waktu hingga 30 menit agar izin grup peran berlaku untuk pengguna di seluruh organisasi.

1. Buka tab browser untuk membuka beranda Microsoft Purview.  Jika sebelumnya Anda menutupnya, buka tab browser dan masukkan **https://admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**, lalu pilih **Kepatuhan**.  Laman browser baru membuka laman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi kiri, bentangkan **Peran & Cakupan**, lalu pilih **Izin**.

1. Pada solusi Microsoft Purview, pilih **Peran**.

1. Di bidang pencarian, masukkan **Risiko dari dalam**, lalu tekan Enter di keyboard Anda.  Perhatikan banyak peran yang muncul.  Masing-masing memiliki tingkat akses yang berbeda.  Pilih **Manajemen risiko dari dalam** dan tinjau deskripsinya.  Gulir ke bawah ke tempat yang menunjukkan anggota dan perhatikan bahwa MOD Administrator dan Megan Bowen terdaftar. Tutup jendela dengan memilih **X** di kanan atas jendela.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke laman portal kepatuhan Microsoft Purview.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan kembali ke sana di tugas selanjutnya.

### Tugas 2 (CATATAN: LEWATI Tugas 2 jika Anda telah menjalankan tugas lab penyiapan untuk mengaktifkan log audit)

Manajemen risiko dari dalam menggunakan log audit Microsoft 365 untuk wawasan pengguna dan aktivitas yang diidentifikasi dalam kebijakan dan wawasan analitik. Dalam tugas ini, Anda akan mengaktifkan kemampuan pencarian log Audit. Catatan: Mungkin perlu waktu beberapa jam setelah Anda mengaktifkan pencarian log audit sebelum dapat mengembalikan hasil saat mencari log audit.  Meskipun dapat memakan waktu beberapa jam sebelum Anda dapat mencari log audit, itu tidak akan berdampak pada kemampuan untuk menyelesaikan tugas lain di lab ini.

1. Pilih tab browser berlabel, **Beranda-Kepatuhan Microsoft 365**.  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge, dan di bilah alamat masukkan **compliance.microsoft.com** dan masuk dengan kredensial admin Anda.

1. Dari panel navigasi kiri, di bagian solusi, pilih **Audit**.

1. Pastikan tab **Pencarian Baru** dipilih (digarisbawahi).

1. Setelah Anda masuk ke laman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas halaman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Mulai merekam aktivitas pengguna dan admin**.  Setelah audit diaktifkan, bilah biru menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.

1. Kembali ke beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi sebelah kiri.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 3

Dalam tugas ini, Anda akan mempelajari pengaturan yang terkait dengan solusi Manajemen Risiko Dari Dalam.  Pengaturan manajemen risiko dari dalam berlaku untuk semua kebijakan manajemen risiko dari dalam, terlepas dari templat yang Anda pilih saat membuat kebijakan.

1. Anda akan diarahkan ke halaman beranda portal kepatuhan Microsoft Purview. Jika tidak, buka tab browser **Beranda-Kepatuhan Microsoft 365**.

1. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **Manajemen risiko dari dalam**.

1. Sebelum mulai menyiapkan kebijakan, ada beberapa pengaturan yang harus dipahami dan dikonfigurasi oleh admin sesuai kebutuhan untuk organisasinya. Dari halaman Manajemen Risiko Dari Dalam, pilih **ikon roda gigi pengaturan** di pojok kanan atas jendela Manajemen risiko dari dalam untuk mengakses pengaturan Risiko Dari Dalam.  
    1. Pastikan Anda berada di tab **Privasi**: untuk pengguna yang melakukan aktivitas yang cocok dengan kebijakan risiko dari dalam Anda, pengaturan ini akan menentukan apakah akan menampilkan nama mereka yang sebenarnya atau menggunakan versi anonim untuk menutupi identitas mereka.  Untuk keperluan pembelajaran ini, Anda dapat membiarkan pengaturannya diatur ke default.
    1. Pilih tab **Indikator kebijakan**. Setelah peristiwa pemicu kebijakan terjadi, aktivitas yang memetakan ke indikator yang dipilih digunakan dalam menentukan skor risiko, untuk pengguna. Indikator kebijakan yang dipilih di sini menyertakan templat kebijakan risiko dari dalam.  Gulir untuk melihat semua indikator yang tersedia dan informasi terkait. Di bagian **Indikator kantor**, pilih **Pilih semua**, lalu pilih **Simpan** di bagian bawah laman (Anda harus menggulir ke bawah).
    1. Pilih tab **Kerangka waktu kebijakan**. Jangka waktu yang Anda pilih di sini berlaku untuk pengguna ketika mereka memicu kecocokan untuk kebijakan risiko dari dalam.   Jendela Aktivasi menentukan berapa lama kebijakan akan secara aktif mendeteksi aktivitas untuk pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan. Deteksi aktivitas terdahulu Menentukan seberapa jauh kebijakan harus terdeteksi aktivitas pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan.  Biarkan nilai default.
    1. Pilih tab **Deteksi cerdas**. Tinjau opsi di sini.  Perhatikan pengaturan domain dan bagaimana pengaturan tersebut berhubungan dengan indikator.
    1. Jelajahi item lain yang tercantum dalam pengaturan dan perhatikan bahwa banyak item dalam pratinjau.

1. Untuk kembali ke ikhtisar Manajemen risiko dari dalam, pilih **Manajemen risiko dari dalam** dari sudut kiri atas laman, di atas tempat yang tertulis Pengaturan.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 4

Dalam tugas ini, Anda akan mempelajari pengaturan untuk membuat kebijakan.  Tujuannya hanyalah untuk memahami berbagai opsi dan fleksibilitas yang terkait dengan pembuatan kebijakan.

1. Anda harus berada di laman Manajemen risiko dari dalam.  Jika belum ada, buka tab browser berlabel, **Manajemen risiko dari dalam - Kepatuhan Microsoft 365**.

1. Dari laman ikhtisar manajemen risiko dari dalam, pilih tab **Kebijakan**, lalu pilih **+ Buat kebijakan**.  Konfigurasikan setiap tab kebijakan berikut.

    1. Templat kebijakan: Di bagian kategori Kebocoran data, pilih **Kebocoran data**.  Baca detail yang terkait dengan templat ini. Di bagian prasyarat, kebijakan DLP ditampilkan dengan tanda centang dalam lingkaran hijau untuk menunjukkan bahwa prasyarat telah terpenuhi.  Ada kebijakan DLP yang telah dikonfigurasikan sebelumnya untuk penyewa lab ini. Pilih **Selanjutnya**. 
    1. Nama dan deskripsi: masukkan nama, **SC900-InsiderRiskPolicy**, lalu pilih **Berikutnya**.
    1. Pengguna dan grup: Tinjau kotak informasi.  Biarkan pengaturan default, **Sertakan semua pengguna dan grup**.  Pilih **Selanjutnya**.
    1. Konten yang akan diprioritaskan: Sesuai deskripsi, Skor risiko ditingkatkan untuk aktivitas apa pun yang berisi konten prioritas, yang pada gilirannya meningkatkan kemungkinan menghasilkan peringatan tingkat keparahan tinggi. Untuk memudahkan, pilih **Saya tidak ingin memprioritaskan konten saat ini**, lalu pilih **Berikutnya**.
    1. Pemicu: Peristiwa pemicu menentukan kapan suatu kebijakan akan mulai menetapkan skor risiko ke aktivitas pengguna.  Anda dapat memilih dari kebijakan DLP yang ada atau jika pengguna melakukan aktivitas eksfiltrasi. Pilih **Pengguna cocok dengan kebijakan pencegahan kehilangan data (DLP)** lalu dari menu menurun, pilih **Data Keuangan AS**. Pilih **Selanjutnya**.
    1. Indikator: Perhatikan bahwa semua indikator kantor yang Anda pilih di tugas sebelumnya dipilih (Anda dapat melihat ini dengan memilih tombol panah arah bawah di sebelah indikator Kantor), lalu pilih **Berikutnya**.
    1. Pada laman Opsi deteksi, biarkan semua pengaturan diatur ke default, tetapi baca deskripsi yang terkait dengan berbagai opsi dan arahkan kursor ke ikon informasi untuk mendapatkan informasi selengkapnya tentang pengaturan tertentu.  Pilih **Selanjutnya**.
    1. Pada laman untuk Memutuskan apakah akan menggunakan ambang indikator default atau pelanggan, biarkan pengaturannya diatur ke default **Ambang default**, lalu pilih **Berikutnya**.
    1. Selesai: tinjau pengaturan, pilih **Kirim**.
    1. Tinjau deskripsi tentang apa yang terjadi selanjutnya, lalu pilih **Selesai**.

1. Anda kembali ke tab Kebijakan di laman Manajemen risiko dari dalam.  Kebijakan yang Anda buat akan dicantumkan.  Jika Anda tidak melihatnya, pilih ikon **Refresh**.

1. Sebagai admin, Anda dapat segera mulai menetapkan skor risiko kepada pengguna berdasarkan aktivitas yang terdeteksi oleh kebijakan yang Anda pilih. Hal ini melewati persyaratan bahwa peristiwa pemicu (seperti kecocokan kebijakan DLP) terdeteksi terlebih dahulu.  Admin akan melakukannya dengan memilih kotak kosong di samping nama kebijakan untuk memilih kebijakan, lalu pilih **Mulai aktivitas penilaian untuk pengguna**, yang ditampilkan di atas tabel kebijakan.  Jendela baru terbuka yang mengharuskan admin mengisi bidang yang tersedia. Kosongkan bidang karena Anda tidak akan mengonfigurasi opsi ini, tetapi untuk informasi selengkapnya tentang mengapa admin ingin melakukan ini, pilih **Mengapa saya melakukan ini??**.  Keluar dari jendela dengan memilih **X** di kanan atas jendela.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke laman Beranda portal kepatuhan Microsoft Purview.

1. Tetap buka tab browser.

### Tinjauan

Di lab ini, Anda telah mempelajari proses penyiapan kebijakan risiko dari dalam, beserta prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.
