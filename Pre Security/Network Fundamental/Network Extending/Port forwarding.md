*Port forwarding* adalah komponen penting dalam menghubungkan aplikasi dan layanan ke Internet. Tanpa penerusan port, aplikasi dan layanan seperti server web hanya tersedia untuk perangkat dalam jaringan langsung yang sama.

Ambil jaringan di bawah ini sebagai contoh. Di dalam jaringan ini, server dengan alamat IP "192.168.1.10" menjalankan server web pada port 80. Hanya dua komputer lain di jaringan ini yang dapat mengaksesnya (ini dikenal sebagai intranet).

![pforward](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/portforwarding-int.png)

Jika administrator menginginkan situs web dapat diakses oleh publik (menggunakan Internet), mereka harus menerapkan *port forwarding*, seperti pada gambar di bawah ini:

![portforward](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/portforwarding.png)

Dengan desain ini, Jaringan #2 sekarang dapat mengakses server web yang berjalan di Jaringan #1 menggunakan alamat IP publik dari Jaringan #1 (82.62.51.70).

Sangat mudah untuk mengacaukan port forwarding dengan perilaku firewall (teknologi yang akan kita bahas di tugas selanjutnya). Namun, pada tahap ini, pahami saja bahwa penerusan port membuka port tertentu (ingat cara kerja paket). Sebagai perbandingan, firewall menentukan apakah lalu lintas dapat melewati port ini (bahkan jika port ini dibuka dengan penerusan port).

Penerusan port dikonfigurasi pada router jaringan.
