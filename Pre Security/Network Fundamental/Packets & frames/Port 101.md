Mungkin sesuai dengan namanya, port adalah titik penting di mana data dapat dipertukarkan. Pikirkan pelabuhan dan pelabuhan. Kapal yang hendak berlabuh di pelabuhan harus menuju pelabuhan yang sesuai dengan ukuran dan fasilitas yang ada di kapal. Ketika kapal berbaris, itu akan terhubung ke pelabuhan di pelabuhan. Ambil contoh, bahwa kapal pesiar tidak dapat berlabuh di pelabuhan yang dibuat untuk kapal penangkap ikan dan sebaliknya.

Port ini menerapkan apa yang bisa diparkir dan di mana — jika tidak kompatibel, tidak bisa parkir di sini. Perangkat jaringan juga menggunakan port untuk menegakkan aturan ketat saat berkomunikasi satu sama lain. Ketika koneksi telah dibuat (kembali ke ruang model OSI), setiap data yang dikirim atau diterima oleh perangkat akan dikirim melalui port ini. Dalam komputasi, port adalah nilai numerik antara 0 dan 65535 (65.535).

Because ports can range from anywhere between 0-65535, there quickly runs the risk of losing track of what application is using what port. A busy harbour is chaos! Thankfully, we associate applications, software and behaviours with a standard set of rules. For example, by enforcing that any web browser data is sent over port 80, software developers can design a web browser such as Google Chrome or Firefox to interpret the data the same way as one another.

Ini berarti bahwa semua browser web sekarang berbagi satu aturan umum: data dikirim melalui port 80. Bagaimana browser terlihat, terasa, dan mudah digunakan tergantung pada keputusan desainer atau pengguna.

Sementara aturan standar untuk data web adalah port 80, beberapa protokol lain telah dialokasikan aturan standar. Port apa pun yang berada dalam 0 dan 1024 (1.024) dikenal sebagai port umum. Mari jelajahi beberapa protokol lain di bawah ini:

|Protokol|Nomor Port|Penjelasan|
|:------:|:--------:|:--------:|
|*File Transfer Protocol(FTP)*|21|Protokol ini digunakan oleh aplikasi berbagi file yang dibangun dengan model klien-server, artinya Anda dapat mengunduh file dari lokasi terpusat.|
|*Secure Shell*(SSH)|22|Protokol ini digunakan untuk login dengan aman ke sistem melalui antarmuka berbasis teks untuk manajemen.|
|*HyperText Transfer Protocol*(HTTP)|80|Protokol ini mendukung *World Wide Web* (WWW)! Browser Anda menggunakan ini untuk mengunduh teks, gambar, dan video halaman web.|
|*HyperText Transfer Protocol Secure*(HTTPS)|443|Protokol ini melakukan hal yang sama persis seperti di atas; namun, dengan aman menggunakan enkripsi.
|*Server Message Block*(SMB)|445|Protokol ini mirip dengan File Transfer Protocol (FTP); namun, selain file, SMB memungkinkan Anda berbagi perangkat seperti printer.|
|*Remote Desktop Protocol*(RDP)|3389|Protokol ini adalah cara yang aman untuk masuk ke sistem menggunakan antarmuka desktop visual (sebagai lawan dari batasan berbasis teks dari protokol SSH).|

Kami hanya membahas secara singkat protokol yang lebih umum dalam keamanan siber. Anda dapat menemukan tabel 1024 port umum yang terdaftar untuk informasi lebih lanjut.

Yang perlu diperhatikan di sini adalah bahwa protokol ini hanya mengikuti standar. Yaitu. Anda dapat mengelola aplikasi yang berinteraksi dengan protokol ini pada port yang berbeda selain yang standar (menjalankan server web pada 8080 alih-alih port standar 80). Perhatikan, bagaimanapun, aplikasi akan menganggap bahwa standar sedang diikuti, jadi Anda harus memberikan tanda titik dua (:) bersama dengan nomor port.

