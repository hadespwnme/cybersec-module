Untuk menjaga komunikasi dan ketertiban, perangkat perlu di mengindentifikasi dan diidentifikasikan didalam jaringan.
Apa gunanya anda tidak tahu dengan siapa anda berbicara pada kemaren?

Perangkat dalam jaringan mirip dengan manusia, bisa di identifikasi kan menggunakan dua cara:
* Nama
* Sidikjari

Sekarang kita bisa merubah nama didalam akta kita, akan tetapi bagaimanapun kita tidak bisa mengubah sidik jari kita.
Setiap manusia memiliki set sidikjari, jadi bagaimanapun kita mengubah nama kita masih ada identitas dibalik itu. Perangkat memiliki hal yang sama, ada dua cara untuk mengindentifikasi nya dan yang satu dapat di tembus.
* *IP address*
* *Media Access Control*(MAC) address -- ini mirip seperti *serial number*

## IP Address
Singkatnya, alamat IP(atau internet protocol) dapat digunakan untuk identifikasi host dalam jaringan dengan jangka waktu. Dimana kemudian almat IP tersebut dapat di asosiasikan dengan perangkat lain tanpa mengubah alamat nya.
Mari kita pisahkan alamat IP dibawah ini:

![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/What%20is%20networking%3F/Image/octets.png)

Sebuah alamat ip adalah sebuah set angka yang dibagi menjadi empat octets. Nilai setiap octet akan diringkas menjadi alamat ip dari perangkat pada jaringan. Angka ini dihitung dengan teknik yang disebut pengalamatan ip dan *subnetting*, tapi ini untuk hari lain pembahasan nya. 
Yang penting adalah disini dipahami bahwa alamat ip dapat berubah dari perangkat ke perangkat, tapi tidak bisa aktif secara bersamaan lebih dari sekali dalam jaringan yang sama.

*IP address* mengikuti satu set standar yang disebut protokol. Protokol ini adalah tulang punggung jaringan dan memaksa banyak perangkat untuk berkomunikasi menggunakan bahasa yang sama. 
Untuk bisa datang pada lain waktu. Namun kita harus ingat bahwa perangkat bisa berada pada jaringan publik maupun *private*. Tergantung mereka menentukan alamat IP, mau publik ataupun *private*.
|Perangkat|Alamat IP|Tipe alamat IP|
|:-------:|:-------:|:------------:|
|DESKTOP-KJE57FD|192.168.1.77|*Private*|
|DESKTOP-KJE57FD|86.157.52.21|Publik|
|CMNatic-PC|192.168.1.74|*Private*|
|CMNatic-PC|86.157.52.21|Publik|

![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/What%20is%20networking%3F/Image/1.png)

Kedua perangkat ini dapat menggunakan alamat ip publik mereka untuk berkomunikasi satu sama lain. IP publik diberika oleh Internet Services Provider(ISP) dengan biaya bulanan (tagihanmu!)
![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/What%20is%20networking%3F/Image/2.png)

Semakin banyak perangkat yang terhubung, semakin sulit untuk mendapatkan alamat IP yang umum. Sebagai contoh, Cisco, sebagai salah satu raksasa dalam perindustrian jaringan. Bahwa akan ada 50 miliar perangkat yang terhubung pada 2021. ([CISCO 2021](https://www.cisco.com/c/dam/en_us/about/ac79/docs/innov/IoT_IBSG_0411FINAL.pdf))
Memasuki versi alamat IP. Sejauh ini kita hanya membahas satu versi dari *Internet Protocol Schema* yang kita tahu sebagai IPv4. Yang menggunakan sistem penomoran 2^32 alamat IP(4.29 miliar), sehingga anda bisa melihat mengapa adanya kekurangan.

IPv6 adalah iterasi baru dari skema peng-alamatan IP untuk membantu mengatasi masalah ini.
Meski terlihat menakutkan, tapi ini memberikan keuntungan:
1. Mendukung lebih dari 2^128 alamat ip (340 miliar lebih), menyelesaikan isu isu yang ada pada IPv4.
2. Lebih efisien karena metodologi baru.
 
Screenshot dibawah ini membandingkan antara IPv6 dan IPv4.
![ipv6](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/What%20is%20networking%3F/Image/ipv6.png)

