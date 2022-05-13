---
lab:
  title: Menjelajahi Microsoft Defender untuk Cloud
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: 580e84e726a6ba9c7d9109881710e08f059d0818
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557572"
---
# <a name="lab-explore-microsoft-defender-for-cloud"></a>Lab: Menjelajahi Microsoft Defender untuk Cloud

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan menjelajahi Microsoft Defender untuk Cloud dan mempelajari cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi Anda.

**Perkiraan Waktu**: 30 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini Anda akan mengikuti tur singkat Microsoft Defender untuk Cloud.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Di sudut kiri atas layar, di sebelah bagian yang tertulis Microsoft Azure, pilih ikon Tampilkan menu portal (tiga garis horizontal juga disebut sebagai ikon hamburger) lalu dari panel navigasi kiri, di bawah Favorit, pilih **Microsoft Defender untuk Cloud**.  Jika tidak tercantum di bawah favorit, lalu di kotak pencarian, masukkan **microsoft Defender untuk Cloud**, lalu dari daftar hasil, pilih **Microsoft Defender untuk Cloud**.

1. Perhatikan informasi yang tersedia di halaman gambaran umum Microsoft Defender untuk Cloud.  

1. Anda mungkin melihat kotak informasi warna biru pada bagian atas halaman yang menunjukkan bahwa Anda mungkin sedang melihat informasi yang dirahasiakan.  Klik **click here**.
    1. Untuk memastikan bahwa Anda mendapatkan visibilitas yang luas tentang penyewa, tetapkan diri Anda sebagai pemegang peran penting.  Pilih **Security Admin** lalu pilih **Get access** di bagian bawah halaman.
    1. Anda mungkin akan melihat pesan berikut: Grup manajemen akar tidak ada.  Sesuai deskripsi, sistem akan membuat grup untuk Anda.  Diperlukan waktu hingga 15 menit untuk menyelesaikannya (tetapi biasanya lebih cepat).  Setelah akses diberikan, pilih **Microsoft Defender untuk Cloud** di sudut kiri atas halaman, di bagian atas yang terdapat tulisan Dapatkan izin, lalu refresh halaman gambaran umum Microsoft Defender untuk Cloud.

1. Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian utama halaman terdapat kartu yang mewakili Secure score, kepatuhan terhadap Peraturan, Wawasan, dan banyak lagi.  

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

1. Dari halaman utama, pilih **Regulatory compliance**. Halaman kepatuhan terhadap peraturan menyediakan daftar kontrol kepatuhan.  Pada tiap kontrol adalah seperangkat penilaian yang didasarkan pada Tolok Ukur Keamanan Azure yang menyediakan rekomendasi tentang cara Anda dapat mengamankan solusi cloud Anda di Azure.
    1. Pilih **IM. Manajemen Identitas** lalu pilih **IM-6 Gunakan kontrol autentikasi yang kuat**.  Daftar ini menunjukkan tindakan tanggung jawab pelanggan yang dapat diambil untuk meningkatkan kondisi keamanan organisasi Anda.
    1. Pilih **X** di sudut kanan atas layar untuk menutup halaman dan kembali ke halaman Gambaran Umum Microsoft Defender untuk Cloud.
    1. Biarkan halaman gambaran umum Microsoft Defender untuk Cloud terbuka, yang akan Anda gunakan di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda akan melewati Skor Aman Azure dan menjelajahi rekomendasi yang dapat meningkatkan skor keamanan Anda.

1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih kartu **Secure Score**.
1. Pilih **Azure Pass – Sponsorship**.  Catat skor aman Anda.
1. Dari halaman rekomendasi, pilih **Terapkan praktik terbaik keamanan** untuk memperluas daftar. Perhatikan bahwa daftar menunjukkan status kesehatan sumber dayanya dengan warna merah.
1. Klik item **There should be more than one owner assigned to your subscription**, yang menunjukkan status kesehatan sumber daya berwarna merah.
1. Di bawahnya tertulis **Sumber daya yang terpengaruh**, pastikan Sumber daya yang tidak sehat dipilih/digarisbawahi, lalu pilih langganan Azure yang tercantum.
1. Di bagian atas halaman Kontrol akses (IAM), klik **+ Add**, lalu dari menu tarik-turun klik **Add role assignment**.
    1. Dari sisi kiri halaman, pilih **Pemilik** (ini harus menjadi item pertama yang tercantum) sehingga baris disorot dengan warna abu-abu, lalu pilih **Berikutnya** dari bagian bawah halaman.
    1. Di sebelah bagian yang tertulis Anggota, pilih **+ Pilih anggota**.
    1. Dari jendela Pilih anggota yang terbuka di sisi kanan layar, pilih **Alex Wilber**, lalu tekan **Pilih** di bagian bawah halaman.  
    1. Dari halaman Tambahkan penetapan peran, pastikan bahwa Alex Wilber terdaftar sebagai anggota, lalu pilih **Berikutnya** diikuti oleh **Tinjau + tetapkan**.
    1. Perlu waktu hingga 24 jam agar status diperbarui, dan setelah skor keamanan Anda juga diperbarui serta semua item di Kelola grup izin dan akses dipenuhi.
    1. Dari pojok kiri atas halaman, di atas bagian yang tertulis Azure Pass, pilih **Microsoft Defender untuk Cloud** untuk menampilkan halaman gambaran umum Microsoft Defender untuk Cloud.
1. Biarkan halaman ini terbuka untuk tugas berikutnya.

### <a name="task-3"></a>Tugas 3

Perlu diingat bahwa Microsoft Defender untuk Cloud ditawarkan dalam dua mode: tanpa fitur keamanan yang ditingkatkan (gratis) dan dengan fitur keamanan yang ditingkatkan yang tersedia melalui paket Microsoft Defender untuk Cloud. Dalam tugas ini, Anda akan menemukan cara mengaktifkan/menonaktifkan berbagai paket Microsoft Defender untuk Cloud.

1. Dari halaman gambaran umum Microsoft Defender untuk Cloud, pilih **Pengaturan lingkungan** dari panel navigasi kiri.
1. Pilih tanda lebih besar dari **>** di sebelah bagian yang tertulis Grup Akar Penyewa untuk memperluasnya (jangan pilih Grup Akar Penyewa secara langsung karena akan mengarahkan Anda ke halaman lain), lalu pilih **Azure Pass - Sponsor**
1. Pada halaman Paket Defender, perhatikan cara Anda dapat memilih Aktifkan semua atau pilih masing-masing paket Defender. Biarkan pengaturan apa adanya dengan semua paket dinonaktifkan.
1. Sekarang Anda dapat menghapus tab browser untuk keluar portal Azure.

### <a name="review"></a>Tinjau

Di lab ini, Anda menjelajahi Microsoft Defender untuk Cloud dan mempelajari cara Azure Secure Score dapat digunakan untuk meningkatkan postur keamanan organisasi Anda.
