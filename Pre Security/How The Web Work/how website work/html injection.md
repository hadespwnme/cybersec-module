apa itu html inject ?html inject adalah 
HTML Injection dikenal juga sebagai Cross Site Scripting.merupakan celah keamanan yang memungkinkan bagi penyerang untuk menginjeksi kode HTML ke dalam halaman web yang dilihat oleh pengguna lain,sobat lihat pada gambar di atas.maksud dari gambar di atas adalah bug html inject,jadi ketika user memasukan <h1>Test</h1> maka yang akan terjadi kode html tersebut akan tereskusi.

ex : ```<h1>test</h1>```

ketika kode itu di masukan,tag htmlny aka ke eksekusi.

contoh kode rentan html inject :

```php
$name  = $_POST['name'];
$kelas  = $_POST['kelas'];
$bio      = "I like Seccodeid";
```
script di atas rentan dengan html inject.di karenakan tidak ada validasi input (filter).

cara mengatasinya tinggal menambahkan  htmlspecialchars.

contoh :
```php
$name  = htmlspecialchars($_POST['name']);
$kelas   =  htmlspecialchars($_POST['kelas']);
$bio      = htmlspecialchars("I like Seccodeid");
```
