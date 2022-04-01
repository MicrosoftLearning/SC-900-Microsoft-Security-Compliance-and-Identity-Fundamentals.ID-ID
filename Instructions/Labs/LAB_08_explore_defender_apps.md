---
lab:
  title: 'Menjelajahi Aplikasi Microsoft Defender untuk Cloud '
  module: 'Module 3 Lesson 4: Describe the capabilities of Microsoft security solutions: Describe threat protection with Microsoft 365 Defender'
ms.openlocfilehash: aa360b3d9e604e384cc5b040ef747425af76e13b
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893996"
---
# <a name="lab-explore-microsoft-defender-for-cloud-apps"></a>Lab: Menjelajahi Aplikasi Microsoft Defender untuk Cloud

## <a name="lab-scenario"></a>Skenario lab
Di lab ini, Anda akan menjelajahi kemampuan Aplikasi Microsoft Defender untuk Cloud.  Anda akan mempelajari informasi yang tersedia di dasbor Cloud Discovery serta kemampuan yang tersedia untuk menyelidiki temuan dan mengontrol dampak terhadap organisasi Anda melalui kebijakan.  Catatan:  Organisasi harus memiliki lisensi untuk menggunakan Aplikasi Microsoft Defender untuk Cloud yang merupakan layanan langganan berbasis pengguna. 

**Perkiraan Waktu**: 15-20 menit

#### <a name="task-1-explore-cloud-discovery"></a>Tugas 1: Mempelajari Cloud Discovery.

1.  Buka Microsoft Edge. Di bilah alamat, masukkan **admin.microsoft.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (dengan ZZZZZZ adalah ID penyewa unik Anda yang disediakan oleh penyedia host lab Anda), lalu pilih **Berikutnya**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Masuk**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**. Ini akan mengarahkan Anda ke halaman pusat admin Microsoft 365.

1. Dari panel navigasi sebelah kiri pada pusat admin Microsoft 365, pilih **Show all**.

1. Di Pusat admin, pilih **Security**.  Halaman browser baru terbuka ke halaman selamat datang di portal Pertahanan Microsoft 365.  

1. Dari bagian bawah panel navigasi kiri halaman Pertahanan Microsoft 365, pilih **More resources**.

1. Pada kartu **Aplikasi Microsoft Defender untuk Cloud**, pilih **Buka**.  Halaman browser baru terbuka ke Dasbor Cloud App Security.  Perhatikan kartu informasi yang tersedia.  Anda mungkin tidak melihat informasi apa pun pada kartu, karena lingkungan penyewa lab ini telah dikonfigurasi sebelumnya serta belum digunakan secara aktif.  

1. Dari panel navigasi sebelah kiri, pilih **Discover**, lalu dari menu tarik-turun, pilih **Cloud Discovery dashboard**.  Dasbor mencakup dan menampilkan ringkasan aplikasi yang ditemukan, kategori aplikasi, tingkat risiko, dan banyak lagi.  
    1. Dari bagian atas halaman Cloud Discovery, pilih tab **Discovered apps**.  Jendela aplikasi yang ditemukan memberikan tampilan yang lebih mendetail tentang aplikasi yang ditemukan, termasuk skor risiko, lalu lintas, jumlah pengguna, dan lainnya.
        1. Dari semua item dalam daftar, pilih **ellipses** di kolom tindakan tabel.  Perhatikan berbagai opsi yang tersedia, termasuk kemampuan untuk menandai aplikasi sebagai disetujui atau tidak.  Pilih elipsis sekali lagi, untuk menutup kotak tindakan.
        1. Memilih item baris tertentu akan membuka halaman detail untuk aplikasi tertentu.  Pilih item dari daftar.  Untuk item yang dipilih, buka setiap tab di bagian atas halaman detail:  **Usage**, **Info, IP**, **Addresses**, **Users**, dan **Alerts**. Setelah selesai menjelajahi halaman detail, kembali ke aplikasi yang ditemukan, dengan memilih **Discovered apps** dari panel navigasi sebelah kiri.
    1. Dari bagian atas halaman, pilih tab **IP addresses** (serupa dengan memilih alamat IP dari panel navigasi sebelah kiri).  Di sini, Anda akan menemukan data termasuk jumlah transaksi, jumlah lalu lintas, dan jumlah unggahan berdasarkan alamat IP.  Perhatikan bahwa Anda juga dapat memfilter menurut alamat IP tertentu atau mengekspor data untuk analisis lebih lanjut.
    1. Dari bagian atas halaman (atau panel navigasi sebelah kiri), pilih **Users**.  Ini adalah jenis informasi yang sama yang diberikan saat Anda memilih alamat IP, tetapi ini terdaftar untuk pengguna individu.  Di sini, sekali lagi, Anda memfilter menurut pengguna tertentu dan mengekspor data untuk analisis lebih lanjut.

1. Informasi yang diberikan di tab ini didasarkan pada laporan cuplikan dari log lalu lintas yang Anda unggah secara manual dari firewall dan proksi atau dari laporan berkelanjutan yang menganalisis semua log yang diteruskan dari jaringan Anda menggunakan Cloud App Security.  Untuk melihat tempat penyiapannya, pilih **elipsis** vertikal di sudut kanan atas halaman.
    1. Pilih opsi pertama, **Create Cloud Discovery snapshot report**. Di sini, Anda akan mengisi detail yang diminta dan mengunggah log lalu lintas untuk menghasilkan dan mengunggah laporan.  Pilih **Berhenti**.  Data yang Anda lihat untuk penyewa lab berasal dari Laporan cuplikan, Anda dapat melihat informasi ini di sudut kanan atas layar.
    1. Untuk melihat opsi laporan berkelanjutan, pilih **ellipses** di sudut kanan atas halaman dan dari menu tarik-turun pilih **Configure automatic upload**.  Tidak ada sumber data yang terhubung, tetapi di sinilah Anda akan menambahkan sumber data. Pilih **Tambahkan sumber data** , lalu dari jendela Tambahkan sumber data, pilih panah tarik-turun di bidang Sumber untuk melihat jenis appliance yang dapat Anda hubungkan sebagai sumber data.  Pilih **Cancel** untuk keluar.

1. Poin lain yang perlu diperhatikan adalah Anda dapat terhubung ke aplikasi secara langsung dengan menyiapkan konektor aplikasi yang akan memberi Anda visibilitas dan kontrol yang lebih besar atas aplikasi cloud Anda. Dari sudut kiri atas layar, pilih **Settings cog icon** dan dari daftar tarik-turun, pilih **App connectors**.  
    1. Pada halaman Aplikasi yang terhubung, Anda akan melihat Office 365 pada daftar dengan status terhubung.  Jika Office 365 menunjukkan kesalahan koneksi, kemungkinan besar karena Audit tidak diaktifkan.
    1. Pilih **+Connect an app** dan dari daftar tarik-turun pilih **Microsoft Azure**.  Dari jendela pop-up Microsoft Azure, pilih **Connect Microsoft Azure**.  Anda akan melihat status terhubung dan informasi terkait pemindaian, data, dan aktivitas pengguna.  Pilih **tutup Close**.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.

#### <a name="task-2-explore-ways-in-which-you-can-investigate-the-recorded-activities"></a>Tugas 2: Menjelajahi cara-cara untuk menyelidiki aktivitas yang direkam.

1. Dari panel navigasi sebelah kiri, di bagian Selidiki, pilih **Activity Log**.  Di sini, Anda mendapatkan visibilitas ke semua aktivitas dari aplikasi yang terhubung.   Karena konektor Office 365 sudah terhubung, Anda seharusnya dapat melihat beberapa data. Setelah menghubungkan Cloud App Security ke aplikasi menggunakan konektor Aplikasi, Cloud App Security akan memindai semua aktivitas yang terjadi - periode waktu pemindaian retroaktif berbeda per aplikasi - dan kemudian diperbarui terus-menerus dengan aktivitas baru.  

1. Pilih kolom aktivitas untuk item apa saja guna menampilkan informasi yang lebih detail. Di ujung kanan item yang dipilih, pilih **elipsis** vertikal.  Perhatikan berbagai opsi.  Pilih kolom aktivitas untuk item yang sama untuk menciutkan tampilan detail.

1. Perhatikan di bagian atas halaman, terdapat opsi untuk menambahkan kebijakan baru dari pencarian atau mengekspor data untuk analisis lebih lanjut.  Pilih **+New policy from search**.  Perhatikan bagaimana Anda dapat membuat kebijakan berdasarkan templat, memilih tingkat keparahan & kategori kebijakan, membuat filter untuk kebijakan, membuat peringatan, dan bahkan mengirim peringatan ke Power Automate.  Pilih **Cancel** untuk keluar dari jendela pembuatan kebijakan.

1. Dari panel navigasi kiri, pilih dan jelajahi opsi **File** dan perhatikan opsi untuk memfilter data, membuat kebijakan file, dan mengekspor data.  

1. Dari panel navigasi kiri, pilih dan jelajahi opsi **pengguna dan akun**.  Perhatikan opsi memfilter data dan mengekspor data.

1. Dari panel navigasi kiri, pilih **Konfigurasi keamanan**. Halaman ini memberi Anda penilaian konfigurasi keamanan untuk akun Azure, Amazon Web Services (AWS), dan Google Cloud Platform (GCP) Anda.

1. Biarkan halaman ini terbuka, karena Anda akan menggunakannya untuk tugas berikutnya.


#### <a name="task-3-in-this-task-you-will-explore-the-policies-and-alerts-pages-in-microsoft-defender-for-cloud-apps"></a>Tugas 3: Dalam tugas ini, Anda akan menjelajahi halaman kebijakan dan peringatan di Microsoft Defender untuk Cloud.

1. Dari panel navigasi kiri, pilih tombol panah bawah di samping bagian dengan tulisan **Kontrol** lalu pilih **Kebijakan**.  Kebijakan yang tercantum memberikan informasi tentang jumlah peringatan yang dihasilkan oleh kebijakan, keparahan, dll. Memilih item baris apa pun, seperti **Proses masuk riskan**, memberikan opsi untuk mengedit kebijakan. Pilih **Batalkan** dari bagian bawah halaman. 

1. Dari panel navigasi sebelah kiri, pilih **Alerts**.  Jika Anda memiliki peringatan yang terdaftar, pilih item dari daftar peringatan. Tinjau informasi yang diberikan.  Dari sisi kanan atas jendela, pilih **Close alert**, guna melihat opsi untuk menutup peringatan.  

1. Tutup jendela browser.

#### <a name="review"></a>Tinjau
Di lab ini, Anda menjelajahi kemampuan Aplikasi Microsoft Defender untuk Cloud.  Anda telah mempelajari informasi yang tersedia di dasbor Cloud Discovery dan kemampuan yang tersedia serta menyelidiki temuan dan mengontrol dampaknya terhadap organisasi Anda melalui kebijakan.