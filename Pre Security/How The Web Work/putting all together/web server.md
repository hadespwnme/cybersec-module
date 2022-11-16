## How Web servers work.

### What is a Web Server?
Server web adalah perangkat lunak yang mendengarkan koneksi masuk dan kemudian menggunakan protokol HTTP untuk mengirimkan konten web ke kliennya. Perangkat lunak server web paling umum yang akan Anda temui adalah Apache, Nginx, IIS, dan NodeJS. Server Web mengirimkan file dari apa yang disebut *directory root*, yang ditentukan dalam pengaturan perangkat lunak. Misalnya, Nginx dan Apache berbagi lokasi default yang sama dari `/var/www/html` di sistem operasi Linux, dan IIS menggunakan `C:\inetpub\wwwroot` untuk sistem operasi Windows. Jadi, misalnya, jika Anda meminta file `http://www.example.com/picture.jpg`, itu akan mengirimkan file `/var/www/html/picture.jpg` dari hard drive lokalnya.

### Virtual Hosts
Server web dapat meng-host beberapa situs web dengan nama domain yang berbeda; untuk mencapai ini, mereka menggunakan host virtual. Perangkat lunak server web memeriksa nama host yang diminta dari header HTTP dan mencocokkannya dengan host virtualnya (host virtual hanyalah file konfigurasi berbasis teks). Jika menemukan kecocokan, situs web yang benar akan disediakan. Jika tidak ditemukan kecocokan, situs web default akan disediakan sebagai gantinya.

Virtual Host dapat membuat direktori root mereka dipetakan ke lokasi berbeda di hard drive. Misalnya, `one.com` dipetakan ke `/var/www/website_one`, dan `two.com` dipetakan ke `/var/www/website_two`.

Tidak ada batasan jumlah situs web berbeda yang dapat Anda host di server web.

### Static Vs Dynamic Content
Konten statis, seperti namanya, adalah konten yang tidak pernah berubah. Contoh umumnya adalah gambar, javascript, CSS, dll., tetapi juga dapat menyertakan HTML yang tidak pernah berubah. Selain itu, ini adalah file yang disajikan langsung dari server web tanpa perubahan apa pun.

Konten dinamis, di sisi lain, adalah konten yang dapat berubah dengan permintaan yang berbeda. Ambil, misalnya, sebuah blog. Di beranda blog, itu akan menampilkan entri terbaru. Jika entri baru dibuat, beranda kemudian diperbarui dengan entri terbaru, atau contoh kedua mungkin halaman pencarian di blog. Bergantung pada kata apa yang Anda cari, hasil yang berbeda akan ditampilkan.

Perubahan pada apa yang akhirnya Anda lihat ini dilakukan dalam apa yang disebut Backend dengan penggunaan bahasa pemrograman dan skrip. Disebut Backend karena apa yang dilakukan semuanya dilakukan di belakang layar. Anda tidak dapat melihat sumber HTML situs web dan melihat apa yang terjadi di Backend, sedangkan HTML adalah hasil pemrosesan dari Backend. Semua yang Anda lihat di browser Anda disebut Frontend.

### Scripting and Backend Languages
Tidak banyak batasan untuk apa yang dapat dicapai oleh bahasa backend, dan inilah yang membuat situs web menjadi interaktif bagi pengguna. Beberapa contoh bahasa ini (tanpa urutan tertentu :p) adalah PHP, Python, Ruby, NodeJS, Perl dan masih banyak lagi. Bahasa ini dapat berinteraksi dengan database, memanggil layanan eksternal, memproses data dari pengguna, dan banyak lagi. Contoh PHP yang sangat mendasar adalah jika Anda meminta situs web `http://example.com/index.php?name=adam`

Jika index.php dibangun seperti ini:
```php
<html>
  <body>Hello 
  <?php echo $_GET["name"]; ?>
  </body>
</html>
```
Itu akan menampilkan yang berikut ke klien:

```php
<html>  
  <body>Hello adam
  </body>
</html>
```
Anda akan melihat bahwa klien tidak melihat kode PHP apa pun karena ada di Backend. Interaktivitas ini membuka lebih banyak masalah keamanan untuk aplikasi web yang belum dibuat dengan aman, seperti yang Anda pelajari di modul lebih lanjut.
