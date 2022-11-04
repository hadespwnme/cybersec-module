Operator Linux adalah cara yang fantastis untuk meningkatkan pengetahuan anda tentang bekerja dengan Linux. Ada beberapa operator penting yang perlu diperhatikan. Kita akan membahas dasar-dasarnya dan memecahnya menjadi potongan-potongan kecil.

Sebagai gambaran umum, saya akan menampilkan operator berikut:

|Symbol/operator|deskripsi|
|:-------------:|:-------:|
| & | Operator ini memungkinkan anda untuk menjalankan perintah di latar belakang terminal anda.|
|&&| Operator ini memungkinkan anda untuk menggabungkan beberapa perintah bersama-sama dalam satu baris diterminal anda.
| > | Operator ini adalah redirector - artinya kita dapat mengambil output dari sebuah perintah (seperti menggunakan cat untuk mengeluarkan file) dan mengarahkannya ke tempat lain.|
| >> | Operator ini melakukan fungsi yang sama dengan operator `>` tetapi menambahkan output daripada mengganti (artinya tidak ada yang ditimpa).|

Mari kita jabarkan lebih detail.

### Operator &
Operator ini memungkinkan kita untuk menjalankan perintah di latar belakang. Sebagai contoh, katakanlah kita ingin menyalin file besar. Ini jelas akan memakan waktu yang cukup lama dan akan membuat kita tidak dapat melakukan hal lain sampai file berhasil disalin.

Operator shell "&" memungkinkan kita untuk menjalankan perintah dan menjalankannya di latar belakang (seperti salinan file ini) yang memungkinkan kita melakukan hal lain!

### Operator &&
Operator shell ini agak menyesatkan dalam arti seberapa akrab dengan mitranya "&". Berbeda dengan operator "&", kita dapat menggunakan "&&" untuk membuat daftar perintah yang akan dijalankan misalnya `command1 && command2`. Namun, perlu dicatat bahwa command2 hanya akan berjalan jika command1 berhasil.

### Operator >
Operator inilah yang disebut sebagai output redirector. Apa artinya ini pada dasarnya adalah bahwa kita mengambil output dari perintah yang kita jalankan dan mengirimkan output itu ke tempat lain.

Contoh yang bagus dari hal ini adalah mengarahkan ulang output dari perintah echo yang kita pelajari di Tugas 4. Tentu saja, menjalankan sesuatu seperti echo howdy akan mengembalikan "howdy" kembali ke terminal kita — itu tidak terlalu berguna. Apa yang bisa kita lakukan sebagai gantinya, adalah mengarahkan "howdy" ke sesuatu seperti file baru!

Katakanlah kita ingin membuat file bernama "love" dengan pesan "sayang". Kita bisa menjalankan `echo "sayang" > love.txt` dimana kita ingin file tersebut dibuat dengan isi "sayang" seperti ini:

![>](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%3E.png)

>Catatan: Jika nilai file yaitu "sayang" sudah ada, isinya akan ditimpa!

### Operator >>
Operator ini juga merupakan redirector output seperti pada operator sebelumnya (>) yang telah kita bahas. Namun, yang membuat operator ini berbeda adalah bahwa alih-alih menimpa konten apa pun di dalam file, misalnya, operator ini hanya menempatkan output di akhir.

Melanjutkan contoh kita sebelumnya dimana kita memiliki file “love.txt” yang isinya “sayang”. Jika menggunakan `echo` untuk menambahkan "kamu" ke file menggunakan operator >, file sekarang hanya memiliki "kamu" dan bukan "sayang".

Operator `>>` memungkinkan untuk menambahkan output ke bagian bawah file — daripada mengganti konten seperti:

![>>](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%3E%3E.png)

