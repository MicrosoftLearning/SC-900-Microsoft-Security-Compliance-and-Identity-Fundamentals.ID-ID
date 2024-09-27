<!---
---
Demo: Judul: Modul aplikasi Microsoft Defender untuk Cloud: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 4: Menjelaskan kemampuan perlindungan ancaman Microsoft Defender XDR; Unit 5: Menjelaskan aplikasi Microsoft Defender untuk Cloud'
---
--->

# Demo: Microsoft Defender untuk Cloud Apps

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan perlindungan ancaman Microsoft Defender XDR
- Unit: Menjelaskan Microsoft Defender untuk Cloud Apps

## Skenario demo

Dalam demo ini, Anda akan menunjukkan kemampuan Aplikasi Microsoft Defender untuk Cloud.  Anda akan memandu pelajar melalui informasi yang tersedia di dasbor Cloud discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan dengan Log aktivitas dan File, serta cara mengontrol dampak terhadap organisasi Anda melalui Kebijakan.  Catatan: Organisasi harus memiliki lisensi untuk menggunakan Microsoft Defender untuk Cloud Apps yang merupakan layanan langganan berbasis pengguna.  

### Demo Bagian 1: Menjelajahi Cloud discovery

1. Di bilah alamat, masukkan **admin.microsoft.com**. Masuk dengan kredensial admin untuk penyewa Microsoft 365 yang disediakan oleh host lab resmi (ALH) Anda, untuk mengakses pusat admin Microsoft 365.

1. Dari panel navigasi kiri pusat admin Microsoft 365, pilih **Tampilkan semua**.

1. Di Pusat admin, pilih **Keamanan**.  Halaman browser baru terbuka ke halaman selamat datang portal Pertahanan Microsoft.  

1. Jika ini pertama kalinya Anda mengunjungi portal Pertahanan Microsoft, Anda mungkin mendapatkan jendela pop-up untuk mengikuti tur cepat.

1. Dari panel navigasi kiri, pilih **Cloud apps** untuk meluaskan daftar, lalu pilih **Cloud Discovery**. Tindakan ini akan membawa Anda ke tampilan Dasbor.  Catat informasi yang tersedia di dasbor. Dari tampilan dasbor, Anda dapat memilih berbagai tab dari bagian atas halaman.  Buka setiap tab di bagian atas laman.

1. Pilih **Aplikasi yang ditemukan**. Jendela aplikasi yang ditemukan menyediakan tampilan aplikasi yang ditemukan lebih terperinci, termasuk skor risiko, lalu lintas, jumlah pengguna, dan banyak lagi.
    1. Dari item apa pun dalam daftar, pilih **elipsis** di kolom tindakan tabel.  Perhatikan berbagai opsi yang tersedia, termasuk kemampuan untuk menandai aplikasi sebagai disetujui atau tidak disanksi.  Pilih elipsis, sekali lagi, untuk menutup kotak tindakan.
    1. Memilih item baris tertentu akan membuka laman detail untuk aplikasi tertentu.  Pilih item dari daftar.  Untuk item yang dipilih, pilih tab **Penggunaan aplikasi cloud** untuk melihat informasi selengkapnya, termasuk **Penggunaan**, **Pengguna, IP**, **Alamat**, dan **Peringatan**. Setelah selesai menjelajahi laman detail, kembali ke laman aplikasi yang ditemukan, dengan memilih **Cloud Discovery** dari bilah di bagian atas laman.  Jika memilih Cloud discovery dari panel navigasi kiri, Anda akan dibawa kembali ke tampilan dasbor.
    1. Dari bagian atas halaman, pilih tab **Alamat IP**. Di sini, Anda akan menemukan data termasuk jumlah transaksi, jumlah lalu lintas, dan jumlah unggahan berdasarkan alamat IP.  Perhatikan bahwa Anda juga dapat memfilter menurut alamat IP tertentu atau mengekspor data untuk analisis lebih lanjut.
    1. Dari bagian atas laman, pilih **Pengguna**.  Ini adalah jenis informasi yang sama yang diberikan saat Anda memilih alamat IP, tetapi terdaftar untuk masing-masing pengguna.  Di sini juga, Anda memfilter menurut pengguna tertentu dan mengekspor data untuk analisis lebih lanjut.

1. Hal penting yang perlu diketahui adalah bahwa informasi yang diberikan di laman Cloud Discovery dan tab terkait didasarkan pada laporan cuplikan dari log lalu lintas yang Anda unggah secara manual dari firewall dan proksi atau dari laporan berkelanjutan yang menganalisis semua log yang diteruskan dari jaringan Anda menggunakan Cloud App Security.  Untuk melihat tempat informasi ini disiapkan, pilih **Tindakan** di pojok kanan atas laman.
    1. Pilih opsi pertama, **Buat laporan snapshot Cloud Discovery**, lalu pilih **Berikutnya**. Di sini, Anda akan mengisi detail yang diminta dan mengunggah log lalu lintas untuk membuat dan mengunggah laporan.  Pilih **Keluar** dan jika diminta dengan Apakah Anda yakin, pilih **Keluar** lagi.  Data yang ditampilkan untuk penyewa lab Anda berasal dari laporan Snapshot, Anda dapat melihat informasi ini di bagian atas jendela Cloud Discovery.
    1. Untuk melihat opsi laporan berkelanjutan, pilih **Tindakan** di pojok kanan atas laman dan dari menu menurun, pilih **Konfigurasikan unggahan otomatis**.  Tidak ada sumber data yang tersambung, tetapi di sinilah Anda akan menambahkan sumber data. Pilih **Tambahkan sumber data**, lalu pilih panah menu dropdown di bidang **Pilih alat** untuk melihat jenis alat yang dapat Anda sambungkan sebagai sumber data.  Pilih **Batal** untuk keluar.
    1. Dari panel navigasi kiri, pilih **Cloud discovery** untuk kembali ke laman Cloud discovery.

1. Dengan aplikasi Microsoft Defender untuk Cloud, Anda dapat terhubung ke aplikasi secara langsung dengan menyiapkan konektor aplikasi yang akan memberi Anda visibilitas dan kontrol yang lebih besar atas aplikasi cloud Anda. Dari pojok kanan atas layar, pilih **Tindakan**, lalu pilih **Pengaturan Cloud Discovery**.  Perhatikan pengaturan yang tersedia.
    1. Dari panel navigasi kiri jendela pengaturan aplikasi Cloud, pilih **Konektor aplikasi (** Anda mungkin perlu menggulir ke bawah).
    1. Laman Konektor aplikasi adalah tempat Anda akan melihat konektor aplikasi apa pun yang sudah disiapkan dan tempat Anda dapat menambahkan konektor aplikasi.
    1. Anda akan melihat Microsoft 365 tercantum. Jika menunjukkan kesalahan koneksi, buka elipsis vertikal di sisi kanan item baris, lalu pilih **Edit pengaturan**.  Untuk menghubungkan kembali, pilih **Hubungkan Office 365** di bagian bawah laman. Sekarang, laman seharusnya menunjukkan bahwa Office 365 terhubung, pilih **Selesai**.  Sekarang, status akan ditampilkan dengan tanda peringatan kuning, menunjukkan tidak ada status terbaru.  Perlu beberapa waktu untuk memperbarui status karena periode waktu pemindaian retroaktif berbeda untuk setiap aplikasi dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya.
    1. Untuk menyiapkan konektor aplikasi baru.  Pilih **+Koneksi aplikasi**.  Pilih status dari daftar menurun.  Anda mungkin juga ingin menyampaikan bahwa daftar menyertakan opsi untuk **Sarankan lebih banyak aplikasi**.  
    1. Secara opsional, Anda mungkin ingin menambahkan konektor Microsoft Azure. Dari daftar menurun, pilih **Microsoft Azure**.  Dari jendela pop-up Microsoft Azure, pilih **Hubungkan Microsoft Azure**, lalu pilih **Selesai**.  Anda akan melihat status terhubung (jika tidak melihatnya, refresh browser) dan informasi tentang pemindaian pengguna, data, dan aktivitas.  

1. Saat berada di laman Pengaturan aplikasi cloud, ada baiknya meluangkan waktu beberapa menit juga untuk menjelajahi beberapa pengaturan Cloud Discovery lainnya.  
    1. Pilih **Aplikasi Kontrol Aplikasi Akses Bersyarat** dan perhatikan deskripsinya, "Kontrol Aplikasi Akses Bersyarat menambahkan kemampuan pemantauan dan kontrol real time untuk aplikasi Anda."
    1. Pilih **Perlindungan** Informasi Microsoft, bicaralah dengan pengaturan yang tersedia.
    1. Anda dapat menjelajahi bagian lain. Sebutkan tingkat integrasi dan fleksibilitas.

1. Kembali ke dasbor Cloud Discovery, dengan memilih **Cloud Discovery** dari panel navigasi paling kiri.

1. Biarkan halaman ini tetap terbuka, karena Anda akan menggunakannya di bagian selanjutnya.

### Demo Bagian 2 - Menjelajahi katalog aplikasi Cloud

Di bagian demo ini, Anda akan menunjukkan kemampuan katalog aplikasi Cloud. Cloud Discovery menganalisis log lalu lintas Anda berdasarkan katalog aplikasi cloud Microsoft Defender untuk Cloud Apps yang berisi lebih dari 31.000 aplikasi cloud. Aplikasi diberi peringkat dan skor berdasarkan lebih dari 80 faktor risiko untuk memberi Anda visibilitas berkelanjutan ke penggunaan cloud, Shadow IT, dan risiko yang ditimbulkan Shadow IT bagi organisasi Anda.  

1. Dari panel navigasi kiri, pilih **Katalog aplikasi cloud**.

1. Katalog aplikasi Cloud memungkinkan Anda memilih aplikasi yang sesuai dengan persyaratan keamanan organisasi Anda. Admin dapat melakukan pemfilteran dasar pada aplikasi seperti yang ditampilkan di bagian atas laman, yang mencakup apakah aplikasi diberi sanksi, tidak diberi sanksi, atau tidak memiliki tag, skor risiko, faktor risiko Kepatuhan, dan faktor risiko keamanan.  Misalnya, pemfilteran berdasarkan faktor risiko kepatuhan memungkinkan Anda menelusuri standar, sertifikasi, dan kepatuhan tertentu yang mungkin dipatuhi oleh aplikasi. Contohnya termasuk HIPAA, ISO 27001, SOC 2, dan PCI-DSS. Pilih **Faktor risiko kepatuhan** untuk melihat opsi yang tersedia.  Anda dapat memfilter lebih lanjut berdasarkan skor risiko, dengan menggerakkan penggeser pada skor risiko di bagian atas laman. Jika Anda memindahkan slide, pastikan sudah mengaturnya sehingga rentangnya diatur dari 0 hingga 10.

1. Admin juga dapat mencari aplikasi berdasarkan kategori.  Misalnya, pada kolom pencarian kategori, masukkan **Jejaring sosial**, lalu pilih **Jejaring sosial**.  Pilih item apa pun dari daftar untuk tampilan terperinci.  Arahkan mouse Anda ke topik apa pun untuk kategori tertentu akan menampilkan ikon informasi yang dapat Anda pilih untuk mendapatkan informasi lebih lanjut tentang topik tersebut.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Demo Bagian 3 - Jelajahi log Aktivitas

Jelajahi cara di mana Anda dapat menyelidiki aktivitas yang direkam dengan log aktivitas.

1. Dari panel navigasi kiri, pilih **Log Aktivitas**. Di sini, Anda mendapatkan visibilitas ke semua aktivitas dari aplikasi yang terhubung. Anda mungkin tidak melihat data apa pun yang tercantum karena memerlukan waktu beberapa jam untuk melakukan pemindaian retroaktif setelah audit diaktifkan dan penyewa lab mungkin memerlukan waktu yang lebih lama dari biasanya. Perhatikan opsi filter yang tersedia dan opsi untuk membuat kebijakan baru dari pencarian.

1. Biarkan laman ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### Demo Bagian 4 - Menjelajahi kebijakan

Di bagian ini, Anda akan menampilkan opsi yang tersedia untuk kebijakan di Microsoft Defender untuk Cloud Apps.

1. Dari panel navigasi kiri, pilih **Kebijakan**.
    1. Pilih **Manajemen kebijakan**.  Kebijakan yang tercantum memberikan informasi tentang jumlah pemberitahuan yang dihasilkan oleh kebijakan, tingkat keparahan, dll. Memilih item baris apa pun memberikan informasi lebih terperinci tentang kebijakan tersebut. Pilih item dari daftar, untuk melihat informasi terperinci tentang kebijakan tersebut.  Sampaikan beberapa opsinya, lalu pilih **Batalkan**.
    2. Perhatikan bahwa Anda juga dapat membuat kebijakan. Pilih **+ Buat kebijakan** untuk melihat jenis kebijakan yang dapat Anda buat.  Pilih **Kebijakan aktivitas** untuk melihat berbagai opsi yang tersedia untuk membuat kebijakan.  Pilih **Batalkan** untuk keluar dari jendela konfigurasi.
    3. Perhatikan bahwa Anda juga dapat memiliki opsi untuk mengekspor informasi kebijakan.

1. Dari panel navigasi kiri, pilih **Templat kebijakan**. Untuk membuat kebijakan dari salah satu templat yang tersedia, pilih **+** di sebelah kanan item baris templat.  Lihat berbagai opsi konfigurasi untuk kebijakan.  Pilih **Batalkan** untuk keluar dari laman.

1. Dari panel navigasi kiri, pilih **Beranda** untuk kembali ke beranda untuk Pertahanan Microsoft.

1. Biarkan tab browser tetap terbuka jika Anda berencana melanjutkan ke demo berikutnya.

### Tinjauan

Dalam demo ini, Anda telah menunjukkan kemampuan Microsoft Defender untuk Cloud Apps.  Anda telah menunjukkan informasi yang tersedia di dasbor Cloud discovery, katalog aplikasi Cloud, kemampuan yang tersedia untuk menyelidiki temuan dengan Log aktivitas dan File, serta cara mengontrol dampak terhadap organisasi Anda melalui Kebijakan
