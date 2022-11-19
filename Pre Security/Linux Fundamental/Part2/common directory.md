### /etc
Direktori root ini adalah salah satu direktori root terpenting di sistem Anda. Folder etc (kependekan dari *etcetera*) adalah lokasi umum untuk menyimpan file sistem yang digunakan oleh sistem operasi Anda.

Misalnya, file sudoers yang di*highligth* pada tangkapan layar di bawah berisi daftar pengguna & grup yang memiliki izin untuk menjalankan sudo atau sekumpulan perintah sebagai pengguna root.

Juga *highlighted* di bawah adalah file "passwd" dan "shadow". Kedua file ini khusus untuk Linux karena menunjukkan bagaimana sistem Anda menyimpan kata sandi untuk setiap pengguna dalam format terenkripsi yang disebut sha512.

![/etc](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%E2%81%84etc.png)

### /var
Direktori "/var", dengan "var" kependekan dari data variabel, adalah salah satu folder root utama yang ditemukan di instalasi Linux. Folder ini menyimpan data yang sering diakses atau ditulis oleh layanan atau aplikasi yang berjalan di sistem. Misalnya, file log dari layanan dan aplikasi yang sedang berjalan ditulis di sini (/var/log), atau data lain yang belum tentu terkait dengan pengguna tertentu (mis. database dan sejenisnya).

![var](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%E2%81%84var.png)

### /root
Berbeda dengan direktori `/home`, folder `/root` sebenarnya adalah rumah bagi pengguna sistem "root". Tidak ada yang lebih dari folder ini selain hanya memahami bahwa ini adalah direktori home untuk pengguna "root". Namun, perlu disebutkan karena anggapan logisnya adalah bahwa pengguna ini akan memiliki datanya di direktori seperti "/home/root" secara default.

![root](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%E2%81%84root.png)

### /tmp
Ini adalah direktori root unik yang ditemukan pada instalasi Linux. Kependekan dari "temporary", direktori /tmp bersifat *volatile* dan digunakan untuk menyimpan data yang hanya perlu diakses sekali atau dua kali. Mirip dengan memori di komputer Anda, setelah komputer dihidupkan ulang, isi folder ini akan dihapus.

Apa yang berguna bagi kita dalam pentesting adalah setiap pengguna dapat menulis ke folder ini secara default. Berarti begitu kita memiliki akses ke mesin, itu berfungsi sebagai tempat yang baik untuk menyimpan hal-hal seperti *enumeration scripts* kita.


![tmp](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Linux%20Fundamental/Image/%E2%81%84tmp.png)

