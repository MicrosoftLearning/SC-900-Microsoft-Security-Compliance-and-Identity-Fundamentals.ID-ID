<!---
---
Laboratorium: Judul: 'Menjelajahi Microsoft Sentinel’ Jalur Pembelajaran/Modul/Judul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 3: Menjelaskan kemampuan keamanan Microsoft Sentinel; Unit 3: Menjelaskan kemampuan mitigasi dan deteksi ancaman di Microsoft Sentinel'
---
--->

# Lab: Menjelajahi Microsoft Sentinel

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Unit: Menjelaskan kemampuan mitigasi dan deteksi ancaman di Microsoft Sentinel

## Skenario laboratorium

, Anda akan mempelajari proses pembuatan instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan melakukan penelusuran singkat beberapa kemampuan utama yang tersedia di Microsoft Sentinel.

**Perkiraan Waktu**: 45-60 menit

### Tugas 1

Buat instans Microsoft Sentinel

1. Anda berada di beranda layanan Azure.  Jika sebelumnya Anda menutup browser, buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**, dan masuk dengan kredensial admin Anda.

1. Di kotak pencarian warna biru di bagian atas laman, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari laman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari laman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Dari tab Dasar di Buat ruang kerja Analitik Log, masukkan berikut ini:
    1. Langganan: biarkan default, ini adalah langganan Azure yang disediakan oleh Authorized Lab Hoster (ALH).
    1. Grup sumber daya: pilih **SC900-Sentinel-RG**. Jika grup sumber daya ini tidak tercantum, buat dengan memilih Buat baru **, masukkan **SC900-Sentinel-RG**, lalu pilih **OK**.**
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Wilayah: **AS Timur** (Ada wilayah default lain yang mungkin dipilih sesuai lokasi Anda).
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Buat**.
    1. Mungkin perlu waktu satu atau dua menit agar ruang kerja ne terdaftar, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Tambahkan**.

1. Setelah ruang kerja baru ditambahkan, laman Microsoft Sentinel | Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih **OK**.  Perhatikan tiga langkah yang tercantum di laman Memulai.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dengan pembuatan instans Microsoft Sentinel, penting bagi pengguna yang akan memiliki tanggung jawab untuk mendukung Microsoft Sentinel memiliki izin yang diperlukan.  Hal ini dilakukan dengan menetapkan izin peran yang diperlukan kepada pengguna yang ditunjuk.  Dalam tugas ini, Anda akan melihat peran Microsoft Sentinel bawaan yang tersedia.

1. Di kotak pencarian warna biru, masukkan **grup sumber daya** lalu pilih **Grup sumber daya** dari hasil pencarian. 

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.  Bekerja di tingkat grup sumber daya akan memastikan bahwa setiap peran yang dipilih akan diterapkan ke semua sumber daya yang merupakan bagian dari instans Microsoft Sentinel yang dibuat di tugas sebelumnya.

1. Dari laman SC900-Sentinel-RG, pilih **Kontrol akses (IAM)** dari panel navigasi kiri.

1. Dari laman Kontrol akses, pilih **Tampilkan akses saya**.  Untuk langganan Azure yang diberikan kepada Anda oleh Host Lab Resmi, peran telah ditentukan yang akan memberi Anda akses untuk mengelola semua sumber daya yang diperlukan, seperti yang ditunjukkan dalam deskripsi. Namun, penting untuk memahami peran spesifik Sentinel yang tersedia.  Tutup jendela tugas dengan memilih **X** di pojok kanan atas jendela.

1. Dari laman Kontrol akses, pilih tab **Peran** di bagian atas laman.
    1. Di kotak pencarian, masukkan **Microsoft Sentinel** untuk melihat peran bawaan yang terkait dengan Microsoft Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Sebagai praktik terbaik, Anda harus menetapkan hak istimewa paling sedikit yang diperlukan untuk peran tersebut.  
    1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari laman kontrol akses, tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru sebelah tulisan Microsoft Azure, pilih **Beranda** untuk kembali ke laman beranda layanan Azure.

1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tugas 3

Tujuan dari tugas ini untuk memandu Anda menelusuri langkah-langkah yang terlibat dalam menyambungkan ke sumber data. Banyak konektor data juga dapat digunakan sebagai bagian dari solusi Microsoft Sentinel, bersama dengan aturan analitik terkait, buku kerja, dan playbook. Hub konten Microsoft Sentinel adalah lokasi terpusat untuk menemukan dan mengelola konten unik (bawaan). Dalam langkah ini, Anda akan menggunakan hub konten untuk menyebarkan solusi Microsoft Defender untuk Cloud bagi Microsoft Sentinel.  Solusi ini memungkinkan Anda menyerap pemberitahuan Keamanan yang dilaporkan dalam Microsoft Defender untuk Cloud.

1. Dari beranda layanan Azure, pilih Microsoft Azure Sentinel, lalu pilih instans yang Anda buat, **SC900-LogAnalytics-workspace**.

1. Dari panel navigasi kiri, pilih **Hub konten**.

1. Luangkan waktu sejenak untuk menggulir ke bawah guna melihat daftar lengkap solusi yang tersedia dan opsi untuk memfilter daftar.  Untuk tugas ini, kita mencari **Microsoft Defender untuk Cloud**.  Pilihlah dari daftar.  Di jendela samping yang terbuka, baca deskripsi, lalu pilih **Instal**.  Solusi ini mencakup satu konektor data dan satu aturan analitik. Mungkin perlu waktu satu menit untuk menginstalnya.  Pilih **Kelola**.

1. Pilih kotak di samping tulisan Microsoft Defender untuk Cloud.  Jendela terbuka di sisi kanan laman.  Pilih **Buka laman konektor**.

1. Perhatikan instruksi konfigurasi  Pilih kotak di samping nama langganan, lalu pilih **Koneksi**.  Jendela pop-op mungkin muncul yang menunjukkan bahwa hanya langganan tempat Anda memiliki izin Pembaca Keamanan yang akan memulai streaming pemberitahuan Microsoft Defender untuk Cloud.  Pilih **OK**.  Status akan berpindah ke tersambung.  Sekarang, konektor diaktifkan, meskipun mungkin perlu beberapa waktu agar konektor muncul di laman konektor data.  

1. Sekarang lihat informasi tentang aturan analitik.  Dari bagian atas laman (di bilah), pilih **Microsoft Defender untuk Cloud**. Batalkan pilih kotak di samping tempat yang tertulis Microsoft Defender untuk Cloud, karena Anda telah mengonfigurasi konektor (mungkin perlu beberapa waktu agar ikon peringatan menghilang). Pilih kotak di samping tulisan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**. Di jendela yang terbuka, Anda akan melihat informasi tentang aturan dan apa yang dilakukannya.  
    1. CATATAN: Detail logika aturan berada di luar cakupan dasar, membahas langkah-langkah untuk mengonfigurasi aturan untuk melihat jenis informasi yang dapat dikonfigurasi sebagai bagian dari aturan. Pilih **Konfigurasi**.
    1. Pilih aturan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**.
    1. Dari jendela yang terbuka di sisi kanan laman, pilih **Buat aturan**.
    1. Buka setiap laman konfigurasi, lalu pilih **Tinjau dan buat**, lalu pilih **Simpan**.

1. Kembali ke laman Sentinel dengan memilih **Microsoft Sentinel | Hub konten** dari bilah di bagian atas laman, di atas tulisan aturan Analitik.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.


### Tugas 4

Dalam tugas ini, Anda akan menelusuri beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari bagian atas laman, pilih tab **Kueri**. Baca deskripsi tentang apa itu kueri hunting. Kueri hunting dapat ditambahkan melalui Hub Konten. Setiap kueri yang sebelumnya diinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan kueri baik sebagai bagian dari solusi atau sebagai kueri mandiri.  Gulir ke bawah untuk melihat opsi yang tersedia. Tutup Konten hub dengan memilih **X** di pojok kanan atas jendela.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi kanan jauh jendela untuk melihat panel informasi.

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Dari sisi kanan layar, pilih **Onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda. Gulir ke bawah ke bagian README.md dan tinjau deskripsinya. Kembali ke tab Azure di browser Anda.

1. Dari panel navigasi kiri, pilih **Analitik**.  Di sana, ada dua aturan aktif, satu yang tersedia secara default dan aturan yang Anda buat di tugas sebelumnya. Pilih aturan **Deteksi Serangan Multitahap Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi kanan jauh jendela untuk melihat panel informasi.

1. Dari panel navigasi kiri, pilih **Otomatisasi**.  Di sini Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi kiri, pilih **Buku kerja**. Baca deskripsi tentang apa itu buku kerja Microsoft Sentinel.  Buku kerja dapat ditambahkan melalui Hub Konten. Setiap buku kerja yang sebelumnya diinstal akan dicantumkan di sini. Pilih **Buka hub konten**.  Hub konten mencantumkan konten yang menyertakan buku kerja baik sebagai bagian dari solusi maupun sebagai buku kerja mandiri. Gulir ke bawah untuk melihat opsi yang tersedia.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.

1. Keluar dan tutup semua tab browser yang terbuka.

### Tinjauan

Dalam demo ini, Anda telah mempelajari langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan mempelajari beberapa opsi yang tersedia di Microsoft Sentinel.
