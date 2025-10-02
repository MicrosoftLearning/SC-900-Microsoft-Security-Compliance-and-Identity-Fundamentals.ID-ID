---
lab:
  title: Menjelajahi Microsoft Sentinel
  module: Describe the security capabilities of Microsoft Sentinel
---

# Lab: Menjelajahi Microsoft Sentinel

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan Microsoft Sentinel
- Unit: Menjelaskan kemampuan mitigasi dan deteksi ancaman di Microsoft Sentinel

## Skenario lab

Di lab ini, Anda akan menelusuri proses pembuatan instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan melakukan penelusuran singkat beberapa kemampuan utama yang tersedia di Microsoft Sentinel.

**Perkiraan Waktu**: 60 menit

### Tugas 1

Untuk membuat instans Microsoft Azure Sentinel, Anda harus terlebih dahulu membuat ruang kerja Analitik Log, yang digunakan untuk menyimpan data dari Microsoft Azure Sentinel.  Setelah memiliki ruang kerja Analitik Log, Anda dapat membuat instans Microsoft Sentinel dan menambahkan ruang kerja analitik log ke dalamnya.  Dalam tugas ini Anda menjalankan setiap langkah ini.

1. Anda berada di beranda layanan Azure.  Jika tidak, buka Microsoft Edge dan di bilah alamat, masukkan **portal.azure.com**, dan masuk dengan kredensial admin Portal Microsoft Azure Anda.

1. Di kotak pencarian biru di bagian atas halaman, masukkan **Analitik** Log dan pilih dari hasil pencarian.
1. Pilih **+ Buat.**
1. Dari tab Dasar di Buat ruang kerja Analitik Log, masukkan berikut ini:
    1. Langganan: biarkan default, ini adalah langganan Azure yang disediakan oleh Authorized Lab Hoster (ALH).
    1. Grup sumber daya: pilih **SC900-Sentinel-RG**. Jika grup sumber daya ini tidak tercantum, buat dengan memilih Buat baru **, masukkan **SC900-Sentinel-RG**, lalu pilih **OK**.**
    1. Nama: **SC900-Sentinel-workspace**.
    1. Wilayah: **AS Timur** (Ada wilayah default lain yang mungkin dipilih sesuai lokasi Anda).
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Buat**.
    1. Mungkin perlu waktu satu atau dua menit agar ruang kerja baru dibuat.
    1. Setelah dibuat, pilih **Buka sumber daya** untuk melihat informasi tentang ruang kerja.
1. Pada titik ini, instans Microsoft Sentinel belum dibuat. Untuk membuat instans Sentinel, Anda harus membuka halaman Microsoft Azure Sentinel. Gunakan bilah pencarian biru di bagian atas halaman, untuk **mencari Microsoft Azure Sentinel** dan memilihnya dari hasil pencarian.
1. Untuk menambahkan ruang kerja ke Microsoft Azure Sentinel, Anda harus masuk ke halaman Microsoft Azure Sentinel. Gunakan bilah pencarian biru di bagian atas halaman, untuk **mencari Microsoft Azure Sentinel**
    1. Dari halaman Microsoft Azure Sentinel, pilih **+ Buat**.
    1. Sekarang Anda dapat menambahkan ruang kerja yang baru saja Anda buat. Pilih **SC900-Sentinel-workspace**, lalu pilih **Tambahkan**.  Ini mungkin memakan waktu beberapa menit, karena uji coba gratis Microsoft Sentinel diaktifkan.  Setelah diaktifkan, Anda memilih **Ok**.
1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Tugas 2

Dengan instans Microsoft Sentinel yang dibuat dan ruang kerja Log Analytics yang ditetapkan padanya, penting bagi pengguna yang akan bertanggung jawab untuk mendukung Microsoft Azure Sentinel memiliki izin yang diperlukan.  Hal ini dilakukan dengan menetapkan izin peran yang diperlukan kepada pengguna yang ditunjuk.  Dalam tugas ini, Anda akan melihat peran Microsoft Sentinel bawaan yang tersedia.

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

1. Dari beranda layanan Azure, pilih Microsoft Azure Sentinel, lalu pilih instans yang Anda buat, **SC900-Sentinel-workspace**.

1. Dari panel navigasi kiri, perluas **Manajemen** Konten lalu pilih **Hub konten**.

1. Luangkan waktu sejenak untuk menggulir ke bawah guna melihat daftar lengkap solusi yang tersedia dan opsi untuk memfilter daftar.  Untuk tugas ini, kita mencari **Microsoft Defender untuk Cloud**.  Pilihlah dari daftar.  Di jendela samping yang terbuka, baca deskripsi, lalu pilih **Instal**.  Setelah penginstalan selesai, kolom status di jendela utama akan ditampilkan sebagai terinstal.

1. Sekali lagi, pilih **Microsoft Defender untuk Cloud** dari daftar. Dari jendela di sebelah kanan, pilih **Kelola**.

1. Di sisi kanan halaman Microsoft Defender untuk Cloud adalah deskripsi dan catatan yang terkait dengan solusi dari Content Hub dan apa yang disertakan sebagai bagian dari solusi ini.  Di jendela utama adalah komponen solusi.  Dalam hal ini ada dua konektor data dan satu aturan data. Segitiga oranye menunjukkan bahwa beberapa konfigurasi diperlukan. Pilih kotak di samping tempat berbunyi **Microsoft Defender untuk Cloud (Legacy) berbasis Langganan**.  Jendela terbuka di sisi kanan laman.  Pilih **Buka laman konektor**.

1. Perhatikan instruksi konfigurasi  Pilih kotak di samping nama langganan, lalu pilih **Koneksi**.  Jendela pop-op mungkin muncul yang menunjukkan bahwa hanya langganan tempat Anda memiliki izin Pembaca Keamanan yang akan memulai streaming pemberitahuan Microsoft Defender untuk Cloud.  Pilih **OK**.  Status akan berpindah ke tersambung.  Sekarang, konektor diaktifkan, meskipun mungkin perlu beberapa waktu agar konektor muncul di laman konektor data.  

1. Sekarang lihat informasi tentang aturan analitik.  Dari bagian atas laman (di bilah), pilih **Microsoft Defender untuk Cloud**. Batalkan pilih kotak di samping tempat yang tertulis Microsoft Defender untuk Cloud, karena Anda telah mengonfigurasi konektor (mungkin perlu beberapa waktu agar ikon peringatan menghilang). Pilih kotak di samping tulisan **Deteksi Aktivitas Penghapusan CoreBackUp dari pemberitahuan keamanan terkait**.  Ini memunculkan halaman Aturan Analitik.  Sekali lagi, pilih **Deteksi Aktivitas Penghapusan CoreBackUp dari aturan pemberitahuan keamanan terkait**. Jendela yang terbuka di sebelah kanan, yang menyediakan informasi tentang aturan dan apa yang dilakukannya.  Pilih **Buat aturan**.  
    1. Meskipun detail logika aturan berada di luar lingkup dasar-dasar, buka setiap tab dalam pembuatan aturan untuk melihat jenis informasi yang dapat dikonfigurasi
    1. Saat Anda mencapai tab Tinjau + buat, pilih **Simpan**.

1. Kembali ke laman Sentinel dengan memilih **Microsoft Sentinel | Hub konten** dari bilah di bagian atas laman, di atas tulisan aturan Analitik.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.


### Tugas 4

Dalam tugas ini, Anda akan menelusuri beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi kiri, perluas **Manajemen ancaman** dan jelajahi opsi yang tercantum dalam manajemen ancaman.
    1. Pilih **Insiden**.  Meskipun tidak ada insiden yang ditemukan, tinjau **bagian Apa itu?**
    1. Pilih **Berburu** lalu tinjau informasi yang disediakan di tab **Berburu (Pratinjau)** .
    1. Pilih **Buku Catatan** dan tinjau **bagian Apa itu?**
    1. Pilih **Inteligensi ancaman** dan tinjau informasi di halaman.
    1. Pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi kanan jauh jendela untuk melihat panel informasi.

1. Dari panel navigasi kiri, perluas **Manajemen** Konten, lalu pilih **Komunitas**. Halaman komunitas mencakup wawasan dan pembaruan keamanan Cyber dari Microsoft Research, tautan ke daftar Blog Microsoft Azure Sentinel, tautan ke Forum Microsoft Sentinel, menautkan edisi terbaru ke Microsoft Sentinel Hub, dan banyak lagi. Jelajahi ini sesuka hati.


1. Dari panel navigasi kiri, perluas **Konfigurasi** dan jelajahi opsi yang tercantum:
    1. pilih **Analitik**.  Di sana, ada dua aturan aktif, satu yang tersedia secara default dan aturan yang Anda buat di tugas sebelumnya. Pilih aturan **Deteksi Serangan Multitahap Tingkat Lanjut**.  Tinjau informasi terperinci. **Catatan**: Anda mungkin perlu memilih "**<<**" di sisi kanan jauh jendela untuk melihat panel informasi.
    1. Dari panel navigasi kiri, pilih **Otomatisasi**.  Di sini, Anda dapat membuat aturan otomatisasi sederhana, mengintegrasikan dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat**, lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat syarat dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Tutup jendela dengan memilih **X** di pojok kanan atas jendela.

1. Dari sudut kiri atas jendela, di banner biru, pilih **Microsoft Azure** untuk kembali ke halaman beranda portal Azure.

1. Keluar dan tutup semua tab browser yang terbuka.

### Tinjauan

Di lab ini Anda menelusuri langkah-langkah untuk menyambungkan Microsoft Sentinel ke sumber data, Anda menyiapkan buku kerja, dan memandu beberapa opsi yang tersedia di Microsoft Azure Sentinel.
