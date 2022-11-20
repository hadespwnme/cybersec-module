Sepanjang seri sejauh ini, kita hanya menyimpan teks dalam file menggunakan kombinasi perintah `echo` dan operator pipa (> dan >>). Ini bukan cara yang efisien untuk menangani data saat Anda bekerja dengan file dengan banyak baris dan semacamnya!

### Introducing terminal text editors
Ada beberapa opsi yang dapat Anda gunakan, semuanya dengan berbagai kemudahan dan kegunaan. Bagian ini akan memperkenalkan Anda pada `nano` tetapi juga menunjukkan kepada Anda alternatif bernama `VIM`.

#### Nano
Dimulai dengan Nano! Untuk membuat atau mengedit file menggunakan nano, kita cukup menggunakan `nano namaFile` -- mengganti "nama file" dengan nama file yang ingin diedit.

![nano](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/nano.png)

Setelah kita menekan enter untuk menjalankan perintah, `nano` akan di*launch* Di mana kita bisa mulai memasukkan atau memodifikasi teks kita. Anda dapat menavigasi setiap baris menggunakan tombol panah "atas" dan "bawah" atau memulai baris baru menggunakan tombol "Enter" di keyboard.

![nano1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/nano%201.png)

Nano memiliki beberapa fitur yang mudah diingat & mencakup hal paling umum yang Anda inginkan dari editor teks, termasuk:
* Mencari text
* Copy dan Paste
* Pergi ke baris sekian
* Melihat kita sedang dibaris keberapa

Kita bisa menggunakan fitur ini menggunakan "CTRL" (di presentasikan `^`di linux), dan hurufnya. Contoh untuk keluar dari `nano` kita bisa menggunakan `CRTL + X`, lalu tekan "Y".

#### VIM
VIM adalah text editor yang lebih canggih, meskipun kamu tidak mengetahui fitur lanjutannya, setidaknya ini dapat membantu kamu dalam memperkuat keterampilan di Linux.

![vim](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/vim1.png)

Beberapa manfaat VIM, walau agak lama untuk mengerti:
* Dapat disesuaikan - Anda dapat memodifikasi pintasan keyboard sesuai pilihan Anda
* Penyorotan Sintaks - ini berguna jika Anda menulis atau memelihara kode, menjadikannya pilihan populer bagi pengembang perangkat lunak
* VIM berfungsi di semua terminal di mana nano mungkin tidak diinstal
* Ada banyak *source* seperti [cheatseat](https://vim.rtorr.com/), tutorial, dan sejenisnya yang tersedia untuk Anda gunakan.



