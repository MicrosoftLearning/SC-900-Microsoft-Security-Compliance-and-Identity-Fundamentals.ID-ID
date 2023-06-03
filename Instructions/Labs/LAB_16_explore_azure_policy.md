<a name="---"></a><!---
---
Lab: Judul: 'Jelajahi Azure Policy' Jalur Pembelajaran/Modul/Pelajaran: 'Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft; Modul 6: Menjelaskan kemampuan tata kelola sumber daya di Azure; Pelajaran 2: Jelaskan Azure Policy'
---
--->

# <a name="lab-explore-azure-policy"></a>Lab: Menjelajahi Azure Policy

Lab ini memetakan ke konten Pelajari berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan kemampuan tata kelola sumber daya di Azure
- Pelajaran: Menjelaskan Azure Policy

## <a name="lab-scenario"></a>Skenario lab

Azure Policy membantu memberlakukan standar organisasi dan menilai kepatuhan dalam skala besar. Azure Policy mengevaluasi sumber daya di Azure dengan membandingkan properti sumber daya tersebut dengan aturan bisnis. Di lab ini, Anda akan membuat kebijakan dan melihat dampak dari kebijakan tersebut.  Anda juga akan mempelajari informasi kepatuhan dan remediasi yang tersedia di halaman kebijakan.

**Perkiraan Waktu**: 15-20 menit

### <a name="task-1"></a>Tugas 1

Dalam tugas ini, Anda akan membuat penetapan kebijakan dasar untuk meminta tag pada grup sumber daya.
1.  Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin untuk langganan Azure Anda (kredensial admin ini berbeda dengan kredensial admin Microsoft 365).
    1. Di jendela Masuk, masukkan **User1-XXXXXXXX@LODSPRODMSLEARNMCA.onmicrosoft.com** (dengan XXXXXXXX adalah ID penyewa unik Anda yang diberikan oleh penyedia hosting lab Anda) lalu pilih **Berikutnya**.

    1. Masukkan kata sandi admin yang disediakan oleh penyedia hosting lab Anda. Pilih **Masuk**.
    1. Jika diminta untuk tetap masuk, pilih **Ya**.

1. Anda sekarang berada di portal Microsoft Azure.  Di kotak pencarian, di bilah biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **policy**, kemudian pilih **Policy** dari hasil pencarian. Tindakan ini akan membuka halaman beranda Kebijakan yang menyediakan tampilan dasbor.  Cakupan tampilan Dasbor adalah langganan Azure yang disediakan oleh authorized lab hoster (ALH). Anda akan melihat kebijakan yang tercantum, ini adalah kebijakan yang dibuat oleh ALH, untuk penggunaan langganan Azure.

1. Bentuk panel navigasi kiri, di bawah Penulisan, pilih **Assignments**.

1. Dari bagian atas halaman, pilih **Assign policy**. Wizard penetapan kebijakan terbuka untuk memandu admin dalam proses penetapan kebijakan.

1. Anda mulai di tab Dasar.
    1. Untuk Cakupan, biarkan pengaturan default. Dalam hal ini, cakupan kebijakan adalah langganan Azure yang disediakan oleh authorized lab hoster (ALH).
    1. Untuk Definisi Kebijakan, pilih **elipsis**.  Muncul daftar definisi kebijakan yang tersedia.  Di bilah pencarian, masukkan, **Memerlukan tag**. Dari hasil pencarian, pilih **Perlu tag pada grup sumber daya** (Anda mungkin perlu menggulir ke bawah), lalu tekan **Tambahkan**.  Catatan: efek dari kebijakan ini adalah Menolak pembuatan grup sumber daya baru yang tidak memenuhi persyaratan.  
    1. Perhatikan nama tugas default.  Pertahankan nama apa adanya.
    1. Pastikan bahwa penegakan Kebijakan diatur ke **Diaktifkan**

1. Pilih **Berikutnya**, lalu pilih **Berikutnya** lagi untuk berpindah ke tab Parameter (Anda juga bisa memilih tab parameter secara langsung).

1. Anda sekarang berada di tab Parameter. Di kolom Tag nama, masukkan **Lingkungan** lalu pilih **Berikutnya**.

1. Di tab Remediasi, biarkan pengaturan default apa adanya lalu pilih **Berikutnya**.

1. Anda sekarang berada di tab Pesan ketidakpatuhan. Di bidang pesan ketidakpatuhan, masukkan **Tag lingkungan diperlukan**, lalu pilih **Berikutnya**. Catatan: pesan ini akan muncul sebagai alasan ketidakpatuhan untuk grup sumber daya yang dibuat sebelum penetapan kebijakan dan tidak memiliki tag Lingkungan.

1. Tinjau penetapan kebijakan, lalu pilih **Buat**.  Jika Anda tidak segera melihat kebijakan, pilih **Refresh**. Catatan: Diperlukan waktu hingga 30 menit agar kebijakan diterapkan, tetapi biasanya lebih cepat.

1. Keluar dari halaman Penetapan kebijakan dengan memilih **X** di sudut kanan atas layar.

1. Anda sekarang berada di halaman beranda layanan Azure.  Biarkan halaman ini tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

### <a name="task-2"></a>Tugas 2

Dalam tugas ini Anda akan melihat dampak penetapan kebijakan Azure, dengan mencoba membuat grup sumber daya di Azure yang tidak memiliki tag.

1. Buka tab browser, Home – Microsoft Azure.

1. Dari bagian atas halaman, di bawah teks tertulis Layanan Azure, pilih **Resource groups**.

1. Dari sudut kiri atas halaman, pilih **+ Create**.

1. Dari tab Dasar pada Buat grup sumber daya, biarkan bidang Langganan apa adanya.

1. Di bidang grup Sumber daya, masukkan,  **SC900-Labs**.

1. Biarkan pengaturan Wilayah ke default, lalu pilih **Berikutnya: Tag**.

1. Biarkan bidang tag Nama dan Nilai kosong.  JANGAN DIPOPULASIKAN, lalu pilih **Review + create**.

1. Anda akan melihat pesan validasi lolos (nama tag dan nilai bukan bidang yang wajib diisi dalam wizard), lalu pilih **Buat**.

1. Anda akan melihat pesan kegagalan di bagian atas layar, “Gagal membuat grup sumber daya". Pilih **View error details**. Kondisi yang merupakan bagian dari kebijakan Azure tidak terpenuhi sehingga pembuatan grup sumber daya diblokir, karena ketidakpatuhan. Catatan: Jika Anda tidak melihat pesan kegagalan dan grup sumber daya yang telah dibuat, hal itu karena kebijakan belum diterapkan.  Buka halaman Kebijakan untuk kebijakan yang Anda buat di tugas sebelumnya dan setelah kebijakan diterapkan, Anda akan melihat bahwa sumber daya tidak sesuai.  Halaman detail akan menyertakan pesan ketidakpatuhan.

1. Ringkasan kesalahan menunjukkan jenis kesalahan, "Resource ‘SC900-Labs’ was disallowed by policy."  Tutup jendela ini dengan memilih **X** di sudut kiri atas layar.

1. Dari jendela Buat grup sumber daya, pilih **Sebelumnya**.

1. Anda kembali ke halaman Tag untuk Buat grup sumber daya.  Di bidang Nama masukkan Lingkungan dan di bidang Nilai, masukkan **SC900-Labs**, lalu pilih **Berikutnya: Tinjau + Buat >** .

1. Verifikasi tag dan pilih **Create**.

1. Di bidang Nama, masukkan **Lingkungan** dan di bidang Nilai, masukkan **Lab** (nilai ini bisa apa saja, kebijakan hanya memerlukan nilai tag), lalu pilih **Berikutnya: Tinjau + Buat >** lalu pilih **Buat**.

1. Anda akan melihat grup sumber daya terdaftar.  

1. Pilih **Beranda** dari breadcrumb di bagian atas halaman untuk kembali ke halaman beranda Azure.

1. Biarkan tab browser tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

### <a name="task-3-optional"></a>Tugas 3 (Opsional)

Dalam tugas ini, Anda akan menjalani langkah-langkah untuk memulihkan grup sumber daya yang tidak patuh. CATATAN: langganan Azure yang digunakan untuk lab akan memerlukan waktu yang lebih lama dari biasanya untuk memperbarui status kepatuhan grup sumber daya yang diperbaiki.

1. Dari halaman beranda Azure, pilih **kebijakan**. Tindakan ini akan membuka halaman beranda Kebijakan yang menyediakan tampilan dasbor.  Cakupan untuk tampilan Dasbor adalah langganan Azure yang disediakan oleh authorized lab hoster.  

1. Anda akan melihat kebijakan yang Anda buat sebelumnya, lalu pilih kebijakan tersebut.

1. Di bagian atas halaman, di bagian Essentials, Anda dapat melihat nama, deskripsi, dan informasi penting lainnya.  Perhatikan bahwa kebijakan ditampilkan sebagai tidak patuh.  Pilih kebijakan untuk informasi lebih lanjut tentang mengapa kebijakan tersebut tidak sesuai. Di sini Anda dapat melihat bahwa sumber daya yang terdaftar sebagai resourgegroup1 tidak sesuai.  Ini adalah contoh grup sumber daya yang telah dibuat, sebelum pembuatan kebijakan. Pilih **Detail** untuk informasi selengkapnya.  Di sini Anda dapat melihat pesan kepatuhan bahwa tag lingkungan diperlukan.  Pilih **X** di kanan atas untuk menutup jendela.

1. Pilih **resourcegroup1** lalu dari bagian atas halaman, pilih **Lihat Sumber Daya**.
    1. Di sebelah tulisan Tag, pilih **edit**
    1. Tempatkan kursor mouse di bidang Tag dan pilih **Lingkungan**.
    1. Tempatkan kursor mouse di kolom Nilai dan pilih **Lab**, lalu pilih **Simpan**.

1. Sekarang kembali ke halaman kebijakan.  Tempatkan kursor mouse Anda pada kotak pencarian warna biru di bagian atas halaman dan pilih **Kebijakan**.

1. Dari panel navigasi sebelah kiri, pilih **Compliance**.  Sama seperti halaman ringkasan, di sini Anda dapat melihat status kepatuhan dari kebijakan dan/atau inisiatif yang tercantum.  CATATAN: meskipun Anda telah menambahkan tag ke grup sumber daya, perlu waktu untuk memperbarui status.  Langganan Azure yang digunakan untuk tujuan lab mungkin memerlukan waktu yang lebih lama dari biasanya. Jika Anda ingin menunggu status kepatuhan untuk sumber daya ini diperbarui, jangan tutup lab. Bergantung pada lingkungan lab, perlu waktu satu jam atau lebih untuk memperbarui.  

### <a name="review"></a>Tinjau

Di lab ini, Anda menjalani proses pembuatan penetapan kebijakan Azure dan dapat melihat dampak dari kebijakan tersebut.
