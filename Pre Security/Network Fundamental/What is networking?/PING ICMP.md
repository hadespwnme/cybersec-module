Ping adalah salah satu alat jaringan paling mendasar yang tersedia untuk kita. Ping menggunakan paket ICMP (Internet Control Message Protocol) untuk menentukan kinerja koneksi antar perangkat, misalnya, jika koneksi ada atau dapat diandalkan.

Waktu yang dibutuhkan untuk paket ICMP yang melakukan "perjalanan" antar perangkat diukur dengan ping, seperti pada gambar di bawah. Pengukuran ini dilakukan dengan menggunakan paket gema ICMP dan kemudian balasan gema ICMP dari perangkat target.

Ping dapat dilakukan terhadap perangkat di jaringan, seperti jaringan rumah anda atau *resource* seperti situs web. Alat ini dapat dengan mudah digunakan dan diinstal pada Sistem Operasi (OS) seperti Linux dan Windows. Sintaks untuk melakukan ping sederhana adalah **ping `ip address or url websites`**. Mari kita lihat ini di tangkapan layar di bawah ini.

![ping](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/What%20is%20networking%3F/Image/ping1.png)

Di sini kita melakukan ping ke perangkat yang memiliki *private address* `192.168.1.254`. Ping memberi tahu kami bahwa kami telah mengirim enam paket ICMP, yang semuanya diterima dengan waktu rata-rata 5,3 detik.
