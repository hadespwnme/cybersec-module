![net](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/network.png)

Lapisan ketiga dari model OSI (lapisan jaringan) adalah tempat keajaiban perutean & perakitan ulang data terjadi (dari potongan kecil ini ke potongan yang lebih besar). Pertama, perutean hanya menentukan jalur paling optimal di mana potongan data ini harus dikirim.

Sementara beberapa protokol pada lapisan ini menentukan dengan tepat apa jalur "optimal" yang harus diambil data untuk mencapai perangkat, kita seharusnya mengetahui keberadaannya hanya pada tahap modul jaringan ini. Secara singkat, protokol ini termasuk **OSPF** (**O**pen **S**hortest **P**ath **F**irst) dan **RIP** (**R**outing **I**nformation **P**rotocol). Faktor-faktor yang menentukan rute apa yang diambil ditentukan oleh hal-hal berikut:
* Jalur apa yang terpendek? Yaitu jalur yang memiliki jumlah perangkat paling sedikit yang perlu dilalui paket.
* Jalan apa yang paling bisa diandalkan? Yaitu. apakah paket telah hilang di jalur itu sebelumnya?
* Jalur mana yang memiliki koneksi fisik lebih cepat? Yaitu. apakah satu jalur menggunakan sambungan tembaga (lebih lambat) atau serat (jauh lebih cepat)?

Pada lapisan ini, semuanya ditangani melalui alamat IP seperti 192.168.1.100. Perangkat seperti router yang mampu mengirimkan paket menggunakan alamat IP dikenal sebagai perangkat Layer 3 — karena mereka mampu bekerja pada lapisan ketiga model OSI.

![rout](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/routing2.png)
