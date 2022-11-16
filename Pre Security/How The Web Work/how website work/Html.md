Situs itu dibuat terutama mengguakan:
* HTML, untuk membangun situs web dan menentukan strukturnya
* CSS, untuk membuat situs web terlihat cantik dengan menambahkan opsi gaya
* JavaScript, terapkan fitur kompleks pada halaman menggunakan interaktivitas

*HyperText Markup Language* (HTML) adalah bahasa penulisan situs web. Elemen (juga dikenal sebagai tag) adalah blok penyusun halaman HTML dan memberi tahu browser cara menampilkan konten. Cuplikan kode di bawah menunjukkan dokumen HTML sederhana, yang strukturnya sama untuk setiap situs web:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Gemar Kode</title>
  </head>
  <body>
    <H1>Welcome To Gemar Kode</H1>
  </body>
</html>
```
Mari kita bedah satu-persatu:
1. `<!DOCTYPE html>` : mendefinisikan bahwa halaman tersebut adalah dokumen HTML5. Ini membantu standarisasi di berbagai browser dan memberi tahu browser untuk menggunakan HTML5 untuk menginterpretasikan halaman.
2. `<html>` : elemen adalah elemen root(akar) dari halaman HTML - semua elemen lainnya muncul setelah elemen ini.
3. `<head>` : elemen berisi informasi tentang halaman (seperti judul halaman)
4. `<body>` : elemen mendefinisikan tubuh dokumen HTML; hanya konten di dalam tubuh yang ditampilkan di browser.
5. `<h1>` : Mendefiniskan tajuk besar
* Ada banyak elemen lain (tag) yang digunakan untuk tujuan yang berbeda. Misalnya, ada tag untuk tombol (<button>), gambar (<img>), list, dan masih banyak lagi.

Tag dapat berisi atribut seperti atribut `class` yang dapat digunakan untuk memberi gaya pada elemen (misalnya membuat tag dengan warna yang berbeda) `<p class="bold-text">`, atau atribut `src` yang digunakan pada gambar untuk menentukan lokasi gambar: `<img src="img/cat.jpg">`.Sebuah elemen dapat memiliki beberapa atribut, masing-masing dengan tujuan uniknya sendiri, misalnya, `<p atribut1="nilai1" atribut2="nilai2">`.

Elemen juga dapat memiliki atribut `id` (`<p id="example">`), yang unik untuk elemen tersebut. Berbeda dengan atribut class, di mana banyak elemen dapat menggunakan `class` yang sama, sebuah elemen harus memiliki `id` yang berbeda untuk mengidentifikasinya secara unik. ID elemen digunakan untuk gaya dan untuk mengidentifikasinya dengan JavaScript.

Anda dapat melihat HTML situs web mana pun dengan mengeklik kanan dan memilih "View Page Source" (Chrome) / "Show Page Source" (Safari).



