<a name="---"></a><!---
---
Lab: Judul: 'Menjelajahi Microsoft Defender untuk Cloud ' Modul: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 4: Menjelaskan kemampuan perlindungan ancaman Microsoft 365; Pelajaran 5: Jelaskan Microsoft Defender for Cloud Apps'
---
--->

# <a name="lab-explore-microsoft-defender-for-cloud-apps"></a>Lab: Menjelajahi Aplikasi Microsoft Defender untuk Cloud

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan perlindungan ancaman Microsoft 365
- Pelajaran: Menjelaskan Aplikasi Microsoft Defender untuk Cloud

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari kemampuan Aplikasi Microsoft Defender untuk Cloud.  Anda akan mempelajari informasi yang tersedia di dasbor Cloud Discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan, dan cara mengontrol dampak terhadap organisasi Anda melalui kebijakan. Catatan: Organisasi harus memiliki lisensi untuk menggunakan Aplikasi Microsoft Defender untuk Cloud yang merupakan layanan langganan berbasis pengguna.

**Perkiraan Waktu**: 15-20 menit

### <a name="task-1---explore-cloud-discovery"></a>Tugas 1 - Menjelajahi temuan Cloud

Mempelajari Cloud Discovery.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia hosting lab Anda) lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di Pusat admin, pilih **Security**.  Halaman browser baru terbuka ke halaman selamat datang di portal Pertahanan Microsoft 365.  

1. Jika ini adalah pertama kalinya Anda mengunjungi portal Pertahanan Microsoft 365, Anda mungkin akan melihat jendela pop-up untuk mengikuti tur singkat.  Tutup jendela ini.

1. Dari panel navigasi kiri, pilih **Aplikasi Cloud** untuk meluaskan daftar, lalu pilih **Cloud Discovery**. Tindakan ini akan membawa Anda ke tampilan Dasbor.  Catat informasi yang tersedia di dasbor. Dari tampilan dasbor, Anda dapat memilih berbagai tab dari bagian atas halaman.  

1. Pilih **Aplikasi yang ditemukan**. Jendela aplikasi yang ditemukan memberikan tampilan yang lebih mendetail tentang aplikasi yang ditemukan, termasuk skor risiko, lalu lintas, jumlah pengguna, dan lainnya.
    1. Dari semua item dalam daftar, pilih **ellipses** di kolom tindakan tabel.  Perhatikan berbagai opsi yang tersedia, termasuk kemampuan untuk menandai aplikasi sebagai disetujui atau tidak.  Pilih **elipsis**, sekali lagi, untuk menutup kotak tindakan.
    1. Memilih item baris tertentu akan membuka halaman detail untuk aplikasi tertentu.  Pilih item dari daftar dan tinjau informasi yang tersedia di halaman ringkasan.  Untuk item yang dipilih, pilih tab **Penggunaan aplikasi cloud** untuk melihat informasi selengkapnya, termasuk **Penggunaan**, **Pengguna, IP**, **Alamat**, dan **Peringatan**. Setelah selesai menjelajahi halaman detail, kembali ke halaman aplikasi yang ditemukan, dengan memilih **Cloud Discovery** dari bread crumb di bagian atas halaman.  Jika memilih Cloud discovery dari panel navigasi kiri, Anda akan dibawa kembali ke tampilan dasbor.
    1. Dari bagian atas halaman, pilih tab **alamat IP**. Di sini Anda akan menemukan data termasuk jumlah transaksi, jumlah lalu lintas dan jumlah unggahan, berdasarkan alamat IP.  Perhatikan bahwa Anda juga dapat memfilter menurut alamat IP tertentu atau mengekspor data untuk analisis lebih lanjut.
    1. Dari bagian atas halaman, pilih **Pengguna**.  Ini adalah jenis informasi yang sama yang diberikan saat Anda memilih alamat IP, namun terdaftar untuk masing-masing pengguna.  Di sini, sekali lagi, Anda memfilter menurut pengguna tertentu dan mengekspor data untuk analisis lebih lanjut.

1. Informasi yang diberikan di halaman Cloud Discovery dan tab terkait didasarkan pada laporan cuplikan dari log lalu lintas yang Anda unggah secara manual dari firewall dan proksi atau dari laporan berkelanjutan yang menganalisis semua log yang diteruskan dari jaringan Anda menggunakan Cloud App Security.  Untuk melihat tempat informasi ini disiapkan, pilih **Tindakan** di pojok kanan atas halaman.
    1. Pilih opsi pertama, **Buat laporan snapshot Cloud Discovery** lalu pilih **Berikutnya**. Di sini, Anda akan mengisi detail yang diminta dan mengunggah log lalu lintas untuk menghasilkan dan mengunggah laporan.  Pilih **Keluar** dan jika diminta dengan Apakah Anda yakin, pilih **Keluar** lagi.  Data yang ditampilkan untuk penyewa lab Anda berasal dari laporan Snapshot, Anda dapat melihat informasi ini di bagian atas jendela Cloud Discovery.
    1. Untuk melihat opsi laporan berkelanjutan, pilih **Tindakan** di pojok kanan atas halaman dan dari menu dropdown pilih **Konfigurasikan unggahan otomatis**.  Tidak ada sumber data yang terhubung, tetapi di sinilah Anda akan menambahkan sumber data. Pilih **Tambahkan sumber data** lalu pilih panah menu dropdown di bidang **Pilih alat** untuk melihat jenis alat yang dapat Anda sambungkan sebagai sumber data.  Pilih **Batal** untuk keluar, 
    1. Dari panel navigasi kiri, pilih **Cloud discovery** untuk kembali ke halaman Cloud discovery.

1. Anda dapat terhubung ke aplikasi secara langsung dengan menyiapkan konektor aplikasi yang akan memberi visibilitas dan kontrol lebih besar atas aplikasi cloud Anda. Dari pojok kanan atas layar, pilih **Tindakan** lalu pilih **Pengaturan Cloud Discovery**.  Dari sisi kiri layar, di bagian Aplikasi yang terhubung, pilih **Konektor aplikasi**.  

    1. Di halaman Aplikasi yang terhubung, pilih *Office 365** dari daftar untuk melihat informasi selengkapnya. Jika Office 365 menampilkan kesalahan koneksi, kemungkinan besar karena Audit tidak diaktifkan.  Jika audit diaktifkan, buka elipsis vertikal di sisi kanan item baris, lalu pilih **edit pengaturan**.  Untuk menghubungkan kembali, pilih **Hubungkan Office 365** di bagian bawah halaman. Halaman seharusnya sekarang menunjukkan bahwa Office 365 terhubung, pilih **Selesai**.  Status sekarang akan ditampilkan dengan tanda peringatan kuning, menunjukkan tidak ada status terbaru.  Perlu beberapa waktu untuk memperbarui status karena periode waktu pemindaian retroaktif berbeda untuk setiap aplikasi, dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya.
    1. Sekarang Anda akan menyiapkan konektor aplikasi baru.  Pilih **+Connect an app** dan dari daftar tarik-turun pilih **Microsoft Azure**.  Dari jendela pop-up Microsoft Azure, pilih **Hubungkan Microsoft Azure** lalu pilih **Selesai**.  Anda akan melihat status terhubung (jika tidak melihatnya, refresh browser) dan informasi tentang pemindaian pengguna, data, dan aktivitas.  Kembali ke dasbor Cloud Discovery, dengan memilih **Cloud Discovery** dari panel navigasi paling kiri.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-part-2---explore-the-cloud-app-catalog"></a>Tugas Bagian 2 - Menjelajahi katalog aplikasi Cloud

Cloud Discovery menganalisis log lalu lintas Anda berdasarkan katalog aplikasi cloud Aplikasi Microsoft Defender untuk Cloud yang berisi lebih dari 31.000 aplikasi cloud. Aplikasi diberi peringkat dan skor berdasarkan lebih dari 80 faktor risiko untuk memberi Anda visibilitas berkelanjutan ke penggunaan cloud, Shadow IT, dan risiko yang ditimbulkan Shadow IT pada organisasi Anda.  Dalam tugas ini, Anda akan mempelajari kemampuan katalog aplikasi Cloud.

1. Dari panel navigasi kiri, pilih **Katalog aplikasi cloud**.

1. Katalog aplikasi Cloud memungkinkan Anda memilih aplikasi yang sesuai dengan persyaratan keamanan organisasi Anda. Admin dapat melakukan pemfilteran dasar pada aplikasi seperti yang ditampilkan di bagian atas halaman, yang mencakup apakah aplikasi diberi sanksi, tidak diberi sanksi, atau tidak memiliki tag, skor risiko, faktor risiko Kepatuhan, dan faktor risiko keamanan.  Misalnya, pemfilteran berdasarkan faktor risiko kepatuhan memungkinkan Anda menelusuri standar, sertifikasi, dan kepatuhan tertentu yang mungkin dipatuhi oleh aplikasi. Contohnya termasuk HIPAA, ISO 27001, SOC 2, dan PCI-DSS. Pilih **Faktor risiko kepatuhan** untuk melihat opsi yang tersedia.  Anda dapat memfilter lebih lanjut berdasarkan skor risiko, dengan menggerakkan penggeser pada skor risiko di bagian atas halaman. Jika Anda memindahkan slide, pastikan untuk mengaturnya sehingga rentangnya diatur dari 0 hingga 10.

1. Admin juga dapat mencari aplikasi berdasarkan kategori.  Misalnya pada kolom pencarian kategori masukkan **Jejaring sosial**, lalu pilih **Jejaring sosial**.  Pilih **Yammer** untuk melihat selengkapnya.  Mengarahkan mouse Anda ke topik apa pun untuk kategori tertentu akan menampilkan ikon informasi yang dapat Anda pilih untuk mendapatkan informasi lebih lanjut tentang topik tersebut.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-3---explore-the-activity-log-and-files"></a>Tugas 3 - Menjelajahi log Aktivitas dan File

Menjelajahi cara-cara menyelidiki aktivitas yang direkam dengan log aktivitas dan file.

1. Dari panel navigasi kiri, pilih dan jelajahi opsi **File** dan catat opsi untuk memfilter data berdasarkan aplikasi, pemilik, tingkat akses, jenis file, dan kebijakan yang cocok. Perhatikan juga opsi untuk membuat kebijakan baru dari penelusuran dan ekspor data.
    1. Pilih **+ Kebijakan baru dari pencarian**.  Perhatikan bagaimana Anda dapat membuat kebijakan berdasarkan templat, memilih tingkat keparahan & kategori kebijakan, membuat filter untuk kebijakan, membuat peringatan, dan bahkan mengirim peringatan ke Power Automate.  Pilih **Batalkan** untuk keluar dari jendela pembuatan kebijakan, lalu pilih **Tinggalkan halaman**.

1. Dari panel navigasi kiri, pilih **Log Aktivitas**. Di sini, Anda mendapatkan visibilitas ke semua aktivitas dari aplikasi yang terhubung. Anda mungkin tidak melihat data apa pun yang tercantum karena memerlukan waktu beberapa jam untuk melakukan pemindaian retroaktif setelah audit diaktifkan dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya. Perhatikan opsi filter yang tersedia dan opsi untuk membuat kebijakan baru dari pencarian.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-4---explore-policies"></a>Tugas 4 - Menjelajahi Kebijakan

Dalam tugas ini, Anda akan mempelajari kebijakan di Aplikasi Microsoft Defender untuk Cloud.

1. Dari panel navigasi kiri, pilih **Kebijakan** lalu pilih **Manajemen kebijakan**.  Kebijakan yang tercantum memberikan informasi tentang jumlah peringatan yang dihasilkan oleh kebijakan, keparahan, dll. Memilih item baris mana pun memberikan informasi yang lebih detail tentang kebijakan. Pilih item dari daftar, mis., **Risky sign-in**.

    1. Perhatikan bahwa Anda juga dapat membuat kebijakan. Pilih **+ Buat kebijakan** untuk melihat jenis kebijakan yang dapat Anda buat.  Pilih **Kebijakan aktivitas** untuk melihat berbagai opsi yang tersedia untuk membuat kebijakan.  Pilih **Batalkan** untuk keluar dari jendela konfigurasi.
    1. Perhatikan bahwa Anda juga dapat memiliki opsi untuk mengekspor informasi kebijakan.

1. Dari panel navigasi kiri, pilih **Template kebijakan**. Untuk membuat kebijakan dari salah satu template yang tersedia, pilih **+** di sebelah kiri item baris template.  Lihat berbagai opsi konfigurasi untuk kebijakan.  Pilih **Batalkan** untuk keluar dari halaman.

1. Tutup jendela browser.

### <a name="review"></a>Tinjau

Di lab ini, Anda menjelajahi kemampuan Aplikasi Microsoft Defender untuk Cloud.  Anda mempelajari informasi yang tersedia di dasbor Cloud Discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan, dan cara mengontrol dampak terhadap organisasi Anda melalui kebijakan.
