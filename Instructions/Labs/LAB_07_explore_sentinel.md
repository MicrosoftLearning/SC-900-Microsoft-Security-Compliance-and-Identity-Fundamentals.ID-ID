---
lab:
  title: Menjelajahi Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: c5a7ba866c82f15a4f78099326fd93a734caead8
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894001"
---
# <a name="lab-explore-microsoft-sentinel"></a>Lab: Menjelajahi Microsoft Sentinel 

## <a name="lab-scenario"></a>Skenario lab
Di lab ini, Anda akan mempelajari proses untuk membuat instans Microsoft Sentinel.  Anda juga akan menyiapkan izin untuk memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah pengaturan dasar ini selesai, Anda akan menjalani langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data Anda, menggunakan analitik bawaan untuk mendapatkan pemberitahuan tentang sesuatu yang mencurigakan, dan terakhir Anda akan menjelajahi kemampuan otomatisasi.  

  

**Perkiraan Waktu**: 30-45 menit

#### <a name="task-1--create-an-microsoft-sentinel-instance"></a>Tugas 1:  Buat instans Microsoft Sentinel.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

2. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger) lalu klik **All Services**.  

4. Di kotak layanan filter, masukkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari daftar.

5. Dari halaman Microsoft Sentinel, pilih **Buat Microsoft Sentinel**.

6. Dari halaman Tambahkan Microsoft Sentinel ke ruang kerja, pilih **Buat ruang kerja baru**.

7. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsor**
   
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-ResourceGroup**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan:::: **East US** (biarkan default)
    1. Pilih **Berikutnya: Tingkat harga >**

8. Untuk Tingkat Harga, biarkan pengaturan default: **Pay-as-you-go (per GB 2018)** , lalu pilih **Berikutnya: Tag >** .

9. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

10. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

11. Jika Anda tidak melihat ruang kerja baru terdaftar, klik **Refresh**, lalu klik **Add**.

12. Setelah ruang kerja baru ditambahkan, Microsoft Sentinel | Halaman berita & panduan akan ditampilkan.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

13. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="task-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel--in-this-task-you-will-go-to-the-access-control-iam-page-for-the-resource-group-that-you-created-with-the-instance-of-microsoft-sentinel-view-the-available-roles-and-assign-yourself-mod-administrator-the-required-role-assigning-the-role-at-the-resource-group-level-will-ensure-the-role-will-apply-to-all-the-resources-that-are-deployed-to-support-microsoft-sentinel"></a>Tugas 2:  Dengan instans Microsoft Sentinel yang dibuat, Anda harus memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.  Dalam tugas ini, Anda akan masuk ke halaman kontrol akses (IAM) untuk grup sumber daya yang Anda buat dengan instans Microsoft Sentinel, melihat peran yang tersedia, dan menetapkan diri Anda sendiri (administrator MOD) dengan peran yang diperlukan. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan berlaku untuk semua sumber daya yang disebarkan untuk mendukung Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di pojok kiri atas halaman, di atas bagian yang tertulis Microsoft Sentinel, pilih **Semua Layanan**.

2. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

3. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-ResourceGroup**.

4. Di SC900-ResourceGroup, klik **Access control (IAM)** di panel navigasi sebelah kiri.

5. Dari halaman Kontrol akses, pilih **View my access**.  Perhatikan bahwa peran saat ini adalah Admin keamanan.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

6. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

7. Jendela Tambahkan penetapan peran akan terbuka.  Pilih panah tarik-turun di bidang Pilih peran untuk menampilkan peran yang tersedia.  Untuk lab ini, klik **Owner**.  CATATAN:  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  Sebagai referensi, tinjau izin di Microsoft Sentinel: https://docs.microsoft.com/en-us/azure/sentinel/roles

8. Dari daftar pengguna yang ditampilkan, pilih **MOD Administrator**.

9. Pilih **Simpan** di bagian bawah halaman.

10. Dari halaman kontrol akses, pilih **View my access** untuk mengonfirmasi peran telah ditambahkan, lalu tutup jendela dengan memilih **X** di sudut kanan atas jendela.

11. Kembali ke halaman Semua layanan Azure, dengan mengeklik **All Services** di pojok kiri atas halaman, di atas yang bertuliskan Grup sumber daya.

#### <a name="task-3--in-this-task-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data-note-it-can-take-a-bit-time-to-show-the-connected-status-of-a-connector-30-minutes-depending-on-the-tenant"></a>Tugas 3:  Dalam tugas ini Anda akan melakukan proses menghubungkan Microsoft Sentinel ke sumber data Anda untuk mulai mengumpulkan data. Catatan: Perlu waktu yang lama untuk menampilkan status terhubung konektor (~30 menit, tergantung pada penyewa).

1. Di kotak Filter layanan pada halaman Semua layanan, masukkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari daftar hasil. 

2. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

3. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

4. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Azure**, lalu dari daftar pilih **Azure Active Directory**.

5. Jendela konektor Azure Active Directory terbuka.  Pilih **Buka halaman konektor**.

6. Dari halaman konektor Azure Active Directory, tinjau deskripsi dan catat konten terkait yang menyertakan buku kerja, kueri, dan templat aturan analitik.  

7. Tab instruksi di jendela utama, menyediakan fasilitas tambahan bagi Microsoft Sentinel untuk berintegrasi dengan Azure Active Directory.   Di bawah konfigurasi, pilih **Sign-in logs**, lalu pilih Apply Changes (dapat memilih beberapa konektor).

8. Di tab Langkah selanjutnya, catat daftar buku kerja yang direkomendasikan.   Di bawah buku kerja yang direkomendasikan, pilih **Azure Sign-in logs** (dapat memilih buku kerja tambahan).

9. Dari halaman buku kerja dan dengan tab templat yang dipilih (digarisbawahi), pilih **Azure Sign-in logs**. 

10. Dari jendela log masuk Azure AD yang terbuka, tinjau deskripsi, dan pilih **View template**.  Keluar dari templat, dengan mengeklik **X** di pojok kanan atas layar.  Pilih **Save** dari bagian bawah halaman, lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.

11. Dari sudut kiri atas halaman Buku Kerja, di atas bagian yang tertulis Buku Kerja, pilih **Microsoft Sentinel**. Hal ini mengembalikan Anda ke halaman Konektor Data microsoft Sentinel.

12. Di bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa sekarang Anda sudah terhubung ke Azure Active Directory.

13. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

14. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan akan terdaftar dan tersedia untuk Anda lihat dan mengawasi data Anda.

15. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="task-4--in-this-task-you-will-walk-through-the-process-of-using-a-built-in-analytics-rule-template-to-create-a-rule-to-get-notified-when-something-suspicious-occurs"></a>Tugas 4:  Di tugas ini, Anda akan mempelajari proses menggunakan templat aturan analitik bawaan untuk membuat aturan agar diberi pemberitahuan ketika terjadi hal yang mencurigakan.

1. Di panel navigasi sebelah kiri, klik **Analitik**.

2. Halaman analitik akan menampilkan aturan yang aktif (Deteksi serangan multitahap tingkat lanjut diaktifkan secara default) dan akan menyediakan akses ke Templat aturan.  Pilih tab **Rule templates**.  Perhatikan daftar templat yang tersedia dan cara lain untuk memfilter daftar.  Menggunakan peringatan analitik bawaan di dalam ruang kerja Microsoft Sentinel, Anda akan diberi tahu saat terjadi sesuatu yang mencurigakan.

3. Di bilah Pencarian, masukkan **Azure Portal**.  Pilih **Failed login attempts to Azure Portal**.  

4. Di jendela yang terbuka, baca deskripsi dan tinjau informasi terkait dengan templat.  Pilih **Create rule** di bagian bawah halaman.

5. Dari wizard aturan Analitik, tinjau informasi, lalu pilih **Berikutnya: Atur logika aturan >** .

6. Halaman Setel logika aturan, adalah tempat Anda menentukan logika untuk aturan analitik baru Anda. Templat sudah menyediakan beberapa logika dan pengaturan yang telah ditentukan sebelumnya.  Gulir halaman untuk melihat pengaturan yang tersedia.  Biarkan default. Pilih **Berikutnya: Pengaturan insiden (pratinjau)>** .

7. Dengan pengaturan Insiden, peringatan Microsoft Sentinel dapat dikelompokkan bersama menjadi Insiden yang harus diperiksa. Anda dapat menyetel apakah peringatan yang dipicu oleh aturan analitik ini harus menghasilkan insiden.  Biarkan pengaturan default dan pilih **Berikutnya: Respons otomatis >** .

8. Di tab Respons otomatis, perhatikan bagaimana Anda dapat menambahkan buku pedoman untuk mengotomatiskan respons.  Demikian pula, Anda dapat membuat aturan otomatisasi insiden.  Pilih **+ Add** baru di bawah otomatisasi insiden.  Jendela untuk membuat otomatisasi baru akan terbuka.  Aturan otomatisasi apa pun yang Anda buat di halaman ini dipicu oleh aturan analitik Anda c Perhatikan bahwa Anda dapat menambahkan ketentuan dan menetapkan tindakan untuk aturan tersebut.   Pilih **Cancel** untuk keluar dari jendela.

9. Pilih **Berikutnya: Tinjau>** untuk meninjau semua detail yang terkait dengan aturan dan berdasarkan templat yang dipilih. Pada titik ini, Anda dapat memilih untuk membuat aturan, dengan memilih **Create** atau keluar tanpa membuat aturan dengan memilih **X** di pojok kanan atas halaman.

10. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="task-5--in-the-previous-task-you-created-an-analytics-rule-to-be-alerted-of-suspicious-activities--embedded-in-that-wizard-is-the-option-to-automate-the-response-to-an-incident-based-on-the-specific-rule--but-you-can-also-create-automation-rules-by-going-directly-to-the-automation-configuration-option"></a>Tugas 5:  Di tugas berikutnya, Anda akan membuat aturan analitik untuk diberikan peringatan tentang aktivitas yang mencurigakan.  Fitur yang tersemat di wizard adalah opsi untuk mengotomatisasi respons untuk insiden berdasarkan aturan tertentu.  Namun, Anda juga dapat membuat aturan otomatisasi dengan langsung ke opsi konfigurasi otomatisasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  

2. Pilih **+ Buat**. Sekarang di menu tarik-turun, perhatikan bagaimana Anda dapat memilih antara menambahkan playbook baru atau menambahkan aturan baru.  Pilih **Tambahkan aturan baru**.  

3. Jendela untuk membuat otomatisasi baru akan terbuka.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.  Hanya saja, perbedaanya adalah kondisi pertamanya, Anda harus mengaitkan aturan analitik yang ingin Anda terapkan pada aturan otomatisasi ini.  Fungsi ini tidak tersedia pada tugas sebelumnya karena otomatisasi masih dikonfigurasikan untuk aturan tertentu.  Pilih **Cancel** untuk keluar dari jendela Buat aturan otomatisasi baru.

4. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.


#### <a name="task-6--delete-microsoft-sentinel-resource-group--microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-lab-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-features-of-capabilities-of-microsoft-sentinel"></a>Tugas 6:  Hapus grup Sumber Daya Microsoft Sentinel.  Microsoft Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Microsoft Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari lab ini minimal, Anda disarankan untuk menghapus grup sumber daya Microsoft Sentinel setelah Anda selesai menjelajahi fitur kemampuan Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di pojok kiri atas halaman, di atas bagian yang tertulis Microsoft Sentinel, pilih **Semua Layanan**.

2. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

3. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-ResourceGroup**.

4. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya,  **SC900-ResourceGroup**, lalu klik **Delete** di bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

5. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser. 


#### <a name="review"></a>Tinjau

Di lab ini, Anda telah mempelajari proses membuat instans Microsoft Sentinel.  Anda juga menyiapkan izin untuk memastikan akses ke sumber daya yang terkait dengan instans Microsoft Sentinel Anda.  Dengan instans Microsoft Sentinel yang dibuat, Anda mengikuti langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data Anda, menggunakan aturan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan terakhir Anda menjelajahi kemampuan otomatisasi. Anda mengakhiri lab dengan menghapus grup sumber daya yang terkait dengan instans Microsoft Sentinel yang Anda buat.
