Mengingat dari tugas kami sebelumnya bahwa perangkat dapat memiliki dua pengidentifikasi: Alamat MAC dan alamat IP, protokol ARP atau disingkat *Address Resolution Protocol*, adalah teknologi yang bertanggung jawab untuk memungkinkan perangkat mengidentifikasi diri mereka sendiri di jaringan.

Sederhananya, protokol ARP memungkinkan perangkat untuk mengaitkan alamat MAC-nya dengan alamat IP di jaringan. Setiap perangkat di jaringan akan menyimpan log alamat MAC yang terkait dengan perangkat lain.

Ketika perangkat ingin berkomunikasi dengan yang lain, mereka akan mengirim siaran ke seluruh jaringan untuk mencari perangkat tertentu. Perangkat dapat menggunakan protokol ARP untuk menemukan alamat MAC (karena itu pengenal fisik) perangkat untuk komunikasi.

### Bagaimana ARP bekerja?
Setiap perangkat dalam jaringan memiliki buku besar untuk menyimpan informasi, yang disebut cache. Dalam konteks protokol ARP, cache ini menyimpan pengidentifikasi perangkat lain di jaringan.

Untuk memetakan kedua pengidentifikasi ini bersama-sama (alamat IP dan alamat MAC), protokol ARP mengirimkan dua jenis pesan:
1. Permintaan ARP / ARP request
2. Jawaban ARP / ARP reply

Ketika **ARP Request** dikirim, sebuah pesan disiarkan ke setiap perangkat lain yang ditemukan di jaringan oleh perangkat, menanyakan apakah alamat MAC perangkat cocok dengan alamat IP yang diminta. Jika perangkat memiliki alamat IP yang diminta, **ARP Reply** dikembalikan ke perangkat awal untuk mengakui hal ini. Perangkat awal sekarang akan mengingat ini dan menyimpannya di dalam cache (entri ARP).

This process is illustrated in the diagram below:

![arp](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/b27c024d90342c60dd5cb35765e7ed7b.png)

