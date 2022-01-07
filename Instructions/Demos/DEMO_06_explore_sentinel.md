---
Demo:
    title: 'Microsoft Sentinel'
    module: 'Modul 3 Pelajaran 3: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan keamanan Microsoft Sentinel'
---


# Demo: 'Microsoft Sentinel' 

### Skenario demo
Pada demo ini, Anda akan mempelajari proses membuat instans Microsoft Sentinel.  Anda juga akan menyiapkan izin guna memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan mempelajari langkah-langkah menghubungkan Microsoft Sentinel ke sumber data, menggunakan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan di penghujung pelatihan, Anda akan menjelajahi kemampuan otomatisasi.  

#### Demo Bagian 1:  Membuat instans Microsoft Sentinel

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, di bilah biru bagian atas halaman di sebelah tulisan Microsoft Azure, ketikkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih **Create Microsoft Sentinel**.

1. Dari halaman Tambahkan Microsoft Sentinel ke halaman ruang kerja, pilih **Create a new workspace**.

1. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsorship**
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-Sentinel-RG**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan: **East US** (biarkan default)
    1. Pilih **Next: Tingkat harga >**

1. Untuk Tingkat Harga, biarkan pengaturan default: **Pay-as-you-go (per GB 2018)**, lalu pilih **Next: Tags >**.

1. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

1. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

1. Mungkin perlu satu atau dua menit untuk mendaftarkan satu ruang kerja, jika Anda masih tidak melihatnya, pilih **Refresh**, lalu pilih **Add**.

1. Setelah ruang karja baru ditambahkan, halaman berita & panduan | Azure Sentinel akan muncul.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Demo Bagian 2:  Karena instans Microsoft Sentinel sudah dibuat, Anda pasti ingin memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebar untuk mendukung Microsoft Sentinel.  Pada tugas ini, Anda akan membuka halaman kontrol akses (IAM) untuk grup sumber daya yang sudah Anda buat dengan instans Microsoft Sentinel, melihat peran yang tersedia, dan menetapkan Anda (administrator MOD) sebagai pemegang peran yang diperlukan. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan diterapkan ke seluruh sumber daya yang disebar untuk mendukung Microsoft Sentinel.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **resource groups**, lalu pilih **Resource groups** dari hasil pencarian.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari SC900-Sentinel-RG, pilih **Access control (IAM)** dari panel navigasi sebelah kiri.

1. Dari halaman Kontrol akses, pilih **View my access**.  Ingat bahwa peran saat ini adalah Administrator layanan.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

1. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

1. Jendela Tambahkan penetapan peran akan terbuka.  Pilih panah tarik-turun di bidang Pilih peran untuk menampilkan peran yang tersedia. Di kotak pencarian pilih peran, ketikkan **Microsoft sentinel** untuk melihat 4 peran yang terkait dengan Microsoft Sentinel. Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  Untuk kenyamanan lab ini, masukkan **Owner** di kotak pencarian dan pilih **Owner** dari hasil tersebut.  Sebagai referensi, tinjau izin di Microsoft Sentinel:  https://docs.microsoft.com/id-id/azure/sentinel/roles

1. Dari daftar pengguna yang ditampilkan, pilih **MOD Administrator**.

1. Pilih **Save** di bagian bawah halaman.

1. Dari halaman kontrol akses, pilih **View my access** untuk mengonfirmasi peran telah ditambahkan, lalu tutup jendela dengan memilih **X** di sudut kanan atas jendela.

#### Demo Bagian 3:  Di bagian demo ini, Anda akan menjalani proses menghubungkan Microsoft Sentinel ke sumber data untuk mulai mengumpulkan data.  Catatan: Perlu waktu yang lama untuk menampilkan status terhubung konektor (~30 menit, tergantung pada penyewa).

1. Di kotak pencarian, di bilah biru bagian atas halaman di sebelah tulisan Microsoft Azure, ketikkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari hasil pencarian.

1. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

1. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Azure**, lalu dari daftar pilih **Azure Active Directory**.

1. Jendela konektor Azure Active Directory terbuka.  Pilih **Open connector page**.

1. Dari halaman konektor Azure Active Directory, tinjau deskripsi dan catat konten terkait yang menyertakan buku kerja, kueri, dan templat aturan analitik.  

1. Tab instruksi di jendela utama, menyediakan fasilitas tambahan untuk Microsoft Sentinel guna diintegrasikan dengan Azure Active Directory.   Di bawah konfigurasi, pilih **Sign-in logs**, lalu pilih Apply Changes (dapat memilih beberapa konektor).  Catatan: perlu beberapa saat sebelum Anda melihat status konektor terhubung (~30 menit atau lebih).  Sebagai acuan:
    1. Tinjau izin di Microsoft Sentinel:  https://docs.microsoft.com/id-id/azure/sentinel/roles
    1. Sambungkan ke Azure Active Directory:  https://docs.microsoft.com/id-id/azure/sentinel/connect-azure-active-directory

1. Di tab Langkah selanjutnya, catat daftar buku kerja yang direkomendasikan.   Di bawah buku kerja yang direkomendasikan, pilih **Azure Sign-in logs** (dapat memilih buku kerja tambahan).

1. Dari halaman buku kerja dan dengan tab templat yang dipilih (digarisbawahi), pilih **Azure Sign-in logs**.

1. Dari jendela log masuk Azure AD yang terbuka, tinjau deskripsi, dan pilih **View template**.  Keluar dari templat, dengan mengeklik **X** di pojok kanan atas layar.  Pilih **Save** dari bagian bawah halaman, lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.

1. Di pojok kiri atas dari halaman Buku kerja, di atas yang bertuliskan Buku kerja, **Microsoft Sentinel**. Ini akan mengembalikan Anda ke halaman Konektor Data Microsoft Sentinel.

1. Di bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa sekarang Anda sudah terhubung ke Azure Active Directory.

1. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

1. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan akan terdaftar dan tersedia untuk Anda lihat dan mengawasi data Anda.  Masuk berikutnya akan tercatat dalam buku kerja, jadi Anda dapat memilih untuk menampilkannya.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Demo Bagian 4 (Opsional):  Di bagian demo ini, Anda akan menjalani proses penggunaan templat aturan analitik bawaan untuk membuat aturan agar mendapat pemberitahuan saat terjadi sesuatu yang mencurigakan.

1. Di panel navigasi sebelah kiri, klik **Analitik**.

1. Halaman analitik akan menampilkan aturan yang aktif (Deteksi serangan multitahap tingkat lanjut diaktifkan secara default) dan akan menyediakan akses ke Templat aturan.  Pilih tab **Rule templates**.  Perhatikan daftar templat yang tersedia dan cara lain untuk memfilter daftar.  Dengan menggunakan peringatan analitik bawaan dalam ruang kerja Microsoft Sentinel, Anda akan diberi tahu jika terjadi sesuatu yang mencurigakan.

1. Di bilah Pencarian, masukkan **Azure Portal**.  Pilih **Failed login attempts to Azure Portal**.  

1. Di jendela yang terbuka, baca deskripsi dan tinjau informasi terkait dengan templat.  Pilih **Create rule** di bagian bawah halaman.
    1. Dari wizard Aturan analitik, tinjau informasinya, lalu pilih **Next: Set rule logic >**.
    1. Halaman Setel logika aturan, adalah tempat Anda menentukan logika untuk aturan analitik baru Anda. Templat sudah menyediakan beberapa logika dan pengaturan yang telah ditentukan sebelumnya.  Gulir halaman untuk melihat pengaturan yang tersedia.  Biarkan default. Pilih **Next: Incident settings (preview)>**.
    1. Dengan pengaturan Insiden, Microsoft Sentinel dapat dikelompokkan bersama menjadi Insiden yang harus diperhatikan. Anda dapat menyetel apakah peringatan yang dipicu oleh aturan analitik ini harus menghasilkan insiden.  Biarkan pengaturan default dan pilih **Next: Automated response >**.
    1. Di tab Respons otomatis, perhatikan bagaimana Anda dapat menambahkan buku pedoman untuk mengotomatiskan respons.  Demikian pula, Anda dapat membuat aturan otomatisasi insiden.  Pilih **+ Add** baru di bawah otomatisasi insiden.  Jendela untuk membuat otomatisasi baru akan terbuka.  Aturan otomasi apa pun yang Anda buat di halaman ini dipicu oleh aturan analisis yang tadinya Anda pilih, dalam hal ini, Upaya masuk yang gagal ke Portal Azure.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.   Pilih **Cancel** untuk keluar dari jendela.
    1. Pilih **Next: Review>** untuk meninjau semua detail yang terkait dengan aturan dan berdasarkan templat yang dipilih. Pada titik ini, Anda dapat memilih untuk membuat aturan, dengan memilih **Create** atau keluar tanpa membuat aturan dengan memilih **X** di pojok kanan atas halaman.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Demo Langkah 5 (Opsional):  Pada langkah sebelumnya, Anda telah membuat aturan analitik untuk diberi tahu tentang aktivitas yang mencurigakan.  Fitur yang tersemat di wizard adalah opsi untuk mengotomatisasi respons untuk insiden berdasarkan aturan tertentu.  Namun, Anda juga dapat membuat aturan otomatisasi dengan langsung ke opsi konfigurasi otomatisasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  

1. Pilih **+ Create**. Sekarang di menu tarik-turun, perhatikan bagaimana Anda dapat memilih antara menambahkan playbook baru atau menambahkan aturan baru.  Pilih **Add new rule**.  
    1. Jendela untuk membuat otomatisasi baru akan terbuka.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.  Hanya saja, perbedaanya adalah kondisi pertamanya, Anda harus mengaitkan aturan analitik yang ingin Anda terapkan pada aturan otomatisasi ini.  Fungsi ini tidak tersedia pada tugas sebelumnya karena otomatisasi masih dikonfigurasikan untuk aturan tertentu.  Pilih **Cancel** untuk keluar dari jendela Buat aturan otomatisasi baru.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Langkah 6: PENGHAPUSAN - Instruktur melakukan langkah ini setelah kelas. Menghapus grup Sumber Daya Microsoft Sentinel.  Microsoft Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Microsoft Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari lab ini minimal, sebaiknya Anda menghapus grup sumber daya Microsoft Sentinel saat Anda selesai menjelajahi fitur kemampuan Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di sudut kiri atas halaman, di atas tempat yang bertuliskan Microsoft Sentinel, pilih **All Services**.

1. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

1. Dari halaman Grup sumber daya, pilih grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya, **SC900-Sentinel-RG**, lalu pilih **Delete** dari bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

1. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser. 

#### Tinjauan

Dalam demo ini, Anda telah melihat proses pembuatan instans Microsoft Sentinel.  Anda telah melihat cara mengatur izin untuk memastikan akses ke sumber daya yang terkait dengan instans Microsoft Sentinel.  Dengan instans Microsoft Sentinel yang dibuat, Anda telah mengikuti langkah-langkah untuk menghubungkan Microsoft Sentinel ke sumber data, cara menggunakan aturan analitik bawaan untuk mendapatkan pemberitahuan tentang sesuatu yang mencurigakan, dan terakhir Anda telah menjelajahi kemampuan otomatisasi. Anda sudah menyelesaikan demo dengan menghapus grup sumber daya yang dikaitkan dengan instans Microsoft Sentinel yang Anda buat.