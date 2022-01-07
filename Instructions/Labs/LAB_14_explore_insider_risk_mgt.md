---
lab:
    title: 'Mempelajari Manajemen Risiko Dari Dalam di Microsoft 365'
    module: 'Modul 4 Pelajaran 3: Menjelaskan kemampuan solusi kepatuhan Microsoft: Menjelaskan kemampuan risiko dari dalam di Microsoft 365'
---


# Lab: Mempelajari Manajemen Risiko Dari Dalam di Microsoft 365

## Skenario lab
Di lab ini, Anda akan mempelajari proses penyiapan kebijakan risiko dari dalam, bersama dengan prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.  Catatan:  lab ini hanya akan memberikan visibilitas tentang hal yang diperlukan untuk menyiapkan Manajemen risiko dari dalam dan opsi yang terkait dengan pembuatan kebijakan.  Lab ini tidak menyertakan tugas untuk memicu kebijakan, karena jumlah kejadian yang perlu terjadi untuk memicu kebijakan berada di luar cakupan latihan ini.


**Perkiraan Waktu**: 25-30 menit

#### Tugas 1: Dalam tugas ini, Anda sebagai administrator global akan mengaktifkan izin untuk Manajemen Risiko Dari Dalam.  Secara khusus, Anda akan menambahkan pengguna ke grup peran Manajemen Risiko Dari Dalam untuk memastikan bahwa pengguna yang ditunjuk dapat mengakses dan mengelola fitur manajemen risiko dari dalam.  Mungkin diperlukan waktu hingga 30 menit agar izin grup peran diterapkan ke pengguna di seluruh organisasi. 

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bawah Pusat admin, pilih **Security**.  Halaman browser baru terbuka ke halaman selamat datang di portal Pertahanan Microsoft 365.  

1. Dari panel navigasi sebelah kiri portal Pertahanan Microsoft 365, pilih **Permissions & roles**.  Anda mungkin perlu menggulir ke bawah untuk melihat opsi ini.

1. Dari halaman Izin dan peran, di bagian **Email & collaboration roles**, pilih **Roles**.

1. Di bilah pencarian, masukkan **Insider risk**, lalu pilih ikon pencarian (kaca pembesar).  Perhatikan lima peran yang muncul.  Masing-masing memiliki tingkat akses yang berbeda.  Pilih **Insider risk management**. 

1. Di jendela yang terbuka, di samping teks Anggota, pilih **Edit**.

1. Untuk menambahkan anggota ke grup peran ini, klik **Choose members**.

1. Pilih **+ Add** dari bagian atas halaman.

1. Dari daftar nama, pilih **MOD Administrator**, **Megan Bowen**, lalu pilih **Add** di bagian bawah halaman, lalu pilih **Selesai** di bagian bawah halaman.

1. Verifikasi anggota yang ditambahkan sudah benar lalu pilih **Save**.

1. Dari bagian bawah jendela Manajemen Risiko Dari Dalam, pilih **Close**.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan kembali lagi di tugas berikutnya.


#### Tugas 2 (LEWATI jika Anda telah menyiapkan tugas lab untuk mengaktifkan log audit): Manajemen risiko dari dalam menggunakan log audit Microsoft 365 untuk wawasan dan aktivitas pengguna yang diidentifikasi dalam kebijakan dan wawasan analitik. Dalam tugas ini, Anda akan mengaktifkan kemampuan pencarian log Audit. Catatan:  Mungkin diperlukan waktu beberapa jam setelah mengaktifkan pencarian log audit sebelum Anda dapat mengembalikan hasil saat mencari log audit.  Meskipun perlu beberapa jam sebelum Anda dapat menelusuri log audit, hal itu tidak akan memengaruhi kemampuan untuk menyelesaikan tugas lain di lab ini.

1. Pilih tab browser berlabel, **Microsoft 365 admin center - Home**.  Jika sebelumnya Anda menutup tab browser ini, buka Microsoft Edge dan di bilah alamat, masukkan **admin.microsoft.com**, lalu masuk dengan kredensial admin Anda.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri pada pusat kepatuhan Microsoft 365, pilih **Show all**.

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.

1. Pastikan bahwa tab **Search** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah berwarna biru di bagian atas halaman yang mengatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak ada tindakan lebih lanjut yang diperlukan.

1. Kembali ke halaman beranda pusat kepatuhan Microsoft 365 dengan memilih **Home** dari panel navigasi sebelah kiri.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

#### Tugas 3: Dalam tugas ini, Anda akan menelusuri pengaturan yang terkait dengan solusi Manajemen Risiko Dari Dalam.  Pengaturan manajemen risiko dari dalam berlaku untuk semua kebijakan manajemen risiko dari dalam, terlepas dari templat yang Anda pilih saat membuat kebijakan. 

1. Anda seyogianya berada di halaman beranda pusat kepatuhan Microsoft 365. Jika tidak, Buka tab browser **Home - Microsoft 365 compliance**.

1. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **Insider risk management**.

1. Sebelum mulai menyiapkan kebijakan, ada beberapa pengaturan yang perlu dikonfigurasi.  Dari halaman Manajemen Risiko Dari Dalam, pilih **setting cog icon** di sudut kanan atas halaman untuk mengakses pengaturan Risiko Dari Dalam.  
    1. Tab privasi:  untuk pengguna yang melakukan aktivitas yang sesuai dengan kebijakan risiko dari dalam, pengaturan ini akan menentukan apakah akan menampilkan nama mereka yang sebenarnya atau menggunakan versi anonim untuk menutupi identitas mereka.  Pilih **Do not show anonymized versions of usernames**, lalu pilih **Save**.  Pilih tab **Indikator kebijakan**.
    
    1. Tab indikator kebijakan: Setelah peristiwa pemicu kebijakan terjadi, aktivitas yang dipetakan ke indikator yang dipilih akan digunakan dalam menentukan skor risiko, bagi pengguna. Indikator kebijakan yang dipilih di sini termasuk templat kebijakan risiko Dari Dalam.  Gulir untuk melihat semua indikator yang tersedia dan informasi terkait lainnya. Di bagian **Office indicators**, klik **Select all**, lalu pilih **Save**.  Pilih tab **Policy timeframes**.
    1. Tab kerangka waktu kebijakan:  Kerangka waktu yang Anda pilih di sini berlaku pada pengguna saat memicu kecocokan untuk kebijakan risiko dari dalam.   Jendela Aktivasi menentukan berapa lama kebijakan akan secara aktif mendeteksi aktivitas untuk pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan. Deteksi aktivitas sebelumnya Menentukan seberapa jauh ke belakang kebijakan untuk mendeteksi aktivitas pengguna dan dipicu saat pengguna melakukan aktivitas pertama yang cocok dengan kebijakan.  Biarkan nilai default.  Pilih tab **Intelligent detections**.
    1. Tab deteksi cerdas:  Tinjau opsi di sini.  Perhatikan pengaturan domain dan bagaimana hubungannya dengan indikator.
    1. Item lain yang tercantum dalam pengaturan sedang dalam pratinjau.  Pelajari hal ini saat ingin dan catat sebagai pratinjau. Ini dapat berubah sewaktu-waktu.

1. Untuk kembali ke ringkasan Manajemen risiko dari dalam, pilih **Insider risk management** dari sudut kiri atas halaman, di atas teks Pengaturan.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

#### Tugas 4:  Dalam tugas ini, Anda akan mempelajari pembuatan kebijakan.

1. Anda seyogianya berada di halaman Manajemen risiko dari dalam.  Jika belum ada, buka tab browser berlabel, **Insider risk management - Microsoft 365 compliance**.

1. Dari halaman Ringkasan manajemen risiko dari dalam, pilih tab **Policies**, lalu pilih **+ Create**.  Konfigurasikan setiap tab kebijakan berikut.

    1. Kerangka kebijakan:  Dari daftar kategori, pilih **Data leaks**, lalu pilih **General data leaks**.  Perhatikan bahwa templat dalam kategori mungkin memiliki prasyarat tambahan.  Baca detail yang terkait dengan templat ini, lalu pilih **Next**.
    
    1. Nama dan deskripsi:  masukkan nama, **SC900-InsiderRiskPolicy**, lalu pilih **Next**.
    1. Pengguna dan grup:  Tinjau kotak informasi.  Biarkan pengaturan default, **Include all users and groups**.  Klik **Next**.
    1. Konten yang harus diprioritaskan: Baca deskripsinya. Pilih **I want to specify SharePoint sites, sensitivity labels, and/or sensitive info types as priority content**, lalu pilih **Next**.
        1. Situs SharePoint: Untuk contoh kebijakan ini, biarkan kosong, pilih **Next**
        1. Jenis info sensitif: untuk contoh kebijakan ini, biarkan kosong lalu pilih **Next**. 
        1. Label sensitivitas: pilih **+ Add or edit sensitivity labels**.  Pilih label yang terdaftar:  **Confidential Finance** dan **Highly Confidential\Project – Falcon**, pilih **Add**, lalu **Next**.
    1. Indikator dan kejadian pemicu: Tinjau informasi selengkapnya.  Kebijakan dipicu oleh pengguna yang melakukan aktivitas eksfiltrasi seperti yang ditentukan (pilih ikon informasi pada setiap poin untuk informasi selengkapnya) ATAU kecocokan dengan kebijakan Pencegahan Kebocoran Data (DLP) yang ada.  Karena Anda tidak memiliki kebijakan DLP yang dikonfigurasi sebagai bagian dari latihan ini, pilih **User performs an exfiltration activity**.  Gulir ke bawah untuk melihat apa yang dipilih secara otomatis.  Perhatikan bahwa indikator kebijakan yang Anda aktifkan di tugas sebelumnya telah dicentang.   Harap diingat bahwa indikator ini hanya akan diaktifkan setelah kebijakan dipicu dan aktivitas apa pun yang dipetakan ke indikator ini akan digunakan saat menghitung skor risiko pengguna.  Selain itu, Deteksi urutan telah diaktifkan.  Jika urutan kegiatan seperti yang ditentukan telah terdeteksi, maka hal itu menunjukkan risiko yang lebih besar.  Pilih ikon informasi untuk informasi selengkapnya tentang indikator mana yang diperlukan.  Pilihan ini mengharuskan indikator tertentu dipilih dan perangkat sudah terpasang.  Agar lebih mudah dan karena kita tidak memiliki perangkat yang terpasang pada penyewa, hapus centang **Select all**.  Klik **Next**.
    1. Ambang Indikator:  di sini, Anda dapat menentukan ambang default atau kustom yang terkait dengan indikator.  Harap diingat bahwa indikator diaktifkan hanya setelah pemicu kebijakan terjadi, sehingga ambang batas ini tidak memengaruhi saat kebijakan dipicu. Pilih **Specify custom thresholds**, Dengan memilih opsi ini, Anda dapat melihat nilai default saat ini. Biarkan pengaturan default, lalu klik **Next**.  
    1. Penyelesaian:  tinjau pengaturan, pilih **Submit**, lalu pilih **Done**.

1. Anda kembali ke tab Kebijakan di halaman Manajemen risiko dari dalam.  Kebijakan yang baru saja Anda buat akan dicantumkan.  

1. Pada kebijakan yang baru saja Anda buat, bidang “Pengguna dalam cakupan” mewakili pengguna yang saat ini diberi skor risiko oleh kebijakan.  Menetapkan skor risiko kepada pengguna terjadi saat kebijakan dipicu, oleh karena itu nilainya menunjukkan 0.  Admin dapat mengonfigurasi kebijakan untuk mulai menetapkan skor risiko kepada pengguna tertentu, berdasarkan aktivitas yang terdeteksi oleh kebijakan yang Anda pilih, DAN mengabaikan persyaratan bahwa kejadian pemicu terdeteksi terlebih dahulu.  Untuk melakukan hal ini, pilih lingkaran kosong di samping nama kebijakan untuk memilih kebijakan, lalu pilih **Start scoring activity for users**, yang ditunjukkan di atas tabel kebijakan.  Isi setiap bidang, lalu pilih **Start scoring activity**.  Diperlukan waktu 24 jam bagi pengguna untuk muncul di tab 'Pengguna'. Setelah itu, Anda dapat memilih pengguna dari tab untuk meninjau aktivitas yang terdeteksi.

#### Tinjauan
Di lab ini, Anda telah mempelajari proses penyiapan kebijakan risiko dari dalam, bersama dengan prasyarat dasar untuk mengonfigurasi dan menggunakan kebijakan manajemen risiko dari dalam.
