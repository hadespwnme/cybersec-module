Misal anda ingin membeli sesuatu dalam olshop(online shop), seenggaknya kalian akan lelalu langkah langkah dibawah ini:
<p align="center">
<img width="200px" src="https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Introduction%20Cyber%20Security/RedTeam/Web%20Aplication%20Security/Image/352114ac8da5f156f42aa551701323a2.png">
</p>

Ada beberapa kategori yang umum dalam melakukan serangan ke sebuah website, perhatikan langkah-langkah berikut ini:
* *Login*: dalam hal ini, penyerang dapat melakukan tindakan dengan mencoba berbagai kemungkinan password atau yang biasa di sebut bruteforce untuk mencoba masuk kedalam website.
* *Search for product*: biasanya penyerang akan meng-exploitasi dengan cara menambahkan karakter tertentu atau kode, contoh dalam hal ini adalah **XSS(Cross Site Scripting)**
* *Provide payment details*: penyerang akan melihat rincian pembayaran dikirim menggunakan teks biasa atau menggunakan enkripsi lemah. Enkripsi adalah membuat data tak terbaca tanpa mengetahui password atau kunci rahasia.

## Kegagalan identifikasi dan otentikasi
Identifikasi merujuk pada kemampuan untuk mengidentifikasi user dengan "keunikannya". Sebaliknya otentikasi adalah kemampuan untuk membuktikan pengguna adalah user yang di klaim. Olshop akan mengidentifikasi dan melakukan otentikasi sebelum pengguna dapat meng-akses system.
Akan tetapi hal ini rentan terhadap berbagai jenis tipe kelemahan, contoh:
1. Mengizinkan penyerang melakukan bruteforce, dalam hal ini mengizinkan banyak melakukan uji coba password untuk mendapatkan login secara valid.
2. Mengizinkan user menggunakan password yang lemah, sehingga mudah untuk di tebak.
3. Menyimpan data sensitif seperti username dan password tanpa di enkripsi. Jika penyerang membaca data berpassword ini, kita tidak ingin mereka melihat hal ini.
<p align="center">
<img width="250px" src="https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Introduction%20Cyber%20Security/RedTeam/Web%20Aplication%20Security/Image/0ac52c1bafa532db2a23e4a9efc6663d.png">
</p>

## Broken access control
*Access control* memastikan pengguna hanya mengakses data(foto, dokumen, dll) sesuai hak mereka masing masing. Sebagai contoh, kalian tidak ingin karyawan marketing kalian mengakses (membaca) dokumen karyawan bagian keuangan. Contoh vulnarabilities dalam akses kontrol:
* Gagal mengaplikasikan *the principle of the least privilege* dan memberi terlalu banyak hak ases kepada pengguna, contoh *Customers* berhak melihat harga barang, tetapi mereka tidak boleh mengubah hal itu.
* Dapat melihat dan memodifikasi akun orang lain menggunakan id uniknya. Sebagai contoh kamu pasti tidak ingin orang lain melihat transaksi yang dilakukan user lainnya.
* Mampu menelusuri halaman yang membutuhkan hak otentikasi, tanpa melakukan otentikasi terlebih dahulu. Sebagai contoh kalian tidak ingin kan pesan masuk yang ada di email kalian terbaca orang lain.

## Injection
Penyerang dapat meng-exploitasi sebuah website dengan memasukkan kode berbahaya bersama dengan input pencarian mereka. Hal ini terjadi karena kurangnya validasi dan sanitasi untuk masukan oleh user. Contoh XSS dan SQLi

## Cryptographic Failure
Kategori ini mengacu pada kegagalan dalam hal kriptografi, yang mana kriptografi ini adalah berkaitan dengan enkripsi dan deskripsi. Enkripsi adalah proses mengubah dari data yang mudah di baca menjadi tak terbaca, enkripsi memastikan mereka yang tidak punya "kunci" nya hanya akan mendapatkan omong kosong.
Deskripsi adalah mengubah chipertext(enkripsi text) menjadi data semula menggunakan "kunci rahasia". Contoh kegagalan dalam enkripsi:
1. Mengirim data yang sensitif tanpa enkripsi, contoh menggunakan HTTP alih alih menggunakan HTTPS, HTTP adalah protokol yang digunakan untuk mengakses web. HTTPS adalah HTTP versi *secure*nya. Orang lain dapat membaca hal yang anda kirim menggunakan HTTP, tapi tidak untuk HTTPS, contoh penyerang melakukan sniffing.
2. Menggunakan algoritma kriptografi yang lemah, salah satu algoritma kriptografi tua adalah menggeser setiap huruf satu persatu. Contoh "HADES IS GOOD GOD" menjadi "IBEFT JT HPPE HPE"
3. Menggunakan kunci yang lemah untuk melakukan enkripsi, sangat mudah untuk memecahkan kode `1234` sebagai kunci enkripsi.
<p align="center">
<img width="200px" src=">
</p>
