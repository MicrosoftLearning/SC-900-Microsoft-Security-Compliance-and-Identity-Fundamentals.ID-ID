---
Demo:
  title: Akses bersyarata Azure Active Directory
  module: 'Module 2 Lesson 3: Describe the capabilities of Microsoft Identity and access management solutions: Explore the access management capabilities of Azure AD'
ms.openlocfilehash: b3fd1d1f73c7f807c7a72b258762579bdf0184ac
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894153"
---
# <a name="demo-azure-active-directory-conditional-access"></a>Demo: Akses Bersyarat Azure Active Directory

### <a name="demo-scenario"></a>Skenario demo
Dalam demo ini, Anda akan mempelajari berbagai opsi yang tersedia untuk kebijakan akses bersyarat.

1. Buka tab **Contoso – Microsoft Azure** yang terbuka di browser Anda. Jika sebelumnya Anda menutup tab, buka halaman browser dan di bilah alamat, masukkan portal.azure.com dan pilih Azure Active Directory. Anda harus masuk sebagai admin di portal Microsoft Azure. Jika tidak, masuk kembali.

1. Dari panel navigasi kiri, pilih **Security**.

1. Dari panel navigasi kiri, pilih **Conditional Access**.

1. Layar Kebijakan Akses Bersyarat akan ditampilkan. Semua Kebijakan Akses Bersyarat dicantumkan di sini. Untuk menampilkan pengaturan yang terkait dengan akses bersyarat, pilih **+ New policy**.

1. Di kolom **Name**, Anda cukup memasukkan nama untuk kebijakan tersebut.

1. Perhatikan bahwa Anda memiliki beberapa opsi di bawah **Assignments**.  Karena kebijakan akses bersyarat seperti pernyataan jika/maka, pengaturan tugas akan seperti pernyataan “jika”.
    1. **Pengguna dan grup** - arahkan kursor ke ikon informasi di sebelah “Pengguna dan grup” dan sebutkan bahwa ini adalah tempat Anda mengatur pengguna dan grup di direktori tempat kebijakan diterapkan. Pilih **0 users and groups selected**.  Sekarang Anda akan melihat opsi untuk Menyertakan atau Mengecualikan pengguna atau grup. Pilih dan jelaskan pengaturan yang tersedia untuk tab **Include**, lalu pilih dan sampaikan pengaturan yang tersedia untuk tab **Exclude**.
    1. **Aplikasi atau tindakan cloud** - arahkan mouse ke ikon informasi di sebelah bagian yang bertuliskan “Aplikasi atau tindakan cloud” dan sebutkan bahwa ini adalah tempat Anda mengatur aplikasi yang digunakan atau tindakan yang dilakukan oleh pengguna, untuk kebijakan akses bersyarat.  Pilih **No cloud apps or actions selected**.
        1. Pilih panah tarik-turun di kotak di bawah tulisan **Select what this policy applies to** dan perhatikan pilihannya.  Biarkan pengaturan default – Cloud apps.
        1. Pilih dan sampaikan pengaturan yang tersedia untuk tab Sertakan. Di bawah tab **Include**, pilih **Select Apps**.  Perhatikan jendela yang terbuka, tempat Anda dapat memilih dari daftar aplikasi.  Jangan pilih apa pun, tutup jendela ini dengan memilih **X** di sudut kanan atas jendela. Kembali memilih **None** untuk menghapus kesalahan.
        1. Kemudian pilih dan sampaikan pengaturan yang tersedia untuk **Exclude tab**.  Di sini, sekali lagi Anda dapat memilih aplikasi tertentu untuk dikecualikan.
    1. **Ketentuan** - arahkan mouse ke ikon informasi di sebelah bagian yang bertuliskan “Ketentuan” dan sebutkan bahwa hal ini menetapkan kapan kebijakan akan diterapkan. Pilih **0 conditions selected**. Sampaikan “sinyal” berbeda yang terdaftar.   Pilih beberapa opsi dengan terlebih dahulu memilih ikon informasi untuk menentukan penjelasannya dan kemudian pilih **Not configured** untuk item tertentu guna menampilkan berbagai opsi.
        1. **Risiko pengguna** - Risiko pengguna menunjukkan peluang identitas atau akun tertentu disusupi. Risiko ini dapat dihitung secara offline menggunakan sumber inteligensi ancaman internal dan eksternal Microsoft.
        1. **Risiko masuk** - Risiko masuk menunjukkan peluang bahwa permintaan autentikasi yang diberikan tidak diotorisasi oleh pemilik identitas. Contohnya mungkin seperti masuk dari alamat IP anonim atau perjalanan tidak biasa, dll.
        1. **Platform Perangkat** - Platform tempat pengguna masuk. Seperti, 'iOS’.
        1. **Lokasi** - Lokasi (ditentukan menggunakan rentang alamat IP) tempat pengguna masuk
        1. **Aplikasi klien** - Perangkat lunak yang digunakan pengguna untuk mengakses aplikasi cloud. Seperti, 'Browser’

1. **Access Controls** – kembali ke analogi bahwa kebijakan akses bersyarat seperti pernyataan jika/maka, kontrol akses adalah analog dengan pernyataan “maka”.
    1. **Berikan** - Arahkan mouse Anda ke ikon informasi di sebelah bagian yang bertuliskan “Berikan” untuk deskripsi.  Pilih **0 controls selected** untuk menunjukkan pilihan yang berbeda.  Sampaikan beberapa di antaranya.  Secara khusus, jelaskan opsi untuk **Require multi-factor authentication**, di bawah Berikan Akses dan cara ini dapat digunakan untuk memberikan kontrol yang sangat terperinci tentang kapan memerlukan MFA.   Juga jelaskan bahwa Anda dapat mengatur beberapa kontrol dan memerlukan semua atau hanya satu dari kontrol yang dipilih.
    1. **Sesi** - Arahkan mouse ke ikon informasi di sebelah bagian yang bertuliskan “Sesi” untuk deskripsi.  Jelaskan bahwa kontrol Sesi memungkinkan pengalaman terbatas dalam aplikasi cloud.  Misalnya, pengguna mungkin dapat mengakses aplikasi cloud tetapi akan diblokir dari mengunduh konten atau cetakan apa pun, sebagai contoh.  Ini adalah topik yang lebih kompleks, maka buatlah tetap sederhana.

1. Setelah kebijakan dikonfigurasi, Anda dapat mengaktifkan kebijakan dengan memilih **On**, kemudian tekan tombol **Create** untuk membuat kebijakan.

1. Pilih **X** di sudut kanan atas halaman untuk menutup kebijakan, lalu pilih Microsoft Azure pada bilah biru di bagian atas halaman untuk kembali ke halaman beranda Portal Azure.

1. Biarkan halaman browser ini terbuka untuk demo berikutnya.

### <a name="review"></a>Tinjau

Dalam demo ini, Anda telah mempelajari berbagai opsi yang tersedia untuk kebijakan akses bersyarat.
