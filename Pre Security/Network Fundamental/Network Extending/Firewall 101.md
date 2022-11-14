![firewal](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Network%20Extending/Image/roomicon.png)

*Firewall* adalah perangkat dalam jaringan yang bertanggung jawab untuk menentukan lalu lintas apa yang diizinkan masuk dan keluar. Pikirkan *firewall* sebagai keamanan perbatasan untuk jaringan. Administrator dapat mengonfigurasi *firewall* untuk **mengizinkan** atau **menolak** lalu lintas masuk atau keluar dari jaringan berdasarkan banyak faktor seperti:
* Lalu lintas dari mana? (apakah *firewall* diberitahu untuk menerima/menolak lalu lintas dari jaringan tertentu?)
* Lalu lintas akan kemana? (sudahkah *firewall* diberitahu untuk menerima/menolak lalu lintas yang ditujukan untuk jaringan tertentu?)
* Lalu lintas untuk port apa? (apakah *firewall* diberitahu untuk menerima/menolak lalu lintas yang ditujukan hanya untuk port 80?)
* Protokol apa yang digunakan lalu lintas? (apakah *firewall* telah diberitahu untuk menerima/menolak lalu lintas yang UDP, TCP atau keduanya?)

*Firewall* melakukan inspeksi paket untuk menentukan jawaban atas pertanyaan-pertanyaan ini.

*Firewall* hadir dalam berbagai bentuk dan ukuran. Dari perangkat keras khusus (sering ditemukan di jaringan besar seperti bisnis) yang dapat menangani sejumlah besar data hingga router perumahan (seperti di rumah Anda!) Atau perangkat lunak seperti Snort, firewall dapat dikategorikan ke dalam 2 hingga 5 kategori.

Kami akan membahas dua kategori utama firewall dalam tabel di bawah ini:

|Kategori Firewall| Penjelasan|
|:---------------:|:---------:|
|*Stateful*|Jenis firewall ini menggunakan seluruh informasi dari sebuah koneksi; daripada memeriksa paket individu, firewall ini menentukan perilaku perangkat berdasarkan seluruh koneksi.Jenis firewall ini menghabiskan banyak sumber daya dibandingkan dengan *firewall stateless* karena pengambilan keputusan bersifat dinamis. Misalnya, firewall dapat mengizinkan bagian pertama dari jabat tangan TCP yang nantinya akan gagal. Jika koneksi dari host buruk, itu akan memblokir seluruh perangkat.|
|*Stateless*| Jenis firewall ini menggunakan seperangkat aturan statis untuk menentukan apakah paket individu dapat diterima atau tidak. Misalnya, perangkat mengirimkan paket yang buruk tidak berarti bahwa seluruh perangkat kemudian diblokir.Sementara firewall ini menggunakan sumber daya yang jauh lebih sedikit daripada alternatif, mereka jauh lebih bodoh. Misalnya, firewall ini hanya efektif sebagai aturan yang ditentukan di dalamnya. Jika suatu aturan tidak benar-benar cocok, itu tidak berguna secara efektif.Namun, firewall ini bagus saat menerima lalu lintas dalam jumlah besar dari sekumpulan host (seperti serangan Distributed Denial-of-Service)|

