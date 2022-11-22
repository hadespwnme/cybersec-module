Pengguna mungkin ingin menjadwalkan tindakan atau tugas tertentu untuk dilakukan setelah sistem di-boot. Ambil contoh, misalnya, menjalankan perintah, mencadangkan file, atau meluncurkan program favorit Anda, seperti Spotify atau Google Chrome.

Kita akan berbicara tentang proses `cron`, tetapi lebih khusus lagi, bagaimana kita dapat berinteraksi dengannya melalui penggunaan `crontab`. Crontab adalah salah satu proses yang dimulai saat boot, yang bertanggung jawab untuk memfasilitasi dan mengelola pekerjaan `cron`.

![cron1](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/cron1.png)

Crontab hanyalah file khusus dengan pemformatan yang dikenali oleh proses `cron` untuk mengeksekusi setiap baris langkah demi langkah. Crontab membutuhkan 6 nilai spesifik:

|Nilai|Penjelasan|
|:---:|:--------:|
|MIN|Menit keberapa akan di eksekusi|
|HOUR|Jam keberapa akan di eksekusi|
|DOM|Hari pada bulan apa di eksekusi|
|MON|Bulan pada tahun apa akan di eksekusi|
|DOW|Hari pada minggu apa akan di eksekusi|
|CMD|Perintah sebenarnya yang akan dieksekusi|

Mari kita gunakan contoh membuat cadangan file. Anda mungkin ingin mencadangkan "Dokumen" "cmnatic" setiap 12 jam. Kami akan menggunakan pemformatan berikut:
`0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/`

Fitur menarik dari crontab adalah ini juga mendukung wildcard atau asterisk (`*`). Jika kita tidak ingin memberikan nilai untuk bidang tertentu itu, yaitu kami tidak peduli bulan, hari, atau tahun apa itu dijalankan - hanya akan jalankan setiap 12 jam, kita cukup memberi tanda bintang.

Ini akan sedikit membingungkan untuk memulainya, itulah sebabnya ada beberapa *source* yang bagus seperti "[Generator Crontab](https://crontab-generator.org/)" online yang memungkinkan Anda menggunakan aplikasi ramah untuk menghasilkan pemformatan untuk Anda! Serta situs "[Cron Guru](https://crontab.guru/)"!

![cron2](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/cron2.png)

![cron3](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/cron3.png)
