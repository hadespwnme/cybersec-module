### What's a router?
Adalah tugas router untuk menghubungkan jaringan dan meneruskan data di antara mereka. Ini dilakukan dengan menggunakan perutean (karenanya dinamai router!).

*Routing* adalah label yang diberikan untuk proses perjalanan data melintasi jaringan. Perutean melibatkan pembuatan jalur antar jaringan sehingga data ini dapat berhasil dikirimkan. Router beroperasi pada Layer 3 dari model OSI. Mereka sering menampilkan antarmuka interaktif (seperti situs web atau konsol) yang memungkinkan administrator untuk mengonfigurasi berbagai aturan seperti penerusan *port* atau *firewall*.

Perutean berguna saat perangkat dihubungkan oleh banyak jalur, seperti pada contoh gambar di bawah ini, di mana jalur yang paling optimalah yang diambil:

![routing](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/routing2.png)

Router adalah perangkat khusus dan tidak melakukan fungsi yang sama seperti *switch*.

Kita dapat melihat bahwa jaringan Komputer A terhubung ke jaringan Komputer B dengan dua router di tengahnya. Pertanyaannya adalah: jalan apa yang akan diambil? Protokol yang berbeda akan memutuskan jalur mana yang harus diambil, faktor-faktornya meliputi:
* Jalur apa yang terpendek
* Jalur apa yang paling bisa diandalkan?
* Jalur mana yang memiliki media yang lebih cepat (misalnya tembaga atau serat)?

### Whats a Switch
Switch adalah perangkat jaringan khusus yang bertanggung jawab untuk menyediakan sarana untuk menghubungkan ke beberapa perangkat. Switch dapat memfasilitasi banyak perangkat (dari 3 hingga 63) menggunakan kabel Ethernet.

Switch dapat beroperasi pada layer 2 dan layer 3 dari model OSI. Namun, ini eksklusif dalam arti bahwa *Switch* di Layer 2 tidak dapat beroperasi pada layer 3.

Ambil contoh, misalnya, *switch* lapisan 2 dalam gambar di bawah ini. *switch* ini akan meneruskan frame (ingat ini bukan lagi paket karena protokol IP telah dihapus) ke perangkat yang terhubung menggunakan alamat MAC mereka.

![switch](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/layer2switch.png)

*Switch* ini bertanggung jawab penuh untuk mengirim frame ke perangkat yang benar.

Sekarang, mari beralih ke *switch* layer 3. *Switch* ini lebih canggih daripada yang ada di layer 2, karena mereka dapat melakukan beberapa tanggung jawab router. Yaitu, mengirim frame ke perangkat (seperti yang dilakukan lapisan 2) dan merutekan paket ke perangkat lain menggunakan protokol IP.

Mari kita lihat diagram di bawah ini dari switch layer 3 yang sedang beraksi. Kita dapat melihat bahwa ada dua alamat IP:
* 192.168.1.1
* 192.168.2.1

Sebuah teknologi yang disebut VLAN (*Virtual Local Area Network*) memungkinkan perangkat tertentu dalam jaringan untuk dipisahkan secara virtual. Pemisahan ini berarti mereka semua dapat memperoleh manfaat dari hal-hal seperti koneksi Internet, tetapi diperlakukan secara terpisah. Pemisahan jaringan ini memberikan keamanan karena itu berarti bahwa aturan yang berlaku menentukan bagaimana perangkat tertentu berkomunikasi satu sama lain. [Segregasi](https://kbbi.web.id/segregasi) ini digambarkan dalam diagram di bawah ini:

![vlan](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/vlans.png)

Dalam konteks diagram di atas, "Departemen Penjualan" dan "Departemen Akuntansi" akan dapat mengakses Internet, tetapi tidak dapat berkomunikasi satu sama lain (walaupun keduanya terhubung ke *switch* yang sama).
