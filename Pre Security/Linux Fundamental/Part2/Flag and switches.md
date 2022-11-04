Mayoritas perintah memungkinkan argumen untuk diberikan. Argumen ini diidentifikasi oleh tanda hubung dan kata kunci tertentu yang dikenal sebagai flag atau switch.

Nanti kita akan membahas bagaimana kita dapat mengidentifikasi perintah apa yang memungkinkan argumen diberikan dan memahami apa yang sebenarnya dilakukan oleh perintah ini.

Saat menggunakan perintah, kecuali dinyatakan. itu akan melakukan perilaku defaultnya. Misalnya, `ls` mencantumkan isi direktori kerja. Namun, file tersembunyi tidak ditampilkan. Kita dapat menggunakan flag dan switch untuk memperluas perilaku perintah.

Kita gunakan contoh `ls`, `ls` memberi tahu kita bahwa hanya ada satu folder bernama "folder1" seperti yang disorot pada tangkapan layar di bawah. Perhatikan bahwa konten dalam tangkapan layar di bawah ini hanyalah contoh.

![ls](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/ls2.png)

Namun, setelah menggunakan argumen `-a` (kependekan dari --all), kita sekarang tiba-tiba memiliki output dengan beberapa file dan folder lagi seperti ".hidden". File dan folder dengan "." adalah file tersembunyi.

![hidden](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/ls-a.png)

Perintah yang menerima ini juga akan memiliki opsi `--help`. Opsi ini akan mencantumkan opsi yang mungkin diterima oleh perintah, memberikan deskripsi singkat dan contoh cara menggunakannya.

![help](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/ls-h.png)

Opsi ini sebenarnya adalah keluaran terformat dari apa yang disebut *man page* (kependekan dari manual), yang berisi dokumentasi untuk perintah dan aplikasi Linux.

### Man(ual) page
Halaman manual adalah sumber informasi yang bagus untuk perintah sistem dan aplikasi yang tersedia di kedua mesin Linux, yang dapat diakses di mesin itu sendiri.

Untuk mengakses dokumentasi ini, kita dapat menggunakan perintah `man` dan kemudian memberikan perintah yang ingin kita baca dokumentasinya. Gunakan contoh `ls`, kita akan menggunakan `man ls` untuk melihat halaman manual untuk `ls` seperti dibawah ini:

![man](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/man.png)

