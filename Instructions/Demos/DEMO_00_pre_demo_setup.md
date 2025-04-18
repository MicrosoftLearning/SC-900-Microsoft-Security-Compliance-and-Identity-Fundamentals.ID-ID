<!---
---
Penyiapan Pra-Demo: Judul: 'Penyiapan Demo'
---
--->

## Penyewa WWL - Ketentuan penggunaan

Jika Anda diberikan penyewa sebagai bagian dari penyajian pelatihan yang dipimpin instruktur, harap diperhatikan bahwa penyewa tersedia untuk mendukung lab praktik dalam pelatihan yang dipimpin instruktur.

Penyewa tidak boleh dibagikan atau digunakan untuk tujuan di luar lab praktik. Penyewa yang digunakan dalam kursus ini adalah penyewa uji coba dan tidak dapat digunakan atau diakses setelah kelas berakhir dan tidak memenuhi syarat perpanjangan.

Penyewa tidak boleh dikonversi ke langganan berbayar. Penyewa yang diperoleh sebagai bagian dari kursus ini tetap menjadi milik Microsoft Corporation dan kami berhak mendapatkan akses dan repositorinya kapan saja.

## Penyiapan Pra-Demo Penyewa Microsoft 365

### Mengaktifkan log audit Microsoft 365 dan pemantauan file

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan Log audit dan pemantauan file di Microsoft 365.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **https://admin.microsoft.com**.

1. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Keamanan**.  Halaman browser baru terbuka ke halaman selamat datang Pertahanan Microsoft.  

1. Dari panel navigasi sebelah kiri portal kepatuhan Microsoft Purview, pilih **Tampilkan semua**.

1. Di panel navigasi kiri, gulir ke bawah dan perluas **Sistem**.  Dari daftar yang diperluas, pilih **Audit**.  Catatan: fungsionalitas audit juga dapat diakses melalui portal Microsoft Purview.

1. Setelah Anda masuk ke halaman Audit, tunggu 1-2 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas laman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Mulai merekam aktivitas pengguna dan admin**.  Setelah audit diaktifkan, bilah biru menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.  Jika Anda melihat pesan, "Maaf, kami mengalami masalah saat mencari tahu apakah aktivitas sedang direkam. Coba refresh halaman," dan tidak ada perubahan setelah me-refresh halaman, Anda harus mengaktifkan audit melalui PowerShell.
    1. Pilih kanan ikon Windows PowerShell biru pada taskbar dan pilih **Jalankan sebagai administrator**.
    1. Untuk mengonfirmasi bahwa modul Exchange Online PowerShell diinstal di komputer, masukkan **`Get-InstalledModule ExchangeOnlineManagement | Format-List Name,Version,InstalledLocation`**.  Anda akan melihat nama, versi, dan lokasi terinstal Exchange OnlineManagement.
    1. Sekarang muat modul, dengan memasukkan **`Import-Module ExchangeOnlineManagement`**.
    1. Untuk menyambungkan, masukkan **`Connect-ExchangeOnline -UserPrincipalName admin@WWLxZZZZZZ.onmicrosoft.com`**.  Untuk UPN, masukkan nama pengguna administrator yang ditemukan di tab sumber daya lab Anda.
    1. Anda akan diminta untuk masuk.  Masukkan nama pengguna dan kata sandi administratif yang ditemukan di tab sumber daya lab Anda.
    1. Untuk mengaktifkan Audit, masukkan **`Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true`**. Pesan ditampilkan yang mengatakan bahwa mungkin perlu waktu hingga 60 menit agar perubahan diterapkan.
    1. Meskipun mungkin perlu waktu hingga 60 menit untuk diterapkan, Anda dapat memverifikasi bahwa perintah diterima dengan memasukkan **`Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled`**.  Jika audit diaktifkan, properti UnifiedAuditLogIngestionEnabled akan menampilkan nilai true.

1. Dari panel navigasi kiri, di bawah Sistem, pilih **Pengaturan**.

1. Dari halaman pengaturan, pilih **Aplikasi cloud**.   Gulir ke bawah, lalu di bawah Perlindungan Informasi pilih **File**.

1. Jika belum diaktifkan, pilih kotak di samping tempatnya berbunyi **Aktifkan pemantauan** file lalu pilih **Simpan**.  

### Mengonfigurasi peran administrator Kepatuhan

Dalam tugas penyiapan ini, Anda akan menambahkan diri Anda sendiri, sebagai administrator MOD, ke grup peran Administrator kepatuhan.

1. Buka tab browser Microsoft Edge baru. Di bilah alamat, masukkan **https://purview.microsoft.com**. Untuk mengakses portal Microsoft Purview baru, pilih kotak di samping tempat yang tertulis, **saya menyetujui ketentuan pengungkapan aliran data dan Pernyataan** Privasi, lalu pilih **Mulai**.  
1. Dari panel navigasi kiri, pilih **Pengaturan**.
1. Dari panel navigasi yang terbuka, pilih **Peran dan cakupan** untuk memperluas opsi, lalu pilih **Grup** peran.
1. Di kotak pencarian di sisi kanan layar, cari pada istilah **Kepatuhan**.  Pilih **Administrator** Kepatuhan.
    1. Pilih **Edit**.
    1. Pilih **Pilih pengguna**.
    1. Cari Administrator MOD, pilih kotak di samping **Administrator** MOD lalu pilih tombol **Pilih** di bagian bawah halaman.
    1. Pilih **Berikutnya** lalu pilih **Simpan**, lalu akhirnya pilih **Selesai**.
1. Ini menyimpulkan penyiapan untuk penyewa Microsoft 365, Anda dapat menutup tab browser.

## Penyiapan Pra-Demo langganan Azure

Untuk penyiapan ini, Anda menggunakan lingkungan Azure yang terpisah dari penyewa Microsoft 365 yang disediakan. Keluar dari Penyewa Microsoft 365 dan masuk menggunakan kredensial Azure.

### Mesin virtual Azure

Periksa apakah VM telah dibuat. Jika belum, siapkan sekarang. Anda akan menggunakan VM sebagai bagian dari demo NSG.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com** dan masuk dengan kredensial Azure yang disediakan oleh host lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian warna biru di bagian atas laman, masukkan **Mesin Virtual**, lalu pilih **Mesin Virtual** dari hasil pencarian.

1. Jika VM sudah tercantum, lewati langkah-langkah berikut. Jika belum, Anda harus membuatnya.  Pilih **Buat**, lalu dari menu menurun, pilih **Azure Virtual machine**. Konfigurasikan parameter berikut (jika parameter tidak tercantum, biarkan nilai default).
    1. Grup sumber daya: pilih **Buat baru** dan masukkan **LabsSC900**, lalu pilih **OK**.
    1. Nama mesin virtual: masukkan **SC900-WinVM**.
    1. Opsi ketersediaan: Dari menu menurun, pilih **Tidak diperlukan redundansi infrastruktur**.
    1. Jenis keamanan: dari menu drop-down, pilih **Standar**.
    1. Gambar: Dari menu menurun, pilih **Windows 11 Pro, versi 22H2 - x64 Gen2** (atau gambar Windows 10 atau Window 11 yang tercantum).
    1. Ukuran: pilih **Lihat semua ukuran** dan pilih **Standard_B1s**, lalu pilih **Pilih** di bagian bawah laman.
    1. Nama pengguna: masukkan **SC900-VM-User**
    1. Kata sandi: masukkan kata sandi dan tuliskan, Anda akan membutuhkannya nanti!!!
    1. Konfirmasi kata sandi: masukkan kembali kata sandi.
    1. Port inbound publik: **Tidak ada**.
    1. Lisensi: pilih tulisan, “Saya mengonfirmasi bahwa saya memiliki lisensi Windows 10/11 yang memenuhi syarat dengan hak host multipenyewa.”  Tanda centang akan muncul.
    1. Pilih **Berikutnya: Disk**
    1. Jenis disk OS: dari menu menurun, pilih **SSD Standar**.
    1. Pilih **Berikutnya: Jaringan**
    1. Grup keamanan jaringan NIC: pilih **Tidak ada**.  Anda akan membuat NSG sebagai bagian dari demo, jadi jangan lakukan di sini!
    1. Hapus IP publik dan NIC saat VM dihapus: pilih kotak sehingga tanda centang muncul.
    1. Pilih **Tinjau + buat**, lalu saat validasi lolos, pilih **Buat**.
    1. Saat penyebaran VM selesai, pilih **Beranda** dari bagian atas laman.

1. Biarkan tab browser Azure tetap terbuka untuk melanjutkan penyiapan prademo.

### Grup keamanan jaringan

Periksa apakah NSG telah dibuat. Jika NSG belum dibuat, siapkan sekarang, tetapi jangan mengaitkan antarmuka apa pun dengannya atau membuat aturan apa pun. Langkah-langkah itu akan diselesaikan sebagai bagian dari demo NSG.

1. Di bilah pencarian warna biru di bagian atas laman, masukkan **Grup keamanan jaringan**. Dari hasil, pilih **Grup keamanan jaringan** (jangan pilih Grup keamanan jaringan klasik).

1. Pilih **Buat grup keamanan jaringan**. Pada tab Dasar di laman Buat grup keamanan jaringan, tentukan pengaturan berikut:
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh hoster lab resmi)
    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Tinjau + buat**, lalu pilih **Buat**.
    1. Saat penyebaran selesai (yang berlangsung sangat cepat), pilih **Buka sumber daya**.

### Microsoft Defender untuk Cloud

Tujuannya di sini hanyalah mengakses Microsoft Defender untuk Cloud untuk pertama kalinya. Ini penting karena dibutuhkan waktu hingga 24 jam agar Defender untuk Cloud mencerminkan skor aman awal.  

1. Buka tab Beranda - Microsoft Azure di browser Anda.

1. Di bilah pencarian berwarna biru, masukkan **Microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini adalah pertama kalinya Anda memasuki Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka laman Memulai, dan mungkin akan diminta untuk melakukan peningkatan.  Gulir ke bagian bawah laman dan pilih **Lewati**.  Anda akan dibawa ke laman Ringkasan.

1. Semua langganan memiliki CSPM dasar yang diaktifkan secara default, yang memberikan skor aman, tetapi dapat memakan waktu hingga 24 jam agar Defender untuk Cloud mencerminkan skor aman awal.

1. Pilih **Beranda** dari bagian atas laman.

1. Biarkan tab browser tetap terbuka untuk melanjutkan penyiapan prademo.

### Microsoft Sentinel

Periksa untuk memastikan bahwa instans Microsoft Azure Sentinel telah dibuat. Jika belum, siapkan sekarang karena Anda akan membutuhkannya sebagai bagian dari demo panduan di Microsoft Sentinel.

1. Buka tab Beranda - Microsoft Azure di browser Anda.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas laman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari laman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari laman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Dari tab Dasar di Buat ruang kerja Analitik Log, masukkan berikut ini:
    1. Langganan: Biarkan diatur ke default.
    1. Grup sumber daya: pilih **Buat Baru**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Wilayah: **AS Timur** (Ada wilayah default lain yang mungkin dipilih sesuai lokasi Anda).
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Buat**.
    1. Mungkin perlu waktu satu atau dua menit agar ruang kerja ne terdaftar, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Tambahkan**.

1. Setelah ruang kerja baru ditambahkan, laman Microsoft Sentinel | Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih **OK**.

### Tinjauan

Dalam penyiapan ini, Anda mengaktifkan kemampuan log audit di penyewa Microsoft 365 dan Anda juga membuat verifikasi bahwa VM telah dikonfigurasi sebelumnya di lingkungan Azure Anda. Anda juga telah menyiapkan lingkungan Defender untuk Cloud dan Microsoft Azure Sentinel.
