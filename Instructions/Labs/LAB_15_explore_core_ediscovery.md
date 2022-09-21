---
ms.openlocfilehash: 430bb5ab95d4abaa73eb4aa02372b21fdbb768df
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892664"
---
<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi alur kerja eDiscovery (Standar) ' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 5: Menjelaskan kemampuan eDiscovery dan audit Microsoft Purview; Pelajaran 2: Menjelaskan solusi eDiscovery di Microsoft 365'
---
--->

# <a name="lab-explore-the-ediscovery-standard-workflow"></a>Lab: Jelajahi alur kerja eDiscovery (Standar)

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan eDiscovery dan kemampuan audit Microsoft Purview
- Pelajaran: Menjelaskan solusi eDiscovery di Microsoft 365

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda akan melalui langkah-langkah yang diperlukan untuk menyiapkan eDiscovery, kemudian melalui alur kerja eDiscovery (Standar), dengan membuat penangguhan eDiscovery, membuat kueri pencarian, lalu mengekspor hasil pencarian.  Catatan:  Lisensi untuk eDiscovery (Standar) memerlukan langganan organisasi yang sesuai dan lisensi per pengguna. Jika Anda tidak yakin lisensi mana yang mendukung eDiscovery (Standar), kunjungi [Memulai eDiscovery (Standar) di Microsoft Purview](https://docs.microsoft.com/microsoft-365/compliance/get-started-core-ediscovery?view=o365-worldwide).

**Perkiraan Waktu**: 20-25 menit

### <a name="task-1"></a>Tugas 1

Untuk mengakses eDiscovery (Standar) atau agar ditambahkan sebagai anggota kasus eDiscovery, pengguna harus diberi izin yang sesuai. Dalam tugas ini, Anda sebagai admin global akan menambahkan pengguna tertentu sebagai anggota grup peran Manajer eDiscovery.

 Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi kiri, pilih **Izin**.

1. Dari halaman Izin & peran, di bagian portal Kepatuhan, pilih **Peran**.

1. Di bidang pencarian, masukkan **eDiscovery** lalu pilih ikon pencarian (kaca pembesar).  Pilih **eDiscovery Manager**.

1. Di jendela yang terbuka, perhatikan bagaimana ada dua subgrup, Manajer eDiscovery dan Administrator eDiscovery.  Baca deskripsi masing-masing.  Untuk lab ini, kita akan menambahkan anggota ke subgrup Administrator eDiscovery. Pilih **Edit**, di samping Administrator eDiscovery.  Sebagai praktik terbaik secara umum, pengguna akan diberi hak istimewa paling sedikit yang diperlukan untuk peran mereka.

1. Untuk menambahkan anggota ke grup peran ini, pastikan Anda berada di tab **Choose eDiscovery Administrator**, lalu pilih **Choose eDiscovery Administrator**.

1. Pilih **+ Add** dari bagian atas halaman.

1. Dari daftar nama, pilih **MOD Administrator**, **Megan Bowen**, lalu pilih **Add** di bagian bawah halaman, lalu pilih **Selesai** di bagian bawah halaman.

1. Verifikasi anggota yang ditambahkan sudah benar, lalu pilih **Save**.

1. Dari bagian bawah jendela eDiscovery, pilih **Close**.

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda, sebagai Administrator eDiscovery (admin MOD adalah administrator eDiscovery), akan membuat kasus untuk mulai menggunakan eDiscovery (Standar).

1. Anda harus tetap berada di halaman peran portal kepatuhan. Jika Anda menutup tab browser dari tugas sebelumnya, buka tab browser baru dan masukkan **compliance.microsoft.com**

1. Dari panel navigasi sebelah kiri, di bagian Solusi, pilih **eDiscovery** lalu pilih **Standar**.

1. Dari bagian atas halaman eDiscovery (Standar), pilih **+ Buat kasus**.

1. Di jendela Kasus baru, masukkan nama Kasus, **SC900 Test Case**, lalu pilih **Save** di bagian bawah halaman.

1. Kasus ini sekarang akan muncul dalam daftar.

1. Sebagai pembuat kasus dan karena Anda memiliki hak istimewa Administrator eDiscovery, Anda dapat mulai bekerja dengannya.  

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### <a name="task-3"></a>Tugas 3

Sekarang setelah membuat kasus eDiscovery (Standar), Anda dapat mulai bekerja dengan kasus.  Dalam tugas ini, Anda akan membuat penangguhan eDiscovery untuk kasus yang baru saja Anda buat.  Secara khusus, Anda akan membuat penangguhan untuk kotak surat pertukaran milik Adele Vance.

1. Buka tab eDiscovery (Standar) di browser Anda.

1. Dari halaman eDiscovery (Standar), pilih kasus yang Anda buat di tab sebelumnya, **Kasus Pengujian SC900**.

1. Dari halaman Beranda kasus, pilih tab **Hold**, lalu pilih **+Create**.

1. Di bidang nama, masukkan **Test hold**, lalu pilih NeXT.

1. Di halaman Pilih lokasi, pilih sakelar pengalih di samping **Kotak surat Exchange** untuk mengatur status ke **Aktif**, pilih **Pilih pengguna, grup, atau tim**.  Di kotak pencarian, masukkan **Adele**, lalu tekan enter di keyboard. Dari hasil pencarian pilih **Adele Vance**, lalu klik Pilih, kemudian pilih **Done**.

1. Dari halaman Pilih lokasi, pilih **Next**.  Untuk kemanfaatan dengan lab, tidak ada lokasi lain yang akan disertakan dalam penangguhan ini.

1. Halaman Kondisi kueri memungkinkan Anda membuat penangguhan, berdasarkan Kata Kunci atau Kondisi tertentu yang dipenuhi, pilih **+Conditions** untuk melihat opsi yang tersedia.  Pilih **Selanjutnya**. Tanpa kondisi apa pun, penangguhan akan mempertahankan semua konten di lokasi yang ditentukan.

1. Tinjau pengaturan Anda dan pilih **Submit**, mungkin perlu satu menit, lalu pilih **Done**.  Penangguhan Test akan muncul di daftar.  Jika Anda tidak langsung melihatnya, pilih **Refresh**

1. Biarkan tab browser ini tetap terbuka, karena Anda akan menggunakannya dalam tugas berikutnya.

### <a name="task-4"></a>Tugas 4

Di penangguhan, Anda akan membuat kueri pencarian.  Setelah pencarian selesai, Anda akan mengekspor dan mengunduh hasilnya untuk penyelidikan di masa mendatang.   Catatan:  Pencarian yang terkait dengan kasus eDiscovery (Standar) tidak terdaftar di halaman pencarian konten di portal kepatuhan Microsoft Purview. Pencarian ini hanya terdaftar di halaman Pencarian dari kasus eDiscovery (Standar) terkait.

1. Buka tab Uji kasus SC900 di browser Anda.

1. Dari halaman Penangguhan kasus, pilih **Searches**.

1. Dari halaman Pencarian, pilih **+ New Search**.

1. Di bidang Nama, masukkan **Test Hold – Sales Search**, lalu pilih **Next** dari bagian bawah halaman.

1. Di halaman Pilih lokasi, pilih **lokasi yang ditangguhkan** dan batalkan pilihan **Tambahkan Konten Aplikasi untuk pengguna Lokal**, karena lingkungan lab Anda tidak memiliki pengguna lokal, lalu pilih **Berikutnya** .

1. Halaman kondisi kueri memungkinkan Anda membuat pencarian, berdasarkan Kata Kunci atau Ketentuan tertentu yang dipenuhi. Di bidang kata kunci masukkan **Sales**, pilih **Next**.

1. Tinjau pengaturan Anda dan pilih **Submit**, mungkin perlu satu menit, lalu pilih **Done**.  Pencarian akan muncul di daftar.  Jika Anda tidak langsung melihatnya, pilih **Refresh**

1. Dari jendela Pencarian, pilih pencarian yang baru saja Anda buat, **Test Hold - Sales Search**.  Jendela yang terbuka dengan tab Ringkasan dipilih.  Setelah pencarian selesai, status akan menunjukkan bahwa pencarian selesai.  Anda akan melihat tab Statistik pencarian (jika Anda tidak melihat tab Statistik pencarian, pencarian mungkin masih berjalan dan mungkin memerlukan beberapa menit untuk diselesaikan).  Pilih tab **Search statistics** dan pilih menu tarik-turun di samping Konten pencarian.  Anda juga dapat melihat informasi selengkapnya untuk laporan Kondisi dan Lokasi teratas.  

1. Dari bagian bawah halaman, pilih **Actions**.  Perhatikan opsi yang tersedia, lalu pilih **Export results**.

    1. Dari jendela hasil Ekspor, biarkan default dan pilih **Export** dari bagian bawah halaman. Anda akan secara otomatis kembali ke jendela “Test Hold - Sasles search". Pilih **tutup** di bagian bawah halaman.

    1. Dari SC900-Uji kasus, pilih **Ekspor** dari bagian atas halaman.
    1. Pilih **Test Hold - Sales Search_Export**
    1. Di jendela yang terbuka, “Uji Penangguhan - Ekspor Pencarian Penjualan”, Anda akan melihat tombol Ekspor, pilih **Copy to clipboard**.
    1. Dari bagian atas jendela, pilih **Download results**. Halaman browser baru terbuka dan jendela pop-up ditampilkan menanyakan apakah Anda ingin membuka file ini, pilih **Open**.
    1. Jika ini adalah pertama kalinya Anda mengunduh konten pencarian, Anda akan diminta untuk menginstal alat Ekspor eDiscovery Microsoft Office 365.  Pilih **Pasang**.
    1. Setelah penginstalan selesai, jendela alat ekspor eDiscovery terbuka.  Di bidang pertama, tempel kunci ekspor yang Anda salin ke clipboard, tempelkan sekarang (Kontrol V pada keyboard atau klik kanan pada mouse dan pilih tempel).
    1. Di bidang kedua, pilih lokasi tempat Anda ingin menyimpan file ekspor, lalu pilih **Start**.  Setelah proses pengunduhan selesai, pilih **Close** dan tutup tab browser ini.
    1. Anda kembali ke jendela “Uji Penangguhan - Ekspor Pencarian Penjualan".  Pilih **Tutup**.
    1. Periksa lokasi unduhan Anda untuk memverifikasi unduhan berhasil diselesaikan.

1. Tutup semua tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda telah melalui langkah-langkah yang diperlukan untuk memulai eDiscovery (Standar), termasuk menyiapkan izin peran untuk eDiscovery dan membuat kasus eDiscovery.  Dengan kasus, Anda telah melalui alur kerja eDiscovery (Standar), dengan membuat penangguhan eDiscovery, membuat kueri pencarian, lalu mengekspor hasil pencarian untuk menggunakan penyelidikan lebih lanjut.
