---
lab:
  title: Mempelajari label sensitivitas di Microsoft Purview
  module: 'Module 4 Lesson 3: Describe the capabilities of Microsoft compliance solutions: Describe information protection and data lifecycle management of Microsoft Purview'
ms.openlocfilehash: 3d69459ebcd4ffa34bd71997ea86a8aeae4d0774
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557590"
---
# <a name="lab-explore-sensitivity-labels-in-microsoft-purview"></a>Lab: Mempelajari label sensitivitas di Microsoft Purview

## <a name="lab-scenario"></a>Skenario lab

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.

**Perkiraan Waktu**: 20-25 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini, Anda akan memperoleh pemahaman tentang hal yang dapat dilakukan oleh label sensitivitas dengan menelusuri pengaturan untuk label sensitivitas yang sudah ada, yang telah dibuat dan kebijakan terkait untuk menerbitkan label.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka pada halaman selamat datang di portal kepatuhan Microsoft Purview.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Information protection**.

1. Pilih tab **Label** dari bagian atas halaman.

1. Kotak informasi berwarna kuning yang ditampilkan yang menunjukkan, "Organisasi Anda belum mengaktifkan kemampuan untuk memproses konten di file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint..."  Pilih **Aktifkan sekarang**.  Setelah melakukan ini, mungkin ada penundaan untuk menyebarkan pengaturan melalui sistem.** **

1. Di tengah halaman, perhatikan bahwa ada label yang sudah dibuat.  Pilih **Confidential - Finance**.  Jendela terbuka yang memberikan informasi tentang label ini.  Perhatikan bagaimana label ini diatur untuk mendukung enkripsi dan penandaan konten.  Pilih Edit Label di bagian atas halaman untuk melihat beberapa pengaturan konfigurasi dasar.

1. Konfigurasi dimulai dengan memberikan nama dan deskripsi untuk label Anda.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Perhatikan cakupan untuk label ini.  Cakupan diatur ke File & email tempat Anda dapat mengonfigurasi Enkripsi dan pengaturan penandaan konten untuk melindungi email berlabel dan file kantor.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Untuk cakupan yang dipilih, File & email, Anda dapat mengonfigurasi untuk mengenkripsi dan/atau menandai konten.  Perhatikan bagaimana pengaturan perlindungan file dan email diatur untuk enkripsi dan penandaan konten file.  Tinjau definisi masing-masing.  Jangan mengubah apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela Enkripsi menunjukkan konfigurasi untuk pengaturan enkripsi.  Jangan mengubah apa pun.  Tinjau kotak informasi di bagian Konfigurasi pengaturan enkripsi dan tinjau pengaturan yang dikonfigurasi. Perhatikan bagaimana akses pengguna ke konten diatur untuk tidak pernah kedaluwarsa.  Anda juga dapat menetapkan izin untuk pengguna dan grup tertentu sehingga hanya mereka yang dapat berinteraksi dengan konten yang menerapkan label ini.  Di bagian pengguna dan grup, penyewa ditentukan sehingga semua pengguna di penyewa Anda dapat melihat konten yang memiliki label ini.  Tim keuangan juga terdaftar dan mereka memiliki izin penulis bersama.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Pada halaman penandaan konten, perhatikan kotak informasi di bagian atas halaman.  Penandaan konten akan diterapkan ke dokumen tetapi hanya header dan footer yang akan diterapkan ke pesan email. Dengan kata lain, marka air tidak diterapkan pada email.  Penandaan konten yang terkait dengan label ini adalah marka air yang bertuliskan, SANGAT RAHASIA.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Sekarang Anda berada di jendela Pelabelan otomatis untuk file dan email.  Baca deskripsi pelabelan otomatis di bagian atas halaman dan kotak informasi di bawahnya.  Perhatikan juga bahwa label ini diatur untuk pelabelan otomatis dalam kondisi tertentu. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Jendela berikutnya menentukan pengaturan perlindungan untuk tim, grup, dan situs yang menerapkan label ini. Ini tidak diaktifkan, pilih **Next** di bagian bawah halaman.

1. Jendela berikutnya adalah fitur pratinjau untuk menerapkan label ini ke kolom database Azure (seperti SQL, Synapse, dan lainnya) yang berisi tipe info sensitif yang Anda pilih secara otomatis.  Fitur ini tidak diaktifkan. Pilih **Cancel** di bagian bawah halaman untuk keluar dari wizard konfigurasi label dan kembali ke halaman Proteksi Informasi.

1. Dari bagian atas halaman Perlindungan Informasi, pilih **Label policies**.  Melalui kebijakan label, label sensitivitas dapat diterbitkan.  

1. Pilih **Confidential-Finance Policy**.  Jendela terbuka yang memberikan informasi tentang kebijakan tersebut.  Kebijakan ini berfungsi untuk menerbitkan label Kebijakan Keuangan Rahasia dan melindungi data yang berisi data keuangan untuk Contoso.  Perhatikan juga bagaimana kebijakan ini diterbitkan kepada semua orang.  

1. Pilih **Edit** kebijakan dari bagian atas jendela.

1. Baca deskripsi di bagian “Pilih label sensitivitas yang akan diterbitkan”.  Perhatikan label yang tertera.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Baca deskripsi di bagian “Terbitkan ke pengguna dan grup”.  Perhatikan label ini tersedia untuk semua pengguna.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Meninjau pengaturan kebijakan.  Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah, "Terapkan label default ke dokumen."  Perhatikan bahwa tidak ada label default. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah, "Terapkan label default ke email."  Pilih panah tarik-turun di kotak input, untuk melihat opsi yang tersedia. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.
    1. Baca deskripsi di bawah, "Terapkan label default ke konten Power BI."  Perhatikan bahwa tidak ada label default. Jangan mengubah pengaturan apa pun.  Pilih **Next** di bagian bawah halaman.

1. Opsi konfigurasi terakhir adalah memberi nama kebijakan Anda.  Jangan mengubah pengaturan apa pun.  Pilih **Cancel** di bagian bawah halaman untuk keluar dari konfigurasi kebijakan dan kembali ke halaman Proteksi informasi.

1. Dari halaman Perlindungan informasi, pilih Pelabelan otomatis.  Perhatikan bahwa tidak ada kebijakan pelabelan otomatis yang dikonfigurasi.  Jangan mengubah pengaturan apa pun.  Jika Anda bertanya-tanya mengapa tidak ada kebijakan di sini, mengingat konfigurasi label diatur ke pelabelan otomatis untuk file dan email, kembali ke langkah-langkah di mana Anda dipandu melalui pengaturan konfigurasi label dan meninjau deskripsi dan kotak informasi terkait pelabelan otomatis untuk file dan email.  Petunjuk:  Di tab pelabelan otomatis untuk lab sensitivitas, tertulis  “Untuk menerapkan label ini ke file yang sudah disimpan secara otomatis (di SharePoint dan OneDrive) atau email yang sudah diproses oleh Exchange, Anda harus membuat kebijakan pelabelan otomatis."

1. Dari panel navigasi sebelah kiri, pilih Beranda untuk kembali ke portal kepatuhan Microsoft Purview.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini, Anda akan melalui proses penerapan label dari sudut pandang pengguna (dalam hal ini, pengguna adalah admin) dan melihat penandaan konten yang dihasilkan oleh label.

1. Dari beranda pusat kepatuhan Microsoft 365, pilih **ikon peluncur aplikasi**, di sebelah bagian yang tertulis Contoso Electronics. **klik kanan ikon Word** dan pilih **Buka di tab baru**.  

1. Pilih **+ New blank document**, kemudian masukkan beberapa teks pada halaman.  Pada bilah berwarna biru di bagian atas halaman, pilih panah bawah, di sebelahnya tertulis DocumenXX - Tersimpan, dan di kotak Nama File masukkan, **Test-label**.

1. Dari bilah menu atas, pilih **Sensitivity**, jika Anda tidak langsung melihat opsi ini, segarkan halaman. Dari menu tarik-turun, pilih **Confidential - Finance**.

1. Dari bilah menu atas, pilih **View**, lalu pilih **Reading view**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

### <a name="task-3-optional"></a>Tugas 3 (opsional)

Selain penandaan konten, setelan proteksi label juga disetel untuk enkripsi. Sesuai izin yang dikonfigurasi dengan label ini, anggota grup keuangan dapat menulis bersama dokumen dengan label ini diterapkan dan pengguna di penyewa Contoso dapat melihat dokumen.  Dalam tugas ini, Anda akan mengirim dokumen ini ke alamat email yang dapat Anda akses (yaitu, alamat email pribadi) dan itu BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com dan lihat apa yang terjadi saat Anda mencoba membuka lampiran.

1. Dari halaman beranda portal kepatuhan Microsoft Purview, pilih **ikon peluncur aplikasi**, di samping Contoso Electronics. **klik kanan ikon Outlook** dan pilih **Buka di tab baru**.

1. Pilih **New message** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Lampirkan**.

1. Pilih **Browse cloud locations**.

1. Dari daftar yang muncul, pilih dokumen yang Anda buat dan beri label **Test-label**. Pilih **Next** dan pilih **Attach as a copy**.  Tekan **Kirim**.

1. Dengan menggunakan browser web di Mesin Virtual lab Anda, masuk ke akun email tujuan pengiriman dokumen.  Perhatian, email mungkin diarahkan ke folder sampah Anda.  Saat Anda mencoba membuka file kata terlampir, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen.

1. Tutup tab browser yang terbuka.

### <a name="review"></a>Tinjau

Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda telah mempelajari pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.
