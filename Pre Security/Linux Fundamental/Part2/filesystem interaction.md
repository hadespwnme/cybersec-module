Kami membahas beberapa perintah paling mendasar saat berinteraksi dengan *filesystem* di mesin Linux. Sebagai contoh, kita telah membahas cara membuat daftar dan menemukan isi folder menggunakan `ls` dan `find` serta menavigasi sistem file menggunakan `cd`.

Dalam tugas ini, kita akan mempelajari beberapa perintah lagi untuk berinteraksi dengan sistem file agar kita dapat:
* membuat file dan folder
* memindahkan file dan folder
* menghapus file dan folder

Untuk lebih spesifik kita liat *command* dibawah ini:

|perintah|nama|tujuan|
|:------:|:--:|:----:|
|touch|touch|membuat file|
|mkdir|make directory|membuat foldeer|
|cp|copy|copy file atau folder|
|mv|move|mindahin file atau folder|
|rm|remove|menghapus file atau folder|
|file|file|menentukan jenis file|

> Tips: seperti kita menggunakan perintah `cat` kita juga bisa menggunakan cara seperti directory1/directory2 untuk semua *command*.

### Creating Files and Folders (touch, mkdir)
Membuat file dan folder di Linux adalah proses yang sederhana. Pertama, kita akan membahas pembuatan file. Perintah `touch` mengambil tepat satu argumen -- nama yang ingin kita berikan pada file yang kita buat. Sebagai contoh, kita dapat membuat file "note" dengan menggunakan `touch note`. Perlu dicatat bahwa `touch` hanya membuat file kosong. Anda perlu menggunakan perintah seperti `echo` atau editor teks seperti `nano` untuk menambahkan konten ke file kosong.

![touch](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/touch.png)

Ini adalah proses serupa untuk membuat folder, yang hanya melibatkan penggunaan perintah `mkdir` dan sekali lagi memberikan nama yang ingin kita tetapkan ke direktori. Misalnya, membuat direktori "folder2" menggunakan `mkdir folder2`.

![mkdir](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/mdkir.png)

### Removing Files and Folders (rm)
`rm` adalah perintah luar biasa dari yang telah kita bahas sejauh ini. Anda cukup menghapus file dengan menggunakan `rm`, namu membutuhkan *flag* -R untuk menghapus direktori.

![rm](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/rm.png)

![rm-r](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/rm-r.png)


###Copying and Moving Files and Folders (cp, mv)
Menyalin dan memindahkan file adalah fungsi penting pada mesin Linux. Dimulai dengan `cp. Perintah ini membutuhkan dua argumen:
1. Nama file yang sudah ada
2. Nama file baru yang kita inginkan

`cp` menyalin seluruh isi file yang ada ke dalam file baru. Pada tangkapan layar di bawah, kami menyalin "note" ke "note2".

![cp](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/cp.png)

Memindahkan file membutuhkan dua argumen, seperti perintah `cp`. Namun, daripada menyalin dan/atau membuat file baru, `mv` akan menggabungkan atau memodifikasi file kedua yang kita berikan sebagai argumen. Anda tidak hanya dapat menggunakan `mv` untuk memindahkan file ke folder baru, tetapi Anda juga dapat menggunakan `mv` untuk mengganti nama file atau folder. Misalnya, pada tangkapan layar di bawah ini, kami mengganti nama file "note2" menjadi "note3". "note3" sekarang akan memiliki konten "note2".

![mv](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/mv.png)

### Determining File Type
Apa yang sering menyesatkan dan sering menarik perhatian orang adalah membuat anggapan dari file tentang apa tujuan atau isinya. File biasanya memiliki apa yang dikenal sebagai ekstensi untuk membuatnya lebih mudah. Misalnya, file teks biasanya memiliki ekstensi ".txt". Tapi ini tidak perlu.

Sejauh ini, file yang kami gunakan dalam contoh kami belum memiliki ekstensi. Tanpa mengetahui konteks mengapa file itu ada -- kita tidak benar-benar tahu tujuannya. Masukkan perintah `file`. Perintah ini membutuhkan satu argumen. Misalnya, kami akan menggunakan `file` untuk mengonfirmasi apakah file "catatan" dalam contoh kami benar-benar file teks, seperti `file note`.

![file](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/file.png)
