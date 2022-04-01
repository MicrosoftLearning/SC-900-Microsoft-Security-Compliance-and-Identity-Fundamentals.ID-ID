---
Demo:
  title: Kebijakan Azure
  module: 'Module 4 Lesson 5: Describe the capabilities of Microsoft compliance solutions: Describe Azure Policy'
ms.openlocfilehash: 898e2d2ae228baf6acbffd7301fcbdf4a6a2dba5
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894068"
---
# <a name="demo-azure-policy"></a>Demo: Azure Policy

### <a name="demo-scenario"></a>Skenario demo
Dalam demo ini, Anda akan mempelajari proses pengaturan kebijakan Azure dan dampak dari kebijakan tersebut.

#### <a name="demo-part-1-create-a-policy-to-require-a-tag-on-a-resource-group-shows-steps-to-create-a-policy-from-a-template"></a>Demo Bagian 1: Membuat kebijakan untuk mengharuskan tag pada grup sumber daya (menunjukkan langkah-langkah untuk membuat kebijakan dari templat)

1. Buka Microsoft Edge. Di bilah alamat, masukkan **portal.microsoft.com**.  Seharusnya Anda sudah masuk. Jika tidak, masuk dengan kredensial admin Anda.

1. Di kotak pencarian, di bilah biru di bagian atas halaman di sebelah tulisan Microsoft Azure, masukkan **policy**, kemudian pilih **Policy** dari hasil pencarian.

1. Sekarang Anda berada di ikhtisar halaman Kebijakan. Perhatikan informasi yang tersedia di dasbor.

1. Bentuk panel navigasi kiri, di bawah Penulisan, pilih **Assignments**.  Anda akan melihat bahwa sudah ada penetapan kebijakan, pilih **ASC Default**.  Tinjau bidang deskripsi. CATATAN: Bidang deskripsi merujuk ke Azure Security Center yang telah diganti namanya menjadi Microsoft Defender untuk Cloud.  Kembali ke halaman Penetapan Kebijakan dengan memilih **X** di pojok kanan atas halaman.

1. Dari bagian atas halaman, pilih **Assign policy**.

1. Wizard Tetapkan kebijakan terbuka untuk memandu admin dalam proses menetapkan kebijakan.  Di samping bidang Definisi kebijakan, pilih **ellipses**.  Muncul daftar definisi kebijakan yang tersedia.  

1. Di bilah pencarian, masukkan, **Tag**.

1. Dari hasil pencarian, pilih **Require a tag on resource group** (Anda mungkin perlu menggulir ke bawah), kemudian tekan **Select**.  Catatan: efek dari kebijakan ini adalah Menolak pembuatan grup sumber daya baru yang tidak memenuhi persyaratan.  

1. Perhatikan nama tugas default.  Biarkan nama apa adanya dan dari bagian bawah halaman, pilih **Next**.

1. Di bidang nama Tag, masukkan **Environment** (grup sumber daya akan memerlukan tag Lingkungan) lalu pilih **Next**.  

1. Dari tab Remediasi, baca deskripsi tetapi jangan ubah pengaturannya. Pilih **Selanjutnya**

1. Dalam pesan ketidakpatuhan, masukkan **An environment tag is required**, kemudian pilih **Next**. Catatan: pesan ini akan muncul sebagai alasan ketidakpatuhan untuk grup sumber daya yang dibuat sebelum penetapan kebijakan dan tidak memiliki tag Lingkungan.  Untuk grup sumber daya yang dibuat setelah kebijakan dibuat, pembuatan grup sumber daya akan ditolak jika tidak ada tag lingkungan.

1. Tinjau penetapan kebijakan, lalu pilih Create.  Jika Anda tidak segera melihat kebijakan, pilih **Refresh**. Catatan: Mungkin perlu waktu hingga 30 menit agar kebijakan diterapkan.

1. Keluar dari halaman Penetapan kebijakan dengan memilih **X** di sudut kanan atas layar.

1. Sekarang Anda berada di halaman beranda layanan Azure.  Biarkan halaman ini tetap terbuka, Anda akan membutuhkannya untuk tugas berikutnya.

#### <a name="demo-part-2--show-the-impact-of-the-policy-by-creating-a-resource-group-without-a-tag-then-fix-it-to-have-a-tag"></a>Bagian Demo 2:  Tunjukkan dampak kebijakan dengan membuat grup sumber daya tanpa tag, lalu perbaiki agar memiliki tag.

1. Dari bagian atas halaman, di bawahnya tertulis Layanan Azure, pilih **Resource groups**. Jika Anda tidak melihat opsi yang tercantum, masukkan Grup sumber daya di bilah pencarian dan pilih dari sana.

1. Dari sudut kiri atas halaman, pilih **+ Create**.

1. Dari tab Dasar grup untuk Membuat sumber daya, biarkan bidang Langganan apa adanya, Azure Pass - Sponsorship.

1. Di bidang grup Sumber daya, masukkan,  **SC900-Labs**.

1. Biarkan pengaturan Wilayah ke default, lalu pilih **Berikutnya: Tag**.

1. Biarkan bidang tag Nama dan Nilai kosong.  JANGAN DIPOPULASIKAN, lalu pilih **Review + create**.

1. Anda akan melihat bahwa telah tervalidasi (nama dan nilai tag bukan bidang wajib di wizard), lalu pilih **Create**.

1. Anda akan melihat pesan kegagalan di bagian atas layar, “Failed to create the resource group. View error details”.  Pilih **View error details**. Kondisi yang merupakan bagian dari kebijakan Azure tidak terpenuhi sehingga pembuatan grup sumber daya diblokir, karena ketidakpatuhan. Catatan: Jika Anda tidak melihat pesan kegagalan dan grup sumber daya yang telah dibuat, hal itu karena kebijakan belum diterapkan.  Buka halaman Kebijakan untuk kebijakan yang Anda buat di tugas sebelumnya dan setelah kebijakan diterapkan, Anda akan melihat bahwa sumber daya tidak sesuai.  Halaman detail akan menyertakan pesan ketidakpatuhan.

1. Ringkasan kesalahan menunjukkan jenis kesalahan, "Resource ‘SC900-Labs’ was disallowed by policy."  Tutup jendela ini dengan memilih **X** di sudut kiri atas layar.

1. Dari jendela Buat grup sumber daya, pilih **<Previous**.

1. Anda kembali ke halaman Tag untuk Buat grup sumber daya.  Di bidang Nama masukkan Lingkungan dan di bidang Nilai, masukkan **SC900-Labs**, lalu pilih **Berikutnya: Tinjau + Buat >** .

1. Verifikasi tag dan pilih **Create**.

1. Anda akan melihat grup sumber daya yang terdaftar.  Karena tag disediakan di grup sumber daya, kondisi yang disertakan sebagai bagian dari kebijakan Azure telah terpenuhi.  Grup sumber daya mematuhi kebijakan.

#### <a name="review"></a>Tinjau

Dalam demo ini, Anda telah menunjukkan proses penyiapan kebijakan Azure dan dampak dari kebijakan tersebut.
