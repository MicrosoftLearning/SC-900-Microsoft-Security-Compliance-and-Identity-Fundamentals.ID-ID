---
lab:
  title: Menjelajahi Kelompok Keamanan Jaringan Azure (NSG)
  module: Describe the basic security capabilities in Azure
---

# Lab: Menjelajahi Grup Keamanan Jaringan (NSG) di Azure

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Unit: Menjelaskan grup Keamanan Jaringan Azure

## Skenario lab

Di lab ini, Anda akan mempelajari fungsi grup keamanan jaringan di Azure.  Anda akan melakukannya dengan membuat grup keamanan jaringan (NSG) dan menetapkan NSG ke antarmuka mesin virtual (VM) yang sudah ada sebelumnya.  Setelah dikonfigurasi, Anda akan mengamati aturan masuk dan keluar default, membuat aturan baru, dan menguji aturan tersebut.  Di lab ini, VM yang akan Anda gunakan dengan NSG dibuat untuk Anda, jadi Anda akan melihat beberapa informasi yang terkait dengan VM tersebut terlebih dahulu.
  
**Perkiraan Waktu**: 45 menit

### Tugas 1

Dalam tugas ini, Anda akan melihat beberapa parameter yang terkait dengan VM yang dibuat untuk digunakan dengan lab ini.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **https://portal.azure.com**.

1. Masuk menggunakan kredensial admin Anda.
    1. Di jendela Masuk, masukkan nama pengguna yang diberikan oleh penyedia host lab Anda, lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika sebelumnya Anda telah masuk, Anda mungkin diminta untuk menyelesaikan autentikasi sekunder, sebagai bagian dari MFA. JIKA sebelumnya Anda belum masuk, Anda mungkin diminta untuk menyelesaikan proses pendaftaran MFA. Ikuti perintah di layar untuk menyiapkan MFA.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Di bagian atas laman, di bawah tulisan Layanan Azure, pilih **Mesin Virtual**.  Jika Anda tidak melihatnya dalam daftar, maka di kotak pencarian, di bilah warna biru di bagian atas laman di sebelah tulisan Microsoft Azure, masukkan **Mesin Virtual**, lalu pilih **Mesin Virtual** dari hasil pencarian.

1. Dari laman Mesin virtual, pilih VM yang terdaftar **SC900-WinVM**.

1. Sekarang, Anda berada di halaman SC900-WinVM.  Perhatikan beberapa informasi dasar tentang VM.

1. Dari panel navigasi kiri, perluas **Jaringan** lalu pilih **Pengaturan** Jaringan.  Bagian penting dari jendela utama menampilkan antarmuka jaringan untuk VM.  Perhatikan bahwa tidak ada yang tercantum di samping Kelompok keamanan jaringan karena tidak ada NSG yang ditetapkan ke antarmuka.

1. Tetap buka tab ini.

### Tugas 2

Dalam tugas ini, Anda akan membuat grup keamanan jaringan, menetapkan antarmuka jaringan VM ke NSG tersebut, dan membuat aturan masuk baru untuk lalu lintas RDP.

1. Dari tab Azure yang terbuka, *klik kanan* tautan **Beranda** di bagian atas halaman. Kemudian, pilih **Buka tautan di tab baru** untuk membuka halaman lain ke layanan Azure.

1. Di bilah pencarian warna biru di bagian atas laman, masukkan **Grup keamanan jaringan** dan dari hasilnya, pilih **Grup keamanan jaringan**. Jangan pilih *Grup keamanan jaringan (klasik)*.

1. Dari tengah halaman, pilih tombol biru berlabel **Buat kelompok keamanan jaringan**.  Atau, Anda dapat memilih **+ Buat** dari bagian atas halaman Kelompok keamanan jaringan.

1. Pada tab Dasar di laman Buat grup keamanan jaringan, tentukan pengaturan berikut:
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh hoster lab resmi)
    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Tinjau + buat**, lalu pilih **Buat**.

1. Setelah penyebaran selesai, pilih **Buka Sumber daya**.

1. Anda akan berada di halaman gambaran umum untuk NSG yang baru saja dibuat.  Jika Anda berada di halaman lain, pilih **Gambaran Umum** dari panel navigasi kiri. Di bagian atas laman di bawah yang bertuliskan Essentials, Anda akan melihat beberapa informasi dasar tentang NSG yang Anda buat.  Dua hal yang perlu diperhatikan adalah bahwa tidak ada aturan Keamanan Kustom dan tidak ada subnet atau antarmuka jaringan yang terkait dengan NSG ini.  Meskipun tidak ada aturan keamanan khusus, ada aturan masuk dan keluar default yang disertakan dengan setiap NSG, seperti yang ditampilkan di laman.  Tinjau aturan masuk dan keluar. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Aturan keluar menolak semua lalu lintas keluar, kecuali lalu lintas antara jaringan virtual dan lalu lintas keluar ke internet.

1. Dari panel navigasi kiri pada halaman NSG-SC900, perluas **Pengaturan** lalu pilih **Antarmuka jaringan**.
    1. Lalu pilih **Kaitkan**.
    2. Di bidang kaitkan antarmuka jaringan, pilih **panah bawah**, pilih **sc900-winvmXXX **, lalu pilih **OK** di bagian bawah jendela. Setelah antarmuka dikaitkan dengan NSG, antarmuka akan muncul dalam daftar.  NSG kini ditetapkan ke antarmuka jaringan VM Anda.

1. Beralih kembali ke tab **SC900-WinVM - Microsoft Azure** di browser.  Refresh halaman. Di samping tempat yang bertuliskan Kelompok keamanan jaringan, Anda kini akan melihat nama NSG yang baru saja Anda buat.  Jika Anda masih tidak melihatnya, tunggu beberapa menit, lalu refresh kembali halaman tersebut.

1. Dari panel navigasi kiri, pilih **Sambungkan**. Dari jendela utama, pilih **Periksa akses** di samping tempat Anda melihat nomor port 3389. Fungsi periksa akses mengirim sinyal (lalu lintas) ke port RDP default (3389) VM untuk memeriksa apakah port tersebut dapat diakses. Proses ini mungkin memerlukan waktu sekitar satu menit, tetapi Anda akan melihat status Tidak dapat diakses.  Ini merupakan hal yang normal karena aturan NSG DenyAllInBound menolak semua lalu lintas masuk ke VM.

1. Beralih kembali ke tab **NSG-SC900 - Microsoft Azure** di browser.

1. Di panel navigasi kiri, pilih **Aturan keamanan masuk**. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure sehingga Anda perlu menyiapkan aturan untuk mengizinkan lalu lintas RDP masuk (lalu lintas di port 3389). Ingat bahwa Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi.

1. Dari bagian atas halaman, pilih **Tambahkan**. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber: **Semua**
    1. Rentang port sumber: **\***
    1. Tujuan:  **Semua**
    1. Layanan:  **RDP**
    1. Tindakan: **Izinkan**
    1. Prioritas: **1000**. Aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama: Biarkan nama default atau buat nama deskriptif sendiri.
    1. Perhatikan tanda peringatan di bagian bawah laman.  Kami menggunakan RDP hanya untuk pengujian dan mendemonstrasikan fungsionalitas NSG.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu melakukan refresh layar).

1. Biarkan tab browser ini terbuka.  

### Tugas 3

Dalam tugas ini, Anda akan menguji aturan NSG masuk yang baru dibuat untuk mengonfirmasi bahwa Anda dapat membuat koneksi desktop jarak jauh (RDP) ke VM.  Begitu berada di dalam VM, Anda akan bekerja memeriksa konektivitas keluar ke Internet dari VM.

1. Buka tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Pilih **Hubungkan** dari panel navigasi kiri.

1. Pilih **periksa akses** (pastikan port diatur ke 3389).  Status harus ditampilkan sebagai "Dapat Diakses".  Jika Anda masih melihat "Tidak dapat diakses", refresh halaman dan coba lagi, mungkin perlu beberapa menit agar aturan masuk baru terlihat oleh opsi centang akses.

1. Sekarang sambungkan langsung ke VM dengan mengklik **Pilih** di kotak yang berbunyi RDP Asal.
   
    1. Dari jendela RDP Asal yang terbuka, pilih **Unduh file RDP**.
    1. Jika peringatan unduhan muncul, pilih **Pertahankan**, lalu pada jendela pop-up yang muncul, pilih **Buka file**.
    1. Jendela Koneksi Desktop Jauh terbuka; pilih **Hubungkan**.
    1. Anda akan diminta memasukkan kredensial.  Masukkan Nama Pengguna dan Kata Sandi host VM (lihat tab sumber daya di panel instruksi lab).
    1. Jendela koneksi Desktop Jauh yang terbuka menunjukkan *Identitas komputer jarak jauh tidak dapat diverifikasi. Anda ingin melanjutkan?*  Pilih **Ya**.

1. Sekarang, Anda terhubung ke VM. Dalam hal ini, Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke VM melalui RDP.  Setelah beberapa detik di layar Selamat Datang, Anda akan melihat jendela Pilih pengaturan privasi untuk perangkat Anda, pilih **Terima**.  Jika jendela Jaringan muncul, pilih **Tidak**.

1. Dengan VM di sesi RDP yang aktif dan berjalan, uji konektivitas keluar ke Internet dari VM.
    1. Dari VM yang terbuka, pilih **Microsoft Edge** untuk membuka browser. Karena ini adalah pertama kalinya Anda membuka VM dan broswer, Anda mungkin diminta untuk beberapa pengaturan dasar.  
    1. Anda mungkin diminta untuk memilih setelan privasi untuk perangkat Anda. Biarkan default dan pilih **Terima**.  
    1. Panel samping untuk Jaringan, dapat ditampilkan.  Pilih **Tidak**.
    1. Jendela mungkin muncul yang berbunyi "Telusuri web dengan browser berkinerja terbaik di Windows," pilih Lanjutkan **, pilih **Mulai tanpa data** Anda, pilih **Konfirmasi dan lanjutkan**, pilih **Lanjutkan tanpa data** ini, lalu akhirnya pilih **Konfirmasi dan mulai telusuri**.**
    1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasi bahwa Anda dapat terhubung ke mesin pencarian.
    1. Setelah mengonfirmasi bahwa Anda dapat mengakses www.bing.com, tutup jendela browser di VM, tetapi biarkan VM aktif.

1. Minimalkan VM dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke laman SC900-WinVM \|Koneksi.

1. Biarkan tab browser tetap terbuka, Anda akan menggunakannya untuk tugas berikutnya.

### Tugas 4

Di tugas sebelumnya, Anda telah mengonfirmasi bahwa Anda dapat membuat koneksi RDP ke VM. Setelah berada di VM, Anda juga telah mengonfirmasi bahwa Anda dapat membuat koneksi keluar ke Internet.  Lalu lintas Internet keluar diizinkan karena aturan keluar default untuk NSG mengizinkan lalu lintas Internet keluar.  Dalam tugas ini, Anda akan melakukan proses pembuatan aturan keluar kustom untuk memblokir lalu lintas Internet keluar dan menguji aturan tersebut.

1. Anda harus berada di laman SC900-WinVM \| Koneksi. Dari panel navigasi kiri, pilih **Jaringan**. Jika sebelumnya Anda menutup tab browser, pilih bilah pencarian warna biru di bagian atas laman dan pilih Mesin virtual, lalu pilih VM, **SC900-WinVM**, lalu pilih **Jaringan**.

1. Pilih tab **Aturan port keluar**. Anda akan melihat aturan keluar default.  Perhatikan aturan default "AllowInternetOutBound". Aturan ini memungkinkan semua lalu lintas Internet keluar. Anda tidak bisa menghapus aturan default, tetapi Anda bisa menimpanya dengan membuat aturan yang memiliki prioritas lebih tinggi. Dari sisi kanan laman, pilih **Tambahkan aturan port keluar**.

1. Di laman Tambah aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber: **Semua**
    1. Rentang port sumber:  **\***
    1. Tujuan: **Tag Tag**
    1. Tag layanan tujuan:  **Internet**
    1. Layanan:  **Kustom** (biarkan default)
    1. Rentang port tujuan: **\*** (pastikan untuk memberi tanda bintang di bidang rentang port tujuan)
    1. Protokol: **Semua**
    1. Tindakan: **Tolak**
    1. Prioritas: **1000**
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul di daftar aturan keluar.  Meskipun muncul dalam daftar, akan memakan waktu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan dengan langkah-langkah berikutnya).  


1. Kembali ke VM Anda (ikon RDP untuk VM harus ditampilkan di bilah tugas di bagian bawah laman).

1. Buka browser Microsoft Edge di VM Anda dan masukkan **www.bing.com**. Laman ini seharusnya tidak ditampilkan. jika Anda dapat terhubung ke internet dan Anda memverifikasi bahwa semua parameter aturan keluar telah ditetapkan dengan benar, kemungkinan karena perlu waktu beberapa menit untuk menerapkan aturan tersebut.  Tutup browser, tunggu beberapa menit dan coba lagi. Langganan Azure di lingkungan lab mungkin memerlukan waktu yang lebih lama dari biasanya.

1. Tutup koneksi desktop jarak jauh, dengan memilih **X** di tengah atas laman tempat alamat IP ditampilkan.  Jendela pop-up muncul yang menunjukkan sesi jarak jauh Anda akan terputus. Pilih **OK**.

1. Dari sudut kiri atas jendela, tepat di bawah bilah biru sebelah tulisan Microsoft Azure, pilih **Beranda** untuk kembali ke laman beranda layanan Azure.

1. Biarkan tab Azure tetap terbuka di browser Anda.

### Tinjauan

Di lab ini, Anda telah menjalani proses penyiapan grup keamanan jaringan (NSG), mengaitkan NSG tersebut ke antarmuka jaringan mesin virtual, dan menambahkan aturan baru ke NSG untuk mengizinkan lalu lintas RDP masuk dan memblokir lalu lintas Internet keluar.
