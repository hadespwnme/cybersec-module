### Downloading Files
Fitur komputasi yang cukup mendasar adalah kemampuan untuk mentransfer file. Misalnya, Anda mungkin ingin mengunduh program, skrip, atau bahkan gambar. Untungnya bagi kita, ada banyak cara untuk mengambil file-file ini.

Kami akan membahas penggunaan `wget`. Perintah ini memungkinkan kami mengunduh file dari web melalui HTTP -- seolah-olah Anda sedang mengakses file di browser Anda. Kita hanya perlu memberikan alamat *source* yang ingin kita unduh. Misalnya, jika saya ingin mengunduh file bernama "myfile.txt" ke mesin saya, dengan asumsi saya tahu alamat webnya -- akan terlihat seperti ini:

`wget http://github.com/yingcrackerhades/misalnyasaja/mytext.txt`

### Transferring Files From Your Host - SCP (SSH)
Secure copy atau `SCP`, sebut aja beigtu -- artinya mengcopy file dengan aman. Berbeda dengan perintah `cp` biasa, perintah ini memungkinkan Anda mentransfer file antara dua komputer menggunakan protokol SSH untuk menyediakan autentikasi dan enkripsi.

Bekerja pada model SOURCE dan DESTINATION, SCP memungkinkan Anda untuk:
* Salin file & direktori dari sistem Anda saat ini ke sistem jarak jauh
* Salin file & direktori dari sistem jarak jauh ke sistem Anda saat ini

Asalkan kita mengetahui nama pengguna dan kata sandi untuk pengguna di sistem Anda saat ini dan pengguna di sistem jarak jauh. Sebagai contoh, mari salin file contoh dari mesin kita ke mesin jarak jauh, yang telah saya susun dengan rapi pada tabel di bawah ini:

|Variable|Nilai|
|:------:|:---:|
|IP adress sistem jarak jauh|192.168.1.30|
|User sistem jarak jauh|ubuntu|
|Nama file di sistem lokal|file1.txt|
|Beri nama file yang ingin kita simpan seperti pada sistem jarak jauh|file2.txt|

Bermodal informasi di atas kita dapat mengtranfer file dari sistem kita ke sistem jarak jauh menggunakan perintah seperti dibawa ini:

`scp file1.txt ubuntu@192.168.1.30:/home/ubuntu/file2.txt`

Jika ingin mengtranfer file dari sistem jarak jauh ke sistem kita seperti ini:

`scp ubuntu@192.168.1.30:/home/ubuntu/file2.txt file1.txt`

### Serving Files From Your Host - WEB
Mesin Ubuntu sudah dibungkus sebelumnya dengan python3. Python sangat membantu menyediakan modul yang ringan dan mudah digunakan yang disebut "HTTPServer". Modul ini mengubah komputer Anda menjadi server web yang cepat dan mudah yang dapat Anda gunakan untuk menyajikan file Anda sendiri, yang kemudian dapat diunduh oleh komputer lain menggunakan perintah seperti `curl` dan `wget`.

"HTTPServer" diPython3 akan melayani file di direktori tempat Anda menjalankan perintah, tetapi ini dapat diubah dengan memberikan opsi yang dapat ditemukan di halaman manual. Sederhananya, yang perlu kita lakukan hanyalah menjalankan `python3 -m http.server` untuk memulai modul! Pada tangkapan layar di bawah, kami melayani dari direktori bernama "server web", yang memiliki satu nama "file".

![httpserver](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/httpserver.png)

Sekarang, mari gunakan `wget` untuk mengunduh file menggunakan alamat IP komputer dan nama file. Salah satu kelemahan modul ini adalah Anda tidak memiliki cara untuk mengindeks, jadi Anda harus tahu persis nama dan lokasi file yang ingin Anda gunakan. Inilah mengapa saya lebih suka menggunakan Updog. [Apa itu Updog?](https://github.com/sc0tfree/updog) Server web yang lebih canggih namun ringan. Tapi untuk saat ini, mari kita tetap menggunakan "Server HTTP" dari Python.

![wget](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/wgete.png)

Pada tangkapan layar di atas, kita dapat melihat bahwa `wget` telah berhasil mengunduh file bernama "file" ke mesin kita. Permintaan ini dicatat oleh SimpleHTTPServer seperti halnya server web mana pun, yang telah saya tangkap dalam tangkapan layar di bawah.

![log](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/httplog.png)
