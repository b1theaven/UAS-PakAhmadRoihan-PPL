# Perancangan Perangkat Lunak UAS

## Nomor 1: Permasalahan

### **Permasalahan dalam Proyek Perangkat Lunak**

Dalam pengelolaan komunitas Discord, banyak server menghadapi tantangan dalam moderasi, pengelolaan peran, serta interaksi anggota. Administrator sering kali harus menangani pelanggaran aturan secara manual, mengatur role pengguna satu per satu, dan menjaga keterlibatan anggota agar komunitas tetap aktif. Proses ini tidak hanya memakan waktu tetapi juga rentan terhadap kesalahan manusia. Selain itu, kurangnya sistem otomatisasi membuat komunitas sulit berkembang secara efektif, terutama dalam komunitas besar dengan ribuan anggota.

---

### **Analisis Penyebab Utama Permasalahan**

1. **Moderasi Manual yang Tidak Efisien**  
   Moderasi yang dilakukan secara manual menyebabkan admin harus terus memantau aktivitas anggota, menangani spam, serta menegakkan aturan komunitas. Ini meningkatkan beban kerja dan risiko kelalaian, terutama jika jumlah anggota sangat besar.

2. **Pengelolaan Role yang Lambat dan Tidak Terorganisir**  
   Dalam komunitas besar, mengelola role berdasarkan aktivitas atau status anggota memerlukan waktu dan usaha yang signifikan. Tanpa sistem otomatisasi, admin harus menetapkan atau mencabut role secara manual, yang dapat menyebabkan keterlambatan atau ketidakkonsistenan dalam struktur komunitas.

3. **Kurangnya Interaksi dan Keterlibatan Anggota**  
   Jika tidak ada fitur yang menarik, komunitas cenderung menjadi pasif dan kurang interaktif. Anggota hanya bergabung tanpa adanya motivasi untuk berpartisipasi dalam diskusi atau kegiatan komunitas.

---

### **Dampak Permasalahan terhadap Pengguna dan Sistem**

- **Beban Kerja yang Tinggi**  
  Admin dan moderator harus menghabiskan banyak waktu untuk tugas-tugas rutin yang bisa diotomatisasi, sehingga mengurangi efisiensi pengelolaan komunitas.
- **Kualitas Moderasi yang Tidak Konsisten**  
  Karena bersifat manual, keputusan yang dibuat oleh admin bisa bervariasi, menyebabkan aturan komunitas diterapkan secara tidak konsisten.
- **Penurunan Aktivitas Anggota**  
  Tanpa sistem interaksi yang baik, anggota cenderung pasif, menyebabkan komunitas kurang berkembang dan kehilangan daya tariknya.

---

### **Solusi yang Dapat Diterapkan dengan Perangkat Lunak**

1. **Bot Moderasi Otomatis**  
   Bot akan memantau aktivitas anggota, mendeteksi spam, menyaring kata-kata kasar, serta mengambil tindakan otomatis seperti memberi peringatan atau melakukan mute/kick/ban jika diperlukan.

2. **Sistem Pengelolaan Role Otomatis**  
   Pengguna akan diberikan atau dicabut role-nya secara otomatis berdasarkan aktivitas mereka, misalnya, memberikan peran khusus bagi anggota yang sering berkontribusi dalam diskusi.

3. **Fitur Interaktif untuk Meningkatkan Keterlibatan**
   - Permainan berbasis teks atau kuis komunitas.
   - Pengingat acara dan sistem polling otomatis.
   - Pemberian hadiah atau badge bagi anggota aktif untuk meningkatkan partisipasi.

---

### **Bagaimana Solusi Ini Memenuhi Kebutuhan Pengguna**

- **Efisiensi dan Otomatisasi**  
  Dengan bot yang menangani moderasi dan manajemen role, admin dapat lebih fokus pada pengembangan komunitas tanpa harus menangani tugas rutin secara manual.
- **Pengelolaan Komunitas yang Lebih Terstruktur**  
  Penerapan sistem otomatisasi memastikan role dan aturan komunitas diterapkan secara konsisten.
- **Meningkatkan Aktivitas dan Partisipasi Anggota**  
  Dengan fitur interaktif yang menarik, anggota lebih termotivasi untuk tetap aktif di komunitas, meningkatkan interaksi dan memperkuat hubungan antaranggota.

Dengan solusi ini, sistem yang dikembangkan akan menciptakan komunitas Discord yang lebih efisien, menarik, dan mudah dikelola.

---

## Nomor 2: Pengujian

Dalam pengujian perangkat lunak untuk bot Discord berbasis JavaScript ini, kami menerapkan kombinasi metode pengujian black box dan white box guna memastikan semua fungsi berjalan sesuai harapan. Pengujian black box dilakukan dengan menguji antarmuka dan fungsionalitas bot tanpa melihat struktur internal kodenya. Misalnya, dalam pengujian ini, kami mengirim perintah melalui chat Discord untuk memverifikasi respons bot, seperti penghapusan pesan spam, pemberian role otomatis, dan penyampaian notifikasi acara. Sementara itu, metode white box testing melibatkan pengujian kode secara mendalam, seperti unit testing dan code coverage, untuk memastikan setiap modul dan fungsi internal beroperasi dengan benar. Dengan demikian, kedua metode ini saling melengkapi untuk mengidentifikasi bug, inkonsistensi, dan area yang perlu perbaikan.

Jenis pengujian yang diterapkan meliputi:

- **Unit Testing:** Menguji fungsi-fungsi individual, seperti fungsi moderasi dan manajemen role, untuk memastikan logika bisnis berfungsi sebagaimana mestinya.
- **Integration Testing:** Memastikan modul-modul yang berbeda, misalnya interaksi antara modul moderasi dan pengelolaan role, bekerja secara harmonis.
- **Functional Testing (Black Box):** Memverifikasi bahwa semua perintah dan fitur interaktif (seperti kuis atau polling) menghasilkan output yang sesuai dengan spesifikasi.
- **System Testing:** Menguji keseluruhan sistem pada lingkungan server Discord yang sebenarnya untuk menilai performa dan kestabilan dalam kondisi nyata.

Hasil pengujian menunjukkan bahwa bot berhasil melakukan moderasi otomatis, mengelola role anggota dengan konsisten, dan menyediakan fitur interaktif tanpa adanya error kritis. Beberapa bug minor yang muncul selama unit testing berhasil diperbaiki melalui iterasi perbaikan kode, sementara integrasi antara modul diuji kembali hingga mencapai kinerja optimal. Kesimpulan dari pengujian ini adalah bahwa perangkat lunak telah memenuhi spesifikasi fungsional dan non-fungsional yang telah ditetapkan, sehingga bot dapat diimplementasikan dalam lingkungan komunitas Discord dengan keandalan tinggi dan responsivitas yang baik.

---

## Nomor 3: Bahasa Pemrograman

Dalam proyek pengembangan bot Discord ini, bahasa pemrograman yang dipilih adalah **JavaScript** yang dijalankan di lingkungan **Node.js**. Pemilihan JavaScript didasarkan pada karakteristik proyek yang membutuhkan pengolahan event-driven dan asynchronous, yang sangat cocok untuk aplikasi real-time seperti bot Discord. Keunggulan lain dari JavaScript adalah ekosistemnya yang kaya dengan pustaka dan modul, terutama **Discord.js**, yang secara khusus dirancang untuk memudahkan interaksi dengan API Discord. Hal ini memungkinkan pengembangan fitur-fitur seperti moderasi otomatis, pengelolaan peran, dan fitur interaktif lainnya dengan lebih cepat dan efisien.

Platform pengembangan yang digunakan dalam proyek ini adalah aplikasi berbasis web yang berfungsi sebagai backend bot, yang kemudian diintegrasikan dengan server Discord untuk memberikan layanan secara real-time. Selama proses pengembangan, beberapa perangkat lunak pendukung juga digunakan, antara lain **Visual Studio Code** sebagai code editor, **Git** untuk version control. Untuk database, platform seperti **MongoDB** digunakan untuk menyimpan data interaksi dan log aktivitas pengguna. Kombinasi teknologi dan perangkat lunak pendukung ini memastikan bahwa bot dapat beroperasi secara andal dan responsif sesuai dengan kebutuhan pengguna.

## Nomor 4: Skema dan Diagram

### Skema Hardware

Hardware yang digunakan dalam perancangan bot Discord akan bergantung pada kebutuhan aplikasi bot dan skala penggunaannya. Berikut adalah poin-poin rinci kebutuhan hardware yang kami gunakan selama perancangan bot/aplikasi:

- Hosting: Disini kami menggunakan shared hosting alternatif yang gratisan untuk menjalankan bot-nya secara efisien dan mudah menggunakan https://bot-hosting.net/ , dimana sebagian besar kebutuhan hardware fisik dialihkan ke penyedia layanan hosting. Alasan kami memilih hosting ini selain gratis juga memiliki vCPU yang memadai untuk menjalankan Node.js dan menangani permintaan dari Discord API secara efisien. Hositng ini juga menawarkan bandwidth yang cukup untuk komunikasi real-time antara bot dan Discord API serta menjamin uptime yang tinggi sehingga bot dapat berjalan tanpa gangguan.Untuk pemilihan paketnya sendiri kami menggunakan paket yang standar dimana kami mendapatkan penggunaan vCPU sebanyak 25%, RAM sebanyak 512 MB, dan SSD sebanyak 2 GB.
- Perangkat Pengembangan: Laptop atau PC dengan spesifikasi standar (CPU minimal dual-core, RAM 4 GB, penyimpanan HDD/SSD) untuk pengembangan dan pengujian bot sebelum deployment.
- Penyimpanan: Minimal 5 GB untuk menyimpan kode bot, library, database lokal (jika diperlukan), dan file pendukung lainnya.

### Skema Software

Software memainkan peran penting dalam pengembangan dan operasional bot Discord. Berikut adalah rincian kebutuhan software yang biasa kami gunakan selama pengembangan:

- Sistem Operasi: Kami menggunakan OS Windows selama pengembangan karena sesuai dengan preferensi kami dan jenis hosting yang akan kami gunakan.
- Runtime Environment: Kami menggunakan Node.js sebagai runtime environment untuk menjalankan bot berbasis JavaScript. Versi yang kami gunakan adalah versi LTS terbaru untuk stabilitas.
- Library dan Framework
  - Discord.js: Library utama yang kami gunakan untuk berinteraksi dengan Discord API, memungkinkan bot untuk menerima perintah, mengirim pesan, dan memodifikasi channel atau role.
  - Express.js: Untuk membuat API tambahan jika bot memerlukan antarmuka web atau endpoint HTTP.
- Database: Kami menggunakan MongoDB karena ini merupakan pilihan populer untuk database NoSQL yang cocok untuk menyimpan data leveling, role management, atau konfigurasi server.
- Alat Pengembangan
  - Code Editor: Kami menggunakan VSCode selama proses pengembangan karena VSCode merupakan editor teks yang ringan, cepat, dan fleksibel untuk pengembangan Node.js. VSCode juga mendukung banyak ekstensi yang kami butuhkan selama perancangan dan editor teks ini memang populer saat-saat ini yang paling sering digunakan.
  - Version Control System: Untuk version control dan kolaborasi pengembangan kami menggunakan GitHub untuk membuat eksprimen tanpa memengaruhi kode utama, dan juga fitur pull requests untuk memeriksa kode sebelum penggabungan.
- Security Tools: Untuk mengelola dan melindungi kredensial seperti token bot atau kunci API, serta keamanan tambahan untuk melindungi dari serangan eksternal kami menggunakan dotenv karena pilihan ini adalah yang paling mudah dan simpel namun sangat worth it.

### Skema Database

Pada skema ini, bot atau aplikasi yang kami buat menerima perintah dari user melalui metode sendCommand dan user menerima respon melalui receiveResponse. Sedangkan bot bergantung pada database untuk berbagai operasi seperti menyimpan log aktivitas, mengambil data pengguna, atau memperbarui data server. Database juga menyimpan atribut-atribut yang dimiliki user yang kalian bisa lihat sendiri [disini](https://ibb.co/pvtzDKKr).

### Skema Actor

- **Sequence Diagram**: [Klik disini untuk melihat.](https://ibb.co/Zp9yVGBN)
- **Activity Diagram**: [Klik disini untuk melihat.](https://ibb.co/NgTZR8Cj)
- **Use Case Diagram**: [Klik disini untuk melihat.](https://ibb.co/xtkCMGM6)

---

## Nomor 5: Implementasi

Dalam proses implementasi sistem bot Discord berbasis JavaScript, langkah awal adalah menyiapkan lingkungan kerja yang terdiri dari konfigurasi perangkat lunak, perangkat keras, dan database. Pertama, kami menginstal Node.js dan package manager (npm) pada komputer pengembang untuk memastikan semua dependensi dan library, seperti Discord.js, tersedia. Selanjutnya, kami menggunakan editor kode seperti Visual Studio Code dan melakukan setup version control dengan Git untuk mengelola perubahan kode. Di samping itu, kami menyiapkan akun di platform hosting untuk deployment dan memastikan lingkungan server telah dikonfigurasi dengan benar. Persiapan ini juga mencakup pembuatan lingkungan pengujian lokal menggunakan emulator atau server Discord uji coba guna mensimulasikan interaksi pengguna.

Setelah lingkungan kerja siap, tahap implementasi dilanjutkan dengan penerapan komponen-komponen perangkat lunak sesuai desain. Pertama, kami mengembangkan modul-modul utama, seperti modul moderasi, pengelolaan peran, dan fitur interaktif, dengan mengacu pada spesifikasi dan diagram perancangan (misalnya activity diagram, use case, dan class diagram). Di sisi backend, pengaturan database (misalnya MongoDB) dilakukan untuk menyimpan data log aktivitas, konfigurasi peran, dan statistik pengguna. Langkah selanjutnya melibatkan integrasi antara kode bot dan API Discord, sehingga setiap perintah yang dikirim melalui server Discord dapat diproses secara real-time. Pada akhirnya, kami melakukan pengujian terintegrasi untuk memastikan bahwa setiap komponen berfungsi secara sinergis sesuai dengan desain yang telah ditetapkan. Dengan iterasi pengujian dan debugging, sistem disempurnakan hingga mencapai kinerja optimal sebelum akhirnya diterapkan ke lingkungan produksi.

[Screenshot 1](https://ibb.co/gkN2rS1)
[Screenshot 2](https://ibb.co/N60chrf9)
[Screenshot 3](https://ibb.co/7J0d8CNd)
[Screenshot 4](https://ibb.co/Wv9Ykyy2)
[Screenshot 5](https://ibb.co/G32FydKb)
