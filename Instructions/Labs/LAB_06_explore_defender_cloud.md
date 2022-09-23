---
ms.openlocfilehash: eeee584ece9bb3ec4edcba5fa2e76a13dd9459c4
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892605"
---
<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi Jalur Pembelajaran/Modul/Pelajaran Microsoft Defender untuk Cloud': 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 2: Menjelaskan kemampuan manajemen keamanan Azure; Pelajaran 3: Menjelaskan Pertahanan Microsoft untuk Cloud'
---
--->

# <a name="lab-explore-microsoft-defender-for-cloud"></a>Lab: Menjelajahi Microsoft Defender untuk Cloud

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan manajemen keamanan Azure
- Pelajaran: Menjelaskan Microsoft Defender untuk Cloud

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan menjelajahi Microsoft Defender untuk Cloud dan mempelajari cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi Anda.  CATATAN: CATATAN: Panduan demo ini mengasumsikan penyaji memiliki izin tingkat admin ke langganan Azure melalui Azure pass.  Langganan Azure, seperti Langganan Cloudslice, yang dikelola oleh Authorized Lab Hoster membatasi akses dan fungsionalitas sehingga beberapa langkah di bawah ini mungkin tidak tersedia atau tidak menampilkan informasi apa pun.

**Perkiraan Waktu**: 30 menit

### <a name="setup"></a>Siapkan

Dalam tugas ini, Anda akan melakukan beberapa pengaturan dasar Microsoft Defender untuk Cloud, guna menyiapkan langganan dan untuk mengaktifkan dan menetapkan kebijakan default.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Di sudut kiri atas layar, di sebelah bagian yang tertulis Microsoft Azure, pilih ikon Tampilkan menu portal (tiga garis horizontal juga disebut sebagai ikon hamburger) lalu dari panel navigasi kiri, di bawah Favorit, pilih **Microsoft Defender untuk Cloud**.  Jika tidak tercantum di bawah favorit, lalu di kotak pencarian, masukkan **microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Jika ini adalah pertama kalinya Anda masuk ke Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka halaman Memulai dan mungkin diminta untuk meningkatkan.  Gulir ke bagian bawah halaman dan pilih **skip**.  Anda akan dibawa ke halaman Ringkasan.
    1. Di bagian atas halaman, Anda akan melihat kotak informasi berwarna biru muda yang menunjukkan, "Menyiapkan semuanya untuk langganan Anda. Hal ini mungkin membutuhkan waktu beberapa menit..."
    1. Setelah langganan siap, akan muncul kotak informasi baru berisi "Satu langganan tidak memiliki kebijakan default yang ditetapkan. Untuk meninjau daftar langganan, buka halaman Kebijakan Keamanan."  Pilih panah kanan di akhir kalimat atau pilih **Pengaturan lingkungan** dari panel navigasi kiri.
        1. Anda sekarang berada di halaman pengaturan Lingkungan. Pilih **Azure pass - Sponsor**.  Catatan:  Jika lingkungan Azure Anda didasarkan pada langganan Azure yang dikelola oleh Authorized Lab Hoster, bukan Azure Pass, Anda akan melihatnya direferensikan. Perluas opsi dengan memilih tanda yang lebih besar dari hingga Anda tidak dapat lagi memperluas opsi dan Anda melihat langganan.
        1. Di panel navigasi kiri, pilih **Kebijakan keamanan**.
        1. Di beranda, di bawah teks Inisiatif default, pilih **Tetapkan kebijakan**.
        1. Di bagian bawah panel, pilih **Tinjau + buat**.
        1. Di bagian bawah halaman, pilih **Buat**.  Tindakan ini akan menetapkan Azure Security Benchmark sebagai inisiatif kebijakan default.  Refresh layar (mungkin perlu beberapa menit untuk diterapkan).
        1. Keluar dari halaman pengaturan lingkungan dengan memilih **X** di halaman.  
        1. Dari halaman Layanan Azure, pilih **Microsoft Defender untuk Cloud** untuk kembali ke halaman ringkasan.

### <a name="task-1"></a>Tugas 1

Dalam tugas ini Anda akan melakukan panduan tingkat tinggi dari beberapa kemampuan Microsoft Defender untuk Cloud

1. Di halaman Ringkasan Microsoft Defender untuk Cloud, perhatikan informasi yang tersedia di halaman tersebut.  Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian utama halaman terdapat kartu yang mewakili Secure score, kepatuhan terhadap Peraturan, Wawasan, dan banyak lagi.

1. Dari bagian atas halaman, pilih **Assessed resources**.  (Perhatikan bahwa hal ini setara dengan memilih Inventaris dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Ini membawa Anda ke halaman **Inventory** yang menunjukkan langganan Azure pass Anda.  Pilih **Azure Pass – Sponsorship**.
    1. Halaman Kesehatan sumber daya menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih **There should be more than one owner assigned to your subscription**.
    1. Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana langkah-langkah perbaikan rinci disediakan bersama dengan opsi mengambil tindakan.  
    1. Pilih **Microsoft Defender untuk Cloud** dari sudut kiri atas layar untuk kembali ke halaman gambaran umum Microsoft Defender untuk Cloud.

1. Dari bagian atas halaman, pilih **Active recommendations**.  (Perhatikan bahwa hal ini setara dengan memilih Rekomendasi dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Halaman rekomendasi menampilkan dasbor Skor Aman Anda.
    1. Di bawah dasbor Skor Aman terdapat daftar kontrol. Setiap kontrol keamanan mewakili risiko keamanan yang harus dikurangi dan juga mencakup informasi tentang skor maksimum yang berhubungan dengan kontrol tersebut, skor saat ini, potensi peningkatan skor, dan status kesehatan sumber daya.  
    1. Pilih salah satu kontrol, seperti **Menerapkan praktik terbaik keamanan**.  Pilih salah satu sub-item, seperti **Harus ada lebih dari satu pemilik yang ditetapkan ke langganan Anda**.  Di halaman yang terbuka, Anda akan melihat deskripsi, langkah-langkah Remediasi, dan sumber daya yang terkena dampak. Keluar dari halaman ini, dengan memilih **X** di pojok kanan atas layar.
    1. Keluar dari halaman rekomendasi dengan memilih **X** di sudut kanan atas layar, untuk kembali ke halaman ikhtisar.

1. Dari halaman utama, pilih **Regulatory compliance**. Halaman kepatuhan terhadap peraturan menyediakan daftar kontrol kepatuhan.  Pada tiap kontrol adalah seperangkat penilaian yang didasarkan pada Tolok Ukur Keamanan Azure yang menyediakan rekomendasi tentang cara Anda dapat mengamankan solusi cloud Anda di Azure.
    1. Pilih **IM. Manajemen Identitas** lalu pilih **IM-6 Gunakan kontrol autentikasi yang kuat**.  Daftar ini menunjukkan tindakan tanggung jawab pelanggan yang dapat diambil untuk meningkatkan kondisi keamanan organisasi Anda.
    1. Pilih **X** di sudut kanan atas layar untuk menutup halaman dan kembali ke halaman Gambaran Umum Microsoft Defender untuk Cloud.
    1. Biarkan halaman gambaran umum Microsoft Defender untuk Cloud terbuka, yang akan Anda gunakan di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Perlu diingat bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang ditingkatkan (gratis) dan dengan fitur keamanan yang ditingkatkan yang tersedia melalui paket Microsoft Defender untuk Cloud. Dalam tugas ini, Anda akan menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.

1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih **Pengaturan lingkungan** dari panel navigasi kiri.
1. Pilih tanda lebih besar dari **>** di sebelah bagian yang tertulis Grup Akar Penyewa untuk memperluasnya (jangan pilih Grup Akar Penyewa secara langsung karena akan mengarahkan Anda ke halaman lain), lalu pilih **Azure Pass - Sponsor**
1. Pada halaman Paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih masing-masing paket Defender. Biarkan pengaturan apa adanya dengan semua paket dinonaktifkan.
1. Tutup semua tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda menjelajahi Microsoft Defender untuk Cloud dan mempelajari cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi Anda.
