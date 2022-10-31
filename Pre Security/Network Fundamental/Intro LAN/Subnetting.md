Seperti yang telah kita bahas sebelumnya di seluruh modul sejauh ini, Jaringan dapat ditemukan dalam segala bentuk dan ukuran - mulai dari kecil hingga besar. *Subnetting* adalah istilah yang diberikan untuk membagi jaringan menjadi lebih kecil, jaringan miniatur di dalam dirinya sendiri. Anggap saja seperti mengiris kue untuk teman-teman Anda. Hanya ada sejumlah kue untuk dibagikan, tetapi semua orang menginginkan sepotong. *Subnetting* adalah Anda memutuskan siapa yang mendapat potongan apa & memesan sepotong kue metaforis ini.

Ambil contoh bisnis, misalnya; Anda akan memiliki departemen yang berbeda seperti:
* Akuntansi
* Keuangan
* SDM(Sumberdaya manusia)

![subnetting](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/subnet22.png)

Apabila anda tahu ke mana harus mengirim informasi dalam kehidupan nyata ke departemen yang benar, jaringan juga perlu tahu. Administrator jaringan menggunakan *subnetting* untuk mengkategorikan dan menetapkan bagian tertentu dari jaringan untuk mencerminkan hal ini.

*Subnetting* dibuat dengan membagi jumlah host yang dapat ditampung dalam jaringan, diwakili oleh nomor yang disebut `subnet mask`. Mari kita lihat kembali diagram kita dari ruang pertama dalam modul ini:

![subnet1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/subnet1.png)

Seperti yang kita ingat, alamat IP terdiri dari empat bagian yang disebut oktet. Hal yang sama berlaku untuk subnet mask yang juga direpresentasikan sebagai sejumlah empat byte (32 bit), mulai dari 0 hingga 255 (0-255).

*Subnet* menggunakan alamat IP dalam tiga cara berbeda:
1. Identifikasi alamat jaringan
2. Identifikasi alamat host
3. Identifikasi *gateway default*

Mari kita bagi ketiga cara itu kedalam tabel agar lebih mudah di pahami:

|Tipe| Tujuan| Penjelasan| Contoh|
|:--:|:-----:|:---------:|:-----:|
|Alamat Network|Alamat ini mengidentifikasi awal jaringan yang sebenarnya dan digunakan untuk mengidentifikasi keberadaan jaringan.|Misalnya, perangkat dengan alamat IP 192.168.1.100 akan berada di jaringan yang diidentifikasi oleh 192.168.1.0|192.168.1.0|
|Alamat Host|Alamat IP di sini digunakan untuk mengidentifikasi perangkat di subnet|Sebagai contoh sebuah perangkat akan memiliki alamat jaringan 192.168.1.1| 192.168.1.100|
|*Default Gateway*| Alamat gateway default adalah alamat khusus yang ditetapkan untuk perangkat di jaringan yang mampu mengirim informasi ke jaringan lain|Data apa pun yang perlu masuk ke perangkat yang tidak berada di jaringan yang sama (yaitu tidak berada di 192.168.1.0) akan dikirim ke perangkat ini. Perangkat ini dapat menggunakan alamat host apa pun tetapi biasanya menggunakan alamat host pertama atau terakhir dalam jaringan (1 atau .254)| 192.168.1.254|

Sekarang, di jaringan kecil seperti di rumah, Anda akan berada di satu subnet karena kemungkinan kecil Anda membutuhkan lebih dari 254 perangkat yang terhubung pada satu waktu. Namun, tempat-tempat seperti bisnis dan kantor akan memiliki lebih banyak perangkat ini (PC, printer, kamera, dan sensor), di mana subnetting dilakukan.

*Subnetting* memiliki beberapa keuntungan seperti:
* Efisiensi
* Keamanan
* Kontrol penuh

Kami akan mengeksplorasi dengan tepat bagaimana *subnetting* memberikan manfaat ini di kemudian hari; namun, untuk saat ini, yang perlu kita pahami hanyalah elemen keamanannya. Mari kita ambil contoh kafe di pinggir jalan. Kafe ini akan memiliki dua jaringan:
1. Satu untuk karyawan, mesin kasir, dan perangkat lain untuk fasilitas
2. Satu untuk pengunjung gunakan sebagai hotspot

*Subnetting* memungkinkan Anda untuk memisahkan kedua kasus penggunaan ini satu sama lain sambil memiliki manfaat koneksi ke jaringan yang lebih besar seperti Internet.
