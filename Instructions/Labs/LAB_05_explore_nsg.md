<!---
---
Lab: Judul: 'Jelajahi Azure Network Security Groups (NSGs)' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 1: Menjelaskan kemampuan keamanan dasar di Azure; Pelajaran 6: Menjelaskan grup Keamanan Jaringan Azure'
---
--->

# Lab: Mempelajari Grup Keamanan Jaringan Azure (NSG)

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Pelajaran: Menjelaskan grup Keamanan Jaringan Azure

## Skenario lab

Di lab ini, Anda akan mempelajari fungsi kelompok keamanan jaringan di Azure.  Anda akan melakukannya dengan membuat kelompok keamanan jaringan (NSG) dan menetapkan NSG ke antarmuka mesin virtual (VM) yang sudah ada sebelumnya.  Setelah dikonfigurasi, Anda akan mengamati aturan masuk dan keluar default, membuat aturan baru, dan menguji aturan tersebut.  Di lab ini, VM yang akan Anda gunakan dengan NSG dibuat untuk Anda, jadi Anda akan melihat beberapa informasi yang terkait dengan VM tersebut terlebih dahulu.
  
**Perkiraan Waktu**: 30-45 menit

### Tugas 1

Dalam tugas ini, Anda akan melihat beberapa parameter yang terkait dengan VM yang dibuat untuk digunakan dengan lab ini.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan nama pengguna yang diberikan oleh penyedia hosting lab Anda, lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Di bagian atas halaman, di bawah yang bertuliskan Layanan Azure, pilih **Mesin Virtual**.  Jika Anda tidak melihatnya dalam daftar, maka di kotak pencarian, di bilah warna biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **Mesin Virtual** lalu pilih **Mesin Virtual** dari hasil pencarian.

1. Dari halaman Mesin virtual, pilih VM yang terdaftar **SC900-WinVM**.

1. Anda sekarang berada di halaman SC900-WinVM.  Perhatikan beberapa informasi dasar tentang VM.

1. Dari bagian atas halaman pilih **Sambungkan**.  Pilih opsi untuk **Memeriksa akses**, yang tercantum di bawah alamat IP.  Pemeriksaan ini akan dilakukan menggunakan port 3389, yang merupakan port untuk konektivitas RDP.  Anda akan melihat pesan "Tidak dapat memverifikasi".  Dari kotak RDP asli, klik **Pilih**.  Di jendela yang terbuka, di bawah "1 Konfigurasikan prasyarat untuk RDP Asli", Anda akan melihat "Azure perlu mengonfigurasi beberapa fitur untuk terhubung ke VM".  Dalam tugas berikutnya, Anda akan menyiapkan NSG untuk secara eksplisit mengizinkan koneksi RDP.


1. Dari panel navigasi kiri, pilih **Jaringan**.  
    1. Tampilan default adalah untuk aturan port masuk.  Perhatikan bahwa antarmuka jaringan untuk VM ini tidak memiliki kelompok keamanan jaringan yang dikonfigurasi.  Hal yang sama berlaku jika Anda memilih Aturan port keluar.
    1. Pilih **Aturan keamanan yang efektif** di sebelah tulisan Antarmuka jaringan.  Perhatikan bahwa dikatakan, "Tidak ada kelompok keamanan jaringan atau kelompok keamanan aplikasi yang dikaitkan dengan antarmuka jaringan".

1. Biarkan tab browser ini terbuka.


### Tugas 2

Dalam tugas ini, Anda akan membuat kelompok keamanan jaringan, menetapkan antarmuka jaringan VM ke NSG tersebut, dan membuat aturan masuk baru untuk lalu lintas RDP.

1. Dari tab NSG yang terbuka, *klik kanan* tautan **Beranda** di bagian atas halaman dan pilih **Buka tautan di tab baru** untuk membuka halaman lain ke layanan Azure.

1. Di bilah pencarian biru di bagian atas halaman, masukkan **Grup keamanan jaringan** dan, dari hasilnya, pilih **Grup keamanan jaringan**. Jangan pilih *Kelompok keamanan jaringan (klasik)*.

1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.

1. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh authorized lab hoster)
    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Review + create**, lalu pilih **Create**.

1. Setelah penyebaran selesai, pilih **Buka Sumber daya**.

1. Di bagian atas halaman di bawah yang bertuliskan Essentials, Anda akan melihat beberapa informasi dasar tentang NSG yang Anda buat.  Dua hal yang perlu diperhatikan adalah bahwa tidak ada aturan Keamanan Kustom dan tidak ada subnet atau antarmuka jaringan yang terkait dengan NSG ini.  Meskipun tidak ada aturan keamanan khusus, ada aturan masuk dan keluar default yang disertakan dengan setiap NSG, seperti yang ditampilkan di halaman.  Tinjau aturan masuk dan keluar. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Aturan keluar menolak semua lalu lintas keluar kecuali lalu lintas antara jaringan virtual dan lalu lintas keluar ke Internet.

1. Dari panel navigasi kiri pada halaman NSG-SC900, di bawah Pengaturan, pilih **Network interfaces**.
    1. Lalu pilih **Kaitkan**.
    2. Di bidang untuk asosiasi antarmuka jaringan, pilih **panah bawah**, pilih **sc900-winvmXXX**, lalu pilih **OK** di bagian bawah jendela. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.

1. Di panel navigasi kiri, pilih **Aturan keamanan masuk**.

1. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure sehingga Anda perlu menyiapkan aturan untuk mengizinkan lalu lintas RDP masuk (lalu lintas di port 3389). Ingat bahwa Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi.

1. Dari bagian atas halaman, pilih **Tambahkan**. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**
    1. Rentang port sumber: **\***
    1. Tujuan:  **Apa saja**
    1. Layanan:  **RDP**
    1. Tindakan:  **Izinkan**
    1. Prioritas: **1000**. Aturan dengan angka yang lebih rendah memiliki prioritas yang lebih tinggi dan diproses terlebih dahulu.
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda sendiri.
    1. Perhatikan tanda peringatan di bagian bawah halaman.  Kami menggunakan RDP hanya untuk tujuan pengujian dan untuk mendemonstrasikan fungsionalitas NSG.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu me-refresh layar).

1. Biarkan tab browser ini terbuka.  

### Tugas 3

Dalam tugas ini, Anda akan menguji aturan NSG masuk yang baru dibuat untuk mengonfirmasi bahwa Anda dapat membuat koneksi desktop jarak jauh (RDP) ke VM.  Setelah berada di dalam VM, Anda akan bekerja untuk memeriksa konektivitas keluar ke Internet dari VM.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda. Jika sebelumnya Anda menutup tab browser, buka tab browser baru, masukkan **https://portal.azure.com**, dan pilih **Komputer virtual**, lalu pilih VM, **SC900-WinVM**.

1. Pilih **Connect** dari panel navigasi kiri.

1. Pilih **periksa akses** (verifikasi port diatur ke 3389).  Status harus ditampilkan sebagai "Dapat Diakses".

1. Sekarang sambungkan langsung ke VM dengan mengklik **Pilih** di kotak yang berbunyi RDP Asli.
   
    1. Dari jendela RDP Asli yang terbuka, pilih **Unduh file RDP**.
    1. Jika peringatan unduhan muncul, pilih **Pertahankan**, lalu pada jendela pop-up yang muncul, pilih **Buka file**.
    1. Jendela Koneksi Desktop Jarak Jauh terbuka; pilih **Sambungkan**.
    1. Anda akan diminta memasukkan kredensial.  Masukkan Nama Pengguna dan Kata Sandi untuk VM (lihat tab sumber daya pada panel instruksi lab).
    1. Jendela koneksi Desktop Jauh terbuka menunjukkan: *Identitas komputer jarak jauh tidak dapat diverifikasi.  Tetap ingin tersambung?*  Pilih **Ya**.

1. Anda sekarang terhubung ke VM. Dalam kasus ini, Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat mengizinkan lalu lintas masuk ke VM lewat RDP.  Setelah beberapa detik di layar Selamat Datang, Anda mungkin melihat jendela untuk Memilih pengaturan privasi untuk perangkat Anda, pilih **Terima**.  Jika jendela Jaringan muncul, pilih **Tidak**.

1. Dengan VM dalam sesi RDP aktif dan berjalan, uji konektivitas keluar ke Internet dari VM.
    1. Dari VM yang terbuka, pilih **Microsoft Edge** untuk membuka browser.  Karena ini adalah pertama kalinya Anda membuka Microsoft Edge, Anda akan melihat jendela pop-up, pilih **Mulai tanpa data Anda**, lalu pilih **Lanjutkan tanpa data ini**, lalu pilih **Konfirmasi dan mulai menjelajah**.
    1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasi bahwa Anda dapat terhubung ke mesin pencarian.
    1. Setelah mengonfirmasi bahwa Anda dapat mengakses www.bing.com, tutup jendela browser di VM, tetapi biarkan VM aktif.

1. Minimalkan VM dengan memilih garis bawah **_** di tab biru yang memperlihatkan alamat IP VM. Ini membawa Anda kembali ke halaman SC900-WinVM \| Connect.

1. Tetap buka tab browser; Anda akan menggunakannya sebagai tugas berikutnya.

### Tugas 4

Di tugas sebelumnya, Anda mengonfirmasi bahwa Anda dapat membuat koneksi RDP ke VM. Setelah berada di VM, Anda juga mengonfirmasi bahwa Anda dapat membuat koneksi keluar ke Internet.  Lalu lintas Internet keluar diizinkan karena aturan keluar default untuk NSG memungkinkan lalu lintas Internet keluar.  Dalam tugas ini, Anda akan melalui proses pembuatan aturan keluar kustom untuk memblokir lalu lintas Internet keluar dan menguji aturan tersebut.

1. Anda harus berada di halaman SC900-WinVM \| Connect. Dari panel navigasi kiri, pilih **Jaringan**. Jika sebelumnya Anda menutup tab browser, pilih bilah pencarian warna biru di bagian atas halaman dan pilih Mesin virtual, lalu pilih VM, **SC900-WinVM**, lalu pilih **Jaringan**.

1. Pilih tab **Aturan port keluar**. Anda akan melihat aturan keluar default.  Catat aturan default "AllowInternetOutBound". Aturan ini mengizinkan semua lalu lintas Internet keluar. Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Di bagian kanan halaman, klik **Add outbound port rule**.

1. Di halaman Tambahkan aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**
    1. Rentang port sumber:  **\***
    1. Tujuan:  **Tag Layanan**
    1. Tag layanan tujuan  **Internet**
    1. Layanan:  **Custom** (biarkan default)
    1. Rentang port tujuan:  **\*** (pastikan untuk meletakkan tanda bintang di bidang rentang port tujuan)
    1. Protokol: **Apa saja**
    1. Tindakan: **Tolak**
    1. Prioritas: **1000**
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda sendiri.
    1. Pilih **Tambahkan**

1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.  Meskipun aturan muncul di daftar, perlu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan ke langkah berikutnya).  


1. Kembali ke VM Anda (ikon RDP untuk VM harus ditampilkan pada bilah tugas di bagian bawah halaman).

1. Buka browser Microsoft Edge di VM Anda dan masukkan **www.bing.com**. Halaman semestinya tidak ditampilkan. Jika Anda dapat terhubung ke internet dan memverifikasi bahwa semua parameter untuk aturan keluar diatur dengan benar, kemungkinan karena diperlukan beberapa menit agar aturan berlaku.  Tutup browser, tunggu beberapa menit, dan coba lagi. Langganan Azure di lingkungan lab mungkin mengalami penundaan yang lebih lama dari penundaan normal.


1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up muncul yang menunjukkan sesi jarak jauh Anda akan terputus. Pilih**OK**.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru di mana tertulis Microsoft Azure, pilih **Beranda** untuk kembali ke beranda layanan Azure.

1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tinjau

Di lab ini, Anda berjalan melalui proses pengaturan kelompok keamanan jaringan (NSG), mengaitkan NSG tersebut ke antarmuka jaringan komputer virtual, dan menambahkan aturan baru ke NSG untuk memungkinkan lalu lintas RDP masuk dan memblokir lalu lintas Internet keluar.
