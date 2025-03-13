<!---
---
Demo: Judul: 'Microsoft Sentinel’ Jalur Pembelajaran/Modul/Judul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 3: Menjelaskan kemampuan keamanan Microsoft Sentinel; Unit 3: Menjelaskan kemampuan mitigasi dan deteksi ancaman di Microsoft Sentinel'
---
--->

# Demo: Microsoft Sentinel

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Unit: Menjelaskan kemampuan mitigasi dan deteksi ancaman di Microsoft Sentinel

## Skenario demo

Dalam demo ini, Anda akan mempelajari beberapa opsi yang tersedia di Microsoft Sentinel, termasuk menggunakan hub konten untuk menemukan solusi paket yang dapat Anda sebarkan.  Namun, pertama, Anda akan mempelajari proses penyiapan izin kontrol akses berbasis peran untuk pengguna yang perlu mengakses sumber daya Microsoft Sentinel Anda.

### Demo bagian 1

Instans Microsoft Sentinel seharusnya dibuat sebagai bagian dari penyiapan prademo. Pastikan instans telah dibuat

1. Buka tab browser, **Beranda- Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan **https://portal.azure.com**. Masuk dengan kredensial Azure yang disediakan oleh host lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas laman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari hasil pencarian.  

1. Pada laman Microsoft Sentinel, Anda akan melihat instans Sentinel Anda tercantum dan pilihlah instans tersebut.  Jika tidak tercantum, buat sekarang.
    1. Dari laman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

    1. Dari laman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**. Dari tab Dasar di Buat ruang kerja Analitik Log, masukkan berikut ini:
        1. Langganan: Biarkan diatur ke default.
        1. Grup sumber daya: pilih **Buat Baru**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
        1. Nama: **SC900-LogAnalytics-workspace**.
        1. Wilayah: **AS Timur** (Ada wilayah default lain yang mungkin dipilih sesuai lokasi Anda).
        1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
        1. Verifikasi informasi yang Anda masukkan, lalu pilih **Buat**.
        1. Mungkin perlu waktu satu atau dua menit agar ruang kerja ne terdaftar, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Tambahkan**.
        1. Setelah ruang kerja baru ditambahkan, laman Microsoft Sentinel | Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih **OK**.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Demo Bagian 2

Seperti semua sumber daya Azure, Anda ingin memastikan bahwa pengguna memiliki izin yang tepat untuk mengakses sumber daya Microsoft Sentinel Anda. Di sini, Anda akan menampilkan langkah-langkah untuk menetapkan peran dan peran yang tersedia untuk digunakan dengan Microsoft Sentinel.  

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas laman di samping bagian yang tertulis Microsoft Azure, masukkan **grup sumber daya**, lalu pilih **Grup sumber daya** dari hasil pencarian. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari laman SC900-Sentinel-RG, pilih **Kontrol akses (IAM)** dari panel navigasi kiri.

1. Dari laman Kontrol akses, pilih **Tampilkan akses saya**.  Anda kemungkinan besar akan melihat penetapan peran kustom yang sudah dikonfigurasi untuk langganan ini dan itu akan memberi Anda izin yang diperlukan.  Peran kustom ini akan disiapkan oleh hoster lab resmi (ALH) yang menyediakan lingkungan lab. Namun, untuk demo, ada baiknya menunjukkan peran spesifik Sentinel.  Tutup jendela tugas dengan memilih **X** di pojok kanan atas jendela.

    1. Dari laman Kontrol akses, pilih **+Tambahkan**, lalu pilih **Tambah penetapan peran**.

    1. Jendela Tambahkan penetapan peran akan terbuka.  Di kotak pencarian, masukkan **Microsoft Sentinel** untuk melihat peran yang terkait dengan Microsoft Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Sebagai praktik terbaik, Anda harus menetapkan hak istimewa paling sedikit yang diperlukan untuk peran tersebut.  

    1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari laman kontrol akses, tutup jendela dengan memilih **X** di pojok kanan atas jendela.

### Demo Bagian 3

Di bagian demo ini, Anda akan menunjukkan langkah-langkah untuk menghubungkan ke sumber data. Banyak konektor data juga dapat digunakan sebagai bagian dari solusi Microsoft Sentinel, bersama dengan aturan analitik terkait, buku kerja, dan playbook. Hub konten Microsoft Sentinel adalah lokasi terpusat untuk menemukan dan mengelola konten unik (bawaan). Dalam langkah ini, Anda akan menggunakan hub konten untuk menyebarkan solusi Microsoft Defender untuk Cloud bagi Microsoft Sentinel.  Solusi ini memungkinkan Anda menyerap pemberitahuan Keamanan yang dilaporkan dalam Microsoft Defender untuk Cloud.

1. Buka tab browser untuk Microsoft Sentinel.

1. Dari panel navigasi kiri, pilih **Hub konten**.

1. Luangkan waktu sejenak untuk menggulir ke bawah guna melihat daftar lengkap solusi yang tersedia dan opsi untuk memfilter daftar.  Untuk tugas ini, kita mencari **Microsoft Defender untuk Cloud**.  Pilihlah dari daftar.  Di jendela samping yang terbuka, baca deskripsi, lalu pilih **Instal**.  Setelah penginstalan selesai, kolom status di jendela utama akan ditampilkan sebagai terinstal.

1. Di sisi kanan halaman Microsoft Defender untuk Cloud adalah deskripsi dan catatan yang terkait dengan solusi dari Content Hub dan apa yang disertakan sebagai bagian dari solusi ini.  Di jendela utama adalah komponen solusi.  Dalam hal ini ada dua konektor data dan satu aturan data. Segitiga oranye menunjukkan bahwa beberapa konfigurasi diperlukan. Pilih kotak di samping tempat berbunyi **Microsoft Defender untuk Cloud (Legacy) berbasis Langganan**.  Jendela terbuka di sisi kanan laman.  Pilih **Buka laman konektor**.

1. Perhatikan instruksi konfigurasi  Pilih kotak di samping nama langganan, lalu pilih **Koneksi**.  Status akan berpindah ke tersambung.  Sekarang, konektor diaktifkan, meskipun mungkin perlu beberapa waktu agar konektor muncul di laman konektor data.  

1. Sekarang lihat informasi tentang aturan analitik.  Dari bagian atas laman (di bilah), pilih **Microsoft Defender untuk Cloud**. Batalkan pilih kotak di samping tempat yang tertulis Microsoft Defender untuk Cloud, karena Anda telah mengonfigurasi konektor (mungkin perlu beberapa waktu agar ikon peringatan menghilang). Pilih kotak di samping tulisan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**.  Ini memunculkan halaman Aturan Analitik.  Sekali lagi, pilih **Deteksi Aktivitas Penghapusan CoreBackUp dari aturan pemberitahuan keamanan terkait**. Jendela yang terbuka di sebelah kanan, yang menyediakan informasi tentang aturan dan apa yang dilakukannya.  Pilih **Buat aturan**.  
    1. Meskipun detail logika aturan berada di luar lingkup dasar-dasar, buka setiap tab dalam pembuatan aturan untuk melihat jenis informasi yang dapat dikonfigurasi
    1. Saat Anda mencapai tab Tinjau + buat, pilih **Simpan**.

1. Kembali ke laman Sentinel dengan memilih **Microsoft Sentinel | Hub konten** dari bilah di bagian atas laman, di atas tulisan aturan Analitik.

1. Sebutkan bahwa dengan menggunakan hub konten, solusi dapat disebarkan dengan mudah dan cepat.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Demo Bagian 4

Di bagian demo ini, Anda akan menunjukkan beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari bagian atas laman, pilih tab **kueri**. Baca deskripsi tentang apa itu kueri hunting. Kueri hunting dapat ditambahkan melalui Hub Konten. Setiap kueri yang sebelumnya diinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan kueri baik sebagai bagian dari solusi atau sebagai kueri mandiri.  Gulir ke bawah untuk melihat opsi yang tersedia.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar.  

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Halaman komunitas mencakup wawasan dan pembaruan keamanan Cyber dari Microsoft Research, tautan ke daftar Blog Microsoft Azure Sentinel, tautan ke Forum Microsoft Sentinel, menautkan edisi terbaru ke Microsoft Sentinel Hub, dan banyak lagi. Jelajahi ini sesuka hati.

1. Dari panel navigasi kiri, pilih **Analitik**.  Di sana, ada dua aturan aktif, satu yang tersedia secara default dan aturan yang Anda buat di tugas sebelumnya. Pilih aturan **Deteksi Serangan Multitahap Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit ditangkap.

1. Dari panel navigasi kiri, pilih **Otomatisasi**.  Di sini, Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat**, lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat syarat dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi kiri, pilih **Buku kerja**. Baca deskripsi buku kerja Microsoft Azure Sentinel.  Buku kerja dapat ditambahkan melalui Hub konten. Buku kerja apa pun yang sebelumnya diinstal akan tercantum di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan buku kerja baik sebagai bagian dari solusi maupun sebagai buku kerja mandiri. Gulir ke bawah untuk melihat opsi yang tersedia.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke laman beranda portal Azure.  

### Tinjauan

Dalam demo ini, Anda telah mempelajari langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan mempelajari beberapa opsi yang tersedia di Microsoft Sentinel.
