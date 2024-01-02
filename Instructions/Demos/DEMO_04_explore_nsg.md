<!---
---
Demo: Judul: 'Grup Keamanan Jaringan (NSG) Azure' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 1: Menjelaskan kemampuan keamanan dasar di Azure; Unit 6: Menjelaskan grup Keamanan Jaringan Azure'
---
--->

# Demo: Grup Keamanan Jaringan Azure (NSG)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Unit: Menjelaskan grup Keamanan Jaringan Azure

## Skenario demo

Dalam demo ini, Anda akan mempelajari fungsi grup keamanan jaringan di Azure dan menerapkan NSG ke mesin virtual yang telah dibuat sebelumnya. Anda akan mulai dengan menampilkan informasi singkat tentang VM yang telah dibuat sebelumnya oleh host lab resmi (ALH). Kemudian, menggunakan NSG yang disiapkan sebagai bagian dari penyiapan prademo, Anda akan menampilkan parameter penting NSG dan aturan masuk dan keluar default. Anda akan menetapkan antarmuka VM ke NSG, membuat aturan RDP baru untuk memungkinkan koneksi ke VM, dan terakhir, Anda akan mengujinya.

### Demo bagian 1

Dalam bagian ini, Anda akan melihat beberapa parameter yang terkait dengan VM yang dibuat sebagai bagian dari demo penyiapan ini (DEMO_00_pre_demo_setup.md).

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com** dan masuk dengan kredensial Azure yang disediakan oleh host lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian warna biru di bagian atas laman, masukkan **Mesin Virtual**, lalu pilih **Mesin Virtual** dari hasil pencarian.

1. Dari laman Mesin virtual, pilih VM yang terdaftar **SC900-WinVM**.  VM ini seharusnya dibuat sebagai bagian dari penyiapan prademo.  Jika tidak tercantum, buat sekarang.

1. Sekarang Anda berada di laman SC900-WinVM.  Perhatikan beberapa informasi dasar tentang VM.

1. Dari panel navigasi kiri, pilih **Jaringan**.  
    1. Tampilan default adalah untuk aturan port masuk.  Perhatikan bahwa antarmuka jaringan untuk VM ini tidak memiliki konfigurasi grup keamanan jaringan.  Hal yang sama berlaku jika Anda memilih Aturan port keluar.
    1. Pilih **Aturan keamanan yang efektif** di sebelah tulisan Antarmuka jaringan.  Perhatikan bahwa itu tertulis, "Tidak ada grup keamanan jaringan atau grup keamanan aplikasi yang dikaitkan dengan antarmuka jaringan".

1. Catatan untuk penyaji, Jika Anda mencoba memeriksa status port da halaman sambungkan, Anda mendapatkan pesan "Tidak dapat memverifikasi".  Ini tidak selalu berarti bahwa port tidak terekspos.  Seperti yang akan Anda perhatikan ketika Anda mengambil tindakan yang sama dengan NSG yang ditetapkan, Anda mendapatkan "Tidak dapat diakses" yang menunjukkan bahwa lalu lintas pada port tersebut diblokir.


1. Biarkan tab browser ini terbuka.

### Demo bagian 2

Di bagian ini, Anda akan menetapkan antarmuka ke NSG, Anda akan menyampaikan aturan masuk dan keluar default yang menunjukkan cara kerja aturan.  Sebagai bagian dari penyiapan prademo, VM harus menetapkan antarmuka jaringan VM ke NSG tersebut dan membuat aturan masuk baru untuk lalu lintas RDP.

1. Buka tab browser baru ke portal Azure (portal.azure.com) dan di bilah pencarian biru di bagian atas laman, masukkan **Grup keamanan jaringan**. Dari hasilnya, pilih **Grup keamanan jaringan** (jangan pilih Grup keamanan jaringan klasik).

1. Pilih NSG yang dibuat sebagai bagian dari penyiapan prademo. Jika Anda belum membuatnya, buatlah sekarang. Pilih **Buat grupkeamanan jaringan ** dan tentukan pengaturan berikut:
    1. Langganan: Biarkan nilainya diatur ke default (ini langganan Azure yang disediakan oleh host lab resmi)
    1. Grup sumber daya:  **LabsSC900** (grup sumber daya sama yang digunakan oleh VM).
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Tinjau + buat**, lalu pilih **Buat**.
    1. Saat penyebaran selesai (yang berlangsung sangat cepat), pilih **Buka sumber daya**.

1. Di bagian atas laman di bawah yang bertuliskan Esensial, Anda akan melihat beberapa informasi dasar tentang NSG yang Anda buat.  Dua hal yang perlu diperhatikan adalah tidak ada aturan Keamanan KUSTOM dan tidak ada subnet atau antarmuka jaringan yang terkait dengan NSG ini.  Meskipun tidak ada aturan keamanan khusus, ada aturan masuk dan keluar default yang disertakan dengan setiap NSG, seperti yang ditampilkan di laman.  Tinjau aturan masuk dan keluar. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Aturan keluar menolak semua lalu lintas keluar kecuali lalu lintas antara jaringan virtual dan lalu lintas keluar ke internet.

1. Dari panel navigasi kiri halaman NSG-SC900, di bagian Pengaturan, pilih **Antarmuka jaringan**.
    1. Lalu pilih **Kaitkan**.
    1. Di bidang untuk memilih asosiasi antarmuka jaringan, pilih **panah menurun**, pilih **sc900-winvmXXX**, lalu pilih **ok** di bagian bawah jendela. Setelah antarmuka dikaitkan dengan NSG, antarmuka akan muncul dalam daftar.

1. Kembalikan VM dengan memilih tab browser untuk VM.  Anda akan melihat bahwa sekarang ada NSG yang terlampir pada antarmuka VM.  Tabel aturan port masuk ditampilkan. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Untuk menguji ini, Anda akan memeriksa status pada port RDP, 3389.
    1. Dari bagian atas laman, pilih **Koneksi**, lalu pilih **Periksa akses** untuk port 3389 (RDP), Anda akan melihat "Tidak dapat diakses".  
    1. Meskipun Anda hanya menguji terhadap port RDP 3389, semua lalu lintas jaringan masuk yang bukan dari jaringan virtual lain atau load balancer diblokir.  

1. Sekarang Anda akan membuat aturan baru untuk mengizinkan lalu lintas RDP masuk.  Dari panel navigasi kiri, pilih **Jaringan**. Tabel Aturan port masuk harus ditampilkan (tab aturan port masuk digarisbawahi).  Di sisi kanan laman, pilih **Tambahkan aturan port masuk**. Poin penting yang harus disampaikan adalah Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan yang memiliki prioritas lebih tinggi. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber: **Semua**
    1. Rentang port sumber: **\***
    1. Tujuan:  **Semua**
    1. Layanan:  **RDP**
    1. Tindakan: **Izinkan**
    1. Prioritas: **1000**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama: Biarkan nama default atau buat nama deskriptif sendiri.
    1. Perhatikan tanda peringatan di bagian bawah laman.  Kami menggunakan RDP hanya untuk pengujian dan mendemonstrasikan fungsionalitas NSG.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu melakukan refresh layar).

### Demo bagian 3

Setelah NSG dikaitkan ke VM Anda dan aturan RDP dibuat, Anda akan menunjukkan dampak NSG dengan menguji konektivitas RDP ke VM.

1. Buka tab SC900-WinVM – Microsoft Azure di browser Anda. 

1. Pilih **Hubungkan** dari panel navigasi kiri.
    1. Anda cukup memilih **periksa akses**.  Status harus ditampilkan sebagai "Dapat Diakses". Atau, jika Anda memiliki waktu, Anda dapat terhubung ke VM dengan membuka instans Koneksi ion Desktop Jauh di Windows.  Opsi ini akan membuka VM setelah berhasil menyambungkannya.  Langkah-langkahnya tercantum di bawah ini.
        1. Pada bilah pencarian Windows, masukkan **Koneksi desktop jarak jauh**, lalu pilih **Buka**.
        1. Di bidang di samping tulisan **Komputer**, masukkan alamat IP publik VM Anda.
        1. Setelah Anda memasukkan alamat IP, nama pengguna akan muncul di bawah bidang tempat Anda memasukkan alamat IP. Jika tidak, bentangkan **Tampilkan Opsi** dan masukkan nama pengguna VM Anda, lalu pilih **Sambungkan**.
        1. Jendela koneksi Desktop Jauh terbuka menunjukkan Identitas komputer jarak jauh tidak dapat diverifikasi. Tetap ingin tersambung? Pilih **Ya**.
        1. Sekarang Anda terhubung ke VM. tekankan kepada pelajar bahwa dalam hal ini, Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke VM melalui RDP.
        1. Minimalkan VM, dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke laman SC900-WinVM | Koneksi.

1. Dari panel navigasi kiri, pilih **Jaringan**, lalu dari jendela utama, pilih **Aturan** port keluar.  Sampaikan tentang aturan keluar default. Aturan default memungkinkan lalu lintas VNet keluar dari jaringan virtual apa pun ke jaringan virtual lainnya dan memungkinkan lalu lintas internet keluar. Jenis lalu lintas keluar lainnya ditolak.  Anda tidak dapat menghapus aturan default, tetapi Anda dapat menimpanya dengan membuat aturan yang memiliki prioritas lebih tinggi dengan cara serupa seperti saat membuat aturan masuk.

1. Jika waktu memungkinkan dan Anda ingin menampilkan langkah-langkah serupa untuk lalu lintas keluar melalui bagian demo opsional yang tercantum di bawah ini.  Jika tidak, keluar dari VM, tetapi tetap buka tab Azure di browser Anda untuk demo berikutnya.

### Demo OPSIONAL bagian 4

Di bagian ini, Anda akan menampilkan aturan keluar NSG saat ini yang memungkinkan lalu lintas internet keluar dari VM.  Kemudian Anda akan membuat aturan untuk memblokir lalu lintas internet keluar dari VM. Terakhir, Anda akan menunjukkan dampak aturan yang baru dibuat dengan mencoba mengakses internet dari VM.

1. Buka VM yang Anda minimalkan di langkah sebelumnya. Di sini, Anda akan menunjukkan konektivitas internet keluar ke Internet, yang diaktifkan oleh salah satu aturan keluar default. Setelah VM terbuka dan Anda masuk sebagai pengguna, pilih **Microsoft Edge** untuk membuka browser.  Karena ini adalah pertama kalinya Anda membuka Microsoft Edge, Anda akan melihat jendela pop-up, pilih **Mulai tanpa data Anda**, lalu pilih **Lanjutkan tanpa data ini**, lalu pilih **Konfirmasi dan mulai menjelajah**.
    1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasi bahwa Anda dapat terhubung ke mesin pencarian.
    1. Setelah mengonfirmasi bahwa Anda dapat mengakses www.bing.com, tutup jendela browser di VM, tetapi biarkan VM aktif.

1. Minimalkan VM, dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke laman SC900-WinVM | Koneksi.  

1. Dari panel navigasi kiri, pilih **Jaringan**.

1. Pilih tab **Aturan port keluar**. Anda akan melihat aturan keluar default.  Perhatikan aturan default "AllowInternetOutBound". Aturan ini memungkinkan semua lalu lintas internet keluar. Anda tidak bisa menghapus aturan default, tetapi Anda bisa menimpanya dengan membuat aturan yang memiliki prioritas lebih tinggi. Dari sisi kanan laman, pilih **Tambahkan aturan port keluar**.

1. Di laman Tambah aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber: **Semua**
    1. Rentang port sumber:  **\***
    1. Tujuan: **Tag Tag**
    1. Tag layanan tujuan:  **Internet**
    1. Layanan:  **Kustom** (biarkan default)
    1. Rentang port tujuan: * (pastikan memberi tanda bintang di bidang rentang port tujuan)
    1. Protokol: **Semua**
    1. Tindakan: **Tolak**
    1. Prioritas: **1000**
    1. Nama: Biarkan nama default atau buat nama deskriptif sendiri.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul di daftar aturan keluar.  Meskipun muncul dalam daftar, akan memakan waktu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan dengan langkah-langkah berikutnya).  

1. Kembali ke VM Anda (ikon untuk VM ditampilkan di bilah tugas di bagian bawah laman).

1. Buka browser Microsoft Edge di VM Anda dan masukkan **www.bing.com**. Laman ini seharusnya tidak ditampilkan.  Catatan: jika Anda dapat terhubung ke internet dan Anda memverifikasi bahwa semua parameter aturan keluar telah ditetapkan dengan benar, kemungkinan karena perlu waktu beberapa menit untuk menerapkan aturan tersebut.  Tutup browser, tunggu beberapa menit dan coba lagi.  Catatan: Langganan Azure di lingkungan lab mungkin memerlukan waktu yang lebih lama dari biasanya.

1. Tutup koneksi desktop jarak jauh, dengan memilih **X** di tengah atas laman tempat alamat IP ditampilkan.  Jendela pop-up muncul yang menunjukkan sesi jarak jauh Anda akan terputus. Pilih **OK**.

1. Buka tab Azure di browser Anda untuk demo Azure berikutnya.

### Tinjauan

Dalam demo ini, Anda telah menunjukkaninformasi dan pengaturan terkait NSG, termasuk proses untuk mengaitkan antarmuka ke NSG, Anda telah menunjukkan aturan masuk dan keluar default, dan terakhir, langkah-langkah untuk membuat aturan baru.
