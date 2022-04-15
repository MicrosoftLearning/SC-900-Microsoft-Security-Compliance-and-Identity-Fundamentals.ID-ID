---
lab:
  title: Mempelajari label sensitivitas di Microsoft 365
  module: 'Module 4 Lesson 3: Describe the capabilities of Microsoft compliance solutions: Describe information protection and governance capabilities of Microsoft 365'
ms.openlocfilehash: ab8d44cf92697deb200bf968a1865d328025984b
ms.sourcegitcommit: c14538b208890797642cfe5c35abf6bea45364bf
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/15/2022
ms.locfileid: "142614446"
---
# <a name="lab-explore-sensitivity-labels-in-microsoft-365"></a>Lab: Mempelajari label sensitivitas di Microsoft 365

## <a name="lab-scenario"></a>Skenario lab
Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda akan melalui pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.


**Perkiraan Waktu**: 20-25 menit

#### <a name="task-1-in-this-task-you-will-gain-an-understanding-of-what-sensitivity-labels-can-do-by-going-through-the-settings-for-an-existing-sensitivity-label-that-have-been-created-and-the-corresponding-policy-to-publish-the-label"></a>Tugas 1: Dalam tugas ini, Anda akan memperoleh pemahaman tentang hal yang dapat dilakukan oleh label sensitivitas dengan menelusuri pengaturan untuk label sensitivitas yang sudah ada, yang telah dibuat dan kebijakan terkait untuk menerbitkan label.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Information protection**.

1. Pilih tab **Label** dari bagian atas halaman.

1. Kotak informasi berwarna kuning yang ditampilkan yang menunjukkan, "Organisasi Anda belum mengaktifkan kemampuan untuk memproses konten di file online Office yang memiliki label sensitivitas terenkripsi yang diterapkan dan disimpan di OneDrive dan SharePoint..."  Pilih Turn on now.  Setelah Anda melakukan ini, mungkin akan ada penundaan pada pengaturan untuk menyebar melalui sistem.


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

1. Dari panel navigasi sebelah kiri, pilih Home untuk kembali ke pusat kepatuhan Microsoft 365.

1. Biarkan halaman ini tetap terbuka, Anda akan menggunakannya di tugas berikutnya.


#### <a name="task-2--in-this-task-you-will-go-through-the-process-of-applying-a-label-from-the-perspective-of-the-user-in-this-case-the-user-is-the-admin-and-view-the-content-marking-that-is-generated-by-the-label"></a>Tugas 2:  Dalam tugas ini, Anda akan melalui proses penerapan label dari sudut pandang pengguna (dalam hal ini, pengguna adalah admin) dan melihat penandaan konten yang dihasilkan oleh label.

1. Pertama, pastikan Anda memiliki pengaturan Office di mesin virtual lab (VM) Anda.  Untuk melakukannya, pilih tab **pusat administrator Microsoft 365** yang membuka browser.  Jika sebelumnya Anda menutup tab, buka tab browser baru dan masukkan **admin.microsoft.com**.
    1. Dari panel navigasi kiri, pilih **Tagihan** untuk melihat semua opsi, lalu pilih **Produk Anda**.
    1. Dari halaman produk Anda, pilih **Percobaan Microsoft 365 E5**
    1. Dari halaman Percobaan Microsoft 365 E5, pilih **Unduh dan instal perangkat lunak** dan ikuti instruksi di halaman tersebut.

1. Dari pojok kiri bawah lab Mesin Virtual, pilih ikon Windows, lalu pilih **Word** lalu pilih **Dokumen kosong**.  Dokumen kosong akan membuka dokumen word baru menggunakan Word versi desktop.

1. Dari bilah menu bagian atas, pilih **Sensitivity**. Dari menu tarik-turun, pilih **Confidential - Finance**.

1. Perhatikan bagaimana dokumen menyertakan marka air.  Marka air akan muncul dalam teks kecil berwarna abu-abu terang yang ditampilkan secara vertikal di halaman. 

1. Simpan file Word.

1. Tutup tab Microsoft Word yang terbuka di browser Anda untuk keluar dari Word.

#### <a name="task-3-optional-in-addition-to-content-marking-the-label-protection-setting-was-set-for-encryption-per-the-permissions-that-were-configured-with-this-label-members-of-the-finance-group-can-co-author-documents-with-this-label-applied-and-users-in-the-contoso-tenant-can-view--in-this-task-you-will-send-this-document-to-an-email-address-to-which-you-have-access-ie-a-personal-email-address-and-that-is-not-part-of-the-wwlxzzzzonmicrosoftcom-domain-and-see-what-happens-when-you-try-to-open-the-attachment"></a>Tugas 3 (opsional): Selain penandaan konten, setelan proteksi label juga disetel untuk enkripsi. Sesuai izin yang dikonfigurasi dengan label ini, anggota grup keuangan dapat menulis bersama dokumen dengan label ini diterapkan dan pengguna di penyewa Contoso dapat melihat dokumen.  Dalam tugas ini, Anda akan mengirim dokumen ini ke alamat email yang dapat Anda akses (yaitu, alamat email pribadi) dan itu BUKAN bagian dari domain WWLxZZZZ.OnMicrosoft.com dan lihat apa yang terjadi saat Anda mencoba membuka lampiran.  

1. Dari beranda pusat kepatuhan Microsoft 365, pilih **ikon peluncur aplikasi**, di sebelah bagian yang tertulis Contoso Electronics. **klik kanan ikon Outlook** dan pilih **Buka di tab baru**.

1. Pilih **New message** dari sudut kiri atas layar.  Masukkan alamat email yang dapat Anda akses dan bukan bagian dari domain WWLxZZZZ.OnMicrosoft.com, kemudian masukkan **Test** di baris subjek.

1. Pilih **Lampirkan**.

1. Pilih **Browse cloud locations**.

1. Dari daftar yang muncul, pilih dokumen yang Anda buat dan beri label **Test-label**. Pilih **Next** dan pilih **Attach as a copy**.  Tekan **Kirim**.

1. Dengan menggunakan browser web di Mesin Virtual lab Anda, masuk ke akun email tujuan pengiriman dokumen.  Perhatian, email mungkin diarahkan ke folder sampah Anda.  Saat Anda mencoba membuka file kata terlampir, Anda akan melihat pemberitahuan bahwa Anda tidak memiliki izin untuk membuka dokumen.

1. Tutup tab browser yang terbuka.


#### <a name="review"></a>Tinjau
Di lab ini, Anda telah mempelajari kemampuan label sensitivitas.  Anda telah mempelajari pengaturan untuk label sensitivitas yang telah dibuat dan kebijakan yang sesuai untuk menerbitkan label.   Kemudian Anda telah melihat cara menerapkan label dan dampak dari label tersebut, dari sudut pandang pengguna.