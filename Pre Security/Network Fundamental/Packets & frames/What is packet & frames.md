*Packets* dan *frames* adalah bagian kecil dari data yang ketika dibentuk bersama-sama membuat informasi atau pesan yang lebih besar. Namun, mereka adalah dua hal yang berbeda dalam model OSI. Sebuah frame berada di layer 2 - layer data link, artinya tidak ada informasi seperti alamat IP. Anggap ini seperti memasukkan amplop ke dalam amplop dan mengirimnya pergi. Amplop pertama adalah paket yang Anda kirimkan, tetapi setelah dibuka, amplop di dalamnya masih ada dan berisi data (ini adalah frame).

Proses ini disebut enkapsulasi yang kita bahas di model OSI. Pada tahap ini, aman untuk mengasumsikan bahwa ketika kita berbicara tentang alamat IP apa pun, kita berbicara tentang paket. Namun, Ketika informasi enkapsulasi dihilangkan, kita berbicara tentang frame itu sendiri.

Paket adalah cara yang efisien untuk mengomunikasikan data di seluruh perangkat jaringan seperti yang dijelaskan dalam Tugas 1. Karena data ini dipertukarkan dalam potongan-potongan kecil, kemungkinan terjadinya kemacetan di seluruh jaringan lebih kecil dari pesan besar yang dikirim sekaligus.

Misalnya, saat memuat gambar dari situs web, gambar ini tidak dikirim ke komputer Anda secara keseluruhan, melainkan potongan-potongan kecil yang direkonstruksi di komputer Anda. Ambil gambar di bawah ini sebagai ilustrasi proses ini. Gambar anjing dibagi menjadi tiga paket, di mana ia direkonstruksi kembali ketika mencapai komputer untuk membentuk gambar akhir.

![packet](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Packets%20%26%20frames/Image/packets1.png)

Paket memiliki struktur berbeda yang bergantung pada jenis paket yang sedang dikirim. Seperti yang akan kita bahas, jaringan penuh dengan standar dan protokol yang bertindak sebagai seperangkat aturan tentang bagaimana paket ditangani pada perangkat. Dengan Internet yang diprediksi memiliki sekitar 50 miliar perangkat yang terhubung pada akhir tahun 2020, segalanya dengan cepat menjadi tidak terkendali jika tidak ada standarisasi.

Mari kita lanjutkan dengan contoh Protokol Internet kita. Paket yang menggunakan protokol ini akan memiliki satu set header yang berisi potongan informasi tambahan ke data yang dikirim melalui jaringan.

Beberapa tajuk terkenal meliputi:

|Header|Deskripsi|
|:----:|:-------:|
|*Time to live*|Bidang ini menetapkan timer kedaluwarsa agar paket tidak menyumbat jaringan Anda jika tidak pernah berhasil mencapai host atau *escape*|
|*Checksum*|Bidang ini menyediakan pemeriksaan integritas untuk protokol seperti TCP/IP. Jika ada data yang diubah, nilai ini akan berbeda dari yang diharapkan dan karena itu rusak.|
|*Source Address*|Alamat IP perangkat dimana tempat paket itu **dikirim** sehingga data tahu ke mana **harus kembali**.|
|*Destination address*|alamat perangkat dikirim kedata sehingga data tahu kemana arah selanjutnya|

