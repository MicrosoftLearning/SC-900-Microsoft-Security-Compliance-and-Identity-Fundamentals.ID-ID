---
Demo:
  title: Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: 607c8097d17041f711aa1f40601e8433fcfce7f0
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894097"
---
# <a name="demo-microsoft-sentinel"></a>Demo: Microsoft Sentinel 

### <a name="demo-scenario"></a>Skenario demo
Dalam demo ini Anda akan melalui proses membuat instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan melalui langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data Anda, menggunakan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan terakhir Anda akan menjelajahi kemampuan otomatisasi.  

#### <a name="demo-part-1--create-an-microsoft-sentinel-instance"></a>Demo Bagian 1:  Membuat instans Microsoft Sentinel

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsor**
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **East US** (biarkan default)
    1. Pilih **Berikutnya: Tingkat harga >**

1. Untuk Tingkat Harga, biarkan pengaturan default: **Pay-as-you-go (per GB 2018)** , lalu pilih **Berikutnya: Tag >** .

1. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman berita & panduan akan ditampilkan.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="demo-part-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel--in-this-task-you-will-go-to-the-access-control-iam-page-for-the-resource-group-that-you-created-with-the-instance-of-microsoft-sentinel-view-the-available-roles-and-assign-yourself-mod-administrator-the-required-role-assigning-the-role-at-the-resource-group-level-will-ensure-the-role-will-apply-to-all-the-resources-that-are-deployed-to-support-microsoft-sentinel"></a>Bagian Demo 2:  Dengan instans Microsoft Sentinel yang dibuat, Anda harus memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.  Dalam tugas ini, Anda akan masuk ke halaman kontrol akses (IAM) untuk grup sumber daya yang Anda buat dengan instans Microsoft Sentinel, melihat peran yang tersedia, dan menetapkan diri Anda sendiri (administrator MOD) dengan peran yang diperlukan. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Ingat bahwa peran saat ini adalah Administrator layanan.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

1. Jendela Tambahkan penetapan peran akan terbuka.  Pilih panah tarik-turun di bidang Pilih peran untuk menampilkan peran yang tersedia. Di kotak pencarian pilih peran, masukkan **Microsoft Sentinel** untuk melihat 4 peran yang terkait dengan Microsoft Sentinel. Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  Untuk kenyamanan lab ini, masukkan **Owner** di kotak pencarian dan pilih **Owner** dari hasil tersebut.  Sebagai referensi, tinjau izin di Microsoft Sentinel: https://docs.microsoft.com/en-us/azure/sentinel/roles

1. Dari daftar pengguna yang ditampilkan, pilih **MOD Administrator**.

1. Pilih **Simpan** di bagian bawah halaman.

1. Dari halaman kontrol akses, pilih **View my access** untuk mengonfirmasi peran telah ditambahkan, lalu tutup jendela dengan memilih **X** di sudut kanan atas jendela.

#### <a name="demo-part-3--in-this-part-of-the-demo-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data--note-it-can-take-a-bit-time-to-show-the-connected-status-of-a-connector-30-minutes-depending-on-the-tenant"></a>Bagian Demo 3:  Di bagian demo ini, Anda akan melalui proses menghubungkan Microsoft Sentinel ke sumber data Anda untuk mulai mengumpulkan data.  Catatan: Perlu waktu yang lama untuk menampilkan status terhubung konektor (~30 menit, tergantung pada penyewa).

1. Di kotak pencarian, pada bilah berwarna biru di bagian atas halaman di samping bagian yang tertulis Microsoft Azure, masukkan **Microsoft Sentinel** lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Azure**, lalu dari daftar pilih **Azure Active Directory**.

1. Jendela konektor Azure Active Directory terbuka.  Pilih **Buka halaman konektor**.

1. Dari halaman konektor Azure Active Directory, tinjau deskripsi dan catat konten terkait yang menyertakan buku kerja, kueri, dan templat aturan analitik.  

1. Tab instruksi di jendela utama, menyediakan fasilitas tambahan bagi Microsoft Sentinel untuk berintegrasi dengan Azure Active Directory.   Di bawah konfigurasi, pilih **Sign-in logs**, lalu pilih Apply Changes (dapat memilih beberapa konektor).  Catatan: perlu beberapa saat sebelum Anda melihat status konektor terhubung (~30 menit atau lebih).  Sebagai acuan:
    1. Tinjau izin di Microsoft Sentinel: https://docs.microsoft.com/en-us/azure/sentinel/roles
    1. Hubungkan ke Azure Active Directory: https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory

1. Di tab Langkah selanjutnya, catat daftar buku kerja yang direkomendasikan.   Di bawah buku kerja yang direkomendasikan, pilih **Azure Sign-in logs** (dapat memilih buku kerja tambahan).

1. Dari halaman buku kerja dan dengan tab templat yang dipilih (digarisbawahi), pilih **Azure Sign-in logs**.

1. Dari jendela log masuk Azure AD yang terbuka, tinjau deskripsi, dan pilih **View template**.  Keluar dari templat, dengan mengeklik **X** di pojok kanan atas layar.  Pilih **Save** dari bagian bawah halaman, lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.

1. Dari sudut kiri atas halaman Buku Kerja, di atas bagian yang tertulis Buku Kerja, pilih **Microsoft Sentinel**. Hal ini mengembalikan Anda ke halaman Konektor Data microsoft Sentinel.

1. Di bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa sekarang Anda sudah terhubung ke Azure Active Directory.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

1. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan akan terdaftar dan tersedia untuk Anda lihat dan mengawasi data Anda.  Masuk berikutnya akan tercatat dalam buku kerja, jadi Anda dapat memilih untuk menampilkannya.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="demo-part-4-optional--in-this-part-of-the-demo-you-will-walk-through-the-process-of-using-a-built-in-analytics-rule-template-to-create-a-rule-to-get-notified-when-something-suspicious-occurs"></a>Demo Bagian 4 (Opsional):  Di bagian demo ini, Anda akan menjalani proses penggunaan templat aturan analitik bawaan untuk membuat aturan agar mendapat pemberitahuan saat terjadi sesuatu yang mencurigakan.

1. Di panel navigasi sebelah kiri, klik **Analitik**.

1. Halaman analitik akan menampilkan aturan yang aktif (Deteksi serangan multitahap tingkat lanjut diaktifkan secara default) dan akan menyediakan akses ke Templat aturan.  Pilih tab **Rule templates**.  Perhatikan daftar templat yang tersedia dan cara lain untuk memfilter daftar.  Menggunakan peringatan analitik bawaan di dalam ruang kerja Microsoft Sentinel, Anda akan diberi tahu saat terjadi sesuatu yang mencurigakan.

1. Di bilah Pencarian, masukkan **Azure Portal**.  Pilih **Failed login attempts to Azure Portal**.  

1. Di jendela yang terbuka, baca deskripsi dan tinjau informasi terkait dengan templat.  Pilih **Create rule** di bagian bawah halaman.
    1. Dari wizard aturan Analitik, tinjau informasi, lalu pilih **Berikutnya: Atur logika aturan >** .
    1. Halaman Setel logika aturan, adalah tempat Anda menentukan logika untuk aturan analitik baru Anda. Templat sudah menyediakan beberapa logika dan pengaturan yang telah ditentukan sebelumnya.  Gulir halaman untuk melihat pengaturan yang tersedia.  Biarkan default. Pilih **Berikutnya: Pengaturan insiden (pratinjau)>** .
    1. Dengan pengaturan Insiden, peringatan Microsoft Sentinel dapat dikelompokkan bersama menjadi Insiden yang harus diperiksa. Anda dapat menyetel apakah peringatan yang dipicu oleh aturan analitik ini harus menghasilkan insiden.  Biarkan pengaturan default dan pilih **Berikutnya: Respons otomatis >** .
    1. Di tab Respons otomatis, perhatikan bagaimana Anda dapat menambahkan buku pedoman untuk mengotomatiskan respons.  Demikian pula, Anda dapat membuat aturan otomatisasi insiden.  Pilih **+ Add** baru di bawah otomatisasi insiden.  Jendela untuk membuat otomatisasi baru akan terbuka.  Aturan otomasi apa pun yang Anda buat di halaman ini dipicu oleh aturan analisis yang tadinya Anda pilih, dalam hal ini, Upaya masuk yang gagal ke Portal Azure.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.   Pilih **Cancel** untuk keluar dari jendela.
    1. Pilih **Berikutnya: Tinjau>** untuk meninjau semua detail yang terkait dengan aturan dan berdasarkan templat yang dipilih. Pada titik ini, Anda dapat memilih untuk membuat aturan, dengan memilih **Create** atau keluar tanpa membuat aturan dengan memilih **X** di pojok kanan atas halaman.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="demo-step-5-optional--in-the-previous-step-you-created-an-analytics-rule-to-be-alerted-of-suspicious-activities--embedded-in-that-wizard-is-the-option-to-automate-the-response-to-an-incident-based-on-the-specific-rule--but-you-can-also-create-automation-rules-by-going-directly-to-the-automation-configuration-option"></a>Demo Langkah 5 (Opsional):  Pada langkah sebelumnya, Anda telah membuat aturan analitik untuk diberi tahu tentang aktivitas yang mencurigakan.  Fitur yang tersemat di wizard adalah opsi untuk mengotomatisasi respons untuk insiden berdasarkan aturan tertentu.  Namun, Anda juga dapat membuat aturan otomatisasi dengan langsung ke opsi konfigurasi otomatisasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  

1. Pilih **+ Buat**. Sekarang di menu tarik-turun, perhatikan bagaimana Anda dapat memilih antara menambahkan playbook baru atau menambahkan aturan baru.  Pilih **Tambahkan aturan baru**.  
    1. Jendela untuk membuat otomatisasi baru akan terbuka.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.  Hanya saja, perbedaanya adalah kondisi pertamanya, Anda harus mengaitkan aturan analitik yang ingin Anda terapkan pada aturan otomatisasi ini.  Fungsi ini tidak tersedia pada tugas sebelumnya karena otomatisasi masih dikonfigurasikan untuk aturan tertentu.  Pilih **Cancel** untuk keluar dari jendela Buat aturan otomatisasi baru.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="step-6-tear-down---instructor-do-this-step-after-class-delete-microsoft-sentinel-resource-group--microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-lab-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-features-of-capabilities-of-microsoft-sentinel"></a>Langkah 6: PENGHAPUSAN - Instruktur melakukan langkah ini setelah kelas. Hapus grup Sumber Daya Microsoft Sentinel.  Microsoft Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Microsoft Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari lab ini minimal, Anda disarankan untuk menghapus grup sumber daya Microsoft Sentinel setelah Anda selesai menjelajahi fitur kemampuan Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di pojok kiri atas halaman, di atas bagian yang tertulis Microsoft Sentinel, pilih **Semua Layanan**.

1. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya, **SC900-Sentinel-RG**, lalu pilih **Delete** dari bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

1. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser. 

#### <a name="review"></a>Tinjau

Dalam demo ini Anda menunjukkan proses membuat instans Microsoft Sentinel.  Anda menunjukkan cara menyiapkan izin untuk memastikan akses ke sumber daya yang terkait dengan instans Microsoft Sentinel Anda.  Dengan instans Microsoft Sentinel yang dibuat, Anda melalui langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, cara menggunakan aturan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan terakhir Anda menjelajahi kemampuan otomatisasi. Anda mengakhiri demo dengan menghapus grup sumber daya yang terkait dengan instans Microsoft Sentinel yang Anda buat.