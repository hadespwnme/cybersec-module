Saat kita mengakses situs web, browser Anda perlu membuat permintaan ke server web untuk aset seperti HTML, Gambar, dan mengunduh tanggapan. Sebelum itu, Anda perlu memberi tahu browser secara spesifik bagaimana dan di mana mengakses sumber daya ini, di sinilah URL akan berperan.

### What is a URL? (Uniform Resource Locator)
Jika Anda pernah menggunakan internet(so pastilah, wong buka iki bae make internet), Anda pernah menggunakan URL sebelumnya. URL sebagian besar merupakan instruksi tentang cara mengakses sumber daya di internet. Gambar di bawah menunjukkan seperti apa URL dengan semua fiturnya (tidak menggunakan semua fitur di setiap permintaan).

![url](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/How%20The%20Web%20Work/HTTP%20in%20detail/Image/newurl.png)

**Schema**: Ini menginstruksikan protokol apa yang digunakan untuk mengakses sumber daya seperti HTTP, HTTPS, FTP (File Transfer Protocol)
**User**: Beberapa layanan memerlukan otentikasi untuk masuk, Anda dapat memasukkan nama pengguna dan kata sandi ke dalam URL untuk masuk.
**Host**: Nama domain atau alamat IP dari server yang ingin Anda akses.
**Port**: Port yang akan Anda sambungkan, biasanya 80 untuk HTTP dan 443 untuk HTTPS, tetapi ini dapat dihosting di port apa pun antara 1 - 65535.
**Path**: Nama file atau lokasi sumber daya yang Anda coba akses.
**Query String**: Bit ekstra informasi yang dapat dikirim ke jalur yang diminta. Misalnya, /blog?id=1 akan memberi tahu jalur blog bahwa Anda ingin menerima artikel blog dengan id 1.
**Fragment**: Ini adalah referensi ke lokasi pada halaman sebenarnya yang diminta. Ini biasanya digunakan untuk halaman dengan konten yang panjang dan dapat memiliki bagian tertentu dari halaman yang terhubung langsung dengannya, sehingga dapat dilihat oleh pengguna segera setelah mereka mengakses halaman tersebut.

### Making a Request
Dimungkinkan untuk membuat permintaan ke server web hanya dengan satu baris "GET / HTTP/1.1"

![line](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/How%20The%20Web%20Work/HTTP%20in%20detail/Image/line.png)

Tetapi untuk pengalaman web yang jauh lebih banyak, Anda juga perlu mengirim data lain. Data lain ini dikirim dalam apa yang disebut header, di mana header berisi informasi tambahan untuk diberikan ke server web yang Anda gunakan untuk berkomunikasi, tetapi kami akan membahasnya lebih lanjut di tugas Header.

Contoh requests:
```
GET / HTTP/1.1
Host: gemarkode.or.id
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://gemarkode.or.id/
```
Mari kita uraikan setiap baris request ini:

**Baris 1**: Permintaan ini mengirimkan metode GET (lebih lanjut tentang ini di tugas Metode HTTP), meminta halaman beranda dengan / dan memberi tahu server web bahwa kami menggunakan protokol HTTP versi 1.1.

**Baris 2**: Kita memberi tahu web server, kita menginginkan website gemarkode.or.id.
**Baris 3**: Kita memberi tau web server bahwa kita menggunakan browser Firefox versi 87.
**Baris 4**: Kami memberi tahu server web bahwa halaman web yang merujuk kami ke sini adalah https://gemarkode.or.id
**Baris 5**:Permintaan HTTP selalu diakhiri dengan baris kosong untuk memberi tahu server web bahwa permintaan telah selesai.

Contoh responses:
```
HTTP/1.1 200 OK
Server: GitHub.com
Date: Fri, 09 Nov 2022 13:34:03 GMT
Content-Type: text/html
Content-Length: 100

<html>
<head>
    <title>GemarKode</title>
</head>
<body>
    Welcome To gemarkode.or.id
</body>
</html>
```
Mari kira jabarkan satu persatu:

**Baris 1**: HTTP 1.1 adalah versi protokol HTTP yang digunakan server dan kemudian diikuti oleh Kode Status HTTP dalam hal ini "200 Ok" yang memberi tahu kita bahwa permintaan telah berhasil diselesaikan.
**Baris 2**: Memberitahu kita server yang digunakan, biasanya juga disertai dengar versinya.
**Baris 3**: Tanggal, waktu, dan zona waktu saat ini dari server web.
**Baris 4**: Header *Content-type* memberi tahu klien jenis informasi apa yang akan dikirim, seperti HTML, gambar, video, pdf, XML.
**Baris 5**: *Content-Length* memberi tahu klien berapa lama responsnya, dengan cara ini kita dapat memastikan tidak ada data yang hilang.
**Baris 6**: Respons HTTP berisi baris kosong untuk mengonfirmasi akhir dari respons HTTP.
**Baris 7-14**: Informasi yang diminta, dalam hal ini *homepage*.
