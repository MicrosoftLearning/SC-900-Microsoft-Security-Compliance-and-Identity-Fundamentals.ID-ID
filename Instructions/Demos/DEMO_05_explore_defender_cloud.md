---
ms.openlocfilehash: ecea12b9b90c6dc3917d0ee93edcdba0436ccd0d
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892461"
---
<a name="---"></a><!---
---
Demo: Judul: 'Microsoft Defender untuk Cloud' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 2: Menjelaskan kemampuan manajemen keamanan Azure; Pelajaran 3: Menjelaskan Pertahanan Microsoft untuk Cloud'
---
--->

# <a name="demo-microsoft-defender-for-cloud"></a>Demo: Microsoft Defender untuk Cloud

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan manajemen keamanan Azure
- Pelajaran: Menjelaskan Microsoft Defender untuk Cloud

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan mempelajari Microsoft Defender untuk Cloud dan menunjukkan cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi.  CATATAN: CATATAN: Panduan demo ini mengasumsikan penyaji memiliki izin tingkat admin ke langganan Azure melalui Azure pass.  Langganan Azure, seperti Langganan Cloudslice, yang dikelola oleh Authorized Lab Hoster membatasi akses dan fungsionalitas sehingga beberapa langkah di bawah ini mungkin tidak tersedia atau tidak menampilkan informasi apa pun.

### <a name="demo-setup"></a>Penyiapan demo

Dalam tugas penyiapan ini, Anda akan melakukan beberapa penyiapan dasar Microsoft Defender untuk Cloud, guna menyiapkan langganan serta mengaktifkan dan menetapkan kebijakan default. Lakukan ini sebelum Anda mendemonstrasikan di depan kelas. 

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Defender untuk Cloud** lalu pilih **Microsoft Defender untuk Cloud** dari hasil pencarian.

1. Jika ini adalah pertama kalinya Anda masuk ke Microsoft Defender untuk Cloud dengan langganan, Anda dapat membuka halaman Memulai dan mungkin diminta untuk meningkatkan.  Gulir ke bagian bawah halaman dan pilih **skip**.  Anda akan dibawa ke halaman Ringkasan.
    1. Di bagian atas halaman, Anda akan melihat kotak informasi berwarna biru muda yang menunjukkan, "Menyiapkan semuanya untuk langganan Anda. Hal ini mungkin membutuhkan waktu beberapa menit..."
    1. Setelah langganan siap, kotak informasi baru akan muncul yang mengatakan, "Satu langganan tidak memiliki kebijakan default yang ditetapkan. Untuk meninjau daftar langganan, buka halaman Kebijakan Keamanan."  Pilih panah kanan di akhir kalimat.
        1. Anda sekarang berada di halaman pengaturan Lingkungan. Pilih **Azure pass - Sponsor**. 
        1. Di panel navigasi kiri, pilih **Kebijakan keamanan**.
        1. Di beranda, di bawah teks Inisiatif default, pilih **Tetapkan kebijakan**.
        1. Di bagian bawah panel, pilih **Tinjau + buat**.
        1. Di bagian bawah halaman, pilih **Buat**.
        1. Di bagian atas halaman, di bawah teks Microsoft Azure, pilih **Microsoft Defender untuk Cloud** dari breadcrumb, untuk kembali ke halaman ringkasan.

### <a name="demo-task"></a>Tugas Demo

Dalam tugas demo ini Anda akan melakukan panduan tingkat tinggi dari beberapa kemampuan Microsoft Defender untuk Cloud.

1. Informasi di bagian atas halaman ringkasan Microsoft Defender untuk Cloud mencakup jumlah langganan Azure, jumlah sumber daya yang dinilai, jumlah rekomendasi aktif, dan peringatan keamanan.  Di bagian utama halaman terdapat kartu yang mewakili Secure score, kepatuhan terhadap Peraturan, Wawasan, dan banyak lagi.  

1. Dari bagian atas halaman, pilih **Assessed resources**.  (Perhatikan bahwa hal ini setara dengan memilih Inventaris dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Ini membawa Anda ke halaman **Inventory** yang menunjukkan langganan Azure pass Anda.  Pilih **Azure Pass – Sponsorship**.
    1. Halaman Kesehatan sumber daya menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih **There should be more than one owner assigned to your subscription**.
    1. Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana langkah-langkah perbaikan rinci disediakan bersama dengan opsi mengambil tindakan.  
    1. Pilih **Microsoft Defender untuk Cloud** dari sudut kiri atas layar untuk kembali ke halaman gambaran umum Microsoft Defender untuk Cloud.

1. Dari bagian atas halaman, pilih **Active recommendations**.  (Perhatikan bahwa hal ini setara dengan memilih Rekomendasi dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Halaman rekomendasi menampilkan dasbor Skor Aman Anda.
    1. Di bawah dasbor Skor Aman terdapat daftar kontrol. Setiap kontrol keamanan mewakili risiko keamanan yang harus dikurangi dan juga mencakup informasi tentang skor maksimum yang berhubungan dengan kontrol tersebut, skor saat ini, potensi peningkatan skor, dan status kesehatan sumber daya.  
    1. Pilih salah satu kontrol, seperti **Enable MFA**.  Pilih salah satu subitem, seperti **MFA should be enabled on accounts with owner permissions on your subscription**.  Di halaman yang terbuka, Anda akan melihat deskripsi, langkah-langkah Remediasi, dan sumber daya yang terkena dampak. Keluar dari halaman ini, dengan memilih **X** di pojok kanan atas layar.
    1. Keluar dari halaman rekomendasi dengan memilih **X** di sudut kanan atas layar, untuk kembali ke halaman ikhtisar.

1. Anda kembali ke halaman Gambaran Umum Microsoft Defender untuk Cloud.  Dari halaman utama, pilih **Regulatory compliance**. (Perhatikan bahwa hal ini setara dengan memilih Rekomendasi dari panel navigasi kiri beranda Microsoft Defender untuk Cloud).
    1. Halaman kepatuhan terhadap peraturan menyediakan daftar kontrol kepatuhan.  Pada tiap kontrol adalah seperangkat penilaian yang didasarkan pada Tolok Ukur Keamanan Azure yang menyediakan rekomendasi tentang cara Anda dapat mengamankan solusi cloud Anda di Azure.
    1. Pilih **IM. Manajemen Identitas** lalu pilih **IM-6 Gunakan kontrol autentikasi yang kuat**.  Daftar ini menunjukkan tindakan tanggung jawab pelanggan yang dapat diambil untuk meningkatkan kondisi keamanan organisasi Anda.
    1. Pilih **X** di sudut kanan atas layar untuk menutup halaman dan kembali ke halaman kepatuhan peraturan.
    1. Pilih **X** di sudut kanan atas layar untuk kembali ke halaman ikhtisar.

1. Perlu diingat bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang ditingkatkan (gratis) dan dengan fitur keamanan yang ditingkatkan yang tersedia melalui paket Microsoft Defender untuk Cloud. Di sini Anda menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.
    1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih **Pengaturan lingkungan** dari panel navigasi kiri.
    1. Pilih tanda lebih besar dari **>** di sebelah bagian yang tertulis Grup Akar Penyewa untuk memperluasnya (jangan pilih Grup Akar Penyewa secara langsung karena akan mengarahkan Anda ke halaman lain), lalu pilih **Azure Pass - Sponsor**
    1. Pada halaman Paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih masing-masing paket Defender. Biarkan pengaturan apa adanya dengan semua paket dinonaktifkan.
    1. Pilih **X** di sudut kanan atas layar untuk kembali ke halaman pengaturan Lingkungan.
    1. Pilih **X** di sudut kanan atas layar untuk kembali ke halaman ikhtisar.

1. Kembali ke halaman beranda portal Azure dengan memilih **Home** di pojok kiri atas halaman.  Biarkan tab browser ini terbuka, karena Anda akan kembali lagi saat demo nanti.

## <a name="review"></a>Tinjau

Dalam demo ini, Anda telah mempelajari Microsoft Defender untuk Cloud dan menunjukkan cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi.
