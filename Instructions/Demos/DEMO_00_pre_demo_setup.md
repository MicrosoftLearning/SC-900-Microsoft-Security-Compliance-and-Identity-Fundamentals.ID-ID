<!---
---
Penyiapan Pra-Demo: Judul: 'Penyiapan Demo'
---
--->

## Penyewa WWL - Ketentuan penggunaan
Jika Anda diberikan penyewa sebagai bagian dari pengiriman pelatihan yang dipimpin instruktur, harap dicatat bahwa penyewa tersedia untuk tujuan mendukung lab langsung dalam pelatihan yang dipimpin instruktur.

Penyewa tidak boleh dibagikan atau digunakan untuk tujuan di luar lab langsung. Penyewa yang digunakan dalam kursus ini adalah penyewa uji coba dan tidak dapat digunakan atau diakses setelah kelas berakhir dan tidak memenuhi syarat untuk ekstensi.

Penyewa tidak boleh dikonversi ke langganan berbayar. Penyewa yang diperoleh sebagai bagian dari kursus ini tetap menjadi milik Microsoft Corporation dan kami berhak untuk mendapatkan akses dan repositori kapan saja.

## Penyiapan Pra-Demo Penyewa Microsoft 365

### Mengaktifkan log audit Microsoft 365

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan log Audit di Microsoft 365.  Meskipun dokumentasi menunjukkan bahwa log audit diaktifkan secara default, sebagian besar penyewa lab tidak mengaktifkan fitur ini, dan perlu waktu beberapa jam untuk menerapkannya.  Mengaktifkan fitur ini bermanfaat, karena Microsoft 365 menggunakan log audit untuk wawasan pengguna dan aktivitas yang diidentifikasi dalam kebijakan dan wawasan analitik.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **https://admin.microsoft.com**.

1. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh hoster lab resmi (ALH) Anda.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi sebelah kiri portal kepatuhan Microsoft Purview, pilih **Tampilkan semua**.

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.  Catatan: fungsi audit juga dapat diakses melalui halaman beranda Pertahanan Microsoft 365.

1. Pastikan bahwa tab **Search** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah warna biru di bagian atas halaman yang menyatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak diperlukan tindakan lebih lanjut.

1. Kembali ke beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi sebelah kiri.

### Microsoft Defender for Cloud Apps pemantauan file

Dalam tugas penyetelan ini, Anda akan mengaktifkan pemantauan file di Microsoft Defender for Cloud Apps.

1. Buka tab browser untuk pusat admin Microsoft 365.  Jika sebelumnya Anda menutupnya, buka tab browser baru dan di bilah alamat, masukkan **https://admin.microsoft.com** dan dari panel navigasi kiri pusat admin Microsoft 365, pilih **Perlihatkan semua**.

1. Di Pusat admin, pilih **Security**.  Halaman browser baru terbuka ke halaman selamat datang di portal Pertahanan Microsoft 365.  

1. Dari panel navigasi kiri, pilih **File**, yang tercantum di bawah Aplikasi cloud.

1. Jika belum diaktifkan, Anda harus memilih **Aktifkan pemantauan file** dan pilih kotak di samping tempatnya **berbunyi Aktifkan pemantauan file** lalu pilih **Simpan**.  

1. Dari panel navigasi kiri, di bawah aplikasi cloud, pilih **File** untuk kembali ke halaman file.  Jika Anda berhasil mengaktifkan pemantauan file, Anda akan melihat opsi filter di bagian atas halaman.  Mungkin perlu beberapa waktu agar file dari penyewa lab yang telah dikonfigurasi sebelumnya ditampilkan.

## Penyiapan Pra-Demo langganan Azure Cloud Slice

Untuk penyiapan ini, Anda menggunakan lingkungan Azure Cloud Slice yang terpisah dari penyewa Microsoft 365 yang disediakan. Keluar dari Penyewa Microsoft 365 dan masuk menggunakan kredensial Azure Cloud Slice.

### Komputer virtual Azure

Periksa apakah VM telah dibuat. Jika tidak, maka siapkan sekarang. Anda akan menggunakan VM sebagai bagian dari demo NSG.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com** dan masuk dengan kredensial Azure yang disediakan oleh hoster lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian biru di bagian atas halaman, masukkan **Virtual Machines** lalu pilih **Virtual Machines** dari hasil pencarian.

1. Jika VM sudah tercantum, lewati langkah-langkah berikut, jika tidak, Anda harus membuatnya.  Pilih **Buat**, lalu dari menu drop-down, pilih **Komputer virtual Azure**. Konfigurasikan parameter berikut (jika parameter tidak tercantum, biarkan nilai default).
    1. Grup sumber daya: Pilih **Buat baru** dan masukkan **LabsSC900**, lalu pilih **OK**.
    1. Nama komputer virtual: masukkan **SC900-WinVM**.
    1. Opsi ketersediaan: Dari menu drop-down, pilih **Tidak diperlukan redundansi infrastruktur**.
    1. Gambar: Dari menu drop-down pilih **Windows 11 Pro, versi 22H2 - x64 Gen2** (atau gambar Windows 10 atau Jendela 11 yang tercantum).
    1. Ukuran: pilih **Lihat semua ukuran** dan pilih **Standard_B1s** lalu pilih **Pilih** di bagian bawah halaman.
    1. Nama pengguna: masukkan **SC900-VM-User**
    1. Kata sandi: masukkan kata sandi dan tuliskan, Anda akan membutuhkannya nanti!!!
    1. Konfirmasi kata sandi: masukkan kembali kata sandi.
    1. Port masuk publik: **Tidak ada**.
    1. Lisensi: pilih tempat yang tertulis, "Saya mengonfirmasi bahwa saya memiliki lisensi Windows 10/11 yang memenuhi syarat dengan hak hosting multi-penyewa."  Tanda centang akan muncul.
    1. Pilih **Berikutnya: Disk**
    1. Jenis disk OS: dari menu drop-down, pilih **SSD Standar**.
    1. Pilih **Berikutnya: Jaringan**
    1. Kelompok keamanan jaringan NIC: pilih **Tidak Ada**.  Anda akan membuat NSG sebagai bagian dari demo, jadi jangan lakukan di sini!
    1. Hapus IP publik dan NIC saat VM dihapus: pilih kotak sehingga tanda centang muncul.
    1. Pilih **Tinjau + buat**, lalu saat validasi lolos, pilih **Buat**.
    1. Setelah penyebaran VM selesai, pilih **Beranda** dari bagian atas halaman.

1. Biarkan tab browser Azure tetap terbuka untuk melanjutkan penyiapan pra-demo.

### Grup keamanan jaringan

Periksa apakah NSG telah dibuat. Jika NSG belum dibuat, siapkan sekarang, tetapi jangan kaitkan antarmuka apa pun ke sana atau buat aturan apa pun. Langkah-langkah tersebut akan dilakukan sebagai bagian dari demo NSG.

1. Di bilah pencarian warna biru di bagian atas halaman, masukkan grup **Kelompok keamanan jaringan** . Dari hasil, pilih **Kelompok keamanan jaringan** (jangan pilih Kelompok keamanan jaringan klasik).

1. Pilih **Buat grup keamanan jaringan**. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh authorized lab hoster)
    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Review + create**, lalu pilih **Create**.
    1. Setelah penyebaran selesai (ini terjadi sangat cepat), pilih **Buka sumber daya**.

### Microsoft Defender for Cloud

Tujuannya di sini hanyalah untuk mengakses Microsoft Defender ke Cloud untuk pertama kalinya. Ini penting karena diperlukan waktu hingga 24 jam bagi Defender untuk Cloud untuk mencerminkan skor aman awal.  

1. Buka tab Home-Microsoft Azure di browser Anda.

1. Di bilah pencarian berwarna biru, masukkan **Microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini adalah pertama kalinya Anda memasuki Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka halaman Memulai, dan mungkin akan diminta untuk melakukan peningkatan.  Gulir ke bagian bawah halaman dan pilih **Lewati**.  Anda akan dibawa ke halaman Ringkasan.

1. Semua langganan memiliki CSPM dasar yang diaktifkan secara default, yang menyediakan skor aman, tetapi dapat memakan waktu hingga 24 jam bagi Defender untuk Cloud untuk mencerminkan skor aman awal.

1. Pilih **Beranda** dari bagian atas halaman.

1. Biarkan tab browser terbuka untuk melanjutkan penyiapan pra-demo.

### Microsoft Sentinel

Periksa apakah instans Microsoft Sentinel telah dibuat. Jika tidak, maka siapkan sekarang karena Anda akan membutuhkannya sebagai bagian dari demo walk-through di Microsoft Sentinel.

1. Buka tab Home-Microsoft Azure di browser Anda.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan: Biarkan diatur ke default.
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Wilayah: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda).
    1. Pilih **Tinjau + Buat** (tidak ada tag yang akan dikonfigurasi).
    1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.
    1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman Berita & panduan akan ditampilkan, menunjukkan bahwa uji coba gratis Microsoft Sentinel telah diaktifkan.  Pilih**OK**.

### Tinjau

Dalam penyiapan ini, Anda mengaktifkan kemampuan log audit di penyewa Microsoft 365 dan Anda juga membuat verifikasi bahwa VM telah dikonfigurasi sebelumnya di lingkungan Azure Cloud Slice Anda. Anda juga menyiapkan lingkungan Defender for Cloud dan Microsoft Sentinel.
