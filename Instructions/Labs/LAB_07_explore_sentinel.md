---
lab:
    title: 'Menjelajahi Microsoft Sentinel'
    module: 'Modul 3 Pelajaran 3: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan keamanan Microsoft Sentinel'
---


# Lab: 'Menjelajahi Microsoft Sentinel' 

## Skenario lab
Pada lab ini, Anda akan mempelajari proses membuat instans Microsoft Sentinel.  Anda juga akan menyiapkan izin guna memastikan akses ke sumber daya yang akan disebarkan untuk mendukung Microsoft Sentinel.  Setelah penyiapan dasar ini selesai, Anda akan mempelajari langkah-langkah menghubungkan Microsoft Sentinel ke sumber data, menggunakan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan di penghujung pelatihan, Anda akan menjelajahi kemampuan otomatisasi.  

  

**Perkiraan Waktu**: 30-45 menit

#### Tugas 1:  Membuat instans Microsoft Sentinel.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

2. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

3. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger) lalu klik **All Services**.  

4. Di kotak layanan filter, masukkan **Microsoft Sentinel**, lalu pilih **Microsoft Sentinel** dari daftar.

5. Dari halaman Microsoft Sentinel, pilih **Create Microsoft Sentinel**.

6. Dari halaman Tambahkan Microsoft Sentinel ke halaman ruang kerja, pilih **Create a new workspace**.

7. Darii tab dasar ruang kerja Buat Log Analitik, masukkan berikut ini:
    1. Langganan:  **Azure Pass – Sponsorship**
   
    1. Grup sumber daya: pilih **Create New**, lalu masukkan nama **SC900-ResourceGroup**, lalu pilih **OK**.
    1. Nama: **SC900-LogAnalytics-workspace**.
    1. Kawasan: **East US** (biarkan default)
    1. Pilih **Next: Tingkat harga >**

8. Untuk Tingkat Harga, biarkan pengaturan default: **Pay-as-you-go (per GB 2018)**, lalu pilih **Next: Tags >**.

9. Untuk Tag, Anda dapat mengosongkannya, lalu pilih **Review + Create**.

10. Verifikasi informasi yang Anda masukkan, lalu pilih **Create**.

11. Jika Anda tidak melihat ruang kerja baru terdaftar, klik **Refresh**, lalu klik **Add**.

12. Setelah ruang karja baru ditambahkan, halaman berita & panduan | Microsoft Sentinel akan muncul.  Perhatikan tiga langkah yang terdaftar pada halaman Memulai.

13. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Tugas 2:  Karena instans Microsoft Sentinel sudah dibuat, Anda pasti ingin memastikan bahwa Anda memiliki akses yang diperlukan ke sumber daya yang disebar untuk mendukung Microsoft Sentinel.  Pada tugas ini, Anda akan membuka halaman kontrol akses (IAM) untuk grup sumber daya yang sudah Anda buat dengan instans Microsoft Sentinel, melihat peran yang tersedia, dan menetapkan Anda (administrator MOD) sebagai pemegang peran yang diperlukan. Menetapkan peran di tingkat grup sumber daya akan memastikan peran akan diterapkan ke seluruh sumber daya yang disebar untuk mendukung Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di sudut kiri atas halaman, di atas tempat yang bertuliskan Microsoft Sentinel, pilih **All Services**.

2. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

3. Di halaman Grup sumber daya, klik grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-ResourceGroup**.

4. Di SC900-ResourceGroup, klik **Access control (IAM)** di panel navigasi sebelah kiri.

5. Dari halaman Kontrol akses, pilih **View my access**.  Perhatikan bahwa peran saat ini adalah Admin keamanan.  Tutup jendela penetapan Administrator MOD dengan mengeklik **X** di bagian pojok kanan atas halaman.

6. Dari halaman Kontrol akses, pilih **+Add**, lalu pilih **Add role assignment**.

7. Jendela Tambahkan penetapan peran akan terbuka.  Pilih panah tarik-turun di bidang Pilih peran untuk menampilkan peran yang tersedia.  Untuk lab ini, klik **Owner**.  CATATAN:  Untuk praktik terbaiknya Anda harus menetapkan hak istimewa minimum yang diperlukan untuk peran.  Sebagai referensi, tinjau izin di Microsoft Sentinel:  https://docs.microsoft.com/en-us/azure/sentinel/roles

8. Dari daftar pengguna yang ditampilkan, pilih **MOD Administrator**.

9. Pilih **Save** di bagian bawah halaman.

10. Dari halaman kontrol akses, pilih **View my access** untuk mengonfirmasi peran telah ditambahkan, lalu tutup jendela dengan memilih **X** di sudut kanan atas jendela.

11. Kembali ke halaman Semua layanan Azure, dengan mengeklik **All Services** di pojok kiri atas halaman, di atas yang bertuliskan Grup sumber daya.

#### Tugas 3:  Pada tugas ini, Anda akan mempelajari proses menghubungkan Microsoft Sentinel ke data sumber Anda untuk mulai mengumpulkan data. Catatan: Perlu waktu yang lama untuk menampilkan status terhubung konektor (~30 menit, tergantung pada penyewa).

1. Di Kotak layanan filter dari halaman Semua layanan, masukkan **Microsoft Sentinel**, lalu klik **Microsoft Sentinel** darii daftar hasil. 

2. Dari halaman Microsoft Sentinel, pilih ruang kerja yang Anda buat dengan instans Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

3. Langkah pertama dengan Microsoft Sentinel adalah dapat mengumpulkan data. Dari panel navigasi kiri, pilih **Data connectors**, yang terdaftar di bawah konfigurasi.

4. Dari halaman Konektor data, gulir ke bawah pada jendela utama untuk melihat daftar ekstensif konektor yang tersedia. Di kotak Pencarian halaman konektor data, masukkan **Azure**, lalu dari daftar pilih **Azure Active Directory**.

5. Jendela konektor Azure Active Directory terbuka.  Pilih **Open connector page**.

6. Dari halaman konektor Azure Active Directory, tinjau deskripsi dan catat konten terkait yang menyertakan buku kerja, kueri, dan templat aturan analitik.  

7. Tab instruksi di jendela utama, menyediakan fasilitas tambahan untuk Microsoft Sentinel guna diintegrasikan dengan Azure Active Directory.   Di bawah konfigurasi, pilih **Sign-in logs**, lalu pilih Apply Changes (dapat memilih beberapa konektor).

8. Di tab Langkah selanjutnya, catat daftar buku kerja yang direkomendasikan.   Di bawah buku kerja yang direkomendasikan, pilih **Azure Sign-in logs** (dapat memilih buku kerja tambahan).

9. Dari halaman buku kerja dan dengan tab templat yang dipilih (digarisbawahi), pilih **Azure Sign-in logs**. 

10. Dari jendela log masuk Azure AD yang terbuka, tinjau deskripsi, dan pilih **View template**.  Keluar dari templat, dengan mengeklik **X** di pojok kanan atas layar.  Pilih **Save** dari bagian bawah halaman, lalu pilih **OK** untuk menyimpan buku kerja ke lokasi default.

11. Di pojok kiri atas dari halaman Buku kerja, di atas yang bertuliskan Buku kerja, **Microsoft Sentinel**. Ini akan mengembalikan Anda ke halaman Konektor Data Microsoft Sentinel.

12. Di bagian atas halaman Konektor data akan menampilkan 1 terhubung, untuk menunjukkan bahwa sekarang Anda sudah terhubung ke Azure Active Directory.

13. Dari panel navigasi sebelah kiri, pilih **Workbooks**.

14. Dari halaman Buku Kerja, pilih tab **My workbooks**, yang berada di atas kotak pencarian.  Buku kerja yang baru disimpan akan terdaftar dan tersedia untuk Anda lihat dan mengawasi data Anda.

15. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Tugas 4:  Di tugas ini, Anda akan mempelajari proses menggunakan templat aturan analitik bawaan untuk membuat aturan agar diberi pemberitahuan ketika terjadi hal yang mencurigakan.

1. Di panel navigasi sebelah kiri, klik **Analitik**.

2. Halaman analitik akan menampilkan aturan yang aktif (Deteksi serangan multitahap tingkat lanjut diaktifkan secara default) dan akan menyediakan akses ke Templat aturan.  Pilih tab **Rule templates**.  Perhatikan daftar templat yang tersedia dan cara lain untuk memfilter daftar.  Dengan menggunakan peringatan analitik bawaan dalam ruang kerja Microsoft Sentinel, Anda akan diberi tahu jika terjadi sesuatu yang mencurigakan.

3. Di bilah Pencarian, masukkan **Azure Portal**.  Pilih **Failed login attempts to Azure Portal**.  

4. Di jendela yang terbuka, baca deskripsi dan tinjau informasi terkait dengan templat.  Pilih **Create rule** di bagian bawah halaman.

5. Dari wizard Aturan analitik, tinjau informasinya, lalu pilih **Next: Set rule logic >**.

6. Halaman Setel logika aturan, adalah tempat Anda menentukan logika untuk aturan analitik baru Anda. Templat sudah menyediakan beberapa logika dan pengaturan yang telah ditentukan sebelumnya.  Gulir halaman untuk melihat pengaturan yang tersedia.  Biarkan default. Pilih **Next: Incident settings (preview)>**.

7. Dengan pengaturan Insiden, Microsoft Sentinel dapat dikelompokkan bersama menjadi Insiden yang harus diperhatikan. Anda dapat menyetel apakah peringatan yang dipicu oleh aturan analitik ini harus menghasilkan insiden.  Biarkan pengaturan default dan pilih **Next: Automated response >**.

8. Di tab Respons otomatis, perhatikan bagaimana Anda dapat menambahkan buku pedoman untuk mengotomatiskan respons.  Demikian pula, Anda dapat membuat aturan otomatisasi insiden.  Pilih **+ Add** baru di bawah otomatisasi insiden.  Jendela untuk membuat aturan otomatisasi baru akan terbuka.  Aturan otomatisasi apa pun yang Anda buat di halaman ini dipicu oleh aturan analitik Anda c Perhatikan bahwa Anda dapat menambahkan ketentuan dan menetapkan tindakan untuk aturan tersebut.   Pilih **Cancel** untuk keluar dari jendela.

9. Pilih **Next: Review>** untuk meninjau semua detail yang terkait dengan aturan dan berdasarkan templat yang dipilih. Pada titik ini, Anda dapat memilih untuk membuat aturan, dengan memilih **Create** atau keluar tanpa membuat aturan dengan memilih **X** di pojok kanan atas halaman.

10. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

#### Tugas 5:  Di tugas berikutnya, Anda akan membuat aturan analitik untuk diberikan peringatan tentang aktivitas yang mencurigakan.  Fitur yang tersemat di wizard adalah opsi untuk mengotomatisasi respons untuk insiden berdasarkan aturan tertentu.  Namun, Anda juga dapat membuat aturan otomatisasi dengan langsung ke opsi konfigurasi otomatisasi.

1. Dari panel navigasi sebelah kiri, pilih **Automation**.  

2. Pilih **+ Create**. Sekarang di menu tarik-turun, perhatikan bagaimana Anda dapat memilih antara menambahkan playbook baru atau menambahkan aturan baru.  Pilih **Add new rule**.  

3. Jendela untuk membuat otomatisasi baru akan terbuka.  Perhatikan bahwa Anda dapat menambahkan kondisi dan mengatur tindakan untuk aturan.  Hanya saja, perbedaanya adalah kondisi pertamanya, Anda harus mengaitkan aturan analitik yang ingin Anda terapkan pada aturan otomatisasi ini.  Fungsi ini tidak tersedia pada tugas sebelumnya karena otomatisasi masih dikonfigurasikan untuk aturan tertentu.  Pilih **Cancel** untuk keluar dari jendela Buat aturan otomatisasi baru.

4. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.


#### Tugas 6:  Menghapus grup Sumber Daya Microsoft Sentinel.  Microsoft Sentinel ditagih berdasarkan volume data yang diserap untuk analisis di Microsoft Sentinel. Meskipun jumlah data yang diserap sebagai hasil dari lab ini minimal, sebaiknya Anda menghapus grup sumber daya Microsoft Sentinel saat Anda selesai menjelajahi fitur kemampuan Microsoft Sentinel.

1. Dari halaman Microsoft Sentinel, di sudut kiri atas halaman, di atas tempat yang bertuliskan Microsoft Sentinel, pilih **All Services**.

2. Di kotak layanan filter, masukkan grup sumber daya, lalu dari daftar yang disediakan, pilih **Resource groups**.

3. Di halaman Grup sumber daya, klik grup sumber daya yang Anda buat dengan Microsoft Sentinel, **SC900-ResourceGroup**.

4. Dari bagian tengah atas halaman, pilih **Delete resource group**.  Tinjau peringatannya.  Masukkan nama grup sumber daya, **SC900-ResourceGroup**, lalu klik **Delete** di bagian bawah halaman.  Diperlukan beberapa menit untuk menghapus grup sumber daya.

5. Setelah Anda memverifikasi grup sumber daya telah dihapus, tutup halaman browser. 


#### Tinjauan

Pada lab ini, Anda sudah mempelajari proses membuat instans Microsoft Sentinel.  Anda juga sudah menyiapkan izin untuk memastikan akses ke sumber daya yang dikaitkan dengan instans Microsoft Sentinel.  Setelah instans Microsoft Sentinel dibuat, Anda sudah mempelajari langkah-langkah menghubungkan Microsoft Sentinel ke sumber data, menggunakan aturan analitik bawaan untuk mendapatkan pemberitahuan tentang semua hal yang mencurigakan, dan di penghujung pelatihan, Anda sudah menjelajahi kemampuan otomatisasi. Anda sudah menyelesaikan lab dengan menghapus grup sumber daya yang dikaitkan dengan instans Microsoft Sentinel yang Anda buat.
