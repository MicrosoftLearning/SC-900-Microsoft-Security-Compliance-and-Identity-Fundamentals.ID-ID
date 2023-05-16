---
demo:
  title: 'Microsoft Defender untuk Cloud'
  module: 'Modul 2: Menjelaskan kemampuan manajemen keamanan Azure'
---



# <a name="demo-microsoft-defender-for-cloud"></a>Demo: Microsoft Defender untuk Cloud

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan manajemen keamanan Azure
- Pelajaran: Menjelaskan Microsoft Defender untuk Cloud

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan mempelajari Microsoft Defender untuk Cloud dan menunjukkan bagaimana hal tersebut dapat digunakan untuk meningkatkan kondisi keamanan organisasi.  CATATAN: langganan Azure yang dikelola oleh Authorized Lab Hoster (AH) mungkin membatasi beberapa akses dan memerlukan waktu lebih lama dari biasanya.

### <a name="demo-task-1"></a>Tugas Demo 1

Dalam tugas demo ini, Anda akan melakukan penelusuran tingkat tinggi dari beberapa kemampuan Microsoft Defender untuk Cloud.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.
1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan nama pengguna yang diberikan oleh penyedia hosting lab Anda, lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Di bilah pencarian berwarna biru, masukkan **Microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini adalah pertama kalinya Anda memasuki Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka halaman Memulai, dan mungkin akan diminta untuk melakukan peningkatan.  Gulir ke bagian bawah halaman dan pilih **Lewati**.  Anda akan dibawa ke halaman Ringkasan.

1. Di halaman Ringkasan Microsoft Defender untuk Cloud, perhatikan informasi yang tersedia di halaman tersebut.  Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian utama halaman terdapat kartu yang mewakili postur Keamanan, Kepatuhan terhadap peraturan, Wawasan, dan lainnya.  Catatan: Inisiatif kebijakan default Microsoft Defender untuk Cloud, yang biasanya harus ditetapkan oleh admin, telah ditetapkan sebagai bagian dari penyiapan langganan Azure. Namun, skor aman akan ditampilkan sebagai 0% karena memerlukan waktu hingga 24 jam bagi Azure untuk mencerminkan skor awal.

1. Dari bagian atas halaman, pilih **Assessed resources**.  (Perhatikan bahwa hal ini setara dengan memilih Inventaris dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Tindakan ini membawa Anda ke halaman **Inventaris** yang mencantumkan sumber daya saat ini. Pilih sumber daya mesin virtual, **sc900-winwm**. Sumber daya ini dikaitkan dengan mesin virtual yang Anda gunakan di lab sebelumnya.
    1. Halaman kesehatan Sumber Daya untuk VM menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih salah satu item dari daftar yang menunjukkan status **tidak sehat**.
    1. Perhatikan detail deskripsi.  Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana petunjuk perbaikan (atau tautan ke petunjuk) disediakan bersama dengan opsi untuk mengambil tindakan.  Keluar dari jendela tanpa melakukan tindakan apa pun.
    1. Kembali ke halaman ringkasan Microsoft Defender untuk Cloud, dengan memilih **Microsoft Defender untuk Cloud | Ringkasan** dari bagian atas halaman, di bagian atas yang bertuliskan Kesehatan sumber daya.

1. Dari panel navigasi kiri, pilih **Rekomendasi**.  (Perhatikan bahwa ini sama dengan memilih rekomendasi Aktif dari bagian atas halaman ringkasan Microsoft Defender untuk Cloud).
    1. Verifikasi, tab **Semua rekomendasi** dipilih (digarisbawahi).  Perhatikan tampilan dasbor yang menunjukkan Rekomendasi aktif berdasarkan tingkat keparahan, Kesehatan sumber daya, dan lainnya.
    1. Perhatikan bahwa beberapa item muncul sebagai sumber daya yang tidak sehat, seperti yang digambarkan oleh bilah merah di sebelah kanan item baris.  Dari daftar, pilih sumber daya yang tidak sehat.  Di halaman yang terbuka, Anda akan melihat deskripsi, langkah Remediasi, dan sumber daya yang terpengaruh. Keluar dari halaman ini, dengan memilih **X** di pojok kanan atas layar.
    1. Keluar dari halaman rekomendasi dengan memilih **X** di sudut kanan atas layar, untuk kembali ke halaman ikhtisar.

1. Dari panel navigasi kiri utama, pilih **Kepatuhan peraturan**. Halaman kepatuhan peraturan menyediakan daftar kontrol kepatuhan berdasarkan tolok ukur keamanan cloud Microsoft (pastikan bahwa tab tolok ukur keamanan cloud Microsoft dipilih/digarisbawahi). Di bawah setiap domain kontrol adalah subset dari kontrol dan untuk setiap kontrol ada satu atau lebih penilaian. Setiap penilaian memberikan informasi termasuk deskripsi, remediasi, dan sumber daya yang terpengaruh.
    1. Mari jelajahi salah satu area domain kontrol. Pilih (luaskan) **NS. Keamanan Jaringan**. Daftar kontrol yang terkait dengan keamanan jaringan ditampilkan.
    1. Pilih **NS-10. Microsoft Defender untuk DNS harus diaktifkan**. Perhatikan daftar penilaian otomatis (yang mencakup penilaian otomatis untuk AWS) dan bagaimana setiap item baris penilaian memberikan informasi termasuk jenis sumber daya, sumber daya yang gagal, dan stasiun kepatuhan. Pilih penilaian yang tercantum.  Di sini Anda melihat informasi termasuk deskripsi, langkah-langkah Remediasi, dan sumber daya yang Terpengaruh.
    1. Pilih **X** di pojok kanan atas layar untuk menutup halaman.
    1. Pilih **Ringkasan** dari panel navigasi kiri untuk kembali ke halaman Ringkasan Microsoft Defender untuk Cloud.
    1. Biarkan halaman ringkasan Microsoft Defender untuk Cloud tetap terbuka, yang akan Anda gunakan di tugas berikutnya.

### <a name="demo-task-2"></a>Tugas Demo 2

Perlu diperhatikan bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang disempurnakan (gratis) dan dengan fitur keamanan yang disempurnakan yang tersedia melalui paket Microsoft Defender untuk Cloud. Dalam tugas ini, Anda akan menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.

1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih **Pengaturan lingkungan** dari panel navigasi kiri.
1. Pilih kotak **Luaskan semua** lalu pilih langganan **MOC--lodXXXXXXXX** yang tercantum di sebelah ikon tombol kuning.
1. Pada halaman Paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih masing-masing paket Defender. 
    1. Verifikasi bahwa status CSPM diatur ke **Aktif**, jika belum, atur sekarang.  
    1. Aktifkan paket untuk Server.  Pilih **Aktif** untuk item baris Server, lalu pilih **Simpan** dari bagian atas halaman.
1. Tutup semua tab browser yang terbuka.

## <a name="review"></a>Tinjau

Dalam demo ini, Anda telah mempelajari Microsoft Defender untuk Cloud dan menunjukkan cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi.
