---
demo:
  title: 'Azure Network Security Groups (NSGs)'
  module: 'Modul 1: Menjelaskan kemampuan keamanan dasar di Azure'
---



# <a name="demo-azure-network-security-groups-nsgs"></a>Demo: Grup Keamanan Jaringan Azure (NSG)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Pelajaran: Menjelaskan grup Keamanan Jaringan Azure

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan menjelajahi fungsi kelompok keamanan jaringan di Azure dan menerapkan NSG ke mesin virtual yang telah dibuat sebelumnya. Anda akan mulai dengan menampilkan informasi singkat tentang VM yang telah dibuat sebelumnya oleh authorized lab hoster (ALH). Anda kemudian akan menunjukkan proses pembuatan NSG, menunjukkan aturan masuk dan keluar default, membuat aturan RDP baru untuk mengizinkan koneksi ke VM, dan mengujinya.

### <a name="demo-part-1"></a>Demo bagian 1

Di bagian ini, Anda akan melihat beberapa parameter yang terkait dengan VM yang dibuat untuk digunakan dengan lab ini.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan nama pengguna yang diberikan oleh penyedia hosting lab Anda, lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Di bagian atas halaman, di bawah yang bertuliskan Layanan Azure, pilih **Mesin Virtual**.  Jika Anda tidak melihatnya dalam daftar, maka di kotak pencarian, di bilah warna biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **Mesin Virtual** lalu pilih **Mesin Virtual** dari hasil pencarian.

1. Dari halaman Mesin virtual, pilih VM yang terdaftar **SC900-WinVM**.

1. Anda sekarang berada di halaman SC900-WinVM.  Catat nama grup Sumber Daya, LabsSC900, tempat VM berada.

1. Di bagian atas halaman, klik **Connect**, lalu dari menu tarik-turun, klik **RDP**. Perhatikan bahwa prasyarat port tidak terpenuhi.  Untuk memenuhi prasyarat, aturan keamanan jaringan masuk dengan port tujuan 3389, yang digunakan oleh RDP, harus dikonfigurasi.  Anda akan melakukannya di tugas berikutnya, saat Anda membuat kelompok keamanan jaringan.

1. Dari panel navigasi kiri, pilih **Jaringan**.  
    1. Tampilan default adalah untuk aturan port masuk.  Perhatikan bahwa antarmuka jaringan untuk VM ini tidak memiliki kelompok keamanan jaringan yang dikonfigurasi.  Hal yang sama berlaku jika Anda memilih Aturan port keluar.
    1. Pilih **Aturan keamanan yang efektif** di sebelah tulisan Antarmuka jaringan.  Perhatikan bahwa dikatakan, "Tidak ada kelompok keamanan jaringan atau kelompok keamanan aplikasi yang dikaitkan dengan antarmuka jaringan".
1. Biarkan tab browser ini terbuka.

### <a name="demo-part-2"></a>Demo bagian 2

Di bagian ini, Anda akan membuat kelompok keamanan jaringan, menetapkan antarmuka jaringan VM ke NSG tersebut, dan membuat aturan masuk baru untuk lalu lintas RDP.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Di bilah pencarian warna biru di bagian atas halaman, masukkan grup **Kelompok keamanan jaringan** . Dari hasil, pilih **Kelompok keamanan jaringan** (jangan pilih Kelompok keamanan jaringan klasik).

1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.

1. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan: Biarkan nilainya diatur ke default (ini adalah langganan Azure yang disediakan oleh authorized lab hoster)
    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Review + create**, lalu pilih **Create**.

1. Setelah penyebaran selesai, pilih **Buka Sumber daya**.

1. Di bagian atas halaman di bawah yang bertuliskan Essentials, Anda akan melihat beberapa informasi dasar tentang NSG yang Anda buat.  Dua hal yang perlu diperhatikan adalah bahwa tidak ada aturan Keamanan KUSTOM dan tidak ada subnet atau antarmuka jaringan yang terkait dengan NSG ini.  Meskipun tidak ada aturan keamanan khusus, ada aturan masuk dan keluar default yang disertakan dengan setiap NSG, seperti yang ditampilkan di halaman.  Tinjau aturan masuk dan keluar. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure.  Aturan keluar menolak semua lalu lintas keluar kecuali lalu lintas antara jaringan virtual dan lalu lintas keluar ke internet.

1. Dari panel navigasi kiri halaman NSG-SC900, di bagian Pengaturan, pilih **Antarmuka jaringan**.
    1. Lalu pilih **Kaitkan**.
    1. Di bidang untuk memilih asosiasi antarmuka jaringan, pilih **panah dropdown**, pilih **sc900-winvmXXX**, lalu pilih **ok** di bagian bawah jendela. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.

1. Di panel navigasi kiri, pilih **Aturan keamanan masuk**. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari jaringan virtual atau load balancer Azure sehingga Anda perlu menyiapkan aturan untuk mengizinkan lalu lintas RDP masuk (lalu lintas di port 3389). Ingat bahwa Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi.

1. Dari bagian atas halaman, pilih **Tambahkan**. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**
    1. Rentang port sumber: **\***
    1. Tujuan:  **Apa saja**
    1. Layanan:  **RDP**
    1. Tindakan:  **Izinkan**
    1. Prioritas: **1000**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama: Biarkan nama default atau buat nama deskriptif Anda sendiri.
    1. Perhatikan tanda peringatan di bagian bawah halaman.  Kami menggunakan RDP hanya untuk tujuan pengujian dan untuk mendemonstrasikan fungsionalitas NSG.
    1. Pilih **Tambahkan**

1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu me-refresh layar). Pada aturan yang baru ditambahkan, Anda akan melihat tanda peringatan.  Sebagaimana dinyatakan di atas, kami menggunakan RDP hanya untuk tujuan pengujian dan untuk mendemonstrasikan fungsionalitas NSG.

### <a name="demo-part-3"></a>Demo bagian 3

Dengan NSG dibuat dan dikaitkan ke VM Anda dan aturan RDP dibuat, Anda akan menunjukkan dampak NSG dengan menguji konektivitas RDP ke VM.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda. Jika sebelumnya Anda menutup tab browser, pilih bilah pencarian warna biru di bagian atas halaman dan pilih Mesin virtual, lalu pilih VM, **SC900-WinVM**.

1. Uji aturan masuk dengan memverifikasi bahwa Anda dapat terhubung ke VM menggunakan RDP.
    1. Pilih **Connect** dari panel navigasi kiri.
    1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
    1. **Open** file yang diunduh dan pilih **Connect**.
    1. Anda akan diminta memasukkan kredensial. Masukkan Nama Pengguna dan Kata Sandi yang Anda gunakan saat membuat Mesin Virtual.  Jika jendela yang meminta kredensial Anda meminta PIN, pilih **More choices**, lalu pilih **Use a different account**.
    1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan. Apakah Anda yakin ingin tetap terhubung? Pilih **Ya**.
    1. Anda sekarang terhubung ke VM. tekankan kepada pelajar bahwa dalam hal ini Anda dapat terhubung ke Mesin Virtual karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke Mesin Virtual melalui RDP.

1. Karena Anda sudah berada di VM, Anda dapat menampilkan konektivitas internet keluar ke Internet, yang diaktifkan oleh salah satu aturan keluar default.
    1. Dari VM, pilih **Microsoft Edge** untuk membuka browser.  Karena ini adalah pertama kalinya Anda membuka Microsoft Edge, Anda akan melihat jendela pop-up, pilih **Mulai tanpa data Anda**, lalu pilih **Lanjutkan tanpa data ini**, lalu pilih **Konfirmasi dan mulai menjelajah**.
    1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasi bahwa Anda dapat terhubung ke mesin pencarian.
    1. Setelah mengonfirmasi bahwa Anda dapat mengakses www.bing.com, tutup jendela browser di VM, tetapi biarkan VM aktif.

1. Minimalkan VM, dengan memilih ikon garis bawah **_** di tab warna biru yang menunjukkan alamat IP VM. Tindakan ini akan membawa Anda kembali ke SC900-WinVM | Hubungkan halaman.  

### <a name="optional-demo-part-4"></a>Demo OPSIONAL bagian 4

Jika masih ada waktu di ruang kelas, Anda mungkin ingin membuat aturan NSG keluar untuk memblokir lalu lintas internet keluar dari VM.

1. Dari panel navigasi kiri, pilih **Jaringan**. Anda harus menggunakan SC900-WinVM | Halaman jaringan.

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

1. Tutup semua tab browser yang terbuka.

1. Sebagai praktik terbaik umum, sebaiknya hentikan atau bongkar VM untuk menghindari biaya tambahan, jika digunakan hanya untuk tujuan demo atau pengujian. Namun, dalam kasus ini, JANGAN bongkar VM, karena ini akan membantu mengumpankan data manajemen kondisi keamanan cloud saat mendemonstrasikan Microsoft Defender untuk Cloud.  VM akan dibongkar saat lab dibatalkan.

#### <a name="review"></a>Tinjau

Dalam demo ini, Anda menunjukkan informasi dan pengaturan terkait NSG, termasuk proses untuk mengaitkan antarmuka ke NSG, Anda menunjukkan aturan masuk dan keluar default, dan terakhir langkah-langkah untuk membuat aturan baru.
