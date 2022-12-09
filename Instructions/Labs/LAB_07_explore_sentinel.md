<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi Microsoft Sentinel' Jalur Pembelajaran/Modul/Judul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 3: Menjelaskan kemampuan keamanan Microsoft Azure Sentinel; Pelajaran 3: Menjelaskan bagaimana Microsoft Azure Sentinel menyediakan manajemen ancaman terintegrasi'
---
--->

# <a name="lab-explore-microsoft-sentinel"></a>Lab: Menjelajahi Microsoft Sentinel

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Pelajaran: Menjelaskan bagaimana Microsoft Sentinel menyediakan manajemen ancaman terintegrasi

## <a name="lab-scenario"></a>Skenario lab

, Anda akan menjalani proses pembuatan instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan melakukan penelusuran singkat beberapa kemampuan utama yang tersedia di Microsoft Sentinel. 

**Perkiraan Waktu**: 45-60 menit

### <a name="task-1"></a>Tugas 1

Buat instans Microsoft Sentinel

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.
1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan nama pengguna yang diberikan oleh penyedia hosting lab Anda, lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Di kotak pencarian warna biru di bagian atas halaman, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan: biarkan default, ini adalah langganan Azure yang disediakan oleh Authorized Lab Hoster (ALH).
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda)
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.
    1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih**OK**.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dengan pembuatan instans Microsoft Sentinel, penting bagi pengguna yang akan memiliki tanggung jawab untuk mendukung Microsoft Sentinel memiliki izin yang diperlukan.  Hal ini dilakukan dengan menetapkan izin peran yang diperlukan kepada pengguna yang ditunjuk.  Dalam tugas ini, Anda akan melihat peran Microsoft Sentinel bawaan yang tersedia.

1. Di kotak pencarian warna biru, masukkan **grup sumber daya** lalu pilih **Grup sumber daya** dari hasil pencarian. 

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.  Bekerja di tingkat grup sumber daya akan memastikan bahwa setiap peran yang dipilih akan diterapkan ke semua sumber daya yang merupakan bagian dari instans Microsoft Sentinel yang dibuat di tugas sebelumnya.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Untuk langganan Azure yang diberikan kepada Anda oleh Authorized Lab Hoster, peran telah ditentukan yang akan memberi Anda akses untuk mengelola semua sumber daya yang diperlukan, seperti yang ditunjukkan dalam deskripsi. Namun, penting untuk memahami peran spesifik Sentinel yang tersedia.  Tutup jendela tugas dengan memilih **X** di pojok kanan atas jendela.

1. Dari halaman Kontrol akses, pilih tab **Peran** di bagian atas halaman/
    1. Di kotak pencarian, masukkan **Microsoft Sentinel** untuk melihat peran bawaan yang terkait dengan Microsoft Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  
    1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari halaman kontrol akses, tutup jendela dengan memilih **X** di pojok kanan atas jendela.

### <a name="task-3"></a>Tugas 3

Tujuan dari tugas ini adalah untuk memandu melalui langkah-langkah yang terlibat dalam menyiapkan konektor data ke instans Microsoft Sentinel Anda dan memilih template buku kerja bawaan untuk memungkinkan Anda mendapatkan wawasan dengan cepat di seluruh data segera setelah menghubungkan data sumber. CATATAN: Langganan lab Azure mungkin memerlukan waktu yang lebih lama dari biasanya dalam menghubungkan ke sumber data dan/atau memvisualisasikan data.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Microsoft Defender untuk Cloud** lalu dari daftar pilih **Microsoft Defender untuk Cloud**.

1. Jendela konektor Microsoft Defender untuk Cloud terbuka. Tinjau deskripsi lalu Pilih **Buka halaman konektor**.

1. Dari halaman konektor Microsoft Defender untuk Cloud, tinjau Deskripsi di sisi kiri jendela.

1. Tab petunjuk di jendela utama, menyediakan persyaratan-persyaratan.  Tinjau instruksi dan informasi konfigurasi.
    1. Dari bagian konfigurasi, pilih kotak kosong di sebelah langganan yang terdaftar, **Langganan MOC--lodXXXXXXXX** sehingga muncul tanda centang di kotak warna biru, lalu pilih **Hubungkan** (opsi koneksi adalah ditampilkan di atas kotak pencarian).  Akan muncul jendela Hubungkan, pilih **OK**.  di kolom status, di sebelah langganan Anda akan melihat pembaruan status menjadi Terhubung.  Jangan khawatir jika Anda tidak melihat status terhubung di jendela di sisi kiri halaman, JANGAN refresh browser.
    1. Gulir ke bawah halaman dan pilih **Aktifkan** untuk membuat insiden secara otomatis dari semua peringatan yang dibuat di layanan yang terhubung.
    1. Sekarang pilih tab **Langkah berikutnya** di bagian atas halaman, untuk melihat buku kerja yang disarankan, untuk konektor data ini.  Microsoft Sentinel hadir dengan template buku kerja bawaan untuk memungkinkan Anda mendapatkan wawasan dengan cepat di seluruh data Anda segera setelah menghubungkan sumber data.
    1. Pilih **Kepatuhan dan Perlindungan ASC** (Catatan: ASC atau Azure Security Center sekarang disebut Microsoft Defender untuk Cloud).  Tindakan ini akan membuka halaman buku kerja.  Di sisi kanan layar, tinjau deskripsi lalu pilih **Simpan** dari bagian bawah layar lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.  Sekarang pilih **Tampilkan buku kerja yang disimpan**.
    1. Di bidang ruang kerja, pilih **Ruang kerja SC900-LogAnalytics**.
    1. Dari bagian atas halaman buku kerja, pilih **Refresh otomatis: Nonaktif**, lalu pilih **5 menit** dan pilih **Terapkan**.
    1. Dari bagian atas halaman buku kerja, pilih **ikon Simpan**.
    1. Dari sudut kiri atas halaman Buku Kerja, di atas bagian yang tertulis Buku Kerja, pilih **Microsoft Sentinel**. Ini mengembalikan Anda ke halaman Gambaran Umum. Anda sekarang akan melihat angka 1 di atas yang bertuliskan terhubung, untuk menunjukkan satu konektor aktif (Anda mungkin perlu memilih refresh).

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-4"></a>Tugas 4

Dalam tugas ini, Anda akan menelusuri beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari tab **kueri**, yang dipilih (digarisbawahi), pilih kueri apa pun dari daftar.  Setelah kueri dipilih, catat informasi yang diberikan tentang kueri tersebut, termasuk kode kueri, serta opsi untuk menjalankan kueri dan melihat hasilnya.  Jangan pilih apa pun.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar.  

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Dari sisi kanan layar, pilih **Onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda. Gulir ke bawah ke bagian README.md dan tinjau deskripsinya. Kembali ke tab Azure di browser Anda.

1. Di panel navigasi sebelah kiri, klik **Analitik**.  Pilih item pertama dari daftar **Deteksi Serangan Multistage Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  Di sini Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan terdaftar dan tersedia untuk dilihat serta untuk memantau data Anda.   CATATAN: Tidak ada aktivitas nyata apa pun yang terjadi di langganan Azure untuk dicerminkan di buku kerja dan langganan lab Azure mungkin memerlukan waktu yang lebih lama dari biasanya dalam mengumpulkan data yang dapat divisualisasikan di buku kerja.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.

1. Tutup semua tab browser yang terbuka.

### <a name="review"></a>Tinjau

Dalam demo ini Anda menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan menjalankan beberapa opsi yang tersedia di Microsoft Sentinel.
