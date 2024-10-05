---
lab:
  title: Menjelajahi Microsoft Defender untuk Cloud
  module: Describe the security management capabilities of Azure
---

# Lab : Menjelajahi Microsoft Defender untuk Cloud

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan manajemen keamanan Azure
- Unit: Menjelaskan manajemen postur keamanan cloud

## Skenario lab

Di lab ini, Anda akan menjelajahi Microsoft Defender untuk Cloud.  CATATAN: langganan Azure yang disediakan oleh Hoster Lab Resmi (ALH) membatasi akses dan mungkin memerlukan waktu yang lebih lama dari biasanya.

**Perkiraan Waktu:**: 30 menit

### Tugas 1

Dalam tugas ini, Anda akan melakukan penelusuran tingkat tinggi dari beberapa kemampuan Microsoft Defender untuk Cloud

1. Anda berada di beranda layanan Azure.  Jika sebelumnya Anda menutup browser, buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**, dan masuk dengan kredensial admin Anda. Jika sebelumnya Anda telah mencatat, Anda mungkin diminta untuk bentuk autentikasi sekunder, sebagai par dari MFA.  Jika sebelumnya Anda belum masuk, Anda mungkin diminta untuk menyiapkan MFA.  Ikuti perintah di layar untuk menyiapkan MFA.

1. Di bilah pencarian berwarna biru, masukkan **Microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini pertama kalinya Anda memasuki Microsoft Defender untuk Cloud dengan langganan, Anda dapat diarahkan ke laman Memulai dan mungkin akan diminta untuk melakukan peningkatan.  Gulir ke bagian bawah laman dan pilih **Ingatkan saya nanti** (atau **Lewati**).  Anda akan dibawa ke laman Ikhtisar.

1. Dari laman Ikhtisar Microsoft Defender untuk Cloud, perhatikan informasi yang tersedia di laman tersebut (jika Anda melihat 0 sumber daya yang dinilai dan rekomendasi aktif, refresh laman browser, mungkin perlu waktu beberapa menit).  Informasi di bagian atas laman mencakup jumlah langganan Azure, jumlah sumber daya yang dinilai, jumlah rekomendasi aktif, dan peringatan keamanan.  Di bagian utama laman, terdapat kartu yang mewakili Postur keamanan, Kepatuhan peraturan, Wawasan, dan banyak lagi.  Catatan: Inisiatif kebijakan default Microsoft Defender untuk Cloud, yang biasanya harus ditetapkan oleh admin, telah ditetapkan sebagai bagian dari penyiapan langganan Azure. Namun, skor aman akan ditampilkan sebagai 0% karena memerlukan waktu hingga 24 jam bagi Azure untuk mencerminkan skor awal.

1. Dari bagian atas laman, pilih **Sumber daya yang dinilai**. 
    1. Tindakan ini membawa Anda ke laman **Inventaris** yang mencantumkan sumber daya saat ini. Pilih sumber daya komputer virtual, **sc900-winvm**. Sumber daya ini dikaitkan dengan mesin virtual yang Anda gunakan di lab sebelumnya.
    1. Laman Kesehatan sumber daya untuk VM menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih salah satu item dari daftar yang menunjukkan status **tidak sehat**.
    1. Perhatikan detail deskripsi.  Pilih panah menurun di samping langkah-langkah Remediasi. Perhatikan bagaimana petunjuk perbaikan (atau tautan ke petunjuk) disediakan bersama dengan opsi untuk mengambil tindakan.  Keluar dari jendela tanpa melakukan tindakan apa pun.
    1. Kembali ke laman ikhtisar Microsoft Defender untuk Cloud, dengan memilih **Microsoft Defender untuk Cloud | Ikhtisar** dari bagian atas laman, di bagian atas yang bertuliskan Kesehatan sumber daya.

1. Dari panel navigasi kiri, pilih **Rekomendasi**.  
    1. Pastikan tab **Semua rekomendasi** dipilih (digarisbawahi).  Perhatikan tampilan dasbor yang menunjukkan Rekomendasi aktif berdasarkan tingkat keparahan, Kesehatan sumber daya, dan banyak lagi.
    1. Dari daftar, pilih salah satu.  Di laman yang terbuka, Anda akan melihat deskripsi dan informasi tambahan yang dapat mencakup langkah remediasi, sumber daya yang terpengaruh, dan banyak lagi. Keluar dari laman ini dengan memilih **X** di pojok kanan atas layar,

1. Dari panel navigasi kiri utama, pilih **Kepatuhan peraturan**.  **CATATAN**: Jika Anda melihat tidak ada langganan untuk menghitung kepatuhan, itu karena mungkin ada penundaan hingga 24 jam agar informasi itu muncul. Beralih ke Tugas 2.  Jika Anda melihat informasi, lanjutkan dengan langkah-langkah berikut.
    1. Laman kepatuhan peraturan menyediakan daftar kontrol kepatuhan berdasarkan tolok ukur keamanan cloud Microsoft (pastikan tab tolok ukur keamanan cloud Microsoft dipilih/digarisbawahi). Pada setiap domain kontrol terdapat subset kontrol dan untuk setiap kontrol, ada satu atau banyak penilaian. Setiap penilaian memberikan informasi termasuk deskripsi, remediasi, dan sumber daya yang terpengaruh.
    1. Mari jelajahi salah satu area domain kontrol. Pilih (bentangkan) **NS. Keamanan Jaringan**. Daftar kontrol yang terkait dengan keamanan jaringan ditampilkan.
    1. Pilih **NS-10. Memastikan keamanan Sistem Nama Domain (DNS)**. Perhatikan daftar penilaian otomatis (yang mencakup penilaian otomatis untuk AWS) dan bagaimana setiap item baris penilaian memberikan informasi termasuk jenis sumber daya, sumber daya yang gagal, dan stasiun kepatuhan. Pilih penilaian yang tercantum.  Di sini, Anda melihat informasi termasuk deskripsi, langkah-langkah Remediasi, dan Sumber daya yang terpengaruh.
    1. Pilih **X** di pojok kanan atas layar untuk menutup laman itu.
    1. Pilih **Ikhtisar** dari panel navigasi kiri untuk kembali ke laman Ikhtisar Microsoft Defender untuk Cloud.
    1. Biarkan laman ikhtisar Microsoft Defender untuk Cloud tetap terbuka, yang akan Anda gunakan di tugas berikutnya.

### Tugas 2

Perlu diperhatikan bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang disempurnakan (gratis) dan dengan fitur keamanan yang disempurnakan yang tersedia melalui paket Microsoft Defender untuk Cloud. Dalam tugas ini, Anda akan menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.

1. Dari halaman ringkasan Microsoft Defender untuk Cloud, perluas **Manajemen** dan pilih **Pengaturan** lingkungan dari panel navigasi kiri.
1. Pilih kotak **Bentangkan semua**, lalu pilih langganan **MOC--lodXXXXXXXX** yang tercantum di sebelah ikon tombol kuning.
1. Pada laman paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih beberapa paket Defender. 
    1. Pastikan status CSPM diatur ke **Aktif**. Jika belum, atur sekarang.  
    1. Aktifkan paket untuk Server.  Pilih **Aktif** untuk item baris Server, lalu pilih **Simpan** dari bagian atas halaman.
1. Dari sudut kiri atas jendela, tepat di bawah bilah biru sebelah tulisan Microsoft Azure, pilih **Beranda** untuk kembali ke laman beranda layanan Azure.
1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tinjauan

Di lab ini, Anda telah menjelajahi Microsoft Defender untuk Cloud.
