<!---
---
Demo: Judul: 'Microsoft Sentinel' Jalur Pembelajaran/Modul/Judul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 3: Menjelaskan kemampuan keamanan Microsoft Azure Sentinel; Unit 3: Menjelaskan kemampuan deteksi dan mitigasi ancaman di Microsoft Azure Sentinel'
---
--->

# Demo: Microsoft Sentinel

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Unit: Menjelaskan kemampuan deteksi dan mitigasi ancaman di Microsoft Azure Sentinel

## Skenario demo

Dalam demo ini, Anda akan menelusuri beberapa opsi yang tersedia dengan Microsoft Sentinel, termasuk menggunakan hub konten untuk menemukan solusi paket yang dapat Anda sebarkan.  Tetapi pertama-tama, Anda akan menelusuri proses penyiapan izin kontrol akses berbasis peran untuk pengguna yang perlu mengakses sumber daya Microsoft Azure Sentinel Anda.

### Demo bagian 1

Instans Microsoft Sentinel seharusnya sudah dibuat sebagai bagian dari penyiapan pra-demo. Verifikasi bahwa itu dibuat.

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan **https://portal.azure.com**. Masuk dengan kredensial Azure yang disediakan oleh hoster lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.  

1. Pada halaman Microsoft Azure Sentinel, Anda akan melihat instans Sentinel Anda tercantum dan memilihnya.  Jika tidak tercantum, buat sekarang.
    1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

    1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
        1. Langganan: Biarkan diatur ke default.
        1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
        1. Nama: **SC900-LogAnalytics-workspace**.
        1. Kawasan:::: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda)
        1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
        1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.
        1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.
        1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih**OK**.

1. Tetap buka halaman ini, karena Anda akan menggunakannya dalam tugas berikutnya.

### Demo Bagian 2

Seperti semua sumber daya Azure, Anda ingin memastikan bahwa pengguna memiliki izin yang tepat untuk mengakses sumber daya Microsoft Azure Sentinel Anda. Di sini Anda akan menampilkan langkah-langkah untuk menetapkan peran dan peran yang tersedia untuk digunakan dengan Microsoft Sentinel.  

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Jika Anda menggunakan langganan Skillable Cloud Slice, penetapan peran diatur ke Pemilik LOD, yang merupakan penetapan peran kustom yang dikonfigurasi untuk langganan Cloud Slice ini dan akan memberi Anda izin yang diperlukan. Namun, untuk tujuan demo, ada baiknya untuk menunjukkan peran spesifik Sentinel.  Tutup jendela tugas dengan memilih **X** di pojok kanan atas jendela.

    1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

    1. Jendela Tambahkan penetapan peran akan terbuka.  Dalam kotak pencarian, masukkan **Microsoft Azure Sentinel** untuk menampilkan peran yang terkait dengan Microsoft Azure Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  

    1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari halaman kontrol akses, tutup jendela dengan memilih **X** di pojok kanan atas jendela.

### Demo Bagian 3

Di bagian demo ini, Anda akan menunjukkan langkah-langkah untuk menghubungkan ke sumber data. Banyak konektor data disebarkan sebagai bagian dari solusi Microsoft Azure Sentinel bersama dengan konten terkait seperti aturan analitik, buku kerja, dan playbook. Hub Konten Microsoft Azure Sentinel adalah lokasi terpusat untuk menemukan dan mengelola konten out-of-the-box (bawaan). Dalam langkah ini, Anda akan menggunakan hub konten untuk menyebarkan solusi Microsoft Defender for Cloud untuk Microsoft Azure Sentinel.  Solusi ini memungkinkan Anda untuk menyerap pemberitahuan Keamanan yang dilaporkan di Microsoft Defender untuk Cloud.

1. Buka tab browser untuk Microsoft Azure Sentinel.

1. Dari panel navigasi kiri, pilih **Hub konten**.

1. Luangkan waktu sejenak untuk menggulir ke bawah untuk melihat daftar panjang solusi yang tersedia dan opsi untuk memfilter daftar.  Untuk demo ini, kami mencari **Microsoft Defender untuk Cloud**.  Pilih dari daftar.  Di jendela samping yang terbuka, baca deskripsi lalu pilih **Instal**.  Solusi ini mencakup satu konektor data dan satu aturan analitik. Mungkin perlu waktu satu menit untuk menginstal.  Pilih **Kelola**.

1. Pilih kotak di samping tempat yang tertulis Microsoft Defender untuk Cloud.  Jendela terbuka di sisi kanan halaman.  Pilih **Buka halaman konektor**.

1. Perhatikan instruksi konfigurasi.  Pilih kotak di samping nama langganan lalu pilih **Sambungkan**.  Status akan berpindah ke tersambung.  Konektor sekarang diaktifkan, meskipun mungkin perlu waktu bagi konektor untuk muncul di halaman konektor data.  

1. Sekarang lihat informasi tentang aturan analitik.  Dari bagian atas halaman (di breadcrumb) pilih **Microsoft Defender untuk Cloud**.  Pilih kotak di samping tempat yang bertuliskan, "Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait". Di jendela yang terbuka, Anda akan melihat informasi tentang aturan dan apa yang dilakukannya.  Anda dapat memilih untuk melalui langkah-langkah untuk mengonfigurasi aturan.  **CATATAN**: Detail logika aturan berada di luar cakupan dasar-dasar tetapi Anda dapat menampilkan jenis informasi yang dapat dikonfigurasi sebagai bagian dari aturan.  
    1. Pilih **Konfigurasi**.
    1. Pilih aturan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**.
    1. Dari jendela yang terbuka di sisi kanan halaman, pilih **Buat aturan**.
    1. Buka setiap halaman konfigurasi, tingkat yang sangat singkat dan tinggi lalu pilih **Tinjau dan buat**, lalu pilih **Simpan**.

1. Kembali ke halaman Sentinel dengan memilih **Microsoft Azure Sentinel | Hub konten** dari bread-crump di bagian atas halaman, di atas tertulis aturan Analytics.

1. Sebutkan bahwa dengan menggunakan hub konten, solusi dapat dengan mudah dan cepat disebarkan.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Demo Bagian 4

Di bagian demo ini, Anda akan menunjukkan beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari bagian atas halaman, pilih tab **kueri** . Baca deskripsi tentang apa itu kueri berburu. Kueri berburu dapat ditambahkan melalui hub Konten. Setiap kueri yang sebelumnya terinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan kueri baik sebagai bagian dari solusi atau sebagai kueri mandiri.  Gulir ke bawah untuk melihat opsi yang tersedia.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar.  

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Anda dapat mengunduh sampel konten dari komunitas privat repositori GitHub untuk membuat buku kerja kustom, kueri berburu, notebook, dan playbook untuk Microsoft Sentinel.  Pilih **Lakukan onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda.  Kembali ke tab Azure di browser Anda.

1. Di panel navigasi sebelah kiri, klik **Analitik**.  Harus ada dua aturan aktif, satu yang tersedia secara default dan aturan yang Anda buat di tugas sebelumnya. Pilih aturan default **Deteksi Serangan Multistage Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  Di sini Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**. Baca deskripsi tentang apa itu buku kerja Microsoft Azure Sentinel.  Buku kerja dapat ditambahkan melalui hub Konten. Buku kerja apa pun yang sebelumnya diinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan buku kerja baik sebagai bagian dari solusi atau sebagai buku kerja mandiri. Gulir ke bawah untuk melihat opsi yang tersedia.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.  

### Tinjau

Dalam demo ini Anda menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan menjalankan beberapa opsi yang tersedia di Microsoft Sentinel.
