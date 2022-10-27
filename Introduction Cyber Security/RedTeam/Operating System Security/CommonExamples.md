## Authentication and weak password
Otentikasi adalah aksi untuk verifikasi identitas mu, baik itu lokal ataupun *server remote*. Otentikasi dapat di capai melalui 3 cara:
* Sesuatu yang mudah di ingat seperti password dan PIN code
* Fingerprint 
* Sesuatu yang anda punya seperti nomor handphone untuk menerima SMS.

Karena password adalah bentuk otentikasi paling umum, maka itu adalah yang paling sering di serang. Banyak user yang menggunakan password yang mudah di tebak dan atau menggunakan password yang sama untuk banyak website.
Selain itu beberapa user menggunakan perincian yang terkait diri mereka seperti tanggal lahir dan nama peliharaan, karena berpikir ini mudah di ingat dan tidak di ketahui penyerang. Namun, penyerang juga tau dan sadar akan kecenderungan hal itu.

*The National Cyber Security Centre*(NCSC) telah mempublish 100.000 password paling umum digunakan. Mari kita lihat 20 password paling sering digunakan pada tabel dibawah ini.

| RANK | Password |
|:----:|:--------:|
|  1   | 123456   |
|2|123456789|
|3|qwerty|
|4|password|
|5|111111|
|6|12345678|
|7|abc123|
|8|1234567|
|9|password1|
|10|12345|
|11|1234567890|
|12|123123|
|13|000000|
|14|iloveyou|
|15|1234|
|16|1q2w3e4r5t|
|17|qwertyuiop|
|18|123|
|19|monkey|
|20|dragon|

Kita bisa lihat 123,1234,12345,...,123456789 dan 1234567890 didalam daftar tersebut. Dictionary words atau kita sebut saja kamus password seperti iloveyou, monkey, dragon adalah kata yang umum digunakan. Kata yamg tidak ada dalam kamus contoh nya qwerty, qwertyuiop, dan 1q2w3e4r5t, itu sangat mudah di prediksi karena mengikuti layout dari keyboard.
![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Introduction%20Cyber%20Security/RedTeam/Operating%20System%20Security/Image/1510e4bd81418a2937060f9c55dad593.gif)

Singkatnya jika penyerang dapat menebak salah satu password media sosial anda, mereka akan tahu data pribadi anda. Oleh karena itu, pilih lah password yang complex dan sulit di terka namun mudah diingat.

## Weak File Permission
Keamanan yang tepat adalah tentang hak istimewa. Dalam dunia kerja, kamu ingin dokumen dapat diakses hanya oleh mereka yang berhak membukanya untuk mendapatkan pekerjaan.
Secara personal, misal kalian ingin merencanakan liburan bersama keluarga ataupun teman, pasti anda hanya akan membagikan berkas perencanaan perjalanan tersebut kepada nereka, dan kalian tidak ingin dokumen perencanaan tersebut diketahui publik. Itulah *the principle of least privilege* atau dalam istilah sederhana nya, "siapa yang dapat mengakses apa?"

Kelemahan dalam memberikan *permission* memudahkan musuh untuk mengetahui kerahasiaan (confidentiality) dan menyerang integritas (integrity).
Mereka dapat menyerang kerahasian dengan hak izin yang lemah untuk mengakses file yang seharusnya tidak dapat mereka akses. Selain itu mereka dapat menyerang integritas dengan memodifikasi file yang seharusnya tidak dapat mereka sunting.
![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Introduction%20Cyber%20Security/RedTeam/Operating%20System%20Security/Image/Screenshot_2022-10-27-21-12-34-16_40deb401b9ffe8e1df2f1cc5ba480b12.jpg)

## Access to malicious program
Contoh terakhir yang dapat kami berikan adalah tentang malicious program. Tergantung pada jenisnya, program ini dapat menyerang kerahasian(confidentiality), integritas(integrity) dan kesediaan(availability).
![alt](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Introduction%20Cyber%20Security/RedTeam/Operating%20System%20Security/Image/831208a805e53bafafbe074f01b84e64.png)

Ada beberapa tipe program berbahaya, contoh trojan horse, ini memberikan penyerang akses ke sistem. Konsekuensinya penyerang dapat membaca file dan bahkan memodifikasi nya.

Beberapa tipe program berbahayang menyerang ketersediaan (availability), seperti Ransomware. Ransomware adalah program berbahaya yang meng enkripsi file user. Enkripsi ini membuat file tidak dapat di baca tanpa mengetahui kunci nya. Dengan kata lain, tanpa kunci file hanya akan menjadi omong kosong tanpa di deskripsi.
Penyerang akan menawarkan jasa untuk mengembalikan hak akses file kepada user. Mereka akan memberikan password enkripsi jika user bersedia membayar kepada mereka.
