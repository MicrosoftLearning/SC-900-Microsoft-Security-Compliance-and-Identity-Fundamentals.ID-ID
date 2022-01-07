---
Demo:
    title: 'Grup Keamanan Jaringan Azure (NSG)'
    module: 'Modul 3 Pelajaran 1: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan keamanan dasar di Azure.'
---

# Demo: Grup Keamanan Jaringan Azure (NSG)

### Skenario demo
Dalam demo ini, Anda akan menunjukkan fungsi grup keamanan jaringan (NSG) di Azure.  Anda akan melakukan ini dengan terlebih dahulu membuat Komputer Virtual (VM) tanpa NSG apa pun, sebagai bagian dari pengaturan prademo. Anda juga akan membuat NSG tanpa antarmuka atau subnet terkait.  Sebagai bagian dari demo, Anda akan menunjukkan aturan masuk dan keluar default untuk NSG. Kemudian, Anda akan melakukan proses menetapkan antarmuka VM ke NSG.  Setelah dikonfigurasi Anda akan menguji koneksi ke VM, menggunakan aturan NSG default dan juga aturan yang akan Anda buat.
  

#### Pengaturan prademo bagian 1
 Instruktur disarankan agar melakukan ini **SEBELUM** kelas karena dapat memakan waktu beberapa menit untuk membuat VM. Dalam pengaturan ini, Anda akan membuat komputer virtual Windows 10.

1. Buka tab **Home – Microsoft Azure** di browser Anda.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com, lalu masuk kembali.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **Virtual machines**, kemudian pilih **Virtual Machines** dari hasil pencarian.  

1. Dari kiri atas halaman, pilih **+Add** kemudian pilih **+Virtual machine**.

1. Dari tab dasar, isi informasi berikut (untuk apa pun yang tidak terdaftar, biarkan pengaturan default):
    1. **Subscription**: verifikasi pengaturan default menjadi Azure Pass – Sponsorship.
    1. **Resource group**: pilih **Create new**, lalu di kolom Nama masukkan **LabsSC900-RG**, lalu pilih **OK**.
    1. **Virtual machines name**:  masukkan **SC900-WinVM**.
    1. **Region**:  biarkan default.
    1. **Availability options**: pastikan untuk memilih **No infrastructure redundancy required**.  CATATAN: opsi ketersediaan harus diatur ke No infrastructure redundancy required, jika tidak, demo tidak akan berfungsi sesuai harapan.  Memiliki opsi ketersediaan memerlukan NSG dan kami sengaja membuat VM tanpa NSG.
    1. **Image**:  dari menu tarik-turun, pilih **Windows 10 Pro, Version 20H2 – Gen 1**.
    1. **Size**:  pilih **see all sizes** dari menu tarik-turun dan pilih **B2s**, lalu tekan **Select** di bagian bawah halaman.
    1. **Username**:  masukkan **AzureUser**.
    1. **Password**:  masukkan **SC900AzureLabs**.
    1. **Public inbounds ports**:  Anda dapat meninggalkan pengaturan default (Anda boleh memilih apa pun di sini karena pengaturan jaringan akan mengesampingkan apa yang Anda lakukan di sini).
    1. **Licensing**:  pilih **I confirm I have an eligible Windows 10 license with multi-tenant hosting rights**, sehingga muncul tanda centang di kotak.
    1. Pilih **Next: Disks**.

1. Sekarang Anda berada di tab Disk untuk konfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Next: Networking >**.

1. Sekarang Anda berada di tab Jaringan untuk konfigurasi VM.  Isi informasi berikut (untuk apa pun yang tidak terdaftar, biarkan pengaturan default):
    1. Kelompok keamanan jaringan NIC:  pilih **None**.  Catatan: Dengan memilih tidak ada, Anda memastikan bahwa NIC tidak memiliki NSG.  Pada langkah berikutnya dalam demo, Anda akan membuat NSG dan menetapkan VM NIC ke NSG yang Anda buat.
    1. Karena pengaturan lain untuk VM akan disimpan sebagai default, lanjutkan dan pilih Berikutnya: **Review + Create>**.

1. Tinjau konfigurasi VM Anda.  Beberapa poin yang perlu diperhatikan: VM ini memiliki alamat IP publik dan tidak ada grup keamanan jaringan NIC.  Dari perspektif keamanan, ini membuat VM terbuka.  Kami akan membahas ini dalam tugas berikutnya. Pilih **Create**.  Mungkin butuh waktu beberapa menit hingga penerapan VM selesai.

1. Perhatikan nama antarmuka jaringan, **sc900-winvmXXX** (XXX akan menjadi khusus untuk antarmuka jaringan VM Anda).

1. Setelah penyebaran VM selesai, pilih **Go to resource**.  Sekarang Anda berada di halaman SC900-WinVM.  Perhatikan alamat IP publik.

1. Dari panel navigasi kiri, pilih **Networking** dan perhatikan antarmuka jaringan **sc900-winvmXXX** (XXX akan menjadi khusus untuk antarmuka jaringan VM Anda).  Seharusnya tidak ada aturan masuk atau keluar yang terkait dengan antarmuka.  

1. Dari bagian atas halaman, pilih **Connect** karena penting untuk memverifikasi bahwa Anda dapat terhubung ke VM.
    1. Dari bagian atas halaman, pastikan bahwa **RDP** dipilih (digarisbawahi).
    1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
    1. **Open** file yang diunduh dan di jendela yang muncul, pilih **Connect**.
    1. Sebuah jendela terbuka yang akan meminta kredensial Anda. Jika jendela default meminta PIN, pilih **More choices**, lalu pilih **Use a different account**.   Kredensial Anda akan diminta.  Untuk Nama pengguna, masukkan **AzureUser**.  Untuk Kata sandi, masukkan **SC900AzureLabs**.
    1. Jendela koneksi Desktop Jarak Jauh terbuka yang menunjukkan, Identitas komputer jarak jauh tidak dapat diverifikasi.  Apakah Anda tetap ingin terhubung?  Pilih **Yes**.
    1. Anda sekarang terhubung ke VM Windows yang baru saja Anda buat. Selesaikan pengaturan Windows. Meskipun Anda terhubung ke VM melalui RDP dan Port RDP yang umum digunakan, VM ini memiliki semua port yang terbuka dan tidak ada yang memfilter lalu lintas.  Tutup koneksi desktop jarak jauh, dengan memilih **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up menunjukkan sesi jarak jauh Anda akan terputus. Pilih **OK**.

1. Anda sekarang kembali ke SC900-WinVM di portal Azure.  Biarkan tab browser ini terbuka untuk tugas berikutnya.

#### Pengaturan Pra-Demo bagian 2
Buat grup keamanan jaringan, tetapi JANGAN tetapkan antarmuka jaringan VM ke NSG.  

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **network security group**, lalu pilih **Network security groups** dari hasil pencarian.  Jangan pilih Kelompok keamanan jaringan klasik.

1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.

1. Pada tab Basics dari halaman Buat kelompok keamanan jaringan, tentukan pengaturan berikut.
    1. Langganan:  Azure Pass – Sponsorship
    1. Grup sumber daya:  **LabsSC900-RG**
    1. Nama:  **NSG-SC900**
    1. Kawasan:  biarkan default **(US) East US**
    1. Pilih **Review + create**, lalu pilih **Create**.

1. Setelah penyebaran selesai, pilih **Go to resource** dan pastikan semuanya benar.  Harus ada 3 masuk default, 3 aturan keluar default, dan tidak ada subnet dan antarmuka yang terkait dengan NSG.  Kembali ke halaman **Home** portal Azure.  

#### Demo
Telusuri pengaturan NSG.  Dalam hal ini, Anda akan melakukan penelusuran ke NSG yang sudah ada (yang Anda buat dengan pengaturan di atas) yang belum ditetapkan ke antarmuka VM. Kemudian Anda akan menunjukkan proses pengaitan antarmuka ke NSG dan proses pembuatan aturan masuk dan keluar.

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **network security group**, lalu pilih **Network security groups** dari hasil pencarian.  Jangan pilih Kelompok keamanan jaringan klasik.

1. Dari halaman NSG, pilih NSG yang Anda buat di pengaturan, **NSG-SC900**.

1. Tab **Overview** di panel navigasi kiri disorot.  Perhatikan aturan masuk dan keluar default di NSG. Meskipun NSG telah dibuat dan ada aturan default untuk memfilter lalu lintas, tidak ada antarmuka yang dikaitkan dengan NSG. Anda dapat melihat ini di kanan atas halaman yang tertulis “Associated with: 0 subnets, 0 network interfaces".  Untuk melakukan hal itu, NSG harus ditetapkan ke sesuatu.  Dalam kasus ini, kita akan menetapkan antarmuka jaringan untuk VM yang telah dibuat sebelumnya.

1. Dari panel navigasi kiri pada halaman NSG-SC900, di bawah Pengaturan, pilih **Network interfaces**.

1. Pilih **+ Associate**, di atas kotak pencarian, lalu dari menu tarik-turun pilih **sc900-winvmXXX** (XXX akan menjadi khusus untuk antarmuka jaringan VM Anda), lalu pilih **Ok**. Saat antarmuka sedang dikaitkan, Anda akan melihat kotak notifikasi di sudut kanan atas layar. Setelah antarmuka dikaitkan ke NSG, ini akan muncul di daftar.

1. Kembali ke tab **Overview**.  Perhatikan bahwa di kanan atas halaman Anda akan melihat “Associated with: 0 subnets, 1 network interfaces”– antarmuka sekarang ditetapkan ke NSG. Juga, tekankan aturan default kepada pelajar. Untuk masuk, hanya lalu lintas dari jaringan virtual Azure lain dan penyeimbang beban Azure yang akan diizinkan. Semua lalu lintas masuk lainnya ke VM akan ditolak. Sebutkan juga aturan keluar default.  Hanya lalu lintas keluar ke vnet lain dan lalu lintas internet keluar yang diperbolehkan.  Sebagai bagian dari demo, sebaiknya Anda meluangkan waktu sebentar untuk menunjukkan bahwa lalu lintas masuk ditolak.
    1. Di bilah pencarian, di bagian atas halaman, masuk dan pilih **Virtual Machines**.
    1. Dari halaman Komputer Virtual, pilih **SC900-WinVM**.
    1. Dari bagian atas halaman SC900-WinVM, pilih **Connect**, lalu pilih **RDP**.
    1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
    1. **Open** file yang diunduh dan pilih **Connect**.
    1. Setelah beberapa detik mencoba untuk menyambungkan, Anda akan melihat pesan kegagalan, yang menunjukkan bahwa Desktop jarak jauh tidak dapat terhubung ke komputer jarak jauh. Pilih **OK**.

1. Sekarang setelah Anda menunjukkan dampak aturan masuk default NSG, Anda akan perlu membuat aturan baru untuk mengizinkan lalu lintas RDP masuk.  Sampaikan bahwa Anda tidak dapat menghapus aturan default yang ada, Anda hanya dapat membuat yang baru dengan prioritas lebih tinggi.
    1. Dari panel navigasi kiri, di bawah Pengaturan, pilih **Networking**.  Anda berada di halaman jaringan VM dan meskipun Anda dapat membuat aturan masuk dan aturan keluar dari sini, kembali ke halaman NSG, bagaimanapun juga demo ini tentang NSG.  **Pilih NSG-SC900**, ini adalah tautan di tengah jendela.

1. Sekarang Anda berada di halaman tinjauan NSG.  Perhatikan informasi tentang NSG. Dari panel navigasi kiri halaman NSG, di bawah pengaturan, pilih **Inbound security rules**, lalu pilih **+ Add** dari bagian atas halaman. Pada halaman Tambahkan aturan keamanan masuk, jelaskan berbagai pengaturan tersebut. Sebaiknya Anda benar-benar membuat aturan untuk mengizinkan lalu lintas RDP masuk, dengan pengaturan berikut:
    1. Sumber: **Any**
    1. Rentang port sumber: **\***
    1. Tujuan: **Any**
    1. Layanan: **RDP**
    1. Tindakan: **Allow**
    1. Prioritas: **300**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu. Jadi, prioritas untuk aturan baru ini harus lebih tinggi daripada prioritas untuk aturan yang ada yang menolak semua lalu lintas masuk.
    1. Nama: **AllowRDP**
    1. Pilih **Add**
    1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan masuk.

1. Sekarang periksa **Outbound security rules**.  Pilih **+ Add** dari bagian atas halaman dan jelaskan berbagai pengaturan tersebut.  Saya sarankan membuat aturan – Pengaturan di bawah ini membuat aturan menolak lalu lintas internet keluar:
    1. Sumber: **Any**
    1. Rentang port sumber: **\***
    1. Tujuan: **Service Tag**
    1. Tag layanan tujuan **Internet**
    1. Layanan: **Custom** (biarkan default)
    1. Rentang port tujuan: **\*** (pastikan untuk menempatkan tanda bintang di bidang rentang port tujuan).
    1. Protokol: **Any**
    1. Tindakan: **Deny**
    1. Prioritas: **4000** (poin yang perlu diperhatikan adalah bahwa prioritas harus lebih tinggi dari prioritas aturan yang ada yang memungkinkan lalu lintas keluar internet)
    1. Nama: **DenyInternet**
    1. Pilih **Add**
    1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.

1. Sekarang kembali ke VM Anda dan uji aturannya.  Dari bagian atas halaman, pilih **SC900-VM**, di atas tulisan aturan keamanan keluar.

1. Uji aturan masuk dengan memverifikasi bahwa Anda dapat terhubung ke VM menggunakan RDP.
    1. Pilih **Connect** dari panel navigasi kiri.
    1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
    1. **Open** file yang diunduh dan pilih **Connect**.
    1. Kredensial Anda akan diminta. Untuk Nama pengguna, masukkan **AzureUser**. Untuk Kata sandi, masukkan **SC900AzureLabs**.  Jika jendela yang meminta kredensial Anda meminta PIN, pilih **More choices**, lalu pilih **Use a different account**.
    1. Jendela koneksi Desktop Jarak Jauh terbuka yang menunjukkan, Identitas komputer jarak jauh tidak dapat diverifikasi. Apakah Anda tetap ingin terhubung? Pilih **Yes**.
    1. Anda sekarang terhubung ke VM. tekankan kepada pelajar bahwa dalam hal ini Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke VM melalui RDP.

1. Sekarang uji aturan NSG keluar
    1. Buka browser Edge di VM.
    1. Masukkan **https://www.bing.com**. Halaman semestinya tidak ditampilkan. Catatan: jika Anda dapat terhubung ke internet dan Anda telah memverifikasi bahwa semua parameter aturan keluar telah diatur dengan benar, kemungkinan karena aturan tersebut memerlukan waktu beberapa menit untuk diterapkan. Tunggu beberapa menit dan coba lagi.

1. Tutup koneksi desktop jarak jauh, dengan memilih **X** di bagian tengah atas halaman tempat alamat IP ditampilkan. Jendela pop-up menunjukkan sesi jarak jauh Anda akan terputus. Pilih **Ok**.

1. Kembali ke halaman Beranda portal Azure, dengan memilih **Microsoft Azure** di bilah biru bagian atas halaman.

#### Penghapusan
**IMPORTANT**: Dalam tugas ini Anda akan menghapus grup sumber daya dan semua sumber daya yang ada di dalamnya.   Ini penting untuk menghindari biaya tambahan.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Dari sudut kiri atas halaman, pilih **All Services**.

1. Di kotak Filter layanan di sebelah tulisan Semua layanan, masukkan **Resource groups**, lalu dari hasil tersebut, pilih **Resource groups**.

1. Pilih **LabsSC900-RG**.

1. Dari bagian tengah atas halaman LabsSC900-RG, pilih **Delete resource group**.

1. Di jendela yang terbuka, masukkan nama grup sumber daya, **LabsSC900-RG**, untuk mengonfirmasi penghapusan grup sumber daya dan semua sumber dayanya, lalu pilih **Delete** dari bagian bawah halaman.

1. Mungkin perlu beberapa menit untuk menghapus semua sumber daya dan grup sumber daya.

#### Tinjauan

Dalam demo ini, Anda telah menunjukkan informasi dan pengaturan terkait NSG, termasuk proses mengaitkan antarmuka ke NSG, Anda telah menunjukkan aturan masuk dan keluar default, dan terakhir langkah-langkah pembuatan aturan baru.
