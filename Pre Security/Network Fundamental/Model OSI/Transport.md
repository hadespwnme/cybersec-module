![transport](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/transport.png)

Layer 4 dari model OSI memainkan peran penting dalam mentransmisikan data melalui jaringan dan bisa sedikit sulit untuk dipahami. Ketika data dikirim antar perangkat, itu mengikuti salah satu dari dua protokol berbeda yang diputuskan berdasarkan beberapa faktor:
* TCP
* UDP

Mari kita mulai dengan TCP. **T**ransmision **C**ontrol **P**rotocol(TCP). Potensi sesuai dengan namanya, protokol ini dirancang dengan mempertimbangkan keandalan dan jaminan. Protokol ini mencadangkan koneksi konstan antara dua perangkat untuk jumlah waktu yang diperlukan untuk mengirim dan menerima data.

Tidak hanya itu, tetapi TCP juga memasukkan pengecekan kesalahan ke dalam desainnya. Pemeriksaan kesalahan adalah bagaimana TCP dapat menjamin bahwa data yang dikirim dari potongan kecil di lapisan sesi (lapisan 5) kemudian telah diterima dan dipasang kembali dalam urutan yang sama.

Mari kita rangkum kelebihan dan kekurangan TCP pada tabel di bawah ini:

|Keuntungan|Kekurangan|
|:--------:|:--------:|
|Menjamin keakuratan data|Membutuhkan koneksi yang andal antara kedua perangkat. Jika satu potongan kecil data tidak diterima, maka seluruh potongan data tidak dapat digunakan|
|Mampu menyinkronkan dua perangkat untuk mencegah satu sama lain dibanjiri data.|Koneksi yang lambat dapat menghambat perangkat lain karena koneksi akan disimpan di komputer penerima sepanjang waktu.|
|Melakukan lebih banyak proses untuk keandalan.|TCP is significantly slower than UDP because more work has to be done by the devices using this protocol.|

TCP digunakan untuk situasi seperti berbagi file, menjelajah internet atau mengirim email. Penggunaan ini karena layanan ini membutuhkan data yang akurat dan lengkap (tidak ada gunanya memiliki setengah file!).

Pada diagram di bawah ini, kita dapat melihat bagaimana gambar anjing dipecah menjadi potongan-potongan kecil data (dikenal sebagai paket) dari "server web", di mana "komputer" mengkonstruksi ulang gambar anjing ke dalam urutan yang benar .

![tcp](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/tcpdog.png)

Sekarang mari kita beralih ke *User Datagram Protocol* (atau disingkat UDP). Protokol ini hampir tidak secanggih saudaranya - protokol TCP. Itu tidak membanggakan banyak fitur yang ditawarkan oleh TCP, seperti pengecekan kesalahan dan keandalan. Faktanya, data apa pun yang dikirim melalui UDP dikirim ke komputer apakah itu sampai di sana atau tidak. Tidak ada sinkronisasi antara kedua perangkat atau jaminan; hanya berharap untuk yang terbaik, dan semoga saja.

Meskipun ini terdengar tidak menguntungkan, tapi tetap memiliki kelebihannya, yang akan kami tata dalam tabel di bawah ini:

|Keuntungan|Kekurangan|
|:--------:|:--------:|
|UDP lebih cepat dari TCP|UDP tidak peduli dengan file yang sudah dikirimkan|
|UDP meninggalkan lapisan aplikasi (perangkat lunak pengguna) untuk memutuskan apakah ada kontrol atas seberapa cepat paket dikirim.|Ini cukup fleksibel untuk pengembang perangkat lunak dalam pengertian ini.|
|UDP tidak memesan koneksi berkelanjutan pada perangkat seperti TCP|Ini berarti bahwa koneksi yang tidak stabil menghasilkan pengalaman yang buruk bagi pengguna.|

Menggunakan contoh yang sama seperti sebelumnya, sekarang kita dapat melihat bahwa hanya Paket #1 dan #3 yang telah diterima oleh "Komputer", yang berarti bahwa setengah dari gambar hilang.

![udp](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/udpdog.png)

UDP berguna dalam situasi di mana ada potongan kecil data yang dikirim. Misalnya, protokol yang digunakan untuk menemukan perangkat (ARP dan DHCP yang kita bahas pada bagian LAN) atau file yang lebih besar seperti streaming video (di mana tidak apa-apa jika beberapa bagian dari video menjadi piksel. Piksel hanyalah bagian yang hilang dari data!)
