---
lab:
    title: 'Menjelajahi Grup Keamanan Jaringan Azure (NSG)'
    module: 'Modul 3 Pelajaran 1: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan keamanan dasar di Azure.'
---


# Lab: Menjelajahi Grup Keamanan Jaringan Azure (NSG)

## Skenario lab
Di lab ini, Anda akan mempelajari fungsi kelompok keamanan jaringan di Azure.  Anda akan menjelelajah dengan membuat VM tanpa perlu kelompok keamanan jaringan (NSG).  Tanpa NSG apa pun untuk memfilter lalu lintas, semua port di VM diekspos ke internet publik.  Anda akan mempelajari proses membuat NSG dan menetapkan antarmuka VM untuk NSG.  Setelah dikonfigurasikan, Anda akan menguji koneksi ke VM, menggunakan aturan NSG default, dan juga aturan yang akan Anda buat.
  

**Perkiraan Waktu**: 15-20 menit

#### Tugas 1:  Dalam tugas ini, Anda akan membuat komputer virtual Windows 10.    
1.	Buka Microsoft Edge.  Di bilah alamat masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.

    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.
1. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger), lalu klik **All Services**.  
1. Di jendela utama, pada Featured, klik Komputer Vitual.  Jika Anda tidak melihat Komputer virtual terdaftar, masukkan di bilah pencarian, lalu klik dari hasil pencarian.
1. Di pojok kiri halaman, klik **+Create**, lalu klik **+Virtual machine**.
1. Di tab basics, isi informasi berikut ini (untuk yang tidak terdaftar, biarkan pengaturan default):
    1. Langganan: pastikan pengaturan default adalah Azure Pass – Sponsorship.

    1. Grup sumber daya:  klik **Create new**, lalu di Bidang nama masukkan **LabsSC900**, lalu klik **OK**.
    1. Nama komputer virtual:  masukkan **SC900-WinVM**.
    1. Image:  di menu tarik-turun, klik **Windows 10 Pro, Version 20H2 – Gen 1**.
    1. Ukuran:  pilih **see all sizes** dari menu tarik-turun dan pilih **B2s**, lalu tekan **Select** di bagian bawah halaman.
    1. Nama pengguna:  masukkan **AzureUser**.
    1. Kata sandi:  masukkan **SC900AzureLabs**.
    1. Port masuk publik:  pilih **None**.
    1. Lisensi:  pilih **I confirm I have an eligible Windows 10 license with multi-tenant hosting rights**, agar tanda centang muncul di kotak.
    1. Pilih **Next: Disks**. 
1. Sekarang Anda berada di tab Disk untuk mengonfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Next: Networking >**.
1. Sekarang Anda berada di tab Jaringan untuk mengonfigurasi VM.  Isi informasi berikut (untuk apa pun yang tidak terdaftar, biarkan pengaturan default):
    1. Kelompok keamanan jaringan NIC  pilih **None**.

    1. Pilih **Next:  Management >**.
1. Sekarang Anda berada di Tab manajemen untuk konfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Next: Advanced>**.
1. Sekarang Anda berada di Tab lanjutan untuk konfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Next: Tags>**.
1. Sekarang Anda berada di Tab tag untuk konfigurasi VM.  Biarkan semua pengaturan ke default dan pilih **Next: Review + Create>**.
1. Tinjau konfigurasi VM Anda.  Beberapa poin yang perlu diperhatikan: VM ini memiliki alamat IP publik dan tidak ada grup keamanan jaringan NIC.  Dari perspektif keamanan, ini membuat VM terbuka.  Kita akan membahas ini dalam tugas berikutnya. Pilih Create.  Perlu beberapa menit agar penyebaran VM selesai.
1. Catat nama antarmuka jaringan, **sc900-winvmXXX** (XXX akan menjadi antarmuka jaringan VM Anda).
1. Setelah penyebaran VM selesai, pilih **Go to resource**.
1. Sekarang Anda berada di halaman SC900-WinVM.  Perhatikan alamat IP publik. 
1. Di bagian atas halaman, klik **Connect**, lalu dari menu tarik-turun, klik **RDP**.
1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**. 
1. Buka file yang diunduh dan klik **Connect**. 
1. Anda akan diminta kredensial Anda.  Untuk Nama Pengguna, masukkan **AzureUser**.  Untuk Kata Sandi, masukkan **SC900AzureLabs**. 
1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan.  Apakah Anda yakin ingin tetap terhubung?  Pilih **Yes**.
1. Sekarang Anda terhubung ke Windows VM yang baru saja Anda buat. Ikuti perintah untuk menyelesaikan penyiapan Windows. Meskipun Anda terhubung ke VM melalui RDP dan biasanya menggunakan Port RDP, VM ini semua port-nya terbuka dan tidak ada yang memfilter lalu lintas. 
1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up menunjukkan Sesi jarak jauh Anda akan terputus. Klik **OK**.
1. Sekarang Anda kembali ke SC900-WinVM di portal Azure.  Biarkan tab browser ini terbuka untuk tugas berikutnya.

#### Tugas 2:  Buat kelompok keamanan jaringan dan tetapkan antarmuka jaringan VM untuk NSG.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Pada pojok kiri atas halaman, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger), lalu klik **All Services**.
1. Di Kotak layanan filter di sebelah yang bertuliskan Semua layanan, masukkan **Network security groups**, kemudian dari hasil tersebut, klik **Network security groups** (jangan memilih Kelompok keamanan jaringan klasik).
1. Dari bagian atas halaman Kelompok keamanan jaringan, pilih **+ Create**.
1. Pada tab basics dari bilah Create network security groups, tentukan pengaturan berikut.
    1. Langganan:  Azure Pass – Sponsorship

    1. Grup sumber daya:  **LabsSC900**
    1. Nama:  **NSG-SC900**
    1. Kawasan:  biarkan default **(US) East US**
    1. Pilih **Review + create**, lalu pilih **Create**.
1. Setelah penyebaran selesai, klik **Go to resource**.
1. Perhatikan aturan masuk dan keluar secara default di NSG.  Meskipun NSG sudah membuat dan ada aturan default untuk memfilter lalu lintas, tidak ada antarmuka yang pernah dikaitkan dengan NSG, jadi VM masih rentan dengan semua port-nya yang terekspos ke internet publik.
1. Dari panel navigasi kiri pada halaman NSG-SC900, di bawah Pengaturan, pilih **Network interfaces**.
1. Klik **+ Associate**, di atas kotak pencarian.
1. Di halaman antarmuka jaringan kaitan, klik **sc900-winvmXXX** (XXX akan menjadi antarmuka jaringan VM Anda).  Saat antarmuka sedang dikaitkan, Anda akan melihat kotak notifikasi di pojok kanan atas layar.
1. Setelah antarmuka dikaitkan ke NSG, antarmuka akan muncul di daftar.
1. Dengan antarmuka VM yang dikaitkan dengan kelompok keamanan jaringan dan aturan NSG default, upaya apa pun untuk menghubungkan ke VM akan gagal.  
1. Di pojok kiri atas halaman, klik **All services**, kemudian di bawah yang bertuliskan unggulan, klik **Virtual Machines**.
1. Dari halaman Komputer Virtual, pilih **SC900-WinVM**.
1. Dari bagian atas halaman **SC900-WinVM**, pilih **Connect**, lalu pilih **RDP**.
1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
1. Buka file yang diunduh dan klik **Connect**.
1. Setelah beberapa detik mencoba untuk terhubung, Anda akan melihat pesan gagal, itu menunjukkan bahwa Dekstop jarak jauh tidak dapat terhubung ke komputer jarak jauh.  Klik **OK**.

#### Tugas 3: Di tugas ini, Anda akan membuat aturan NSG untuk mengizinkan lalu lintas masuk menggunakan RDP di port 3389.  Anda akan menguji aturan tersebut dengan mencoba terhubung ke VM menggunakan RDP. 

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Dari panel navigasi kiri, di bawah Pengaturan, pilih **Networking**.
1. Dengan aturan tab port masuk yang dipilih, Anda melihat aturan masuk default. Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Dari bagian kanan halaman, klik **Add inbound port rule**:
1. Di halaman aturan keamanan masuk, tentukan pengaturan berikut:
    1. Sumber:  **Any**

    1. Rentang port sumber: *
    1. Tujuan:  **Any**
    1. Layanan:  **RDP**
    1. Tindakan:  **Allow**
    1. Prioritas:  **300**; Catatan: aturan dengan angka lebih rendah memiliki prioritas lebih tinggi dan diproses terlebih dahulu.
    1. Nama:  **AllowRDP**
1. Pilih **Add**
1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan masuk.
1. Sekarang pastikan Anda dapat terhubung ke VM menggunakan RDP.  Pilih **Connect** dari panel navigasi kiri.
1. Verifikasi alamat IP diatur ke alamat IP Publik, biarkan nomor port default dan pilih **Download DRP file**.
1. Buka file yang diunduh dan klik **Connect**.
1. Anda akan diminta kredensial Anda.  Untuk Nama Pengguna, masukkan **AzureUser**.  Untuk Kata Sandi, masukkan **SC900AzureLabs**.
1. Sebuah jendela koneksi Desktop Jarak Jauh akan terbuka itu menunjukkan bahwa identitas komputer jarak jauh tidak bisa diverifikasikan.  Apakah Anda yakin ingin tetap terhubung?  Pilih **Yes**.
1. Sekarang Anda terhubung ke VM. Dalam kasus ini, Anda dapat terhubung ke VM karena aturan lalu lintas masuk yang Anda buat mengizinkan lalu lintas masuk ke VM lewat RDP.
1. Biarkan VM terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### Tugas 4:  Aturan keluar default untuk NSG mengizinkan lalu lintas internet keluar sehingga Anda harus memvalidasi bahwa Anda dapat terhubung ke internet.  Anda harus melewati proses membuat aturan keluar khusus untuk memblokir lalu lintas internet keluar dan menguji aturan tersebut.

1. Dari VM, klik **Edge** untuk membuka browser.  
1. Masukkan **https://www.bing.com** di bilah alamat browser dan pastikan Anda dapat terhubung ke mesin pencarian.
1. Tutup browser di VM Anda, tetapi biarkan VM terbuka, karena Anda akan memerlukannya di langkah berikutnya.
1. Kembali ke Portal Azure, buka Tab Microsoft Azure – SC900-WinVM di browser Anda.
1. Dari panel navigasi kiri, di bawah Pengaturan, pilih **Networking**.
1. Klik tab **Outbound port rules**.  Anda akan melihat aturan keluar default.  Catat aturan default "AllowInternetOutBound". Aturan ini mengizinkan semua lalu lintas internet keluar. Anda tidak dapat menghapus aturan default, tetapi Anda dapat menggantinya dengan membuat aturan dengan prioritas yang lebih tinggi. Di bagian kanan halaman, klik **Add outbound port rule**.
1. Di halaman Tambahkan aturan keamanan keluar, tentukan pengaturan berikut:
    1. Sumber:  **Any**

    1. Rentang port sumber:  *
    1. Tujuan:  **Service Tag**
    1. Tag layanan tujuan  **Internet**
    1. Layanan:  **Custom** (biarkan default)
    1. Rentang pelabuhan tujuan:  * (pastikan ada asterisk di bidang rentang port tujuan)
    1. Protokol: **Any**
    1. Tindakan: **Deny**
    1. Prioritas:  **4000**
    1. Nama:  **DenyInternet**
1. Pilih **Add**
1. Setelah aturan ditetapkan, aturan itu akan muncul di daftar aturan keluar.  Meskipun aturan muncul di daftar, perlu beberapa menit untuk diterapkan (tunggu beberapa menit sebelum melanjutkan ke langkah berikutnya).  
1. Kembali ke VM Anda.
1. Buka browser Edge di VM Anda, lalu masukkan **https://www.bing.com**.  Halaman semestinya tidak ditampilkan.  Catatan: jika Anda dapat terhubung ke internet dan Anda telah memverifikasi bahwa semua parameter aturan keluar telah diatur dengan benar, kemungkinan karena aturan tersebut memerlukan waktu beberapa menit untuk diterapkan.  Tutup browser, tunggu beberapa menit, dan coba lagi.
1. Tutup koneksi desktop jarak jauh, dengan mengeklik **X** di bagian tengah atas halaman tempat alamat IP ditampilkan.  Jendela pop-up menunjukkan Sesi jarak jauh Anda akan terputus. Klik **OK**.
1. Di tugas ini, Anda berhasil mengonfigurasi aturan keluar di NSG Anda, serta memblokir lalu lintas internet keluar.

#### Tugas 5:  PENTING: Dalam tugas ini, Anda akan menghapus grup sumber daya dan semua sumber daya yang ada di dalamnya.   Ini penting untuk menghindari biaya tambahan.

1. Buka Tab SC900-WinVM – Microsoft Azure di browser Anda.

1. Dari sudut kiri atas halaman, pilih **All Services**.
1. Di kotak Filter layanan di sebelah tulisan Semua layanan, masukkan **Resource groups** lalu dari hasil tersebut, pilih **Resource groups**.
1. Klik **LabsSC900**.
1. Di bagian tengah atas halaman LabsSC900, klik **Delete resource group**.
1. DI jendela yang terbuka, masukkan nama grup sumber daya **LabsSC900**, untuk konfirmasi penghapusan grup sumber daya dan semua sumber daya di dalamnya, lalu klik **Delete** di bagian bawah halaman.
1. Mungkin perlu beberapa menit agar semua sumber daya dan grup sumber daya terhapus.

#### Tinjauan

Di lab ini, Anda sudah mempelajari proses pengaturan VM yang disertai atau tidak disertai kelompok keamanan jaringan (NSG) dan melihat hasil aturan NSG default.  Anda juga sudah mempelajari proses pembuatan aturan NSG.