TCP (atau singkatnya *Transmission Control Protocol*) adalah salah satu dari aturan yang digunakan dalam jaringan.

Protokol ini sangat mirip dengan model OSI yang telah kita bahas sebelumnya di modul sejauh ini. Protokol TCP/IP terdiri dari empat lapisan dan bisa dibilang hanya merupakan versi ringkasan dari model OSI. Lapisan-lapisan ini adalah:
* *Application*
* *Transport*
* *Internet*
* *Network Interface*

Sangat mirip dengan cara kerja model OSI, informasi ditambahkan ke setiap lapisan model TCP saat potongan data (atau paket) melintasinya. Seperti yang Anda ingat, proses ini dikenal sebagai enkapsulasi - di mana kebalikan dari proses ini adalah dekapsulasi.

Salah satu fitur yang menentukan dari TCP adalah **berbasis koneksi**, yang berarti bahwa TCP harus membuat koneksi antara klien dan perangkat yang bertindak sebagai server **sebelum** data dikirim.

Karena itu, TCP menjamin bahwa setiap data yang dikirim akan diterima oleh yang yang lain. Proses ini dinamakan *Three-way handsshake*, yang akan segera kita bahas. Tabel yang ada dibawah ini membandingkan kelebihan dan kekurangan TCP:

|Kelebihan TCP|Kekurangan TCP|
|:-----------:|:------------:|
|Menjamin Integritas data|Membutuhkan koneksi yang andal antara kedua perangkat. Jika satu potongan kecil data tidak diterima, maka seluruh potongan data tidak dapat digunakan dan harus dikirim ulang.|
|Mampu menyinkronkan dua perangkat untuk mencegah satu sama lain dibanjiri data dengan urutan yang salah.|Koneksi yang lambat dapat menghambat perangkat lain karena koneksi akan dicadangkan di perangkat lain sepanjang waktu.|
|Melakukan lebih banyak proses untuk keandalan|TCP secara signifikan lebih lambat daripada UDP karena lebih banyak pekerjaan (komputasi) yang harus dilakukan oleh perangkat yang menggunakan protokol ini.|

Paket TCP berisi berbagai bagian informasi yang dikenal sebagai *header* yang ditambahkan dari enkapsulasi. Mari kita jelaskan beberapa header penting dalam tabel di bawah ini:

|Header|Deskripsi|
|:----:|:-------:|
|*Source Port*|Nilai ini adalah port yang dibuka oleh pengirim untuk mengirim paket TCP. Nilai ini dipilih secara acak (keluar port 0-65535 yang belum digunakan pada saat itu).|
|*Destination Port*|Nilai ini adalah nomor port yang dijalankan aplikasi atau layanan di host jarak jauh (yang menerima data); misalnya, server web berjalan di port 80. Berbeda dengan port sumber, nilai ini tidak dipilih secara acak.|
|*Source IP*|Ini adalah alamat IP perangkat yang mengirimkan paket.|
|*Destination IP*|Ini adalah alamat IP perangkat yang menjadi tujuan paket tersebut.|
|*Sequence Number	*|Saat koneksi terjadi, bagian pertama dari data yang dikirimkan diberi nomor acak. Kami akan menjelaskan ini lebih mendalam lebih lanjut.|
|*Acknowledgement Number*|Setelah suatu data diberi nomor urut, maka nomor untuk data selanjutnya akan memiliki nomor urut + 1. Kami juga akan menjelaskannya lebih mendalam.|
|*Checksum*|Nilai inilah yang memberikan integritas TCP. Perhitungan matematis dibuat di mana output diingat. Saat perangkat penerima melakukan perhitungan matematis, data pasti rusak jika output berbeda dari yang dikirim.|
|*Data*|Header ini adalah tempat penyimpanan data, yaitu byte dari file yang sedang dikirim.|
|*Flag*|Header ini menentukan bagaimana paket harus ditangani oleh salah satu perangkat selama proses *handshake*. Tanda tertentu akan menentukan perilaku tertentu, yang akan kami jelaskan di bawah ini|

Selanjutnya, kita akan membahas *Three-way handshake* - istilah yang diberikan untuk proses yang digunakan untuk membuat koneksi antara dua perangkat.*Three-way handshake* berkomunikasi menggunakan beberapa pesan khusus - tabel di bawah ini menyoroti pesan utama:
|Langkah|Pesan|Deskripsi|
|:-----:|:---:|:-------:|
|1|SYN|Pesan SYN adalah paket awal yang dikirim oleh klien selama proses *handshake*. Paket ini digunakan untuk memulai koneksi dan menyinkronkan kedua perangkat bersama-sama (kami akan menjelaskannya lebih lanjut nanti).|
|2|SYN/ACK|Paket ini dikirim oleh perangkat penerima (server) untuk mengakui upaya sinkronisasi dari klien.|
|3|ACK|Paket *acknowledgement* dapat digunakan oleh klien atau server untuk mengakui bahwa serangkaian pesan/paket telah berhasil diterima.|
|4|DATA|Setelah koneksi dibuat, data (seperti byte file) dikirim melalui pesan "DATA".|
|5|FIN|Paket ini digunakan untuk menutup koneksi dengan bersih (dengan benar) setelah selesai.|
|#|RST|Paket ini tiba-tiba mengakhiri semua komunikasi. Ini adalah pilihan terakhir dan menunjukkan ada beberapa masalah selama proses berlangsung. Misalnya, jika layanan atau aplikasi tidak berfungsi dengan benar, atau sistem mengalami kesalahan seperti sumber daya rendah.|

Gambar di bawah menunjukkan proses *Three-way handshake* normal antara Alice dan Bob. Dalam kehidupan nyata, ini akan berada di antara dua perangkat.

![tcphandshake](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Packets%20%26%20frames/Image/tcphandshake.png)

Setiap data yang dikirim diberikan urutan nomor acak dan direkonstruksi menggunakan urutan nomor ini dan bertambah dengan 1. Kedua komputer harus menyetujui urutan nomor yang sama agar data dikirim dalam urutan yang benar. Perintah ini disepakati selama tiga langkah:
1. SYN:Inilah Nomor Urutan Awal (ISN) saya untuk disinkronkan dengan (0)
2. SYN/ACK: Inilah Nomor Urutan Awal (ISN) saya untuk disinkronkan dengan (5.000), dan saya MENGETAHUI urutan nomor awal Anda (0)
3. ACK: SAYA MENGETAHUI Nomor Urutan Awal (ISN) Anda sebesar (5.000), berikut adalah beberapa data yang merupakan ISN+1 saya (5.000 + 1)
|Perangkat|Nomor Urut Awalan(ISN)|Nomor Urut Akhir|
|:-------:|:--------------------:|:--------------:|
|Client(Pengirim)|0|0+1=1|
|Client(Pengirim)|1|1+1=2|
|Client(Pengirim)|2|2+1=3|

###TCP Closing a Connection:
Mari kita jelaskan dengan cepat proses di balik TCP menutup koneksi. Pertama, TCP akan menutup koneksi setelah perangkat menentukan bahwa perangkat lain telah berhasil menerima semua data.

Karena TCP mencadangkan sumber daya sistem pada perangkat, hal terbaik adalah menutup koneksi TCP sesegera mungkin.

Untuk memulai penutupan koneksi TCP, perangkat akan mengirimkan paket "FIN" ke perangkat lain. Tentu saja, dengan TCP, perangkat lain juga harus mengakui paket ini.

Mari tunjukkan proses ini menggunakan Alice dan Bob seperti yang kita lakukan sebelumnya.

![tcphandshake2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Packets%20%26%20frames/Image/tcphandshake-2.png)

Dalam ilustrasi, kita dapat melihat bahwa Alice telah mengirimkan paket "FIN" kepada Bob. Karena Bob menerima ini, dia akan memberi tahu Alice bahwa dia menerimanya dan dia juga ingin menutup koneksi (menggunakan FIN). Alice telah mendengar Bob dengan keras dan jelas dan akan memberi tahu Bob bahwa dia mengakui hal ini.
