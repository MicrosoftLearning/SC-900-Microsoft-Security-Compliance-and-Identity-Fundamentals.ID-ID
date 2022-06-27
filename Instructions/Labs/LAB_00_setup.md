---
lab:
  title: Siapkan
ms.openlocfilehash: ccbb76933233296b92dabd0e03fc63a0b51bf139
ms.sourcegitcommit: 36aae92c28418fa89da73bd283833356bf87bff9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/17/2022
ms.locfileid: "146458312"
---
# <a name="lab-setup"></a>Lab: Pengaturan

## <a name="lab-scenario"></a>Skenario lab

Lab penyiapan ini terdiri dari dua tugas terpisah.  Tugas pertama berlaku dan direkomendasikan hanya jika lingkungan lab Anda menyertakan penggunaan Azure pass. Tugas kedua difokuskan untuk mengaktifkan Log Audit Microsoft dan menerapkan serta direkomendasikan terlepas dari apakah lingkungan Anda menggunakan Azure Pass atau tidak.

**Perkiraan Waktu**: 5-10 menit

### <a name="setup-part-1---redeem-azure-pass"></a>Penyiapan bagian 1 - Menukarkan Azure Pass

Tugas ini berlaku dan direkomendasikan hanya jika lingkungan lab yang Anda gunakan menyertakan Azure Pass. Dalam tugas ini, Anda akan menukarkan Azure pass Anda menggunakan kredensial yang sama dengan penyewa Microsoft 365 Anda.  Hal ini akan memberikan pengalaman yang lebih mulus saat berpindah antara Microsoft 365 dan Azure.

1. Jika Anda memiliki jendela browser yang terbuka, sebaiknya tutup semua browser.

1. Klik kanan pada ikon Microsoft Edge dan pilih **New InPrivate window** untuk membuka sesi Penjelajahan In-Private baru.

1. Di bilah alamat, masukkan **www.microsoftazurepass.com**.  

1. Pilih tombol **start** untuk memulai.

    1. Di jendela Masuk, masukkan email **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.  Jika diminta untuk tetap masuk, pilih **Ya**.
    1. Pilih **Confirm Microsoft Account** jika alamat email yang benar terdaftar.
    1. Masukkan kode promo Anda di kotak kode Promo dan klik **Claim Promo Code**.  
    1. Di halaman "Profil Anda", biarkan semua informasi default, pilih **Saya setuju dengan perjanjian langganan, detail penawaran, dan pernyataan privasi.** lalu pilih **Daftar**.
    1. Jika jendela survei terbuka, Anda memilih untuk menutupnya dengan memilih **X** atau merespons yang sesuai dan pilih **Submit**.

1. Mungkin perlu beberapa menit untuk mengaktifkan akun Anda.  Setelah diaktifkan, Anda akan diarahkan ke halaman Beranda portal Azure. Jendela Selamat Datang di Microsoft Azure terbuka, pilih **Maybe later** . Anda mungkin mendapatkan jendela pop-up "Optimize your cloud workloads with personalized recommendations", pilih **X** di sudut kanan atas jendela.

1. Biarkan tab browser di halaman beranda portal Azure terbuka, Anda akan kembali ke sana di demo berikutnya.

### <a name="setup-part-2---enable-microsoft-365-audit-log"></a>Penyiapan bagian 2 - Mengaktifkan log audit Microsoft 365

Dalam tugas penyiapan ini, Anda akan mengaktifkan kemampuan log Audit di Microsoft 365.  Meskipun dokumentasi menunjukkan bahwa log audit diaktifkan secara default, sebagian besar penyewa lab tidak mengaktifkan fitur ini dan mungkin perlu beberapa jam untuk menerapkannya.  Mengaktifkan fitur ini bermanfaat karena Microsoft 365 menggunakan log audit untuk wawasan pengguna dan aktivitas yang diidentifikasi dalam kebijakan dan wawasan analitik.

1. Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di bagian pusat Admin, pilih **Compliance**.  Halaman browser baru terbuka ke halaman selamat datang di pusat kepatuhan Microsoft 365.  

1. Dari panel navigasi sebelah kiri, di bagian solusi, pilih **Audit**.  Catatan: fungsi audit juga dapat diakses melalui halaman beranda Pertahanan Microsoft 365 (sebelumnya disebut sebagai pusat keamanan Microsoft 365).

1. Pastikan bahwa tab **Search** dipilih (digarisbawahi).

1. Setelah Anda diarahkan ke halaman Audit, tunggu 2-3 menit.  Jika Audit TIDAK diaktifkan, Anda akan melihat bilah berwarna biru di bagian atas halaman yang mengatakan mulai merekam aktivitas pengguna dan admin.  Pilih **Start recording user and admin activity**.  Jika diminta untuk mengonfirmasi bahwa pengaturan organisasi perlu diperbarui, pilih **Ya**. Setelah audit diaktifkan, bilah berwarna biru akan menghilang.  Jika bilah berwarna biru tidak ada, maka audit sudah diaktifkan, dan tidak ada tindakan lebih lanjut yang diperlukan.  Cara lain untuk memeriksa apakah audit diaktifkan adalah melalui PowerShell, tetapi itu di luar cakupan kursus ini.

1. Kembali ke halaman beranda pusat kepatuhan Microsoft 365 dengan memilih **Home** dari panel navigasi sebelah kiri.

### <a name="review"></a>Tinjau

Dalam penyiapan ini, Anda telah menukarkan Azure pass, menggunakan kredensial yang sama dengan penyewa Microsoft 365 Anda.  Anda juga telah mengaktifkan kemampuan log audit di Microsoft 365.
