<!---
---
Lab: Judul: 'Jelajahi Microsoft Sentinel' Jalur Pembelajaran/Modul/Judul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 3: Menjelaskan kemampuan keamanan Microsoft Azure Sentinel; Unit 3: Menjelaskan kemampuan deteksi dan mitigasi ancaman di Microsoft Azure Sentinel'
---
--->

# Lab: Menjelajahi Microsoft Sentinel

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Unit: Menjelaskan kemampuan deteksi dan mitigasi ancaman di Microsoft Azure Sentinel

## Skenario lab

, Anda akan menjalani proses pembuatan instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan melakukan penelusuran singkat beberapa kemampuan utama yang tersedia di Microsoft Sentinel.

**Perkiraan Waktu**: 45-60 menit

### Tugas 1

Buat instans Microsoft Sentinel

1. Anda harus berada di halaman beranda untuk layanan Azure.  Jika sebelumnya Anda menutup browser, buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**, dan masuk dengan kredensial admin Anda.

1. Di kotak pencarian warna biru di bagian atas halaman, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan: biarkan default, ini adalah langganan Azure yang disediakan oleh Authorized Lab Hoster (ALH).
    1. Grup sumber daya: pilih **SC900-Sentinel-RG**. Jika grup sumber daya ini tidak tercantum buat dengan memilih **Buat baru**, masukkan **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda)
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.
    1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih**OK**.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

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

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru di mana tertulis Microsoft Azure, pilih **Beranda** untuk kembali ke beranda layanan Azure.

1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tugas 3

Tujuan dari tugas ini adalah untuk memanding Anda melalui langkah-langkah yang terlibat dalam menyambungkan ke sumber data. Banyak konektor data disebarkan sebagai bagian dari solusi Microsoft Azure Sentinel bersama dengan konten terkait seperti aturan analitik, buku kerja, dan playbook. Hub Konten Microsoft Azure Sentinel adalah lokasi terpusat untuk menemukan dan mengelola konten out-of-the-box (bawaan). Dalam langkah ini, Anda akan menggunakan hub konten untuk menyebarkan solusi Microsoft Defender for Cloud untuk Microsoft Azure Sentinel.  Solusi ini memungkinkan Anda untuk menyerap pemberitahuan Keamanan yang dilaporkan di Microsoft Defender untuk Cloud.

1. Dari beranda layanan Azure, pilih Microsoft Azure Sentinel, lalu pilih instans yang Anda buat, **SC900-LogAnalytics-workspace**.

1. Dari panel navigasi kiri, pilih **Hub konten**.

1. Luangkan waktu sejenak untuk menggulir ke bawah untuk melihat daftar panjang solusi yang tersedia dan opsi untuk memfilter daftar.  Untuk tugas ini, Anda mencari **Microsoft Defender untuk Cloud**.  Pilih dari daftar.  Di jendela samping yang terbuka, baca deskripsi lalu pilih **Instal**.  Solusi ini mencakup satu konektor data dan satu aturan analitik. Mungkin perlu waktu satu menit untuk menginstal.  Pilih **Kelola**.

1. Pilih kotak di samping tempat yang tertulis Microsoft Defender untuk Cloud.  Jendela terbuka di sisi kanan halaman.  Pilih **Buka halaman konektor**.

1. Perhatikan instruksi konfigurasi.  Pilih kotak di samping nama langganan lalu pilih **Sambungkan**.  Jendela pop-op mungkin muncul yang menunjukkan bahwa hanya langganan tempat Anda memiliki izin Pembaca Keamanan akan memulai streaming Microsoft Defender untuk pemberitahuan Cloud.  Pilih**OK**.  Status akan berpindah ke tersambung.  Konektor sekarang diaktifkan, meskipun mungkin perlu waktu bagi konektor untuk muncul di halaman konektor data.  

1. Sekarang lihat informasi tentang aturan analitik.  Dari bagian atas halaman (di breadcrumb) pilih **Microsoft Defender untuk Cloud**. Batalkan pilih kotak di samping tempat yang berbunyi Microsoft Defender untuk Cloud, karena Anda telah mengonfigurasi konektor (mungkin perlu beberapa waktu agar ikon peringatan menghilang). Pilih kotak di samping tempat yang **bertuliskan, Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**. Di jendela yang terbuka, Anda akan melihat informasi tentang aturan dan apa yang dilakukannya.  
    1. Meskipun detail logika aturan berada di luar cakupan dasar, lakukan langkah-langkah untuk mengonfigurasi aturan untuk melihat jenis informasi yang dapat dikonfigurasi sebagai bagian dari aturan. Pilih **Konfigurasi**.
    1. Pilih aturan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**.
    1. Dari jendela yang terbuka di sisi kanan halaman, pilih **Buat aturan**.
    1. Buka setiap halaman konfigurasi, lalu pilih **Tinjau dan buat**, lalu pilih **Simpan**.

1. Kembali ke halaman Sentinel dengan memilih **Microsoft Azure Sentinel | Hub konten** dari remah roti di bagian atas halaman, di atasnya tertulis aturan Analitik.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.


### Tugas 4

Dalam tugas ini, Anda akan menelusuri beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari bagian atas halaman, pilih tab **Kueri** . Baca deskripsi tentang apa itu kueri berburu. Kueri berburu dapat ditambahkan melalui hub Konten. Setiap kueri yang sebelumnya terinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan kueri baik sebagai bagian dari solusi atau sebagai kueri mandiri.  Gulir ke bawah untuk melihat opsi yang tersedia. Tutup hub Konten dengan memilih **X** di sudut kanan atas jendela.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi paling kanan jendela untuk melihat panel informasi.

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Dari sisi kanan layar, pilih **Onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda. Gulir ke bawah ke bagian README.md dan tinjau deskripsinya. Kembali ke tab Azure di browser Anda.

1. Di panel navigasi sebelah kiri, klik **Analitik**.  Harus ada dua aturan aktif, satu yang tersedia secara default dan aturan yang Anda buat di tugas sebelumnya. Pilih aturan default **Deteksi Serangan Multistage Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi paling kanan jendela untuk melihat panel informasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  Di sini Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**. Baca deskripsi tentang apa itu buku kerja Microsoft Azure Sentinel.  Buku kerja dapat ditambahkan melalui hub Konten. Buku kerja apa pun yang sebelumnya diinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan buku kerja baik sebagai bagian dari solusi atau sebagai buku kerja mandiri. Gulir ke bawah untuk melihat opsi yang tersedia.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.

1. Keluar dan tutup semua tab browser yang terbuka.

### Tinjau

Dalam lV ini Anda menelusuri langkah-langkah untuk menyambungkan Microsoft Sentinel ke sumber data, Anda menyiapkan buku kerja, dan memandu beberapa opsi yang tersedia di Microsoft Azure Sentinel.
