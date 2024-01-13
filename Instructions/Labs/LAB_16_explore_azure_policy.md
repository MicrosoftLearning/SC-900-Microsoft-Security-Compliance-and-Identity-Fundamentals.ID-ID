<!---
---
Lab: Judul: 'Menjelajahi Azure Policy' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 6: Menjelaskan kemampuan tata kelola sumber daya di Azure; Unit 2: Menjelaskan Azure Policy'
---
--->

# Lab: Menjelajahi Azure Policy

Lab ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan kemampuan tata kelola sumber daya di Azure
- Unit: Menjelaskan Azure Policy

## Skenario laboratorium

Azure Policy membantu memberlakukan standar organisasi dan menilai kepatuhan dalam skala besar. Azure Policy mengevaluasi sumber daya di Azure dengan membandingkan properti sumber daya tersebut dengan aturan bisnis. Di lab ini, Anda akan membuat kebijakan dan melihat dampak dari kebijakan tersebut.  Anda juga akan mempelajari informasi kepatuhan dan remediasi yang tersedia di laman kebijakan.

**Perkiraan Waktu**: 15-20 menit

### Tugas 1

Dalam tugas ini, Anda akan membuat penetapan kebijakan dasar untuk mewajibkan tag pada grup sumber daya.
1.  Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin untuk langganan Azure Anda (kredensial admin ini berbeda dengan kredensial admin Microsoft 365).
    1. Di jendela Masuk, masukkan **User1-XXXXXXXX@LODSPRODMSLEARNMCA.onmicrosoft.com** (dengan XXXXXXXX adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Sekarang, Anda berada di portal Microsoft Azure.  Di kotak pencarian, pada bilah berwarna biru di bagian atas laman di samping bagian yang tertulis Microsoft Azure, masukkan **kebijakan**, lalu pilih **Kebijakan** dari hasil pencarian. Tindakan ini akan membuka laman beranda Kebijakan yang menyediakan tampilan dasbor.  Cakupan tampilan Dasbor adalah langganan Azure yang disediakan oleh host lab resmi (ALH). Anda akan melihat kebijakan yang tercantum, ini adalah kebijakan yang dibuat oleh ALH, untuk penggunaan langganan Azure.

1. Dari panel navigasi kiri, di bagian Penulisan, pilih **Tugas**.

1. Dari bagian atas laman, pilih **Tugaskan kebijakan**. Wizard penetapan kebijakan terbuka untuk memandu admin dalam proses penetapan kebijakan.

1. Anda mulai di tab Dasar.
    1. Untuk Cakupan, biarkan pengaturan default. Dalam hal ini, cakupan kebijakan adalah langganan Azure yang disediakan oleh host lab resmi (ALH).
    1. Untuk Definisi Kebijakan, pilih **elipsis**.  Daftar definisi kebijakan yang tersedia telah disediakan.  Di bilah pencarian, masukkan, **Wajibkan tag**. Dari hasil pencarian, pilih **Wajibkan tag pada grup sumber daya** (Anda mungkin perlu menggulir ke bawah), lalu tekan **Tambah**.  Catatan: Efek dari kebijakan ini adalah Menolak pembuatan grup sumber daya baru yang tidak memenuhi persyaratan.  
    1. Perhatikan nama tugas default.  Pertahankan nama apa adanya.
    1. Pastikan Penegakan kebijakan diatur ke **Diaktifkan**

1. Pilih **Berikutnya**, lalu pilih **Berikutnya** lagi untuk berpindah ke tab Parameter (Anda juga bisa memilih tab parameter secara langsung).

1. Sekarang Anda berada di tab Parameter. Di kolom Tag nama, masukkan **Lingkungan**, lalu pilih **Berikutnya**.

1. Di tab Remediasi, biarkan pengaturan default apa adanya, lalu pilih **Berikutnya**.

1. Sekarang berada di tab Pesan ketidakpatuhan. Di bidang pesan ketidakpatuhan, masukkan **Tag lingkungan diperlukan**, lalu pilih **Berikutnya**. Catatan: Pesan ini akan muncul sebagai alasan ketidakpatuhan untuk grup sumber daya yang dibuat sebelum penetapan kebijakan dan tidak memiliki tag Lingkungan.

1. Tinjau penetapan kebijakan, lalu pilih **Buat**.  Jika Anda tidak segera melihat kebijakan, pilih **Refresh**. Catatan: Diperlukan waktu hingga 30 menit agar kebijakan diterapkan, tetapi biasanya lebih cepat.

1. Keluar laman Penugasan Kebijakan dengan memilih **X** di pojok kanan atas layar.

1. Sekarang, Anda berada di laman beranda layanan Azure.  Biarkan halaman ini tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

### Tugas 2

Dalam tugas ini, Anda akan melihat dampak penetapan kebijakan Azure, dengan mencoba membuat grup sumber daya di Azure yang tidak memiliki tag.

1. Buka tab browser, Beranda – Microsoft Azure.

1. Dari bagian atas laman, di bawah yang bertuliskan Layanan Azure, pilih **Grup sumber daya**.

1. Dari pojok kiri atas laman, pilih **+ Buat**.

1. Dari tab Dasar pada Buat grup sumber daya, biarkan bidang Langganan apa adanya.

1. Di bidang Grup sumber daya, masukkan **SC900-Labs**.

1. Biarkan Wilayah diatur ke pengaturan default, lalu pilih **Berikutnya: Tag**.

1. Biarkan bidang Nama dan Nilai tag kosong.  JANGAN MENGISINYA, lalu pilih **Tinjau + buat**.

1. Anda akan melihat pesan validasi lolos (nama tag dan nilai bukan bidang yang wajib diisi dalam wizard), lalu pilih **Buat**.

1. Anda akan melihat pesan kegagalan di bagian atas layar, “Gagal membuat grup sumber daya". Pilih **Lihat detail kesalahan**. Kondisi yang merupakan bagian dari kebijakan Azure tidak terpenuhi sehingga pembuatan grup sumber daya diblokir, karena ketidakpatuhan. Catatan: Jika Anda tidak melihat pesan kegagalan dan grup sumber daya dibuat, itu karena kebijakan belum berlaku.  Buka halaman Kebijakan untuk kebijakan yang Anda buat di tugas sebelumnya dan setelah kebijakan diterapkan, Anda akan melihat bahwa sumber daya tidak sesuai.  Laman detail akan menyertakan pesan ketidakpatuhan.

1. Ringkasan kesalahan menunjukkan jenis kesalahan, "Sumber Daya 'SC900-Labs' tidak diizinkan oleh kebijakan.  Tutup jendela dengan memilih **X** di pojok kanan atas layar.

1. Dari jendela Buat grup sumber daya, pilih **Sebelumnya**.

1. Anda kembali ke halaman Tag untuk Buat grup sumber daya.  Di bidang Nama masukkan Lingkungan dan di bidang Nilai, masukkan **SC900-Labs**, lalu pilih **Berikutnya: Tinjau + Buat >**.

1. Periksa tag dan pilih **Buat**.

1. Di bidang Nama, masukkan **Lingkungan** dan di bidang Nilai, masukkan **Lab** (nilai ini bisa apa saja, kebijakan hanya memerlukan nilai tag), lalu pilih **Berikutnya: Tinjau + Buat >** lalu pilih **Buat**.

1. Anda akan melihat grup sumber daya terdaftar.  

1. Pilih **Beranda** dari bilah alamat di bagian atas laman untuk kembali ke laman beranda Azure.

1. Biarkan tab browser tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

### Tugas 3 (Opsional)

Dalam tugas ini, Anda akan menjalani langkah-langkah untuk memulihkan grup sumber daya yang tidak patuh. CATATAN: Langganan Azure yang digunakan untuk lab akan memerlukan waktu yang lebih lama dari biasanya untuk memperbarui status kepatuhan grup sumber daya yang diperbaiki.

1. Dari laman beranda Azure, pilih **kebijakan**. Tindakan ini akan membuka laman beranda Kebijakan yang menyediakan tampilan dasbor.  Cakupan untuk tampilan Dasbor adalah langganan Azure yang disediakan oleh host lab resmi.  

1. Anda akan melihat kebijakan yang Anda buat sebelumnya, lalu pilih kebijakan tersebut.

1. Di bagian atas halaman, di bawah Esensial, Anda dapat melihat nama, deskripsi, dan informasi penting lainnya.  Perhatikan bahwa kebijakan ditampilkan sebagai tidak patuh.  Pilih kebijakan untuk informasi lebih lanjut tentang mengapa kebijakan tersebut tidak sesuai. Di sini, Anda dapat melihat bahwa sumber daya yang terdaftar sebagai resourgegroup1 tidak sesuai.  Ini adalah contoh grup sumber daya yang telah dibuat, sebelum pembuatan kebijakan. Pilih **Detail** untuk informasi selengkapnya.  Di sini, Anda dapat melihat pesan kepatuhan bahwa tag lingkungan diperlukan.  Pilih **X** di kanan atas untuk menutup jendela.

1. Pilih **resourcegroup1**, lalu dari bagian atas laman, pilih **Lihat Sumber Daya**.
    1. Di sebelah tulisan Tag, pilih **edit**
    1. Tempatkan kursor mouse di bidang Tag dan pilih **Lingkungan**.
    1. Tempatkan kursor mouse di kolom Nilai dan pilih **Lab**, lalu pilih **Simpan**.

1. Sekarang, kembali ke laman kebijakan.  Tempatkan kursor mouse Anda pada kotak pencarian warna biru di bagian atas laman dan pilih **Kebijakan**.

1. Dari panel navigasi kiri, pilih **Kepatuhan**.  Seperti halnya laman ikhtisar, di sini Anda dapat melihat status kepatuhan kebijakan dan/atau inisiatif yang tercantum.  CATATAN: Meskipun Anda telah menambahkan tag ke grup sumber daya, perlu waktu untuk memperbarui status.  Langganan Azure yang digunakan untuk lab mungkin memerlukan waktu yang lebih lama dari biasanya. Jika Anda ingin menunggu status kepatuhan sumber daya ini diperbarui, jangan tutup lab. Bergantung pada lingkungan lab, perlu waktu satu jam atau lebih untuk memperbarui.  

### Tinjauan

Di lab ini, Anda telah menjalani proses pembuatan penetapan kebijakan Azure dan dapat melihat dampak dari kebijakan tersebut.

