*Sensitive Data Exposure* terjadi ketika situs web tidak melindungi (atau menghapus) informasi teks-jelas yang sensitif dengan benar kepada pengguna akhir; biasanya ditemukan di *source code* frontend situs.

Sekarang kita tahu bahwa website dibangun menggunakan banyak elemen HTML (tag), yang semuanya dapat kita lihat hanya dengan "View Page Source". Pengembang situs web mungkin lupa menghapus kredensial masuk, tautan tersembunyi ke bagian pribadi situs web, atau data sensitif lainnya yang ditampilkan dalam HTML atau JavaScript.

Informasi sensitif berpotensi dimanfaatkan untuk memajukan akses penyerang di berbagai bagian aplikasi web. Misalnya, mungkin ada komentar HTML dengan kredensial masuk sementara, dan jika Anda melihat *source code* halaman dan menemukannya, Anda dapat menggunakan kredensial ini untuk masuk di tempat lain di aplikasi (atau lebih buruk, digunakan untuk mengakses komponen backend lain dari situs ).

Setiap kali Anda menilai aplikasi web untuk masalah keamanan, salah satu hal pertama yang harus Anda lakukan adalah meninjau *source code* halaman untuk melihat apakah Anda dapat menemukan kredensial masuk yang terbuka atau tautan tersembunyi.

![html](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/How%20The%20Web%20Work/how%20website%20work/Image/html_source.png)
