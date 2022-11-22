Kami secara singkat menyentuh file log dan di mana mereka dapat ditemukan di Dasar-Dasar Linux Bagian 1. Namun, mari kita rekap dengan cepat. Terletak di direktori `/var/log`, file dan folder ini berisi informasi logging untuk aplikasi dan layanan yang berjalan di sistem Anda. Sistem Operasi (OS) telah menjadi sangat bagus dalam mengelola log ini secara otomatis dalam proses yang dikenal sebagai "rotating".

Saya telah meng *highlight* beberapa log dari tiga layanan yang berjalan di mesin Ubuntu:
* Sebuah web server Apache2
* Log untuk layanan fail2ban, yang digunakan untuk memantau percobaan brute force, misalnya
* Layanan UFW yang digunakan sebagai firewall

![log1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/log1.png)

Layanan dan log ini adalah cara yang bagus untuk memantau kesehatan sistem Anda dan melindunginya. Tidak hanya itu, log untuk layanan seperti server web berisi informasi tentang setiap permintaan - memungkinkan pengembang atau administrator untuk mendiagnosis masalah kinerja atau menyelidiki aktivitas penyusup. Misalnya, dua jenis file log yang menarik di bawah ini:
* access log
* error log

![log2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/log2.png)

Ada, tentu saja, log yang menyimpan informasi tentang bagaimana OS berjalan sendiri dan tindakan yang dilakukan oleh pengguna, seperti upaya otentikasi.
