Salah satu cara fantastis untuk menunjukkan seberapa efisien Anda dengan sistem seperti ini adalah menggunakan serangkaian perintah untuk mencari file dengan cepat di seluruh sistem yang dapat diakses oleh pengguna. Tidak perlu secara konsisten menggunakan `cd` dan `ls` untuk mencari tahu di mana. Sebagai gantinya, kita dapat menggunakan perintah seperti `find` untuk mengotomatiskan hal-hal seperti ini untuk kita!

### Penggunaan find
Perintah `find` itu luar biasa dalam artian itu dapat digunakan dengan sangat sederhana atau agak rumit tergantung pada apa yang ingin kamu lakukan dengan tepat. Kalian dapat mempraktekkan nya dimanapun yang menggunakan Linux. Tapi, mari kita tetap berpegang pada dasar-dasarnya terlebih dahulu.

Screenshot dibawah menampilkan direktori yang tersedia untuk kita.

![ls](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/Screenshot%20from%202022-11-03%2021-47-29.png)

1. Documents
2. Downloads
3. Pictures

Sekarang, tentu saja, direktori dapat berisi lebih banyak direktori di dalamnya. Ini membuat sakit kepala ketika kita harus melihat setiap persatu hanya untuk mencoba dan mencari file tertentu. Kita dapat menggunakan `find` untuk melakukan ini untuk kita!

Mari kita mulai dengan sederhana dan berasumsi bahwa kita sudah mengetahui nama file yang kita cari — tetapi tidak dapat mengingat di mana tepatnya! Dalam hal ini, kami mencari "passwords.txt"

Jika kita mengingat nama file, kita cukup menggunakan `find -name passwords.txt` di mana perintah akan melihat setiap folder di direktori kita saat ini untuk file tertentu seperti di bawah ini.

![find]()

"Find" telah berhasil menemukan file — ternyata terletak di folder1/passwords.txt — sweet. Namun misalkan kita tidak mengetahui nama file tersebut, atau ingin mencari setiap file yang memiliki ekstensi seperti ".txt". Temukan mari kita melakukannya juga!

Kita cukup menggunakan apa yang dikenal sebagai wildcard (*) untuk mencari apa pun yang memiliki .txt di akhir. Dalam kasus ini, kita ingin menemukan setiap file .txt yang ada di direktori kami saat ini. Kita akan membuat perintah seperti `find -name *.txt` . Di mana "find" dapat menemukan setiap file .txt dan kemudian memberi kita lokasi masing-masing file:

![find2]()

### Penggunaan grep
Utilitas hebat lainnya yang bagus untuk dipelajari adalah penggunaan `grep`. Perintah `grep` memungkinkan kita untuk mencari isi file untuk nilai tertentu yang kita cari.

Ambil contoh log akses server web. Dalam hal ini, access.log server web memiliki 253 entri.

![wc](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/wc.png)

Menggunakan perintah seperti `cat` tidak akan berhasil dengan baik di sini. Katakanlah misalnya jika kita ingin mencari file log ini untuk melihat hal-hal yang dikunjungi oleh pengguna/alamat IP tertentu? Melihat melalui 253 entri tidak terlalu efisien mengingat kita ingin menemukan nilai tertentu.

Kita dapat menggunakan `grep` untuk mencari seluruh isi file ini untuk setiap entri dari nilai yang kita cari. Mengikuti contoh log akses server web, kami ingin melihat semua yang telah dikunjungi oleh alamat IP "81.143.211.56" (perhatikan bahwa ini adalah contoh fiktif)

![grep](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/grep.png)

"Grep" telah mencari melalui file ini dan telah menunjukkan kepada kita entri apa pun dari apa yang telah kami berikan dan yang terkandung dalam file log ini untuk IP.
