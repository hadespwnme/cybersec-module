*Processes* adalah program yang berjalan di mesin Anda. Mereka dikelola oleh kernel, di mana setiap proses akan memiliki ID yang terkait dengannya, juga dikenal sebagai PID-nya. PID bertambah untuk urutan di mana proses dimulai. Yaitu. proses ke-60 akan memiliki PID 60.

### Viewing Processes
Kita dapat menggunakan perintah `ps` yang *friendly* untuk memberikan daftar proses yang berjalan sebagai sesi pengguna kita dan beberapa informasi tambahan seperti kode statusnya, sesi yang menjalankannya, berapa banyak waktu penggunaan CPU yang digunakannya, dan nama dari program aktual atau perintah yang sedang dijalankan:

![ps1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/ps1.png)

Perhatikan bagaimana pada tangkapan layar di atas, proses kedua ps memiliki PID 204, dan kemudian pada perintah di bawahnya, ini kemudian dinaikkan menjadi 205.

Untuk melihat proses yang dijalankan oleh pengguna lain dan yang tidak dijalankan dari suatu sesi (yaitu proses sistem), kita perlu memberikan `aux` ke perintah `ps` seperti: `ps aux`.

![ps2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/ps2.png)

Catatan kita dapat melihat total 5 proses -- perhatikan bagaimana kita sekarang memiliki "root" dan "cmnatic"

Perintah lain yang sangat berguna adalah perintah `top`. `top` memberi Anda statistik *real time* tentang proses yang berjalan di sistem Anda alih-alih sekali tampil. Statistik ini akan di*refresh* setiap 10 detik, tetapi juga akan di*refresh* saat Anda menggunakan tombol panah untuk menelusuri berbagai baris. Perintah hebat lainnya untuk mendapatkan wawasan tentang sistem Anda adalah melalui perintah `top`.

![top](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/top1.png)

### Managing Processes
Anda dapat mengirim sinyal yang menghentikan proses; ada berbagai jenis sinyal yang berkorelasi dengan seberapa "bersih" proses ditangani oleh kernel. Untuk mematikan perintah, kita dapat menggunakan perintah `kill` dengan nama yang sesuai dan PID terkait yang ingin kita matikan. yaitu, untuk membunuh PID 1337, kami menggunakan `kill 1337`.

Di bawah ini adalah beberapa sinyal yang dapat kami kirim ke suatu proses saat dimatikan:
* SIGTERM - Hentikan prosesnya, tetapi izinkan untuk melakukan beberapa tugas pembersihan sebelumnya
* SIGKILL - Matikan prosesnya - tidak melakukan pembersihan apa pun setelah fakta
* SIGSTOP - Hentikan/tangguhkan proses

### How do Processes Start?
Mari kita mulai dengan berbicara tentang *namespace*. Sistem Operasi (OS) menggunakan ruang nama untuk akhirnya membagi sumber daya yang tersedia di komputer untuk (seperti CPU, RAM, dan prioritas) proses. Anggap saja seperti membagi komputer Anda menjadi beberapa irisan -- mirip dengan kue. Proses dalam irisan itu akan memiliki akses ke sejumlah daya komputasi, namun, itu akan menjadi sebagian kecil dari apa yang sebenarnya tersedia untuk setiap proses secara keseluruhan.

*Namespace* sangat bagus untuk keamanan karena merupakan cara untuk mengisolasi proses dari yang lain -- hanya yang berada di ruang nama yang sama yang dapat melihat satu sama lain.

Kami sebelumnya berbicara tentang cara kerja PID, dan di sinilah ia berperan. Proses dengan ID 0 adalah proses yang dimulai saat sistem melakukan booting. Proses ini adalah init sistem di Ubuntu, seperti **systemd**, yang digunakan untuk menyediakan cara mengelola proses pengguna dan berada di antara sistem operasi dan pengguna.

Misalnya, setelah sistem mem-boot dan menginisialisasi, **systemd** adalah salah satu proses pertama yang dimulai. Program atau perangkat lunak apa pun yang ingin kita mulai akan dimulai sebagai apa yang dikenal sebagai proses *child* dari systemd. Artinya dikendalikan oleh systemd, tetapi akan berjalan sebagai prosesnya sendiri (walaupun berbagi sumber daya dari systemd) untuk memudahkan kita mengidentifikasi dan sejenisnya.

![proccess](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/process1.png)

###  Getting Processes/Services to Start on Boot
Beberapa aplikasi dapat dijalankan pada boot dari sistem yang kita miliki. Misalnya, server web, server *database*, atau server transfer file. Perangkat lunak ini seringkali *citical* dan sering diminta untuk memulai selama boot-up sistem oleh administrator.

Dalam contoh ini, kita akan memberi tahu server web apache untuk memulai apache secara manual dan kemudian memberi tahu sistem untuk meluncurkan apache2 saat boot.

Masukkan penggunaan `systemctl` -- perintah ini memungkinkan kita untuk berinteraksi dengan proses/daemon systemd. Melanjutkan contoh kita, `systemctl` adalah perintah yang mudah digunakan dengan format berikut: `systemctl [option] [service]`

Misalnya, untuk memberitahu apache untuk memulai, kami akan menggunakan `systemctl start apache2`. Tampaknya cukup sederhana, bukan? Sama dengan jika kita ingin menghentikan apache, kita tinggal mengganti [option] dengan `stop` (bukan *start* seperti yang diberitahu tadi)

Ada empat opsi `systemctl`:
* start
* stop
* enable
* disable

### An Introduction to Backgrounding and Foregrounding in Linux
Proses dapat berjalan dalam dua status: Di background dan di foreground. Misalnya, perintah yang Anda jalankan di terminal Anda seperti "echo" atau hal semacam itu akan berjalan di latar depan(foreground) terminal Anda karena ini adalah satu-satunya perintah yang disediakan yang belum diperintahkan untuk dijalankan di latar belakang. "Echo" adalah contoh yang bagus karena keluaran `echo` akan kembali kepada Anda di latar depan, tetapi tidak di latar belakang - ambil tangkapan layar di bawah, misalnya.

![bg1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/bg1.png)

Di sini kami menjalankan `echo "Hi THM"` , di mana kami mengharapkan output dikembalikan kepada kami seperti di awal. Namun setelah menambahkan operator `&` ke perintah, kami hanya diberi ID dari proses `echo` alih-alih keluaran sebenarnya -- karena sedang berjalan di latar belakang.

Ini bagus untuk perintah seperti menyalin file karena itu berarti kita dapat menjalankan perintah di latar belakang dan melanjutkan dengan perintah apa pun yang ingin kita jalankan (tanpa harus menunggu salinan file selesai terlebih dahulu)

Kita dapat melakukan hal yang persis sama saat menjalankan hal-hal seperti skrip -- alih-alih mengandalkan operator `&`, kita dapat menggunakan `Ctrl + Z` pada keyboard untuk melatarbelakangi suatu proses. Ini juga merupakan cara yang efektif untuk "menjeda" eksekusi skrip atau perintah seperti pada contoh di bawah ini:

![bg2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/bg2.png)

Skrip ini akan terus mengulang "This will keep on looping until I stop!" sampai saya menghentikan atau menangguhkan proses. Dengan menggunakan Ctrl + Z (seperti yang ditunjukkan oleh T^Z). Sekarang terminal kita tidak lagi dipenuhi pesan -- sampai kita mengedepankannya, yang akan kita bahas di bawah.

### Foregrounding a process
Sekarang kita memiliki proses yang berjalan di latar belakang, misalnya, skrip kita "background.sh" yang dapat dikonfirmasi dengan menggunakan perintah `ps aux`, kita dapat melakukan *back-pedal* dan membawa proses ini kembali ke latar depan untuk berinteraksi.

![bg3](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/bg3.png)

Dengan latar belakang proses kita menggunakan `Ctrl + Z` atau operator `&`, kita dapat menggunakan `fg` untuk mengembalikannya ke fokus seperti di bawah ini, di mana kita dapat melihat perintah fg digunakan untuk mengembalikan proses latar belakang ke penggunaan di terminal, di mana output dari skrip sekarang dikembalikan kepada kami.

![bg4](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/bg4.png)

![bg5](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/bg5.png)

