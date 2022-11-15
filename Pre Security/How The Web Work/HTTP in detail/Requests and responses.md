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
> GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/

