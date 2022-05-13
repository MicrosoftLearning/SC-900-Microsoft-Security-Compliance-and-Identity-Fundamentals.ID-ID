---
Demo:
  title: Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: 242d971510a428170a0d531b1ddcdf422ed4f9c9
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557326"
---
# <a name="demo-microsoft-sentinel"></a>Demo: Microsoft Sentinel

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini Anda akan melalui proses membuat instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan melalui langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data Anda dan membuat buku kerja untuk memantau dan memvisualisasikan data Anda.  Terakhir, Anda akan menampilkan beberapa opsi lain yang tersedia, termasuk analitik bawaan untuk mendapatkan pemberitahuan tentang apa pun yang mencurigakan, kemampuan otomatisasi, dan banyak lagi.

### <a name="pre-demo-setup--create-an-microsoft-sentinel-instance"></a>Pengaturan prademo:  Membuat instans Microsoft Sentinel

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsor**
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **US Timur** (Wilayah default yang berbeda dapat dipilih berdasarkan lokasi Anda)
    1. Pilih **Berikutnya: Tag >**

1. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman berita & panduan akan ditampilkan.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

### <a name="demo-part-2"></a>Demo Bagian 2

Dengan instans Microsoft Sentinel yang dibuat, Anda harus memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.  

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Sebagai Administrator MOD, peran saat ini adalah Administrator layanan.  Ini akan memberi Anda izin yang diperlukan, tetapi untuk tujuan demo Anda mungkin ingin menunjukkan peran spesifik Sentinel.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

    1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

    1. Jendela Tambahkan penetapan peran akan terbuka.  Di kotak pencarian, masuki **Microsoft Sentinel** untuk melihat 4 peran yang terkait dengan Microsoft Sentinel.
    1. Dari salah satu peran yang tercantum, pilih **lihat** untuk melihat detail peran tersebut.  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  

    1. Tutup jendela dengan memilih **X** di sudut kanan atas jendela.

1. Dari halaman kontrol akses, tutup jendela dengan memilih **X** di sudut kanan atas jendela.

### <a name="demo-part-3"></a>Demo Bagian 3

Di bagian demo ini, Anda akan melalui proses menghubungkan Microsoft Sentinel ke sumber data Anda untuk mulai mengumpulkan data.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Office 365** lalu dari daftar pilih **Office 365**.

1. Jendela konektor Office 365 terbuka.  Pilih **Buka halaman konektor**.

1. Dari halaman konektor Office 365, tinjau Deskripsi di sisi kiri jendela.

1. Tab instruksi di jendela utama, menyediakan prasyarat untuk Microsoft Sentinel untuk diintegrasikan dengan Office 365, ini semua harus menampilkan tanda centang hijau.   Di bawah konfigurasi, pilih **Exchange** dan **SharePoint** lalu pilih Terapkan Perubahan.  Anda akan langsung melihat status terhubung di sisi kiri jendela.

1. Tutup jendela dengan memilih **X** di sudut kanan atas jendela untuk kembali ke halaman konektor data.

1. Di bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa sekarang Anda sudah terhubung ke Office 365. Jika Anda tidak melihat ini, pilih **Refresh**. Mungkin perlu waktu beberapa menit agar halaman ini diperbarui.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

### <a name="demo-part-4"></a>Demo Bagian 4

Dalam bagian demo ini Anda akan melalui proses menyiapkan buku kerja untuk Office 365, guna memvisualisasikan dan memantau data Anda.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

1. Dalam kotak pencarian, masukkan Office 365 lalu pilih **Office 365**.

1. Dari jendela yang terbuka di sisi kanan layar, tinjau deskripsi lalu pilih **Simpan** dari bagian bawah layar lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.  Sekarang pilih **Tampilkan buku kerja yang disimpan**.

1. Halaman Buku Kerja Office 365 terbuka.  Pilih panah dropdown di samping **Operasi: batalkan set**, lalu pilih **Semua**.  Sekarang pilih panah dropdown di samping **Pengguna: kueri tertunda** dan pilih **Semua**.  Pilih **ikon simpan (disk)** . Tutup jendela dengan memilih **X** di sudut kanan atas jendela. Perlu waktu beberapa menit agar data mulai muncul di buku kerja, sehingga Anda akan kembali ke buku kerja nanti.

1. Dari sudut kiri atas halaman Buku Kerja, di atas bagian yang tertulis Buku Kerja, pilih **Microsoft Sentinel**. Ini mengembalikan Anda ke halaman Gambaran Umum.

### <a name="demo-part-5"></a>Demo Bagian 5

Dalam bagian ini Anda akan menunjukkan beberapa opsi yang tersedia di Sentinel.

1. Dari panel navigasi sebelah kiri, pilih **Hunting**.  Dari tab **kueri**, yang dipilih (digarisbawahi), pilih kueri apa pun dari daftar.  Setelah kueri dipilih, perhatikan informasi yang diberikan tentang kueri tersebut, termasuk kode untuk kueri, serta opsi untuk menjalankan kueri dan melihat hasil.  Jangan pilih apa pun.

1. Dari panel navigasi sebelah kiri, pilih **MITRE ATT&CK**.  MITRE ATT&CK adalah pangkalan pengetahuan taktik dan teknik yang umum digunakan oleh penyerang. Dengan Microsoft Sentinel, Anda dapat melihat deteksi yang sudah aktif di ruang kerja Anda, dan yang tersedia bagi Anda untuk dikonfigurasi, untuk memahami cakupan keamanan organisasi Anda, berdasarkan taktik dan teknik dari kerangka kerja MITRE ATT&CK®.  Pilih sel apa pun dari matriks dan catat informasi yang tersedia di sisi kanan layar.  

1. Dari panel navigasi sebelah kiri, pilih **Komunitas**. Analis keamanan Microsoft terus-menerus membuat dan menambahkan buku kerja, playbook, dan kueri berburu baru, serta masih banyak lagi, mempostingnya ke komunitas agar dapat digunakan di lingkungan Anda. Anda dapat mengunduh sampel konten dari komunitas privat repositori GitHub untuk membuat buku kerja kustom, kueri berburu, notebook, dan playbook untuk Microsoft Sentinel.  Pilih **Lakukan onboard konten komunitas**.  Tab baru ke repositori GitHub terbuka, kemudian Anda dapat mengunduh konten untuk mengaktifkan skenario Anda.  Kembali ke tab Azure di browser Anda.

1. Di panel navigasi sebelah kiri, klik **Analitik**.  Pilih item pertama dari daftar **Deteksi Serangan Multistage Tingkat Lanjut**.  Perhatikan informasi terperinci.  Microsoft Sentinel menggunakan Fusion, mesin korelasi berdasarkan algoritme pembelajaran mesin yang dapat diskalakan, untuk secara otomatis mendeteksi serangan multitahap (dikenal juga sebagai ancaman persisten tingkat lanjut) dengan mengidentifikasi kombinasi perilaku anomali dan aktivitas mencurigakan yang diamati pada berbagai tahap rantai pematian. Atas dasar penemuan ini, Microsoft Sentinel menghasilkan insiden yang akan sulit diambil.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  Di sini Anda dapat membuat aturan otomatisasi saja, berintegrasi dengan playbook yang ada, atau membuat playbook baru.  Pilih **+ Buat** lalu pilih **Aturan otomatisasi**.  Perhatikan jendela yang terbuka di sisi kanan layar dan opsi yang tersedia untuk membuat kondisi dan tindakan.  Pilih **Batal** dari bagian bawah halaman.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan terdaftar dan tersedia untuk dilihat serta untuk memantau data Anda.  Pilih **Office 365** lalu dari jendela yang terbuka di sisi kanan layar, pilih **Tampilkan buku kerja yang disimpan**.  Perhatikan visualisasi yang terkait dengan beban kerja Office 365 Anda.  

1. Tutup jendela dengan memilih **X** di sudut kanan atas jendela.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru, pilih **Beranda** untuk kembali ke halaman beranda portal Azure.

### <a name="task-6"></a>Tugas 6

Penghapusan penyediaan pasca-kursus. Microsoft Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Microsoft Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari demo ini minimal, Anda disarankan untuk menghapus grup sumber daya Microsoft Sentinel setelah Anda selesai menjelajahi kemampuan Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di pojok kiri atas halaman, di atas bagian yang tertulis Microsoft Sentinel, pilih **Semua Layanan**.

2. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

3. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-ResourceGroup**.

4. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya,  **SC900-ResourceGroup**, lalu klik **Delete** di bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

5. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser.

### <a name="review"></a>Tinjau

Dalam demo ini Anda dipandu untuk menelusuri langkah-langkah untuk menyambungkan Microsoft Sentinel ke sumber data, menyiapkan buku kerja, dan dipandu melalui beberapa opsi yang tersedia di Microsoft Sentinel.
