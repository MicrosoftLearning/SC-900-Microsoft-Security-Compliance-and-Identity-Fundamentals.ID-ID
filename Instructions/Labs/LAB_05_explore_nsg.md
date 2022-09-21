---
ms.openlocfilehash: d2377516343cb85c279c1a2d6347c59f573d73c7
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892197"
---
<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi Azure Network Security Groups (NSGs)' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft; Modul 1: Menjelaskan kemampuan keamanan dasar di Azure; Pelajaran 6: Menjelaskan grup Keamanan Jaringan Azure'
---
--->

# <a name="lab-explore-azure-network-security-groups-nsgs"></a>Lab: Mempelajari Grup Keamanan Jaringan Azure (NSG)

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan solusi keamanan Microsoft
- Modul: Menjelaskan kemampuan keamanan dasar di Azure
- Pelajaran: Menjelaskan grup Keamanan Jaringan Azure

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan mempelajari fungsi kelompok keamanan jaringan di Azure.  Anda akan menjelelajah dengan membuat VM tanpa perlu kelompok keamanan jaringan (NSG). Anda akan mempelajari proses membuat NSG dan menetapkan antarmuka VM untuk NSG.  Setelah dikonfigurasi, Anda akan mengamati aturan masuk dan keluar default dan membuat aturan baru.
  
**Perkiraan Waktu**: 15-20 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini, Anda akan membuat komputer virtual Windows 10.

1. Buka Microsoft Edge.  Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.
1. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger) lalu klik **All Services**.  
1. Di jendela utama, pada Featured, klik Komputer Vitual.  Jika Anda tidak melihat Komputer virtual terdaftar, masukkan di bilah pencarian, lalu klik dari hasil pencarian.
1. Dari pojok kiri halaman, pilih **+Buat**, lalu klik **Mesin virtual Azure**.
1. Di tab basics, isi informasi berikut ini (untuk yang tidak terdaftar, biarkan pengaturan default):
    1. Langganan: pastikan pengaturan default adalah Azure Pass – Sponsorship.

    1. Grup sumber daya: pilih **Buat baru** lalu di bidang Nama masukkan **LabsSC900**, lalu pilih **OK**.
    1. Nama mesin virtual: masukkan **SC900-WinVM**.
    1. Wilayah: jika bidang wilayah tidak diisi sebelumnya, pilih wilayah yang paling dekat dengan lokasi Anda.
    1. Gambar:  dari menu drop-down, pilih **Windows 10 Pro, Versi 21H2 – Gen 2**.
    1. Ukuran: pilih **lihat semua ukuran** dari menu drop-down dan pilih **B2s**, lalu tekan **Pilih** di bagian bawah halaman.
    1. Nama pengguna:  Masukkan nama pengguna pilihan Anda.  Harap dicatat, karena Anda akan membutuhkannya untuk mengakses Mesin Virtual.
    1. Kata sandi:  Masukkan kata sandi pilihan Anda.  Harap dicatat, karena Anda akan membutuhkannya untuk mengakses Mesin Virtual.
    1. Port masuk publik:  biarkan default, **Izinkan port yang dipilih**.
    1. Pilih port masuk: biarkan default, **RDP 3389**.
    1. Lisensi: pilih **Saya mengonfirmasi bahwa saya memiliki lisensi Windows 10 yang memenuhi syarat dengan hak hosting multi-penyewa**, sehingga tanda centang muncul di kotak.
    1. Pilih **Selanjutnya:Disk**.
1. Sekarang Anda berada di tab Disk untuk mengonfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Berikutnya: Jaringan >** .
1. Sekarang Anda berada di tab Jaringan untuk mengonfigurasi VM.  Untuk opsi grup keamanan jaringan NIC, pilih **Tidak Ada**. Biarkan semua pengaturan lain pada nilai default.  Catatan: tujuan dalam memilih tidak ada pada langkah ini adalah untuk menelusuri langkah-langkah membuat grup keamanan jaringan dari awal, dalam tugas berikutnya.
1. Dari bagian bawah halaman, pilih **Berikutnya: Tinjau + Buat>** lalu setelah validasi berlalu, pilih **buat**. Perlu beberapa menit agar penyebaran VM selesai.
1. Setelah penyebaran VM selesai, pilih **Go to resource**.
1. Sekarang Anda berada di halaman SC900-WinVM.
1. Di bagian atas halaman, klik **Connect**, lalu dari menu tarik-turun, klik **RDP**.
1. Perhatikan bahwa prasyarat port tidak terpenuhi.  Untuk memenuhi prasyarat, aturan keamanan jaringan masuk dengan port tujuan 3389, yang digunakan oleh RDP, harus dikonfigurasi.  Anda akan melakukannya di tugas berikutnya, ketika Anda membuat grup keamanan jaringan.
1. Biarkan tab browser ini terbuka.

### <a name="task-2"></a>Tugas 2

Buat grup keamanan jaringan, tetapkan antarmuka jaringan VM ke NSG tersebut, dan buat aturan masuk baru untuk lalu lintas RDP.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Pada pojok kiri atas halaman, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger), lalu klik **All Services**.
1. Di Kotak layanan filter di sebelah yang bertuliskan Semua layanan, masukkan **Network security groups**, kemudian dari hasil tersebut, klik **Network security groups** (jangan memilih Kelompok keamanan jaringan klasik).
1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.
1. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan:  Azure Pass – Sponsorship

    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Wilayah: biarkan default.
    1. Pilih **Review + create**, lalu pilih **Create**.
1. Setelah penyebaran selesai, pilih **Buka Sumber daya**.
1. Perhatikan aturan masuk dan keluar secara default di NSG.  Meskipun NSG telah dibuat dan ada aturan default untuk memfilter lalu lintas, tidak ada antarmuka yang dikaitkan dengan NSG.
1. Dari panel navigasi kiri pada halaman NSG-SC900, di bawah Pengaturan, pilih **Network interfaces**.
1. Klik **+ Associate**, di atas kotak pencarian.
1. Di sisi kanan halaman, adalah bidang untuk memilih antarmuka jaringan yang akan dikaitkan dengan NSG. Pilih panah tenggelam ke bawah, lalu pilih **sc900-winvmXXX** (XXX akan spesifik untuk antarmuka jaringan VM Anda), lalu pilih **ok** di bagian bawah jendela.
1. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.
1. Di panel navigasi kiri, pilih **Aturan keamanan masuk**.
1. Aturan masuk default menolak semua lalu lintas masuk yang bukan dari Vnet atau penyeimbang muatan Azure sehingga Anda perlu menyiapkan aturan untuk mengizinkan lalu lintas RDP masuk (lalu lintas pada port 3389). Ingat bahwa Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi.
1. Dari bagian atas halaman, pilih **Tambahkan**:
1. Di jendela aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**

    1. Rentang port sumber: **\***
    1. Tujuan:  **Apa saja**
    1. Layanan:  **RDP**
    1. Tindakan:  **Izinkan**
    1. Prioritas:  **300**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama:  **AllowRDP**
1. Pilih **Tambahkan**
1. Setelah aturan disediakan, aturan akan muncul dalam daftar aturan masuk (Anda mungkin perlu me-refresh layar).
1. Sekarang pastikan Anda dapat terhubung ke VM menggunakan RDP.  Pilih bidang pencarian di bagian atas halaman, di samping tempat dikatakan Microsoft Azure, untuk melihat layanan terbaru.  Pilih **Komputer virtual**.
1. Pilih VM, **SC900-WinVM**.
1. Di bagian atas halaman, klik **Connect**, lalu dari menu tarik-turun, klik **RDP**.
1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
1. Buka file yang diunduh dan klik **Connect**.
1. Anda akan diminta kredensial Anda.  Masukkan Nama Pengguna dan Kata Sandi yang Anda gunakan saat membuat Mesin Virtual.
1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan.  Apakah Anda yakin ingin tetap terhubung?  Pilih **Ya**.
1. Sekarang Anda terhubung ke VM. Dalam kasus ini, Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat mengizinkan lalu lintas masuk ke VM lewat RDP.
1. Biarkan VM terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

### <a name="task-3"></a>Tugas 3

Aturan keluar default untuk NSG mengizinkan lalu lintas internet keluar sehingga Anda harus memvalidasi bahwa Anda dapat terhubung ke internet.  Anda harus melewati proses membuat aturan keluar khusus untuk memblokir lalu lintas internet keluar dan menguji aturan tersebut.

1. Dari VM, klik **Edge** untuk membuka browser.  
1. Masukkan **www.bing.com** di bilah alamat browser dan konfirmasikan bahwa Anda dapat terhubung ke mesin cari.
1. Tutup browser di VM Anda, tetapi biarkan VM terbuka, karena Anda akan memerlukannya di langkah berikutnya.
1. Kembali ke Portal Azure, buka Tab Microsoft Azure – SC900-WinVM di browser Anda.
1. Dari panel navigasi kiri, di bawah Pengaturan, pilih **Networking**.
1. Klik tab **Outbound port rules**.  Anda akan melihat aturan keluar default.  Catat aturan default "AllowInternetOutBound". Aturan ini mengizinkan semua lalu lintas internet keluar. Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Di bagian kanan halaman, klik **Add outbound port rule**.
1. Di halaman Tambahkan aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber:  **Apa saja**

    1. Rentang port sumber:  **\***
    1. Tujuan:  **Tag Layanan**
    1. Tag layanan tujuan  **Internet**
    1. Layanan:  **Custom** (biarkan default)
    1. Rentang port tujuan: * (pastikan untuk memberi tanda bintang di bidang rentang port tujuan)
    1. Protokol: **Apa saja**
    1. Tindakan: **Tolak**
    1. Prioritas:  **4000**
    1. Nama:  **DenyInternet**
1. Pilih **Tambahkan**
1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.  Meskipun aturan muncul di daftar, perlu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan ke langkah berikutnya).  
1. Kembali ke VM Anda.
1. Buka browser Edge di VM Anda dan masukkan **www.bing.com**. Halaman semestinya tidak ditampilkan.  Catatan: jika Anda dapat terhubung ke internet dan Anda telah memverifikasi bahwa semua parameter aturan keluar telah diatur dengan benar, kemungkinan karena aturan tersebut memerlukan waktu beberapa menit untuk diterapkan.  Tutup browser, tunggu beberapa menit, dan coba lagi.
1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up menunjukkan Sesi jarak jauh Anda akan terputus. Pilih **OK**.
1. Di tugas ini, Anda berhasil mengonfigurasi aturan keluar di NSG Anda, serta memblokir lalu lintas internet keluar.

### <a name="tear-down"></a>Penghapusan

VM adalah sumber daya yang ditagih dan meskipun biaya menjalankan VM dalam demo ini sangat kecil, sebaiknya Anda menghapus grup sumber daya yang berisi VM dan sumber daya terkait, di akhir kursus.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Dari sudut kiri atas halaman, pilih **All Services**.
1. Di kotak Filter layanan di sebelah tulisan Semua layanan, masukkan **Resource groups** lalu dari hasil tersebut, pilih **Resource groups**.
1. Klik **LabsSC900**.
1. Di bagian tengah atas halaman LabsSC900, klik **Delete resource group**.
1. DI jendela yang terbuka, masukkan nama grup sumber daya **LabsSC900**, untuk konfirmasi penghapusan grup sumber daya dan semua sumber daya di dalamnya, lalu klik **Delete** di bagian bawah halaman.
1. Mungkin perlu beberapa menit agar semua sumber daya dan grup sumber daya terhapus.
1. Tutup semua tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini Anda berjalan melalui proses pengaturan kelompok keamanan jaringan (NSG), mengaitkan NSG tersebut ke antarmuka jaringan komputer virtual, dan menambahkan aturan baru ke NSG untuk memungkinkan lalu lintas RDP masuk dan memblokir lalu lintas internet keluar.
