---
lab:
    title: 'Mempelajari Azure Policy'
    modul: 'Modul 4 Pelajaran 5: Menjelaskan kemampuan solusi kepatuhan Microsoft: Menjelaskan Azure Policy'
---


# Lab: Mempelajari Azure Policy

## Skenario lab
Azure Policy membantu menegakkan standar organisasi dan menilai kepatuhan dalam skala besar. Azure Policy mengevaluasi sumber daya di Azure dengan membandingkan properti sumber daya tersebut dengan aturan bisnis. Di lab ini, Anda akan mulai dengan mempelajari halaman arahan Azure policy. Setelah pembelajaran awal halaman Azure policy, Anda akan membuat kebijakan dan melihat dampak dari kebijakan tersebut.


**Perkiraan Waktu**: 20-25 menit

#### Tugas 1: Menjelajahi halaman kebijakan Azure secara singkat.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    
    1. Masukkan kata sandi admin yang harus disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Sekarang Anda berada di Portal Microsoft Azure.  Di kotak pencarian, di bilah biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **policy**, kemudian pilih **Policy** dari hasil pencarian. Ini membuka halaman beranda Kebijakan yang menyediakan tampilan dasbor.  Cakupan informasi yang Anda lihat menerapkan Azure Pass yang digunakan, sebagai bagian dari lab ini.   Perhatikan informasi yang tersedia di dasbor.

1. Terdapat sebuah item bernama ASC Default (ASC mengacu pada Azure Security Center yang kini disebut Pertahanan Microsoft untuk Cloud) yang cakupannya yaitu Azure Pass – Sponsorship.   Pilih **ASC Default**.

1. Di bagian atas halaman, di bagian Essentials, Anda dapat melihat nama, deskripsi, dan informasi penting lainnya.  Baca deskripsi (arahkan kursor ke deskripsi dengan mouse). CATATAN: Bidang deskripsi mereferensikan Azure Security Center yang telah diubah namanya menjadi Pertahanan Microsoft untuk Cloud.

1. Perhatikan informasi yang disediakan oleh dasbor yang diperbarui untuk mencerminkan item yang dipilih, definisi inisiatif ASC Default.  Harap diingat bahwa definisi inisiatif adalah kumpulan definisi kebijakan yang disesuaikan untuk mencapai tujuan tunggal yang menyeluruh. Informasi dapat dilihat menurut grup, kebijakan, sumber daya yang tidak sesuai, atau kejadian.

1. Keluar dari halaman ASC dan kembali ke halaman beranda Kebijakan dengan memilih **X** di pojok kanan atas jendela.

1. Dari panel navigasi sebelah kiri, pilih **Getting started**.  Di sini, Anda dapat melihat berbagai opsi termasuk opsi untuk menelusuri kebijakan bawaan dan menetapkan kebijakan dalam skala besar, Anda dapat membuat definisi kebijakan khusus untuk lingkungan Anda, merekomendasikan penetapan kebijakan, dan banyak lagi.

1. Dari panel navigasi sebelah kiri, pilih **Compliance**.  Sama seperti halaman ringkasan, di sini Anda dapat melihat status kepatuhan dari kebijakan dan/atau inisiatif yang tercantum.  Dari halaman Kepatuhan Kebijakan, Anda juga dapat menetapkan kebijakan atau inisiatif (Anda akan menetapkan kebijakan di tugas berikutnya).

1. Dari panel navigasi sebelah kiri, pilih **Remediation**.  Halaman ini menyediakan daftar kebijakan yang memiliki sumber daya yang tidak sesuai.  Dengan memilih kebijakan di halaman remediasi, Anda dapat memicu pembuatan tugas untuk meremediasi kebijakan.  

1. Dari panel navigasi sebelah kiri, di bagian penulisan, pilih **Assignments**.  Dari sini, Anda dapat melihat penetapan kebijakan dan/atau inisiatif saat ini serta Anda dapat membuat penetapan atau inisiatif kebijakan.  Anda akan kembali lagi di tugas berikutnya.  

1. Dari panel navigasi sebelah kiri, pilih **Definitions**.  Dari halaman ini, pilih **Audit machines with insecure password security setting**.  Ini adalah definisi inisiatif, yang mencakup banyak kebijakan.  Untuk melihat seperti apa definisi kebijakan, pilih **Audit Windows machines that do not have a maximum password age of 70 days**.  Saat halaman terbuka, Anda akan melihat definisi kebijakan aktual dalam struktur Java Script Object Notation (JSON).   Seperti yang Anda lihat dari teks berwarna merah, definisi kebijakan berisi elemen yang menentukan nama tampilan, deskripsi, parameter, aturan kebijakan, dan banyak lagi. JANGAN MENGUBAH APA PUN.  

1. Keluar dari halaman Definisi kebijakan, dengan memilih **X** di sudut kanan atas halaman.

1. Keluar dari halaman Definisi inisiatif, dengan memilih **X** di sudut kanan atas halaman.

1. Biarkan tab browser ini (Policy – Microsoft Azure) terbuka untuk tugas berikutnya.

#### Tugas 2:  Dalam tugas ini, Anda akan membuat penetapan kebijakan dasar untuk mewajibkan tag pada grup sumber daya.

1. Buka tab browser, Policy – Microsoft Azure.

1. Bentuk panel navigasi kiri, di bawah Penulisan, pilih **Assignments**.

1. Dari bagian atas halaman, pilih **Assign policy**.

1. Wizard Tetapkan kebijakan terbuka untuk memandu admin dalam proses menetapkan kebijakan.  Di samping bidang Definisi kebijakan, pilih **ellipses**.  Muncul daftar definisi kebijakan yang tersedia.  

1. Di bilah pencarian, masukkan, **Tag**.

1. Dari hasil pencarian, pilih **Require a tag on resource group** (Anda mungkin perlu menggulir ke bawah), kemudian tekan **Select**.  Catatan: efek dari kebijakan ini adalah Menolak pembuatan grup sumber daya baru yang tidak memenuhi persyaratan.  

1. Perhatikan nama tugas default.  Biarkan nama apa adanya dan dari bagian bawah halaman, pilih **Next**.

1. Di bidang Nama tag, masukkan **Environment**, lalu pilih **Next**.  

1. Dalam pesan ketidakpatuhan, masukkan **An environment tag is required**, kemudian pilih **Next**. Catatan: pesan ini akan muncul sebagai alasan ketidakpatuhan untuk grup sumber daya yang dibuat sebelum penetapan kebijakan dan tidak memiliki tag Lingkungan.  Untuk grup sumber daya yang dibuat setelah kebijakan dibuat, pembuatan grup sumber daya akan ditolak jika tidak ada tag lingkungan.

1. Tinjau penetapan kebijakan, lalu pilih Create.  Jika Anda tidak segera melihat kebijakan, pilih **Refresh**. Catatan: Mungkin perlu waktu hingga 30 menit agar kebijakan diterapkan.

1. Keluar dari halaman Penetapan kebijakan dengan memilih **X** di sudut kanan atas layar.

1. Sekarang Anda berada di halaman beranda layanan Azure.  Biarkan halaman ini tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

#### Tugas 3:  Dalam tugas ini, Anda akan melihat dampak penetapan kebijakan Azure, dengan membuat grup sumber daya di Azure yang tidak memiliki tag, maka Anda akan melihat pembaharuan grup sumber daya yang menyertakan tag.  Catatan: Mungkin perlu waktu hingga 30 menit agar kebijakan yang dibuat di tugas sebelumnya diterapkan, tetapi biasanya terjadi lebih cepat.

1. Buka tab browser, Home – Microsoft Azure.

1. Dari bagian atas halaman, di bawah teks tertulis Layanan Azure, pilih **Resource groups**.

1. Dari sudut kiri atas halaman, pilih **+ Create**.

1. Dari tab Dasar grup untuk Membuat sumber daya, biarkan bidang Langganan apa adanya, Azure Pass - Sponsorship.

1. Di bidang grup Sumber daya, masukkan, **SC900-Labs**.

1. Biarkan pengaturan Wilayah tetap default, lalu pilih **Next: Tags**.

1. Biarkan bidang tag Nama dan Nilai kosong.  JANGAN DIPOPULASIKAN, lalu pilih **Review + create**.

1. Anda akan melihat bahwa telah tervalidasi (nama dan nilai tag bukan bidang wajib di wizard), lalu pilih **Create**.

1. Anda akan melihat pesan kegagalan di bagian atas layar, “Failed to create the resource group. View error details”.  Pilih **View error details**. Kondisi yang merupakan bagian dari kebijakan Azure tidak terpenuhi sehingga pembuatan grup sumber daya diblokir, karena ketidakpatuhan. Catatan: Jika Anda tidak melihat pesan kegagalan dan grup sumber daya yang telah dibuat, hal itu karena kebijakan belum diterapkan.  Buka halaman Kebijakan untuk kebijakan yang Anda buat di tugas sebelumnya dan setelah kebijakan diterapkan, Anda akan melihat bahwa sumber daya tidak sesuai.  Halaman detail akan menyertakan pesan ketidakpatuhan.

1. Ringkasan kesalahan menunjukkan jenis kesalahan, "Resource ‘SC900-Labs’ was disallowed by policy."  Tutup jendela ini dengan memilih **X** di sudut kiri atas layar.

1. Dari jendela Buat grup sumber daya, pilih **<Previous**.

1. Anda kembali ke halaman Tag untuk Buat grup sumber daya.  Di bidang Nama masukkan Lingkungan dan di bidang Nilai, SC900-Labs, lalu pilih **Next: Review + Create >**.

1. Verifikasi tag dan pilih **Create**.

1. Anda akan melihat grup sumber daya yang terdaftar.  Karena tag disediakan di grup sumber daya, kondisi yang disertakan sebagai bagian dari kebijakan Azure telah terpenuhi.  Grup sumber daya mematuhi kebijakan.

1. Sebelum Anda keluar, hapus Azure policy.
    1. Dari sudut kiri atas halaman, pilih Beranda, untuk kembali ke halaman beranda Azure.
    
    1. Di bawah teks tertulis layanan Azure, pilih Azure policy.
    1. Di bagian tengah halaman, Anda akan melihat daftar penetapan tugas Azure policy.  Pilih elipsis untuk penetapan kebijakan yang Memerlukan tag pada grup sumber daya, lalu pilih Delete assignment.
    1. Anda akan diminta untuk mengonfirmasi bahwa Anda ingin menghapus tugas.  Pilih Yes.


#### Tinjauan

Di lab ini, Anda telah membuka halaman arahan Azure policy. Setelah mempelajari awal halaman Azure policy, Anda telah menjalani proses pembuatan kebijakan dan Anda telah dapat melihat dampak dari kebijakan tersebut.