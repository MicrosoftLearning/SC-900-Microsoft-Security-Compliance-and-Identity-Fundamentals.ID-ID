---
lab:
    title: 'Mempelajari Pertahanan Microsoft untuk Cloud'
    modul: 'Modul 3 Pelajaran 2: Menjelaskan kemampuan solusi keamanan Microsoft: Menjelaskan kemampuan manajemen keamanan Azure'
---

# Lab: Mempelajari Pertahanan Microsoft untuk Cloud

## Skenario lab
Pada lab ini, Anda akan menjelajahi Pertahanan Microsoft dan mempelajari cara Skor Aman Azure dapat digunakan untuk meningkatkan kondisi keamanan organsisasi Anda.

**Perkiraan Waktu**: 30 menit

#### Tugas 1: Dalam tugas ini, Anda akan mengenal secara singkat mengenai Pertahanan Microsoft untuk Cloud.
1.	Buka Microsoft Edge. Di bilah alamat, masukkan **portal.azure.com**.

1. Masuk dengan kredensial admin Anda.
    1. Di jendela Masuk, masukkan **admin@WWLxZZZZZZ.onmicrosoft.com** (di mana ZZZZZZ adalah ID penyewa unik Anda yang diberikan oleh penyedia host lab), lalu pilih **Next**.
    1. Masukkan kata sandi admin yang akan disediakan oleh penyedia host lab Anda. Pilih **Sign in**.
    1. Ketika diminta untuk tetap masuk, pilih **Yes**.

1. Pada pojok kiri atas layar, di sebelah yang bertuliskan Microsoft Azure klik ikon menu portal Tampilkan (tiga garis horizontal yang juga disebut sebagai ikon hamburger) lalu dari panel navigasi kiri, di bawah Favorit, pilih **Pertahanan Microsoft untuk Cloud**.  Jika tidak tercantum dalam daftar favorit, ketikkan **Microsoft Defender for Cloud** di kotak pencarian, lalu pilih **Microsoft Defender for Cloud** dari daftar pencarian.

1. Perhatikan informasi yang tersedia pada halaman gambaran umum Pertahanan Microsoft untuk Cloud.  

1. Anda mungkin melihat kotak informasi warna biru pada bagian atas halaman yang menunjukkan bahwa Anda mungkin sedang melihat informasi yang dirahasiakan.  Klik **click here**.
    1. Untuk memastikan bahwa Anda mendapatkan visibilitas yang luas tentang penyewa, tetapkan diri Anda sebagai pemegang peran penting.  Pilih **Security Admin** lalu pilih **Get access** di bagian bawah halaman.
    1. Anda mungkin akan melihat pesan berikut: Grup manajemen akar tidak ada.  Sesuai deskripsi, sistem akan membuat grup untuk Anda.  Hal ini bisa memerlukan waktu hingga 15 menit untuk selesai (tetapi biasanya lebih cepat).  Setelah akses didapatkan, klik **Microsoft Defender for Cloud** di ujung kiri atas halaman, di atas yang bertuliskan Dapatkan izin, lalu segarkan halaman gambaran umum Microsoft Defender for Cloud.

1. Informasi di bagian atas halaman mencatumkan jumlah langganan Azure, jumlah Sumber daya yang dinilai, jumlah rekomendasi yang aktif, serta peringatan keamanan.  Di bagian isi halaman ada kartu yang mewakili Skor aman, Kepatuhan terhadap peraturan, Wawasan, Azure Defender, dan banyak lainnya.  

1. Dari bagian atas halaman, pilih **Assessed resources**.  (Perhatikan bahwa ini sama dengan memilih Inventaris dari panel navigasi kiri halaman beranda Pertahanan Microsoft untuk Cloud).
    1. Ini membawa Anda ke halaman **Inventory** yang menunjukkan langganan Azure pass Anda.  Pilih **Azure Pass – Sponsorship**.
    1. Halaman Kesehatan sumber daya menyediakan daftar rekomendasi.  Dari daftar yang tersedia, pilih **There should be more than one owner assigned to your subscription**.
    1. Pilih panah tarik-turun di samping Langkah-langkah perbaikan. Perhatikan bagaimana langkah-langkah perbaikan rinci disediakan bersama dengan opsi mengambil tindakan.  
    1. Pilih **Microsoft Defender for Cloud** dari sudut kiri atas layar untuk kembali ke halaman ikhtisar Pertahanan Microsoft untuk Cloud.

1. Dari bagian atas halaman, pilih **Active recommendations**.  (Perhatikan bahwa ini sama dengan memilih Rekomendasi dari panel navigasi kiri halaman beranda Pertahanan Microsoft untuk Cloud).
    1. Halaman rekomendasi menampilkan dasbor Skor Aman Anda.
    1. Di bawah dasbor Skor Aman terdapat daftar kontrol. Setiap kontrol keamanan mewakili risiko keamanan yang harus dikurangi dan juga mencakup informasi tentang skor maksimum yang berhubungan dengan kontrol tersebut, skor saat ini, potensi peningkatan skor, dan status kesehatan sumber daya.  
    1. Pilih salah satu kontrol, seperti **Enable MFA**.  Pilih salah satu subitem, seperti **MFA should be enabled on accounts with owner permissions on your subscription**.  Di halaman yang terbuka, Anda akan melihat deskripsi, langkah-langkah Remediasi, dan sumber daya yang terkena dampak. Keluar dari halaman ini, dengan memilih **X** di pojok kanan atas layar.
    1. Keluar dari halaman rekomendasi dengan memilih **X** di sudut kanan atas layar, untuk kembali ke halaman ikhtisar.

1. Dari halaman utama, pilih **Regulatory compliance**. Halaman kepatuhan terhadap peraturan menyediakan daftar kontrol kepatuhan.  Pada tiap kontrol adalah seperangkat penilaian yang didasarkan pada Tolok Ukur Keamanan Azure yang menyediakan rekomendasi tentang cara Anda dapat mengamankan solusi cloud Anda di Azure.
    1. Klik **IM. Identity Management**, lalu pilih **IM-6 Use strong authentication controls**.  Daftar ini menunjukkan tindakan tanggung jawab pelanggan yang dapat diambil untuk meningkatkan kondisi keamanan organisasi Anda.
    1. Pilih **X** di ujung kanan atas layar untuk menutup halaman dan kembali ke halaman Gambaran Umum Pertahanan Microsoft untuk Cloud. 
    1. Biarkan halaman gambaran umum Pertahanan Microsoft untuk Cloud terbuka, Anda akan menggunakannya di tugas berikutnya.


#### Tugas 2: Dalam tugas ini, Anda akan melewati Skor Aman Azure dan menjelajahi rekomendasi yang dapat meningkatkan skor keamanan Anda. 

1. Dari halaman gambaran umum Pertahanan Microsoft untuk Cloud, klik kartu **Secure Score**.
1. Pilih **Azure Pass – Sponsorship**.  Catat skor aman Anda.
1. Dari halaman rekomendasi, pilih **Implement security best practices** untuk memperluas daftar. Perhatikan bahwa hal ini menampilkan status kesehatan sumber daya dengan warna merah.
1. Klik item **There should be more than one owner assigned to your subscription**, yang menunjukkan status kesehatan sumber daya berwarna merah. 
1. Di bawah tulisan **Affected resources**, pastikan Sumber daya yang tidak sehat telah dipilih/digarisbawahi, lalu pilih langganan Azure yang tercantum.
1. Di bagian atas halaman Kontrol akses (IAM), klik **+ Add**, lalu dari menu tarik-turun klik **Add role assignment**.
    1. Dari bagian kiri halaman, pilih **Owner** (semestinya ini merupakan item pertama dalam daftar) sehingga baris itu akan disoroti warna abu-abu, lalu pilih **Next** dari bagian bawah halaman.
    1. Di samping tulisan Anggota, pilih **+ Select members**. 
    1. Dari jendela Pilih anggota yang terbuka di sebelah kanan layar, pilih **Alex Wilber**, lalu tekan **Select** di bagian bawah halaman.  
    1. Dari halaman Tambah penugasan peran, pastikan bahwa Alex Wilber terdaftar sebagai anggota, lalu pilih **Next** yang diikuti dengan memilih **Review + assign**.
    1. Perlu waktu hingga 24 jam agar status diperbarui, dan setelah skor keamanan Anda juga diperbarui serta semua item di Kelola grup izin dan akses dipenuhi.
    1. Di pojok kiri atas halaman, di atas yang bertuliskan Azure Pass, pilih **Microsoft Defender for Cloud** untuk kembali ke halaman gambaran umum Pertahanan Microsoft untuk Cloud.
1. Biarkan halaman ini terbuka untuk tugas berikutnya.


#### Tugas 3:  Mengingat kembali bahwa Pertahanan Microsoft untuk Cloud ditawarkan dalam dua mode: tanpa fitur peningkatan keamanan (gratis) dan dengan fitur peningkatan keamanan yang tersedia melalui rencana Pertahanan Microsoft untuk Cloud. Dalam tugas ini, Anda akan mengetahui cara mengaktifkan/menonaktifkan berbagai rencana Pertahanan Microsoft untuk Cloud.

1.	Dari halaman gambaran umum Pertahanan Microsoft untuk Cloud, pilih **Environment settings** dari panel navigasi kiri.
1. Pilih simbol lebih besar dari **>** di samping tulisan Grup Root Penyewa untuk memperluasnya (jangan memilih Grup Root Penyewa secara langsung karena Anda akan diarahkan ke halaman lain), lalu pilih **Azure Pass - Sponsorship**
1.	Di halaman rencana Pertahanan, perhatikan bahwa Anda dapat memilih Aktifkan semua atau memilih salah satu rencana Pertahanan. Biarkan pengaturan seperti adanya dengan semua rencana diatur ke nonaktif.
1.	Sekarang Anda dapat menutup tab browser untuk keluar portal Azure.


#### Tinjauan
Pada lab ini, Anda telah menjelajahi Pertahanan Microsoft untuk Cloud dan mempelajari bahwa  Skor Aman Azure dapat digunakan untuk meningkatkan kondisi keamanan organsisasi Anda.
