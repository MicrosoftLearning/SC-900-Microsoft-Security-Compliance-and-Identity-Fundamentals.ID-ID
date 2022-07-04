---
lab:
  title: Mempelajari manajemen risiko orang dalam di Microsoft Purview
  module: 'Module 4 Lesson 4: Describe the capabilities of Microsoft compliance solutions: Describe insider risk capabilities in Microsoft Purview'
ms.openlocfilehash: b284151be19a0f9add77ef4c015520c7e4a7f363
ms.sourcegitcommit: b8b861a8c884a56f094213e47a59be48ba898ca1
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/29/2022
ms.locfileid: "146741879"
---
# <a name="lab-explore-insider-risk-management-in-microsoft-purview"></a>Lab: Mempelajari manajemen risiko orang dalam di Microsoft Purview

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari proses penyiapan kebijakan risiko dari dalam, bersama dengan prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.  Catatan: lab ini hanya akan memberikan visibilitas tentang apa yang diperlukan untuk menyiapkan manajemen risiko Insider dan opsi yang terkait dengan pembuatan kebijakan.  Lab ini tidak menyertakan tugas untuk memicu kebijakan, karena jumlah kejadian yang perlu terjadi untuk memicu kebijakan berada di luar cakupan latihan ini.

**Perkiraan Waktu**: 25-30 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini, Anda sebagai administrator global akan mengaktifkan izin untuk Manajemen Risiko Dari Dalam.  Secara khusus, Anda akan menambahkan pengguna ke grup peran Manajemen Risiko Dari Dalam untuk memastikan bahwa pengguna yang ditunjuk dapat mengakses dan mengelola fitur manajemen risiko dari dalam.  Mungkin diperlukan waktu hingga 30 menit agar izin grup peran diterapkan ke pengguna di seluruh organisasi.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi sebelah kiri portal Kepatuhan Microsoft Purview, pilih **Izin**.

1. Dari halaman izin & peran yang memiliki tulisan, "Lihat dan kelola peran yang digunakan untuk melakukan tugas khusus solusi di pusat kepatuhan." pilih **Peran**.

1. Di bidang pencarian, masukkan **Risiko Insider** lalu pilih ikon pencarian (kaca pembesar).  Perhatikan banyak peran yang muncul.  Masing-masing memiliki tingkat akses yang berbeda.  Pilih **Insider risk management**.

1. Di jendela yang terbuka, di samping teks Anggota, pilih **Edit**.

1. Untuk menambahkan anggota ke grup peran ini, klik **Choose members**.

1. Pilih **+ Add** dari bagian atas halaman.

1. Dari daftar nama, pilih **MOD Administrator**, **Megan Bowen**, lalu pilih **Add** di bagian bawah halaman, lalu pilih **Selesai** di bagian bawah halaman.

1. Verifikasi anggota yang ditambahkan sudah benar, lalu pilih **Save**.

1. Dari bagian bawah jendela Manajemen Risiko Dari Dalam, pilih **Close**.

1. Dari panel navigasi sebelah kiri, pilih **Beranda** untuk kembali ke halaman portal kepatuhan Microsoft Purview.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### <a name="task-2-skip-if-you-did-the-setup-lab-task-to-enable-the-audit-log"></a>Tugas 2 (LEWATI jika Anda menjalankan tugas lab penyiapan untuk mengaktifkan log audit)

Manajemen risiko dari dalam menggunakan log audit Microsoft 365 untuk wawasan dan aktivitas pengguna yang diidentifikasi dalam kebijakan dan wawasan analitik. Dalam tugas ini, Anda akan mengaktifkan kemampuan pencarian log Audit. Catatan:  Mungkin diperlukan waktu beberapa jam setelah mengaktifkan pencarian log audit sebelum Anda dapat mengembalikan hasil saat mencari log audit.  Meskipun perlu beberapa jam sebelum Anda dapat menelusuri log audit, hal itu tidak akan memengaruhi kemampuan untuk menyelesaikan tugas lain di lab ini.

1. Pilih tab browser berlabel, **Beranda-Kepatuhan Microsoft 365**.  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan di bilah alamat masukkan **compliance.microsoft.com** dan masuk dengan kredensial administrator Anda.

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.

1. Pastikan bahwa tab **Search** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah berwarna biru di bagian atas halaman yang mengatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak ada tindakan lebih lanjut yang diperlukan.

1. Kembali ke beranda portal kepatuhan Microsoft Purview dengan memilih **Beranda** dari panel navigasi sebelah kiri.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-3"></a>Tugas 3

Dalam tugas ini, Anda akan menelusuri pengaturan yang terkait dengan solusi Manajemen Risiko Dari Dalam.  Pengaturan manajemen risiko dari dalam berlaku untuk semua kebijakan manajemen risiko dari dalam, terlepas dari templat yang Anda pilih saat membuat kebijakan.

1. Anda akan diarahkan ke halaman beranda portal kepatuhan Microsoft Purview. Jika tidak, Buka tab browser **Home - Microsoft 365 compliance**.

1. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **Insider risk management**.

1. Sebelum mulai menyiapkan kebijakan, ada beberapa pengaturan yang perlu dikonfigurasi.  Dari halaman Manajemen Risiko Dari Dalam, pilih **setting cog icon** di sudut kanan atas halaman untuk mengakses pengaturan Risiko Dari Dalam.  
    1. Pastikan Anda berada di tab **Privasi**: untuk pengguna yang melakukan aktivitas yang cocok dengan kebijakan risiko insider Anda, pengaturan ini akan menentukan apakah akan menampilkan nama mereka yang sebenarnya atau menggunakan versi anonim untuk menutupi identitas mereka.  Pilih **Do not show anonymized versions of usernames**, lalu pilih **Save**.

    1. Pilih tab **Indikator kebijakan**. Setelah peristiwa pemicu kebijakan terjadi, aktivitas yang dipetakan ke indikator yang dipilih akan digunakan dalam menentukan skor risiko, bagi pengguna. Indikator kebijakan yang dipilih di sini termasuk templat kebijakan risiko Dari Dalam.  Gulir untuk melihat semua indikator yang tersedia dan informasi terkait lainnya. Di bagian **Office indicators**, klik **Select all**, lalu pilih **Save**.
    1. Pilih tab **Policy timeframes**. Kerangka waktu yang Anda pilih di sini berlaku pada pengguna saat memicu kecocokan untuk kebijakan risiko dari dalam.   Jendela Aktivasi menentukan berapa lama kebijakan akan secara aktif mendeteksi aktivitas untuk pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan. Deteksi aktivitas sebelumnya Menentukan seberapa jauh ke belakang kebijakan untuk mendeteksi aktivitas pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan.  Biarkan nilai tetapi default.  Pilih tab **Intelligent detections**.
    1. Pilih tab **Intelligent detections**. Tinjau opsi di sini.  Perhatikan pengaturan domain dan bagaimana hubungannya dengan indikator.
    1. Jelajahi item lain yang tercantum dalam pengaturan dan perhatikan bahwa banyak item dalam pratinjau.

1. Untuk kembali ke ringkasan Manajemen risiko dari dalam, pilih **Insider risk management** dari sudut kiri atas halaman, di atas teks Pengaturan.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-4"></a>Tugas 4

Dalam tugas ini, Anda akan mempelajari pembuatan kebijakan.

1. Anda seyogianya berada di halaman Manajemen risiko dari dalam.  Jika belum ada, buka tab browser berlabel, **Insider risk management - Microsoft 365 compliance**.

1. Dari halaman gambaran umum manajemen risiko Insider, pilih tab **Kebijakan** lalu pilih **+ Buat kebijakan**.  Konfigurasikan setiap tab kebijakan berikut.

    1. Kerangka kebijakan:  Dari daftar kategori, pilih **Data leaks**, lalu pilih **General data leaks**.  Perhatikan bahwa templat dalam kategori mungkin memiliki prasyarat tambahan.  Baca detail yang terkait dengan templat ini, lalu pilih **Next**.

    1. Nama dan deskripsi: masukkan nama, **SC900-InsiderRiskPolicy**, lalu pilih **Berikutnya**.
    1. Pengguna dan grup:  Tinjau kotak informasi.  Biarkan pengaturan default, **Include all users and groups**.  Pilih **Selanjutnya**.
    1. Konten yang harus diprioritaskan: Baca deskripsinya. Pilih **I want to specify SharePoint sites, sensitivity labels, and/or sensitive info types as priority content**, lalu pilih **Next**.
        1. Situs SharePoint: Untuk contoh kebijakan ini, biarkan kosong, pilih **Next**
        1. Jenis info sensitif: untuk contoh kebijakan ini, biarkan kosong lalu pilih **Next**.
        1. Label sensitivitas: pilih **+ Add or edit sensitivity labels**.  Pilih label yang terdaftar:  **Confidential Finance** dan **Highly Confidential\Project – Falcon**, pilih **Add**, lalu **Next**.
    1. Pemicu: Tinjau informasi selengkapnya.  Kebijakan dipicu oleh pengguna yang melakukan aktivitas eksfiltrasi seperti yang ditentukan (pilih ikon informasi pada setiap poin untuk informasi selengkapnya) ATAU kecocokan dengan kebijakan Pencegahan Kebocoran Data (DLP) yang ada.  Karena Anda tidak memiliki kebijakan DLP yang dikonfigurasi sebagai bagian dari latihan ini, pilih **User performs an exfiltration activity**.  Perhatikan bahwa indikator kebijakan yang Anda aktifkan di tugas sebelumnya telah dicentang.   Harap diingat bahwa indikator ini hanya akan diaktifkan setelah kebijakan dipicu dan aktivitas apa pun yang dipetakan ke indikator ini akan digunakan saat menghitung skor risiko pengguna. Pilih **Selanjutnya**.
    1. Ambang Indikator: di sini Anda dapat menentukan ambang default atau kustom yang terkait dengan indikator.  Harap diingat bahwa indikator diaktifkan hanya setelah pemicu kebijakan terjadi, sehingga ambang batas ini tidak memengaruhi saat kebijakan dipicu. Pilih **Specify custom thresholds**, Dengan memilih opsi ini, Anda dapat melihat nilai default saat ini. Biarkan pengaturan default, lalu klik **Next**.  
    1. Indikator: Perhatikan bahwa semua indikator office yang Anda pilih di tugas sebelumnya dipilih.  Gulir halaman untuk melihat indikator kebijakan lain yang tersedia dan item lain yang dipilih secara otomatis.   Deteksi urutan diaktifkan.  Jika urutan kegiatan seperti yang ditentukan telah terdeteksi, maka hal itu menunjukkan risiko yang lebih besar.  Arahkan mouse Anda pada ikon informasi untuk informasi yang lebih detail.  Item ini mengharuskan indikator tertentu dipilih dan perangkat harus terpasang.  Untuk mempermudah dan karena kita tidak memiliki perangkat yang terpasang di penyewa ini, hapus centang **Pilih semua**.
    1. Selesai: tinjau pengaturan, pilih **Kirim**, lalu pilih **Selesai**.

1. Anda kembali ke tab Kebijakan di halaman Manajemen risiko dari dalam.  Kebijakan yang baru saja Anda buat akan dicantumkan.  

1. Pada kebijakan yang baru saja Anda buat, bidang “Pengguna dalam cakupan” mewakili pengguna yang saat ini diberi skor risiko oleh kebijakan.  Menetapkan skor risiko kepada pengguna terjadi saat kebijakan dipicu, oleh karena itu nilainya menunjukkan 0.  Admin dapat mengonfigurasi kebijakan untuk mulai menetapkan skor risiko kepada pengguna tertentu, berdasarkan aktivitas yang terdeteksi oleh kebijakan yang Anda pilih, DAN mengabaikan persyaratan bahwa kejadian pemicu terdeteksi terlebih dahulu.  Untuk melakukan hal ini, pilih lingkaran kosong di samping nama kebijakan untuk memilih kebijakan, lalu pilih **Start scoring activity for users**, yang ditunjukkan di atas tabel kebijakan.  Isi setiap bidang, lalu pilih **Start scoring activity**.  Diperlukan waktu 24 jam bagi pengguna untuk muncul di tab 'Pengguna'. Setelah itu, Anda dapat memilih pengguna dari tab untuk meninjau aktivitas yang terdeteksi.  Pilih **Tutup** di bagian bawah jendela.

1. Tutup semua tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda telah mempelajari proses penyiapan kebijakan risiko dari dalam, bersama dengan prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.
