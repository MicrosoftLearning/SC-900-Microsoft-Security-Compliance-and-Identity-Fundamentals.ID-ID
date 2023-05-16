---
demo:
  title: 'Azure Policy'
  module: 'Modul 6: Menjelaskan kemampuan tata kelola sumber daya di Azure'
---


# <a name="demo-azure-policy"></a>Demo: Azure Policy

Demo ini memetakan ke konten Learn berikut:

- Jalur Pembelajaran: Menjelaskan kemampuan kepatuhan Microsoft
- Modul: Menjelaskan kemampuan tata kelola sumber daya di Azure
- Pelajaran: Menjelaskan Azure Policy

## <a name="demo-scenario"></a>Skenario demo

Dalam demo ini, Anda akan menjalani proses penyiapan kebijakan Azure dan dampak dari kebijakan tersebut.

### <a name="demo-part-1"></a>Demo Bagian 1

Membuat kebijakan untuk mengharuskan tag pada grup sumber daya (menunjukkan langkah-langkah untuk membuat kebijakan dari templat)

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.  Anda harus sudah masuk, jika belum, masuk dengan kredensial admin Anda.

1. Di kotak pencarian, di bilah biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **policy**, kemudian pilih **Policy** dari hasil pencarian.

1. Anda sekarang berada di ringkasan halaman Kebijakan. Perhatikan informasi yang tersedia di dasbor.

1. Dari panel navigasi kiri, di bagian Penulisan, pilih **Tugas**.  Anda akan melihat bahwa sudah ada penetapan kebijakan, pilih **ASC Default**.  Tinjau bidang deskripsi. CATATAN: Kolom deskripsi mereferensikan Azure Security Center yang telah diubah namanya menjadi Microsoft Defender untuk Cloud.  Kembali ke halaman Penetapan Kebijakan dengan memilih **X** di pojok kanan atas halaman.

1. Dari bagian atas halaman, pilih **Assign policy**. Wizard Tetapkan kebijakan terbuka untuk memandu admin dalam proses menetapkan kebijakan.

1. Anda mulai di tab Dasar.
    1. Untuk Cakupan, biarkan pengaturan default. Dalam hal ini, cakupan kebijakan adalah langganan Azure yang disediakan oleh authorized lab hoster (ALH).
    1. Untuk Definisi Kebijakan, pilih **elipsis**.  Muncul daftar definisi kebijakan yang tersedia.  Di bilah pencarian, masukkan, **Memerlukan tag**. Dari hasil pencarian, pilih **Require a tag on resource group** (Anda mungkin perlu menggulir ke bawah), kemudian tekan **Select**.  Catatan: efek dari kebijakan ini adalah Menolak pembuatan grup sumber daya baru yang tidak memenuhi persyaratan.  
    1. Perhatikan nama tugas default.  Pertahankan nama apa adanya.
    1. Pastikan bahwa Penegakan kebijakan diatur ke **Diaktifkan**, pilih **Berikutnya**.

1. Anda sekarang berada di tab Parameter. Di kolom Tag nama, masukkan **Lingkungan** lalu pilih **Berikutnya**.

1. Di tab Remediasi, biarkan pengaturan default apa adanya lalu pilih **Berikutnya**.

1. Anda sekarang berada di tab Pesan ketidakpatuhan. Di bidang pesan ketidakpatuhan, masukkan **Tag lingkungan diperlukan**, lalu pilih **Berikutnya**. Catatan: pesan ini akan muncul sebagai alasan ketidakpatuhan untuk grup sumber daya yang dibuat sebelum penetapan kebijakan dan tidak memiliki tag Lingkungan.  

1. Tinjau penetapan kebijakan, lalu pilih **Buat**.  Jika Anda tidak segera melihat kebijakan, pilih **Refresh**. Catatan: Diperlukan waktu hingga 30 menit agar kebijakan diterapkan, tetapi biasanya lebih cepat.

1. Keluar dari halaman Penetapan kebijakan dengan memilih **X** di sudut kanan atas layar.

1. Anda sekarang berada di halaman beranda layanan Azure.  Biarkan halaman ini tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

### <a name="demo-part-2"></a>Demo Bagian 2

Dalam tugas ini Anda akan melihat dampak penetapan kebijakan Azure, dengan mencoba membuat grup sumber daya di Azure yang tidak memiliki tag.

1. Buka tab browser, Home – Microsoft Azure.

1. Dari bagian atas halaman, di bawah teks tertulis Layanan Azure, pilih **Resource groups**.

1. Dari sudut kiri atas halaman, pilih **+ Create**.

1. Dari tab Dasar pada Buat grup sumber daya, biarkan bidang Langganan apa adanya.

1. Di bidang grup Sumber daya, masukkan,  **SC900-Labs**.

1. Biarkan pengaturan Wilayah ke default, lalu pilih **Berikutnya: Tag**.

1. Biarkan bidang tag Nama dan Nilai kosong.  JANGAN DIPOPULASIKAN, lalu pilih **Review + create**.

1. Anda akan melihat pesan yang menunjukkan bahwa validasi telah lolos (nama tag dan nilai bukan bidang yang wajib diisi dalam wizard), lalu pilih **Buat**.

1. Anda akan melihat pesan kegagalan di bagian atas layar, “Gagal membuat grup sumber daya. Pilih **Lihat detail kesalahan**”. Kondisi yang merupakan bagian dari kebijakan Azure tidak terpenuhi sehingga pembuatan grup sumber daya diblokir, karena ketidakpatuhan. Catatan: Jika Anda tidak melihat pesan kegagalan dan grup sumber daya yang telah dibuat, hal itu karena kebijakan belum diterapkan.  Buka halaman Kebijakan untuk kebijakan yang Anda buat di tugas sebelumnya dan setelah kebijakan diterapkan, Anda akan melihat bahwa sumber daya tidak sesuai.  Halaman detail akan menyertakan pesan ketidakpatuhan.

1. Ringkasan kesalahan menunjukkan jenis kesalahan, "Resource ‘SC900-Labs’ was disallowed by policy."  Tutup jendela ini dengan memilih **X** di sudut kiri atas layar.

1. Dari jendela Buat grup sumber daya, pilih **Sebelumnya**.

1. Anda kembali ke halaman Tag untuk Buat grup sumber daya.  Di bidang Nama masukkan Lingkungan dan di bidang Nilai, masukkan **SC900-Labs**, lalu pilih **Berikutnya: Tinjau + Buat >** .

1. Verifikasi tag dan pilih **Create**.

1. Di bidang Nama, masukkan **Lingkungan** dan di bidang Nilai, masukkan **Lab** (nilai ini bisa apa saja, kebijakan hanya memerlukan nilai tag), lalu pilih **Berikutnya: Tinjau + Buat >** lalu pilih **Buat**.

1. Anda akan melihat grup sumber daya terdaftar.  

1. Beri tahu peserta bahwa jika ada grup sumber daya yang dibuat sebelum kebijakan, maka grup sumber daya tersebut sekarang akan muncul sebagai tidak patuh terhadap penetapan kebijakan ini dan perlu diperbaiki, dengan menerapkan tag Lingkungan.  Terdapat grup sumber daya yang sudah ada sebelumnya berlabel ResourceGroup1 yang tidak patuh dan dapat diperbaiki, tetapi waktu pembaruan status, setelah perbaikan, lebih lama dari biasanya untuk lingkungan lab.

### <a name="review"></a>Tinjau

Dalam demo ini, Anda telah menunjukkan proses penyiapan kebijakan Azure dan dampak dari kebijakan tersebut.
