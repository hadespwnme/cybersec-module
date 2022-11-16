### Load Balancers
Saat lalu lintas situs web mulai menjadi cukup besar atau menjalankan aplikasi yang memerlukan bandwith tinggi, satu server web mungkin tidak lagi melakukan tugasnya. Penyeimbang muatan menyediakan dua fitur utama, memastikan situs web dengan lalu lintas tinggi dapat menangani beban dan menyediakan *failover* jika server menjadi tidak responsif.

*Load balancer* juga melakukan pemeriksaan berkala dengan setiap server untuk memastikan mereka berjalan dengan benar; ini disebut **health check**. Jika server tidak merespons dengan tepat atau tidak merespons, *load balancer* akan berhenti mengirim lalu lintas hingga merespons dengan tepat lagi.

![loadbalancer](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/How%20The%20Web%20Work/putting%20all%20together/Image/loadbalancer.png)

### CDN (*Content Delivery Networks*)
CDN dapat menjadi sumber yang bagus untuk mengurangi lalu lintas ke situs web yang sibuk. Ini memungkinkan Anda untuk menghosting file statis dari situs web Anda, seperti JavaScript, CSS, Gambar, Video, dan menghostingnya di ribuan server di seluruh dunia. Saat pengguna meminta salah satu file yang dihosting, CDN bekerja di tempat server terdekat berada secara fisik dan mengirim permintaan ke sana alih-alih ke sisi lain dunia.

### Databases
Seringkali situs web membutuhkan cara menyimpan informasi untuk penggunanya. Server web dapat berkomunikasi dengan database untuk menyimpan dan memanggil kembali data darinya. *Database* dapat berkisar dari hanya file teks sederhana hingga kelompok kompleks dari beberapa server yang memberikan kecepatan dan ketahanan. Anda akan menemukan beberapa database umum: MySQL, MSSQL, MongoDB, GraphQL, Postgres, dan banyak lagi; masing-masing memiliki fitur khusus.

### WAF (*Web Application Firewall*)
WAF berada di antara *request* web Anda dan server web; tujuan utamanya adalah untuk melindungi server web dari peretasan atau penolakan serangan layanan. Ini menganalisis permintaan web untuk teknik serangan umum, apakah permintaan tersebut berasal dari browser asli dan bukan bot. Ini juga memeriksa apakah permintaan web dalam jumlah berlebihan dikirim dengan menggunakan sesuatu yang disebut *rate limiting*, yang hanya akan mengizinkan sejumlah permintaan dari IP per detik. Jika permintaan dianggap sebagai serangan potensial, itu akan dibatalkan dan tidak pernah dikirim ke server web.

![waf](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/How%20The%20Web%20Work/putting%20all%20together/Image/waf.png)
