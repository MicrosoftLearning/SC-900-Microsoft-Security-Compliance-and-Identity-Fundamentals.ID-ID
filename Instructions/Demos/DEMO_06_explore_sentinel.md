---
demo:
  title: 'Microsoft Sentinel'
  module: 'Modul 3: Menjelaskan kemampuan keamanan Microsoft Azure Sentinel'
---



# <a name="demo-microsoft-sentinel"></a>Demo: Microsoft Sentinel

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Pelajaran: Menjelaskan bagaimana Microsoft Sentinel menyediakan manajemen ancaman terintegrasi

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan menjalani proses pembuatan instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data Anda, dan memilih buku kerja untuk memantau dan memvisualisasikan data Anda.  Terakhir, Anda akan menampilkan beberapa opsi lain yang tersedia, termasuk analitik bawaan untuk mendapatkan pemberitahuan jika ada yang mencurigakan, kemampuan otomatisasi, dan banyak lagi.

### <a name="pre-demo-setup--create-a-microsoft-sentinel-instance"></a>Penyiapan pra-demo: Membuat instans Microsoft Sentinel

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan: Biarkan diatur ke default.
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda)
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.
    1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih**OK**.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="demo-part-2"></a>Demo Bagian 2

Dengan instans Microsoft Sentinel dibuat, Anda pasti ingin memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.  

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Sebagai Administrator MOD, peran saat ini adalah Administrator layanan.  Ini akan memberi Anda izin yang diperlukan, tetapi untuk tujuan demo Anda mungkin ingin menunjukkan peran spesifik Sentinel.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

    1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

    1. Jendela Tambahkan penetapan peran akan terbuka.  Di kotak pencarian, masuki **Microsoft Sentinel** untuk melihat 4 peran yang terkait dengan Microsoft Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  

    1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari halaman kontrol akses, tutup jendela dengan memilih **X** di pojok kanan atas jendela.

### <a name="demo-part-3"></a>Demo Bagian 3

Di bagian demo ini, Anda akan menunjukkan langkah-langkah untuk menghubungkan ke sumber data.  Secara khusus, Anda akan terhubung ke konektor data Microsoft Defender untuk Cloud.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Microsoft Defender untuk Cloud** lalu dari daftar pilih **Microsoft Defender untuk Cloud**.

1. Jendela konektor Microsoft Defender untuk Cloud terbuka. Tinjau deskripsi lalu Pilih **Buka halaman konektor**.

1. Dari halaman konektor Microsoft Defender untuk Cloud, tinjau Deskripsi di sisi kiri jendela.

1. Tab petunjuk di jendela utama, menyediakan persyaratan-persyaratan.  Tinjau instruksi dan informasi konfigurasi.
    Tab petunjuk di jendela utama, menyediakan persyaratan-persyaratan.  Tinjau instruksi dan informasi konfigurasi.
    1. Dari bagian konfigurasi, pilih kotak kosong di sebelah langganan yang terdaftar, **Langganan MOC--lodXXXXXXXX** sehingga muncul tanda centang di kotak warna biru, lalu pilih **Hubungkan** (opsi koneksi adalah ditampilkan di atas kotak pencarian).  Akan muncul jendela Hubungkan, pilih **OK**.  di kolom status, di sebelah langganan Anda akan melihat pembaruan status menjadi Terhubung.  Jangan khawatir jika Anda tidak melihat status terhubung di jendela di sisi kiri halaman, JANGAN refresh browser.
    1. Gulir ke bawah halaman dan pilih **Aktifkan** untuk membuat insiden secara otomatis dari semua peringatan yang dibuat di layanan yang terhubung.
    1. Sekarang pilih tab **Langkah berikutnya** di bagian atas halaman, untuk melihat buku kerja yang disarankan, untuk konektor data ini.  Microsoft Sentinel hadir dengan template buku kerja bawaan untuk memungkinkan Anda mendapatkan wawasan dengan cepat di seluruh data Anda segera setelah menghubungkan sumber data.
    1. Pilih **Kepatuhan dan Perlindungan ASC** (Catatan: ASC atau Azure Security Center sekarang disebut Microsoft Defender untuk Cloud).  Tindakan ini akan membuka halaman buku kerja.  Di sisi kanan layar, tinjau deskripsi lalu pilih **Simpan** dari bagian bawah layar lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.  Sekarang pilih **Tampilkan buku kerja yang disimpan**.  
    1. Di bidang ruang kerja, pilih **Ruang kerja SC900-LogAnalytics**.
    1. Dari bagian atas halaman buku kerja, pilih **Refresh otomatis: Nonaktif**, lalu pilih **5 menit** dan pilih **Terapkan**.
    1. Dari bagian atas halaman buku kerja, pilih **ikon Simpan**.
    1. Dari sudut kiri atas halaman Buku Kerja, di atas bagian yang tertulis Buku Kerja, pilih **Microsoft Sentinel**. Ini mengembalikan Anda ke halaman Gambaran Umum. Anda sekarang akan melihat angka 1 di atas yang bertuliskan terhubung, untuk menunjukkan satu konektor aktif (Anda mungkin perlu memilih refresh).

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="demo-part-4"></a>Demo Bagian 4

Di bagian demo ini, Anda akan menunjukkan beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari tab **kueri**, yang dipilih (digarisbawahi), pilih kueri apa pun dari daftar.  Setelah kueri dipilih, catat informasi yang diberikan tentang kueri tersebut, termasuk kode kueri, dan opsi untuk menjalankan kueri dan lihat hasilnya.  Jangan pilih apa pun.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar.  

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Anda dapat mengunduh sampel konten dari komunitas privat repositori GitHub untuk membuat buku kerja kustom, kueri berburu, notebook, dan playbook untuk Microsoft Sentinel.  Pilih **Lakukan onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda.  Kembali ke tab Azure di browser Anda.

1. Di panel navigasi sebelah kiri, klik **Analitik**.  Pilih item pertama dari daftar **Deteksi Serangan Multistage Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  Di sini Anda dapat membuat aturan otomatisasi saja, berintegrasi dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan terdaftar dan tersedia untuk dilihat serta untuk memantau data Anda.   CATATAN: Tidak ada aktivitas nyata apa pun yang terjadi di langganan Azure untuk dicerminkan di buku kerja dan langganan lab Azure mungkin memerlukan waktu yang lebih lama dari biasanya dalam mengumpulkan data yang dapat divisualisasikan di buku kerja.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.  

### <a name="review"></a>Tinjau

Dalam demo ini Anda menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan menjalankan beberapa opsi yang tersedia di Microsoft Sentinel.
