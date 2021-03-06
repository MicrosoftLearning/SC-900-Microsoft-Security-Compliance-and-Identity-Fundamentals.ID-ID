---
lab:
  title: Mempelajari portal kepatuhan Microsoft Purview & Manajer Kepatuhan
  module: 'Module 4 Lesson 2: Describe the capabilities of Microsoft compliance solutions: Describe the compliance management capabilities of Microsoft Purview'
ms.openlocfilehash: 4745dddb860e82ddc05e7c88deb0e0644046e0b5
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557490"
---
# <a name="lab-explore-the-microsoft-purview-compliance-portal--compliance-manager"></a>Lab: Mempelajari portal kepatuhan Microsoft Purview & Manajer Kepatuhan

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari halaman beranda portal kepatuhan Microsoft Purview dan bagaimana kemampuan manajer Kepatuhan dapat membantu organisasi meningkatkan postur kepatuhan mereka.

**Perkiraan Waktu**: 15-20 menit

### <a name="task-1"></a>Tugas 1

Pelajari halaman beranda portal kepatuhan Microsoft Purview dan pelajari cara menyesuaikan tampilan kartu dan panel navigasi.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  
1. Bagian kartu di halaman beranda menunjukkan sekilas kepada Anda, bagaimana kinerja organisasi Anda dengan kondisi kepatuhan Anda, solusi yang tersedia untuk organisasi Anda, dan banyak lagi.
1. Dari jendela utama, gulir ke bawah untuk melihat kartu lainnya. Kartu yang tersedia di layar beranda dan posisi kartu dapat diubah untuk mengakomodasi preferensi masing-masing administrator.  
1. Menempatkan kursor mousedi atas bilah judul kartu apa pun akan mengubah bilah judul menjadi warna abu-abu.  Saat Anda melihat kursor berubah menjadi bentuk salib, Anda dapat memindahkan kartu ke lokasi yang Anda inginkan.
1. Di bilah judul setiap kartu, Anda juga akan melihat elipsis yang memberikan tindakan yang dapat Anda lakukan.  Pilih elips pada katalog Solusi dan pilih **Remove**.
1. Anda dapat menambahkan kartu, dengan memilih **+ Add cards**.  Jendela Tambahkan kartu ke beranda Anda akan terbuka.  Arahkan kursor mouse di atas kartu Katalog solusi yang ditampilkan di jendela ini dan seret ke lokasi di layar beranda tempat Anda ingin menempatkan kartu.
1. Dari panel navigasi sebelah kiri halaman beranda portal kepatuhan Microsoft Purview, perhatikan bahwa hanya Katalog Solusi yang ditampilkan.  Dari panel navigasi kiri, pilih **...Tampilkan semua**.  Perhatikan bagaimana semua solusi tambahan muncul di bawah bagian solusi.  
1. Pilih **Show less** untuk menyembunyikan.
1. Sebagai administrator kepatuhan, mungkin ada serangkaian solusi yang Anda kelola untuk organisasi kami dan karena itu, Anda mungkin ingin hanya memiliki solusi yang tercantum di panel navigasi yang Anda lihat. Untuk menyesuaikan dengan preferensi Anda, pilih **Customize navigation**.  
1. Dari jendela berlabel Sesuaikan panel navigasi Anda, perhatikan cara Anda dapat memilih item yang ingin Anda tampilkan di panel navigasi dan membatalkan pilihan item yang tidak ingin Anda lihat. Untuk tujuan lab ini, tetap pilih semua item dan tekan **Simpan** di bagian bawah jendela.  
1. Biarkan tab browser terbuka.

### <a name="task-2"></a>Tugas 2

Pelajari tentang kondisi kepatuhan organisasi Anda melalui Pengelola Kepatuhan.

1. Dari panel navigasi sebelah kiri portal kepatuhan Microsoft Purview, pilih **Manajer Kepatuhan**.  Atau, Anda dapat memilih Pengelola Kepatuhan pada bilah judul kartu Pengelola Kepatuhan.

1. Dari bagian atas halaman Pengelola Kepatuhan, pastikan **Overview** terpilih (digarisbawahi). Gulir ke bawah untuk melihat semua informasi yang tersedia di halaman  Informasi di halaman ini mencakup skor kepatuhan Anda, poin yang Anda raih, dan poin yang dikelola Microsoft yang dicapai.   Anda akan melihat Tindakan perbaikan penting, Solusi yang memengaruhi skor Anda, dan perincian skor kepatuhan menurut kategori atau penilaian.

1. Dari bagian atas halaman Ikhtisar, pilih **Improvement actions**.  Ini adalah tindakan yang dapat meningkatkan skor kepatuhan organisasi. Perhatikan bahwa saat tindakan peningkatan diambil, poin mungkin memerlukan waktu hingga 24 jam untuk diperbarui.  Perhatikan filter yang tersedia.

1. Dari daftar tindakan perbaikan, pilih **Enable self-service password reset**.  Setiap tindakan perbaikan memiliki bagian ringkasan bersama dengan halaman detail tempat Anda dapat memilih implementasi, pengujian, standar terkait dan persyaratan peraturan, serta dokumen.

1. Keluar dari tindakan peningkatan ini dengan memilih **Tindakan Peningkatan** dari breadcrumb di kiri atas halaman.  Sekarang Anda kembali ke halaman tindakan perbaikan.

1. Dari bagian atas halaman, pilih **Solutions**. Pada halaman ini Anda akan melihat bagaimana kontribusi solusi pada skor Anda dan peluang yang tersisa untuk perbaikan.

1. Dari bagian atas halaman, pilih **Assessments**. Pada halaman ini Anda akan melihat Acuan Dasar Perlindungan Data.  Hal ini adalah penilaian default yang disediakan Microsoft di Pengelola Kepatuhan untuk acuan dasar perlindungan data Microsoft 365.  Penilaian dasar ini memiliki seperangkat kontrol untuk peraturan dan standar utama perlindungan data dan tata kelola data umum. Pengelola Kepatuhan menjadi lebih membantu saat membuat dan mengelola penilaian Anda sendiri untuk memenuhi kebutuhan khusus organisasi Anda.

1. Pilih **Data Protection Baseline**.  Perhatikan informasi yang tersedia di tab progres.  Anda juga dapat melihat informasi tentang Kontrol, , tindakan peningkatan Anda, dan tindakan Microsoft.  

1. Dari bagian kiri atas halaman, di atasnya tertulis Penilaian (breadcrumb), pilih **Assessment** untuk kembali ke halaman penilaian.  

1. Dari bagian atas halaman, pilih **Assessment templates**.  Halaman ini mencantumkan templat yang tersedia. Anda dapat membuat penilaian untuk organisasi Anda dengan menggunakan templat yang sudah ada atau membuat templat baru.

1. Dari daftar templat yang disertakan, pilih **ISO/IEC27001:2013**. Dari bagian kanan atas halaman, pilih **+ Create assessment**.  Perhatikan di bagian sisi kiri layar bahwa hanya ada dua langkah untuk membuat penilaian dari templat.  Pilih Batal dari bagian bawah halaman.

1. Tutup tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda mempelajari halaman beranda portal kepatuhan Microsoft Purview dan cara-cara tempat kemampuan manajer Kepatuhan dapat membantu organisasi meningkatkan postur kepatuhan mereka.
