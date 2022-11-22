### Introducing Packages & Software Repo
Saat pengembang ingin mengirimkan perangkat lunak ke komunitas, mereka akan mengirimkannya ke repositori "apt". Jika disetujui, program dan alat mereka akan dirilis ke "alam bebas". Dua dari fitur Linux yang paling menarik terungkap di sini: Aksesibilitas pengguna dan kelebihan alat sumber terbuka(open source).

Saat menggunakan perintah `ls` pada mesin Linux Ubuntu 20.04, file-file ini berfungsi sebagai gateway/registry.

![apt1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/apt1.png)

![apt2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/apt2.png)

Sementara vendor Sistem Operasi akan memelihara repositori mereka sendiri, Anda juga dapat menambahkan repositori komunitas ke daftar Anda! Ini memungkinkan Anda untuk memperluas kemampuan OS Anda. Repositori tambahan dapat ditambahkan dengan menggunakan perintah `add-apt-repository` atau dengan mendaftarkan penyedia lain! Misalnya, beberapa vendor akan memiliki tempat penyimpanan yang lebih dekat dengan lokasi geografisnya, contoh repo indo.

### Managing Your Repositories (Adding and Removing)
Biasanya kita menggunakan perintah `apt` untuk menginstal perangkat lunak ke sistem Ubuntu kita. Perintah `apt` adalah bagian dari perangkat lunak manajemen paket yang juga bernama apt. Apt berisi seluruh rangkaian alat yang memungkinkan kita mengelola paket dan sumber perangkat lunak kita, dan menginstal atau menghapus perangkat lunak pada saat yang bersamaan.

Salah satu metode untuk menambahkan repositori adalah dengan menggunakan perintah `add-apt-repository` yang sudah diilustrasikan di atas, tetapi kita akan berjalan melalui penambahan dan penghapusan repositori secara manual. Meskipun Anda dapat menginstal perangkat lunak melalui penggunaan penginstal paket seperti `dpkg`, manfaat apt berarti setiap kali kami memperbarui sistem kita, repositori yang berisi perangkat lunak yang kami tambahkan juga akan diperiksa pembaruannya.

Dalam contoh ini, kita akan menambahkan editor teks yaitu Sublime Text ke mesin Ubuntu kita sebagai repositori karena ini bukan bagian dari repositori default Ubuntu. Saat menambahkan perangkat lunak, integritas dari apa yang kita unduh dijamin dengan penggunaan apa yang disebut kunci GPG (Gnu Privacy Guard). Kunci-kunci ini pada dasarnya adalah pemeriksaan keamanan dari pengembang yang mengatakan, "inilah perangkat lunak kami". Jika kunci tidak sesuai dengan kepercayaan sistem Anda dan apa yang digunakan pengembang, perangkat lunak tidak akan diunduh.

Jadi, untuk memulai, kami perlu menambahkan kunci GPG untuk pengembang Sublime Text 3.

1. Mari unduh kunci GPG dan gunakan kunci apt untuk mempercayainya: `wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`
2. Sekarang setelah kami menambahkan kunci ini ke daftar tepercaya kita, kita sekarang dapat menambahkan repositori Sublime Text 3 ke daftar sumber apt kita. Praktik yang baik adalah memiliki file terpisah untuk setiap repositori komunitas/pihak ketiga yang berbeda yang kita tambahkan.
2.1. Mari buat file bernama sublime-text.list di `/etc/at/sources.list.d` dan masukkan informasi repositori seperti ini:

![source1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/sources1.png)

2.2. Dan sekarang gunakan Nano atau editor teks pilihan Anda untuk menambah & menyimpan repositori Sublime Text 3 ke dalam file yang baru dibuat ini:

![source2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/sources2.png)

2.3. Setelah kita menambahkan entri ini, kita perlu memperbarui apt untuk mengenali entri baru ini -- ini dilakukan dengan menggunakan perintah `apt update`

2.4. Setelah berhasil diperbarui, sekarang kita dapat melanjutkan untuk menginstal perangkat lunak yang telah kita percayai dan ditambahkan ke apt menggunakan `apt install sublime-text`

Menghapus paket semudah membalik. Proses ini dilakukan dengan menggunakan perintah `add-apt-repository --remove ppa:PPA_Name/ppa` atau dengan menghapus secara manual file yang sebelumnya kita tambahkan. Setelah dihapus, kita bisa menggunakan `apt remove [nama-perangkat lunak-di sini]` yaitu `apt remove sublime-text`

