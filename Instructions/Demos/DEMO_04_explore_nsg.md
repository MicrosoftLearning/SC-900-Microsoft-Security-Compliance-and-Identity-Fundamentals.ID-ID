<!---
---
Demo: Judul: 'Azure Network Security Groups (NSGs)' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 1: Menjelaskan kemampuan keamanan dasar di Azure; Pelajaran 6: Menjelaskan grup Keamanan Jaringan Azure'
---
--->

# Demo: Grup Keamanan Jaringan Azure (NSG)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Pelajaran: Menjelaskan grup Keamanan Jaringan Azure

## Skenario demo

Dalam demo ini, Anda akan menjelajahi fungsi kelompok keamanan jaringan di Azure dan menerapkan NSG ke mesin virtual yang telah dibuat sebelumnya. Anda akan mulai dengan menampilkan informasi singkat tentang VM yang telah dibuat sebelumnya oleh authorized lab hoster (ALH). Kemudian, menggunakan NSG yang disiapkan sebagai bagian dari penyiapan pra-demo, Anda akan menampilkan parameter penting NSG dan aturan masuk dan keluar default. Anda akan menetapkan antarmuka VM ke NSG, membuat aturan RDP baru untuk memungkinkan koneksi ke VM, dan akhirnya Anda akan mengujinya.

### Demo bagian 1

Di bagian ini, Anda akan melihat beberapa parameter yang terkait dengan VM yang dibuat sebagai bagian dari demo penyiapan (DEMO_00_pre_demo_setup.md).

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com** dan masuk dengan kredensial Azure yang disediakan oleh hoster lab resmi (ALH).  Ini membawa Anda ke beranda layanan Azure.

1. Di kotak pencarian biru di bagian atas halaman, masukkan **Virtual Machines** lalu pilih **Virtual Machines** dari hasil pencarian.

1. Dari halaman Mesin virtual, pilih VM yang terdaftar **SC900-WinVM**.  VM ini seharusnya dibuat sebagai bagian dari penyiapan pra-demo.  Jika tidak tercantum, buat sekarang.

1. Anda sekarang berada di halaman SC900-WinVM.  Perhatikan beberapa informasi dasar tentang VM.

1. Dari panel navigasi kiri, pilih **Jaringan**.  
    1. Tampilan default adalah untuk aturan port masuk.  Perhatikan bahwa antarmuka jaringan untuk VM ini tidak memiliki kelompok keamanan jaringan yang dikonfigurasi.  Hal yang sama berlaku jika Anda memilih Aturan port keluar.
    1. Pilih **Aturan keamanan yang efektif** di sebelah tulisan Antarmuka jaringan.  Perhatikan bahwa dikatakan, "Tidak ada kelompok keamanan jaringan atau kelompok keamanan aplikasi yang dikaitkan dengan antarmuka jaringan".

1. Catatan untuk penyaji, Jika Anda mencoba memeriksa status port pada halaman sambungkan, Anda mendapatkan pesan "Tidak dapat memverifikasi".  Ini tidak selalu berarti bahwa port tidak terekspos.  Seperti yang akan Anda catat ketika Anda mengambil tindakan yang sama dengan NSG yang ditetapkan, Anda mendapatkan "Tidak dapat diakses" yang menunjukkan bahwa lalu lintas pada port tersebut diblokir.


1. Biarkan tab browser ini terbuka.

### Demo bagian 2

Di bagian ini, Anda akan menetapkan antarmuka ke NSG, Anda akan berbicara dengan aturan masuk dan keluar default yang menunjukkan cara kerja aturan.  Sebagai bagian dari penyiapan pra-demo, VM harus menetapkan antarmuka jaringan VM ke NSG tersebut, dan membuat aturan masuk baru untuk lalu lintas RDP.

1. Buka tab browser baru ke portal Azure (portal.azure.com) dan di bilah pencarian biru di bagian atas halaman, masukkan Grup **keamanan jaringan**. Dari hasil, pilih **Kelompok keamanan jaringan** (jangan pilih Kelompok keamanan jaringan klasik).

1. Pilih NSG yang dibuat sebagai bagian dari penyiapan pra-demo. Jika sebelumnya Anda tidak membuatnya, lakukan sekarang. Pilih **Buat grup keamanan jaringan** dan tentukan pengaturan berikut:
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh authorized lab hoster)
    1. Grup sumber daya:  **LabsSC900** (grup sumber daya yang sama yang digunakan oleh VM).
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Review + create**, lalu pilih **Create**.
    1. Setelah penyebaran selesai (ini terjadi dengan sangat cepat), pilih **Buka sumber daya**.

1. Di bagian atas halaman di bawah yang bertuliskan Essentials, Anda akan melihat beberapa informasi dasar tentang NSG yang Anda buat.  Dua hal yang perlu diperhatikan adalah bahwa tidak ada aturan Keamanan KUSTOM dan tidak ada subnet atau antarmuka jaringan yang terkait dengan NSG ini.  Meskipun tidak ada aturan keamanan khusus, ada aturan masuk dan keluar default yang disertakan dengan setiap NSG, seperti yang ditampilkan di halaman.  Tinjau aturan masuk dan keluar. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Aturan keluar menolak semua lalu lintas keluar kecuali lalu lintas antara jaringan virtual dan lalu lintas keluar ke internet.

1. Dari panel navigasi kiri halaman NSG-SC900, di bagian Pengaturan, pilih **Antarmuka jaringan**.
    1. Lalu pilih **Kaitkan**.
    1. Di bidang untuk memilih asosiasi antarmuka jaringan, pilih **panah dropdown**, pilih **sc900-winvmXXX**, lalu pilih **ok** di bagian bawah jendela. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.

1. Kembalikan VM dengan memilih tab browser untuk VM.  Anda akan melihat bahwa sekarang ada NSG yang terpasang pada antarmuka VM.  Tabel aturan port masuk ditampilkan. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Untuk menguji ini, Anda akan memeriksa status pada port RDP, 3389.
    1. Dari bagian atas halaman, pilih **Sambungkan** lalu pilih **Periksa akses** untuk port 3389 (RDP), Anda akan melihat "Tidak dapat diakses".  
    1. Meskipun Anda hanya menguji terhadap port RDP 3389, semua lalu lintas jaringan masuk yang bukan dari jaringan virtual lain atau load balancer diblokir.  

1. Sekarang Anda akan membuat aturan untuk mengizinkan lalu lintas masuk pada port RDP.  Dari panel navigasi kiri, pilih **Jaringan**. Tabel Aturan port masuk harus ditampilkan (tab aturan port masuk digarisbawari).  Dari sisi kanan halaman, pilih **Tambahkan aturan port masuk**. Poin penting untuk dipanggil adalah Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**
    1. Rentang port sumber: **\***
    1. Tujuan:  **Apa saja**
    1. Layanan:  **RDP**
    1. Tindakan:  **Izinkan**
    1. Prioritas: **1000**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda sendiri.
    1. Perhatikan tanda peringatan di bagian bawah halaman.  Kami menggunakan RDP hanya untuk tujuan pengujian dan untuk mendemonstrasikan fungsionalitas NSG.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu me-refresh layar).

### Demo bagian 3

Dengan NSG yang terkait dengan VM Anda dan aturan RDP yang dibuat, Anda akan menunjukkan dampak NSG dengan menguji konektivitas RDP ke VM.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda. 

1. Pilih **Connect** dari panel navigasi kiri.
    1. Anda cukup memilih **periksa akses**.  Status harus ditampilkan sebagai "Dapat Diakses". Atau, jika Anda punya waktu, Anda dapat tersambung ke VM dengan membuka instans Koneksi Desktop Jarak Jauh di Windows.  Opsi ini akan membuka VM setelah berhasil menyambungkannya.  Tercantum di bawah ini adalah langkah-langkahnya:
        1. Pada bilah pencarian Windows Anda, masukkan **Koneksi desktop jarak jauh** lalu pilih **Buka**.
        1. Di bidang di samping di mana tertulis **Komputer**, masukkan alamat IP publik VM Anda.
        1. Setelah Anda memasukkan alamat IP, nama pengguna akan muncul di bawah bidang tempat Anda memasukkan alamat IP. Jika tidak, lalu perluas **Tampilkan Opsi** dan masukkan nama pengguna untuk VM Anda, lalu pilih **Sambungkan**.
        1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan. Apakah Anda yakin ingin tetap terhubung? Pilih **Ya**.
        1. Anda sekarang terhubung ke VM. tekankan kepada pelajar bahwa dalam hal ini Anda dapat terhubung ke Mesin Virtual karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke Mesin Virtual melalui RDP.
        1. Minimalkan VM, dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke SC900-WinVM | Hubungkan halaman.

1. Dari panel navigasi kiri pilih **Jaringan** lalu dari jendela utama, pilih **Aturan port keluar**.  Bicaralah dengan aturan keluar default. Aturan default memungkinkan lalu lintas VNet keluar dari jaringan virtual apa pun ke jaringan virtual lainnya dan memungkinkan lalu lintas internet keluar. Jenis lalu lintas keluar lainnya ditolak.  Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi dengan cara yang sama seperti Anda membuat aturan masuk.

1. Jika timer Anda mengizinkan dan Anda ingin menampilkan langkah serupa untuk lalu lintas keluar melalui bagian demo opsional yang tercantum di bawah ini.  Jika tidak, keluar dari VM, tetapi biarkan tab Azure terbuka di browser Anda untuk demo berikutnya.

### Demo OPSIONAL bagian 4

Di bagian ini, Anda akan menampilkan aturan keluar NSG saat ini yang memungkinkan lalu lintas internet keluar, dari VM.  Kemudian Anda akan membuat aturan untuk memblokir lalu lintas internet keluar dari VM, Akhirnya, Anda akan menunjukkan dampak aturan yang baru dibuat dengan mencoba mengakses internet dari VM.

1. Buka VM yang Anda minimalkan di langkah sebelumnya. Di sini Anda akan menampilkan konektivitas internet keluar ke Internet, yang diaktifkan oleh salah satu aturan keluar default. Setelah VM terbuka dan Anda masuk sebagai pengguna, pilih **Microsoft Edge** untuk membuka browser.  Karena ini adalah pertama kalinya Anda membuka Microsoft Edge, Anda akan melihat jendela pop-up, pilih **Mulai tanpa data Anda**, lalu pilih **Lanjutkan tanpa data ini**, lalu pilih **Konfirmasi dan mulai menjelajah**.
    1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasi bahwa Anda dapat terhubung ke mesin pencarian.
    1. Setelah mengonfirmasi bahwa Anda dapat mengakses www.bing.com, tutup jendela browser di VM, tetapi biarkan VM aktif.

1. Minimalkan VM, dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke SC900-WinVM | Hubungkan halaman.  

1. Dari panel navigasi kiri, pilih **Jaringan**.

1. Pilih tab **Aturan port keluar**. Anda akan melihat aturan keluar default.  Catat aturan default "AllowInternetOutBound". Aturan ini mengizinkan semua lalu lintas internet keluar. Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Di bagian kanan halaman, klik **Add outbound port rule**.

1. Di halaman Tambahkan aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**
    1. Rentang port sumber:  **\***
    1. Tujuan:  **Tag Layanan**
    1. Tag layanan tujuan  **Internet**
    1. Layanan:  **Custom** (biarkan default)
    1. Rentang port tujuan: * (pastikan untuk memberi tanda bintang di bidang rentang port tujuan)
    1. Protokol: **Apa saja**
    1. Tindakan: **Tolak**
    1. Prioritas: **1000**
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda sendiri.
    1. Pilih **Tambahkan**

1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.  Meskipun aturan muncul di daftar, perlu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan ke langkah berikutnya).  

1. Kembali ke VM Anda (ikon untuk VM harus ditampilkan di bilah tugas di bagian bawah halaman).

1. Buka browser Microsoft Edge di VM Anda dan masukkan **www.bing.com**. Halaman semestinya tidak ditampilkan.  Catatan: jika Anda dapat terhubung ke internet dan Anda memverifikasi bahwa semua parameter untuk aturan keluar telah ditetapkan dengan benar, kemungkinan karena perlu waktu beberapa menit untuk menerapkan aturan tersebut.  Tutup browser, tunggu beberapa menit, dan coba lagi.  Catatan: Langganan Azure di lingkungan lab mungkin memerlukan waktu yang lebih lama dari biasanya.

1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up muncul yang menunjukkan sesi jarak jauh Anda akan terputus. Pilih**OK**.

1. Biarkan tab Azure tetap terbuka di browser Anda untuk demo Azure berikutnya.

### Tinjau

Dalam demo ini, Anda menunjukkan informasi dan pengaturan terkait NSG, termasuk proses untuk mengaitkan antarmuka ke NSG, Anda menunjukkan aturan masuk dan keluar default, dan terakhir langkah-langkah untuk membuat aturan baru.
