### Interaksi dengan *file system*
Dapat mengoperasikan mesin tanpa tergantung dengan desktop itu cukup penting. Lagi pula, Apa gunanya bisa login tapi tak bisa mengoperasikan nya.

|Perintah|Nama lengkap|
|:------:|:----------:|
|ls|list/daftar|
|cd|change directory/pindah folder|
|cat|concatenate|
|pwd|tampilkan folder sekarang|

### Daftar file di folder sekarang (ls)
Sebelum kita dapat melakukan sesuatu seperti mencari tahu isi file atau folder apa pun, kita perlu mengetahui apa yang ada terlebih dahulu. Ini dapat dilakukan dengan menggunakan perintah `ls` (singkatan dari listing)

![ls](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/Screenshot%20from%202022-11-03%2021-47-29.png)

Pada screenshot di atas, kita bisa melihat ada direktori/folder berikut:
* Downloads
* Documents
* Pictures

> Tips pro: Anda dapat membuat daftar isi direktori tanpa harus menavigasi ke sana dengan menggunakan ls dan nama direktori. `ls namafolder`

### Pindah Direktori (cd)
Sekarang kita tahu folder apa yang ada, kita perlu menggunakan perintah "*cd*" (singkatan dari *change directory*) untuk mengubah ke direktori yang dituju. Katakanlah jika saya ingin membuka direktori "*Pictures*" - saya akan melakukan `cd Pictures`. Dan lagi, kita ingin mengetahui isi direktori "Pictures" ini dan untuk melakukannya, kita akan menggunakan `ls` lagi:

![cd](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/Screenshot%20from%202022-11-03%2021-48-49.png)

Pada kasus diatas ada 4 gambar.


### Melihat isi sebuah file.
Meskipun mengetahui tentang keberadaan file itu termasuk sudah bagus — hal itu tidak terlalu berguna kecuali kita dapat melihat isinya.

Kita akan mem)1bahas beberapa alat yang tersedia untuk kita yang memungkinkan kita mentransfer file dari satu mesin ke mesin lain di ruang selanjutnya. Tapi untuk saat ini, kita akan berbicara tentang melihat isi file teks menggunakan perintah yang disebut `cat`.

`Cat` adalah kependekan dari *concatenating* & merupakan cara yang fantastis untuk menampilkan konten file (bukan hanya file teks!).

Gambar di bawah ini memperlihatkan kombinasi penggunaan `ls` dan `cat` pada direktori tutor:

![cat](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/cat.png)

