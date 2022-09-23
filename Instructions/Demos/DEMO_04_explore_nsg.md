---
ms.openlocfilehash: ce07082f318bbb7b96e3eac0d8f549795bdf488d
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892435"
---
<a name="---"></a><!---
---
Demo: Judul: 'Azure Network Security Groups (NSGs)' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 1: Menjelaskan kemampuan keamanan dasar di Azure; Pelajaran 6: Menjelaskan grup Keamanan Jaringan Azure'
---
--->

# <a name="demo-azure-network-security-groups-nsgs"></a>Demo: Grup Keamanan Jaringan Azure (NSG)

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Pelajaran: Menjelaskan grup Keamanan Jaringan Azure

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan menunjukkan fungsi grup keamanan jaringan (NSG) di Azure.  Anda akan melakukan ini dengan terlebih dahulu membuat Komputer Virtual (VM) tanpa NSG apa pun, sebagai bagian dari pengaturan prademo. Anda juga akan membuat NSG tanpa antarmuka atau subnet terkait.  Sebagai bagian dari demo, Anda akan menunjukkan aturan masuk dan keluar default untuk NSG. Kemudian, Anda akan melakukan proses menetapkan antarmuka VM ke NSG.  Setelah dikonfigurasikan, Anda akan menguji koneksi ke VM, menggunakan aturan NSG default, dan juga aturan yang akan Anda buat.
  
### <a name="pre-demo-setup-part-1"></a>Pengaturan prademo bagian 1

 Instruktur disarankan agar melakukan ini **SEBELUM** kelas karena dapat memakan waktu beberapa menit untuk membuat VM. Dalam pengaturan ini, Anda akan membuat komputer virtual Windows 10.

1. Buka tab **Home – Microsoft Azure** di browser Anda.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **Virtual machines**, kemudian pilih **Virtual Machines** dari hasil pencarian.  

1. Dari kiri atas halaman, pilih **+Add** kemudian pilih **+Virtual machine**.

1. Di tab basics, isi informasi berikut ini (untuk yang tidak terdaftar, biarkan pengaturan default):
    1. **Subscription**: verifikasi pengaturan default menjadi Azure Pass – Sponsorship.
    1. **Resource group**: pilih **Create new**, lalu di kolom Nama masukkan **LabsSC900-RG**, lalu pilih **OK**.
    1. **Nama mesin virtual**: masukkan **SC900-WinVM**.
    1. **Wilayah**: biarkan default.
    1. **Availability options**: pastikan untuk memilih **No infrastructure redundancy required**.  CATATAN: opsi ketersediaan harus diatur ke No infrastructure redundancy required, jika tidak, demo tidak akan berfungsi sesuai harapan.  Memiliki opsi ketersediaan memerlukan NSG dan kami sengaja membuat VM tanpa NSG.
    1. **Gambar**:  dari menu drop-down, pilih **Windows 10 Pro, Versi 21H2 – Gen 2**.
    1. **Ukuran**: pilih **lihat semua ukuran** dari menu drop-down dan pilih **B2s**, lalu tekan **Pilih** di bagian bawah halaman.
    1. **Username**:  Masukkan nama pengguna pilihan Anda.  Harap dicatat, karena Anda akan membutuhkannya untuk mengakses Mesin Virtual.
    1. **Password**:  Masukkan kata sandi pilihan Anda.  Harap dicatat, karena Anda akan membutuhkannya untuk mengakses Mesin Virtual.
    1. **Port masuk publik**: biarkan default, **Izinkan port yang dipilih**.
    1. **Pilih port masuk**: biarkan default, **RDP 3389**
    1. **Lisensi**: pilih **Saya mengonfirmasi bahwa saya memiliki lisensi Windows 10 yang memenuhi syarat dengan hak hosting multi-penyewa**, sehingga tanda centang muncul di kotak.
    1. Pilih **Selanjutnya:Disk**.

1. Sekarang Anda berada di tab Disk untuk mengonfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Berikutnya: Jaringan >** .
1. Sekarang Anda berada di tab Jaringan untuk mengonfigurasi VM.  Untuk opsi grup keamanan jaringan NIC, pilih **Tidak Ada**. Biarkan semua pengaturan lain pada nilai default.
1. Dari bagian bawah halaman, pilih **Berikutnya: Tinjau + Buat>** lalu setelah validasi berlalu, pilih **buat**. Perlu beberapa menit agar penyebaran VM selesai.
1. Setelah penyebaran VM selesai, pilih **Go to resource**.
1. Sekarang Anda berada di halaman SC900-WinVM.
1. Di bagian atas halaman, klik **Connect**, lalu dari menu tarik-turun, klik **RDP**.
1. Perhatikan bahwa prasyarat port tidak terpenuhi.  Untuk memenuhi prasyarat, aturan keamanan jaringan masuk dengan port tujuan 3389, yang digunakan oleh RDP, harus dikonfigurasi.  Anda akan melakukannya di tugas berikutnya, ketika Anda membuat grup keamanan jaringan.
1. Biarkan tab browser ini terbuka.


### <a name="pre-demo-setup-part-2"></a>Pengaturan Pra-Demo bagian 2

Buat grup keamanan jaringan, tetapi JANGAN tetapkan antarmuka jaringan VM ke NSG.  

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **network security group**, lalu pilih **Network security groups** dari hasil pencarian.  Jangan pilih Kelompok keamanan jaringan klasik.

1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.

1. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan:  Azure Pass – Sponsorship
    1. Grup sumber daya:  **LabsSC900-RG**
    1. Nama:  **NSG-SC900**
    1. Wilayah:  biarkan default
    1. Pilih **Review + create**, lalu pilih **Create**.

1. Setelah penyebaran selesai, pilih **Go to resource** dan pastikan semuanya benar.  Harus ada 3 masuk default, 3 aturan keluar default, dan tidak ada subnet dan antarmuka yang terkait dengan NSG.  Kembali ke halaman **Home** portal Azure.  

### <a name="demo"></a>Demo

Telusuri pengaturan NSG.  Dalam hal ini, Anda akan melakukan penelusuran ke NSG yang sudah ada (yang Anda buat dengan pengaturan di atas) yang belum ditetapkan ke antarmuka VM. Anda kemudian akan menunjukkan proses mengaitkan antarmuka ke NSG serta proses pembuatan aturan masuk dan keluar.

1. Buka tab browser, **Home-Microsoft Azure**.  Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan masuk kembali.

1. Di kotak pencarian, di bilah biru di bagian atas halaman sebelah tulisan Microsoft Azure, masukkan **network security group**, lalu pilih **Network security groups** dari hasil pencarian.  Jangan pilih Kelompok keamanan jaringan klasik.

1. Dari halaman NSG, pilih NSG yang Anda buat di pengaturan, **NSG-SC900**.

1. Tab **Overview** di panel navigasi kiri disorot.  Perhatikan aturan masuk dan keluar secara default di NSG. Meskipun NSG telah dibuat dan ada aturan default untuk memfilter lalu lintas, tidak ada antarmuka yang dikaitkan dengan NSG. Anda dapat melihat ini di kanan atas halaman yang tertulis “Associated with: 0 subnets, 0 network interfaces".  Untuk melakukan hal itu, NSG harus ditetapkan ke sesuatu.  Dalam kasus ini, kita akan menetapkan antarmuka jaringan untuk VM yang telah dibuat sebelumnya.

1. Dari panel navigasi kiri pada halaman NSG-SC900, di bawah Pengaturan, pilih **Network interfaces**.

1. Pilih **+ Associate**, di atas kotak pencarian, lalu dari menu tarik-turun pilih **sc900-winvmXXX** (XXX akan menjadi khusus untuk antarmuka jaringan VM Anda), lalu pilih **Ok**. Saat antarmuka sedang dikaitkan, Anda akan melihat kotak notifikasi di pojok kanan atas layar. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.

1. Kembali ke tab **Overview**.  Perhatikan bahwa di kanan atas halaman Anda akan melihat “Associated with: 0 subnets, 1 network interfaces”– antarmuka sekarang ditetapkan ke NSG. Juga, tekankan aturan default kepada pelajar. Untuk masuk, hanya lalu lintas dari jaringan virtual Azure lain dan penyeimbang beban Azure yang akan diizinkan. Semua lalu lintas masuk lainnya ke VM akan ditolak. Sebutkan juga aturan keluar default.  Hanya lalu lintas keluar ke vnet lain dan lalu lintas internet keluar yang diperbolehkan.  Sebagai bagian dari demo, sebaiknya Anda meluangkan waktu sebentar untuk menunjukkan bahwa lalu lintas masuk ditolak.
    1. Di bilah pencarian, di bagian atas halaman, masuk dan pilih **Virtual Machines**.
    1. Dari halaman Komputer Virtual, pilih  **SC900-WinVM**.
    1. Dari bagian atas halaman SC900-WinVM, pilih **Connect**, lalu pilih **RDP**.
    1. Perhatikan bahwa prasyarat port tidak terpenuhi.  Untuk memungkinkan memenuhi prasyarat, aturan keamanan jaringan masuk dengan port tujuan 3389, yang digunakan oleh RDP, harus dikonfigurasi.  

1. Sekarang Anda akan membuat aturan baru untuk mengizinkan lalu lintas RDP masuk.  Sampaikan bahwa Anda tidak dapat menghapus aturan default yang ada, Anda hanya dapat membuat yang baru dengan prioritas lebih tinggi. Dari panel navigasi kiri, di bawah Pengaturan, pilih **Networking**.  Anda berada di halaman jaringan VM.
1. Verifikasi bahwa tab **Aturan port masuk** dipilih (digaris bawahi) lalu pilih **Tambahkan aturan port masuk** untuk membuat aturan untuk mengizinkan lalu lintas RDP masuk, dengan pengaturan berikut:
    1. Sumber: **Apa saja**
    1. Rentang port sumber: **\***
    1. Tujuan: **Apa saja**
    1. Layanan: **RDP**
    1. Tindakan: **Izinkan**
    1. Prioritas: **300**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu. Jadi, prioritas untuk aturan baru ini harus lebih tinggi daripada prioritas untuk aturan yang ada yang menolak semua lalu lintas masuk.
    1. Nama: **AllowRDP**
    1. Pilih **Tambahkan**
    1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan masuk.

1. Sekarang pilih tab **Aturan port keluar** dan tinjau aturan default.  Pilih **Tambahkan aturan port keluar** dari bagian atas halaman dan jelaskan berbagai pengaturan tersebut.  Saya sarankan membuat aturan – Pengaturan di bawah ini membuat aturan menolak lalu lintas internet keluar:
    1. Sumber: **Apa saja**
    1. Rentang port sumber: **\***
    1. Tujuan: **Tag Layanan**
    1. Tag layanan tujuan **Internet**
    1. Layanan: **Custom** (biarkan default)
    1. Rentang port tujuan: **\*** (pastikan untuk memberi tanda bintang di bidang rentang port tujuan).
    1. Protokol: **Apa saja**
    1. Tindakan: **Tolak**
    1. Prioritas: **4000** (poin yang perlu diperhatikan adalah bahwa prioritas harus lebih tinggi dari prioritas aturan yang ada yang memungkinkan lalu lintas keluar internet)
    1. Nama: **DenyInternet**
    1. Pilih **Tambahkan**
    1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.

1. Sekarang kembali ke VM Anda dan uji aturannya.  Dari bagian atas halaman, pilih **SC900-VM**.

1. Uji aturan masuk dengan memverifikasi bahwa Anda dapat terhubung ke VM menggunakan RDP.
    1. Pilih **Connect** dari panel navigasi kiri.
    1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
    1. **Open** file yang diunduh dan pilih **Connect**.
    1. Anda akan diminta kredensial Anda. Masukkan Nama Pengguna dan Kata Sandi yang Anda gunakan saat membuat Mesin Virtual.  Jika jendela yang meminta kredensial Anda meminta PIN, pilih **More choices**, lalu pilih **Use a different account**.
    1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan. Apakah Anda yakin ingin tetap terhubung? Pilih **Ya**.
    1. Sekarang Anda terhubung ke VM. tekankan kepada pelajar bahwa dalam hal ini Anda dapat terhubung ke Mesin Virtual karena aturan lalu lintas masuk yang Anda buat memungkinkan lalu lintas masuk ke Mesin Virtual melalui RDP.

1. Sekarang uji aturan NSG keluar
    1. Buka browser Edge di VM.
    1. Masukkan **www.bing.com**. Halaman semestinya tidak ditampilkan. Catatan: jika Anda dapat terhubung ke internet dan Anda telah memverifikasi bahwa semua parameter aturan keluar telah diatur dengan benar, kemungkinan karena aturan tersebut memerlukan waktu beberapa menit untuk diterapkan. Silakan tunggu beberapa menit, lalu coba kembali.

1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan. Jendela pop-up menunjukkan Sesi jarak jauh Anda akan terputus. Pilih **Ok**.

1. Kembali ke halaman Beranda portal Azure, dengan memilih **Microsoft Azure** di bilah biru bagian atas halaman.

### <a name="post-course-delivery-tear-down"></a>Penghapusan setelah penyampaian kursus

VM adalah sumber daya yang ditagih dan meskipun biaya menjalankan VM dalam demo ini sangat kecil, sebaiknya Anda menghapus grup sumber daya yang berisi VM dan sumber daya terkait, di akhir penyampaian kursus.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Dari sudut kiri atas halaman, pilih **All Services**.

1. Di kotak Filter layanan di sebelah tulisan Semua layanan, masukkan **Resource groups** lalu dari hasil tersebut, pilih **Resource groups**.

1. Pilih **LabsSC900-RG**.

1. Dari bagian tengah atas halaman LabsSC900-RG, pilih **Delete resource group**.

1. Di jendela yang terbuka, masukkan nama grup sumber daya, **LabsSC900-RG**, untuk mengonfirmasi penghapusan grup sumber daya dan semua sumber dayanya, lalu pilih **Delete** dari bagian bawah halaman.

1. Mungkin perlu beberapa menit agar semua sumber daya dan grup sumber daya terhapus.

#### <a name="review"></a>Tinjau

Dalam demo ini, Anda telah menunjukkan informasi dan pengaturan terkait NSG, termasuk proses mengaitkan antarmuka ke NSG, Anda telah menunjukkan aturan masuk dan keluar default, dan terakhir langkah-langkah pembuatan aturan baru.
