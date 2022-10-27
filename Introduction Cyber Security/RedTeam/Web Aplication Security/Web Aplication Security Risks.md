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
