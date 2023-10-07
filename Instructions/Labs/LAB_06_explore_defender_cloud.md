<!---
---
Lab: Judul: 'Jelajahi Microsoft Defender untuk Cloud' Jalur Pembelajaran/Modul/Unit: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 2: Menjelaskan kemampuan manajemen keamanan Azure; Unit 3: Menjelaskan manajemen postur keamanan cloud'
---
--->

# Lab: Menjelajahi Microsoft Defender untuk Cloud

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan manajemen keamanan Azure
- Unit: Menjelaskan manajemen postur keamanan cloud

## Skenario lab

Di lab ini, Anda akan menjelajahi Microsoft Defender untuk Cloud.  CATATAN: langganan Azure yang disediakan oleh Authorized Lab Hoster (ALH) membatasi akses dan mungkin memerlukan waktu yang lebih lama dari biasanya.

**Perkiraan Waktu**: 30 menit

### Tugas 1

Dalam tugas ini, Anda akan melakukan penelusuran tingkat tinggi dari beberapa kemampuan Microsoft Defender untuk Cloud

1. Anda harus menjadi halaman beranda untuk layanan Azure.  Jika sebelumnya Anda menutup browser, ppen Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**, dan masuk dengan kredensial admin Anda.

1. Di bilah pencarian berwarna biru, masukkan **Microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini adalah pertama kalinya Anda memasuki Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka halaman Memulai, dan mungkin akan diminta untuk melakukan peningkatan.  Gulir ke bagian bawah halaman dan pilih **Ingatkan saya nanti** (atau **Lewati**).  Anda akan dibawa ke halaman Ringkasan.

1. Dari halaman Gambaran Umum Microsoft Defender untuk Cloud, perhatikan informasi yang tersedia di halaman tersebut (jika Anda melihat 0 sumber daya yang dinilai dan rekomendasi aktif, refresh halaman browser, mungkin perlu waktu beberapa menit).  Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian utama halaman, terdapat kartu yang mewakili postur Keamanan, Kepatuhan terhadap peraturan, Wawasan, dan lainnya.  Catatan: Inisiatif kebijakan default Microsoft Defender untuk Cloud, yang biasanya harus ditetapkan oleh admin, telah ditetapkan sebagai bagian dari penyiapan langganan Azure. Namun, skor aman akan ditampilkan sebagai 0% karena memerlukan waktu hingga 24 jam bagi Azure untuk mencerminkan skor awal.

1. Dari bagian atas halaman, pilih **Assessed resources**. 
    1. Tindakan ini membawa Anda ke halaman **Inventaris** yang mencantumkan sumber daya saat ini. Pilih sumber daya mesin virtual, **sc900-winwm**. Sumber daya ini dikaitkan dengan mesin virtual yang Anda gunakan di lab sebelumnya.
    1. Halaman kesehatan Sumber Daya untuk VM menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih salah satu item dari daftar yang menunjukkan status **tidak sehat**.
    1. Perhatikan detail deskripsi.  Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana petunjuk perbaikan (atau tautan ke petunjuk) disediakan bersama dengan opsi untuk mengambil tindakan.  Keluar dari jendela tanpa melakukan tindakan apa pun.
    1. Kembali ke halaman ringkasan Microsoft Defender untuk Cloud, dengan memilih **Microsoft Defender untuk Cloud | Ringkasan** dari bagian atas halaman, di bagian atas yang bertuliskan Kesehatan sumber daya.

1. Dari panel navigasi kiri, pilih **Rekomendasi**.  
    1. Verifikasi, tab **Semua rekomendasi** dipilih (digarisbawahi).  Perhatikan tampilan dasbor yang menunjukkan Rekomendasi aktif berdasarkan tingkat keparahan, Kesehatan sumber daya, dan lainnya.
    1. Dari daftar, pilih item.  Di halaman yang terbuka, Anda akan melihat deskripsi dan informasi tambahan yang mungkin menyertakan langkah-langkah remediasi, sumber daya yang terpengaruh, dan lainnya. Keluar dari halaman ini, dengan memilih **X** di pojok kanan atas layar.

1. Dari panel navigasi kiri utama, pilih **Kepatuhan peraturan**.  **CATATAN**: Jika Anda melihat bahwa tidak ada langganan untuk menghitung kepatuhan, itu karena mungkin ada penundaan hingga 24 jam agar informasi muncul. Pindah ke Tugas 2.  Jika Anda melihat informasi, lanjutkan dengan langkah-langkah berikut.
    1. Halaman kepatuhan peraturan menyediakan daftar kontrol kepatuhan berdasarkan tolok ukur keamanan cloud Microsoft (pastikan bahwa tab tolok ukur keamanan cloud Microsoft dipilih/digarisbawahi). Di bawah setiap domain kontrol adalah subset dari kontrol dan untuk setiap kontrol ada satu atau lebih penilaian. Setiap penilaian memberikan informasi termasuk deskripsi, remediasi, dan sumber daya yang terpengaruh.
    1. Mari jelajahi salah satu area domain kontrol. Pilih (luaskan) **NS. Keamanan Jaringan**. Daftar kontrol yang terkait dengan keamanan jaringan ditampilkan.
    1. Pilih **NS-10. Pastikan keamanan Sistem Nama Domain (DNS).** Perhatikan daftar penilaian otomatis (yang mencakup penilaian otomatis untuk AWS) dan bagaimana setiap item baris penilaian memberikan informasi termasuk jenis sumber daya, sumber daya yang gagal, dan stasiun kepatuhan. Pilih penilaian yang tercantum.  Di sini Anda melihat informasi termasuk deskripsi, langkah-langkah Remediasi, dan sumber daya yang Terpengaruh.
    1. Pilih **X** di pojok kanan atas layar untuk menutup halaman.
    1. Pilih **Ringkasan** dari panel navigasi kiri untuk kembali ke halaman Ringkasan Microsoft Defender untuk Cloud.
    1. Biarkan halaman ringkasan Microsoft Defender untuk Cloud tetap terbuka, yang akan Anda gunakan di tugas berikutnya.

### Tugas 2

Perlu diperhatikan bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang disempurnakan (gratis) dan dengan fitur keamanan yang disempurnakan yang tersedia melalui paket Microsoft Defender untuk Cloud. Dalam tugas ini, Anda akan menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.

1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih **Pengaturan lingkungan** dari panel navigasi kiri.
1. Pilih kotak **Luaskan semua** lalu pilih langganan **MOC--lodXXXXXXXX** yang tercantum di sebelah ikon tombol kuning.
1. Pada halaman Paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih masing-masing paket Defender. 
    1. Verifikasi bahwa status CSPM diatur ke **Aktif**, jika belum, atur sekarang.  
    1. Aktifkan paket untuk Server.  Pilih **Aktif** untuk item baris Server, lalu pilih **Simpan** dari bagian atas halaman.
1. Dari sudut kiri atas jendela, tepat di bawah bilah biru di mana tertulis Microsoft Azure, pilih **Beranda** untuk kembali ke beranda layanan Azure.
1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tinjau

Di lab ini, Anda mempelajari Microsoft Defender untuk Cloud.
