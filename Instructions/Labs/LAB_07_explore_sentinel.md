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

1. Setelah ruang kerja baru ditambahkan, laman Microsoft Sentinel | Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih **OK**.

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

Dalam demo ini, Anda telah mempelajari langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan mempelajari beberapa opsi yang tersedia di Microsoft Sentinel.
