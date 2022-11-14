*Virtual Private Network* (atau singkatnya VPN) adalah teknologi yang memungkinkan perangkat di jaringan terpisah untuk berkomunikasi secara aman dengan membuat jalur khusus antara satu sama lain melalui Internet (dikenal sebagai *tunnel*). Perangkat yang terhubung dalam terowongan ini membentuk jaringan pribadinya sendiri.

Misalnya, hanya perangkat dalam jaringan yang sama (seperti dalam bisnis) yang dapat berkomunikasi secara langsung. Namun, VPN memungkinkan dua kantor terhubung. Mari kita ambil gambar di bawah ini, di mana terdapat tiga jaringan:

![vpn1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/vpn1.png)

1. jaringan #1 (Kantor #1)
2. jaringan #2 (Kantor #2)
3. jaringan #3 (Dua perangkat terhubung melalu VPN)

Perangkat yang terhubung di Jaringan #3 masih merupakan bagian dari Jaringan #1 dan Jaringan #2 tetapi juga terbentuk bersama untuk membuat jaringan pribadi (Jaringan #3) yang hanya dapat dikomunikasikan oleh perangkat yang terhubung melalui VPN ini.

Mari kita bahas beberapa keuntungan lain yang ditawarkan oleh VPN pada tabel di bawah ini:

|Keuntungan|Penjelasan|
|:--------:|:--------:|
|Memungkinkan jaringan di lokasi geografis yang berbeda untuk dihubungkan.|Misalnya, bisnis dengan banyak kantor akan menganggap VPN bermanfaat, karena ini berarti sumber daya seperti server/infrastruktur dapat diakses dari kantor lain.|
|Menawarkan privasi|Teknologi VPN menggunakan enkripsi untuk melindungi data. Ini berarti bahwa itu hanya dapat dipahami di antara perangkat yang dikirim dan tujuannya, yang berarti data tidak rentan terhadap penyusup. Enkripsi ini berguna di tempat-tempat dengan WiFi publik, di mana tidak ada enkripsi yang disediakan oleh jaringan. Anda dapat menggunakan VPN untuk melindungi lalu lintas Anda agar tidak dilihat oleh orang lain.|
|Menawarkan anonym|Wartawan dan aktivis bergantung pada VPN untuk melaporkan masalah global dengan aman di negara-negara di mana kebebasan berbicara dikendalikan. Biasanya, lalu lintas Anda dapat dilihat oleh ISP Anda dan perantara lainnya karena dilacak. Tingkat anonimitas yang disediakan VPN hanya sebesar bagaimana perangkat lain di jaringan menghargai privasi. Misalnya, VPN yang mencatat semua data/riwayat Anda pada dasarnya sama dengan tidak menggunakan VPN dalam hal ini.|

Teknologi VPN telah meningkat selama bertahun-tahun. Mari kita telusuri beberapa teknologi VPN yang ada di bawah ini:
|Teknologi VPN|Penjelasan|
|:-----------:|:--------:|
|PPP|Teknologi ini digunakan oleh PPTP (dijelaskan di bawah) untuk memungkinkan otentikasi dan menyediakan enkripsi data. VPN bekerja dengan menggunakan kunci privat dan sertifikat publik (mirip dengan SSH). Kunci & sertifikat pribadi harus cocok agar Anda dapat terhubung. Teknologi ini tidak mampu meninggalkan jaringan dengan sendirinya (non-routable).|
|PPTP|*Point-to-Point Tunneling Protocol* (PPTP) adalah teknologi yang memungkinkan data dari PPP untuk melakukan perjalanan dan meninggalkan jaringan. PPTP sangat mudah diatur dan didukung oleh sebagian besar perangkat. Namun, dienkripsi dengan lemah dibandingkan dengan alternatif.|
|IPSec|*Internet Protocol Security* (IPsec) mengenkripsi data menggunakan kerangka kerja Internet Protocol (IP) yang ada. IPSec is difficult to set up in comparison to alternatives; however, if successful, it boasts strong encryption and is also supported on many devices.|

