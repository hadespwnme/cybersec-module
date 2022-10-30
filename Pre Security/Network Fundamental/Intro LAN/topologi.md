# Local Area Network (LAN) Topologies
Selama bertahun-tahun, telah terjadi eksperimen dan implementasi berbagai desain jaringan. Mengacu pada jaringan, ketika kita merujuk pada istilah "topologi", kita sebenarnya mengacu pada desain atau tampilan jaringan yang ada. Mari kita bahas kelebihan dan kekurangan topologi tersebut di bawah ini.

### Topologi bintang / Star topologies 
Premis utama topologi bintang adalah bahwa perangkat terhubung secara individual melalui perangkat jaringan pusat seperti switch atau hub. Terlepas dari biayanya, topologi ini adalah yang paling umum ditemukan saat ini karena keandalan dan skalabilitasnya.

Setiap informasi yang dikirim ke perangkat dalam topologi ini dikirim melalui perangkat pusat yang terhubung. Mari kita telusuri beberapa kelebihan dan kekurangan topologi ini di bawah ini:

Karena lebih banyak pemasangan kabel & pembelian peralatan jaringan khusus diperlukan untuk topologi ini, itu lebih mahal daripada topologi lainnya. Namun, meskipun biaya tambahan, ini memberikan beberapa keuntungan yang signifikan. Misalnya, topologi ini sifatnya jauh lebih terukur, yang berarti sangat mudah untuk menambahkan lebih banyak perangkat karena permintaan jaringan meningkat.

Sayangnya, semakin besar skala jaringan, semakin banyak pemeliharaan yang diperlukan agar jaringan tetap berfungsi. Ketergantungan yang meningkat pada pemeliharaan ini juga dapat membuat pemecahan masalah menjadi lebih sulit. Selain itu, topologi star masih rentan terhadap kegagalan - meskipun berkurang. Misalnya, jika perangkat keras terpusat yang menghubungkan perangkat gagal, perangkat ini tidak lagi dapat mengirim atau menerima data. Untungnya, perangkat keras terpusat ini seringkali kuat.

![star](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/star.png)

### Bus Topologies
Jenis koneksi ini bergantung pada koneksi tunggal yang dikenal sebagai *backbone cable*. Jenis topologi ini mirip dengan "daun" dari pohon dalam artian bahwa perangkat (*daun*) berasal dari tempat cabang berada di kabel ini. Karena semua data yang ditujukan untuk setiap perangkat berjalan di sepanjang kabel yang sama, sangat cepat rentan menjadi lambat dan macet jika perangkat dalam topologi secara bersamaan meminta data. Kemacetan ini juga menghasilkan pemecahan masalah yang sangat sulit, menjadi sulit karena untuk mengidentifikasi perangkat mana yang mengalami masalah dengan data yang semuanya berjalan di sepanjang rute yang sama.

Namun, dengan ini dikatakan, topologi bus adalah salah satu topologi yang lebih mudah dan lebih hemat biaya untuk diatur karena biayanya, seperti pemasangan kabel atau peralatan jaringan khusus yang digunakan untuk menghubungkan perangkat ini.

Terakhir, kelemahan lain dari topologi bus adalah hanya ada sedikit "kelebihan" jika terjadi kegagalan. Kerugian ini terjadi karena ada satu titik kegagalan di sepanjang *backbone cable*. Jika kabel ini putus, perangkat tidak dapat lagi menerima atau mengirimkan data di sepanjang bus.

![bus](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/bus.png)

### Ring Topologies
Topologi ring (juga dikenal sebagai topologi token) memiliki beberapa kesamaan. Perangkat seperti komputer terhubung langsung satu sama lain untuk membentuk *loop*, artinya kabel yang dibutuhkan sedikit dan ketergantungan yang lebih kecil pada perangkat keras khusus seperti dalam topologi star

Topologi ring bekerja dengan mengirimkan data melintasi loop hingga mencapai perangkat yang dituju, menggunakan perangkat lain di sepanjang loop untuk meneruskan data. Menariknya, sebuah perangkat hanya akan mengirim data yang diterima dari perangkat lain dalam topologi ini jika tidak bisa mengirim sendiri. Jika perangkat kebetulan memiliki data untuk dikirim, ia akan mengirim datanya sendiri terlebih dahulu sebelum mengirim data dari perangkat lain.

Karena hanya ada satu arah untuk data yang melintasi topologi ini, maka cukup mudah untuk memecahkan masalah yang muncul. Namun, ini adalah pedang bermata dua karena ini bukan cara yang efisien untuk perjalanan data melintasi jaringan, karena mungkin harus mengunjungi banyak perangkat terlebih dahulu sebelum mencapai perangkat yang dimaksud.

Terakhir, topologi ring "kurang" rentan terhadap kemacetan, seperti dalam topologi bus, karena sejumlah besar lalu lintas tidak melintasi jaringan pada satu waktu. Desain topologi ini, bagaimanapun, berarti bahwa kesalahan seperti kabel terputus, atau perangkat rusak akan mengakibatkan putusnya seluruh jaringan.
![ring](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/ring.png)

### what's switch?
*Switch* adalah perangkat khusus dalam jaringan yang dirancang untuk menggabungkan beberapa perangkat lain seperti komputer, printer, atau perangkat berkemampuan jaringan lainnya menggunakan *etherne*t. Berbagai perangkat ini dicolokkan ke port switch. *Switch* biasanya ditemukan di jaringan yang lebih besar seperti bisnis, sekolah, atau jaringan berukuran serupa, di mana ada banyak perangkat untuk terhubung ke jaringan. *Switch* dapat menghubungkan sejumlah besar perangkat dengan memiliki port 4, 8, 16, 24, 32, dan 64 untuk dihubungkan ke perangkat.

*Switch* jauh lebih efisien daripada rekan mereka yang lebih rendah (hub/repeater). *Switch* melacak perangkat apa yang terhubung ke port yang mana. Dengan cara ini, ketika mereka menerima sebuah paket, alih-alih mengulangi paket itu ke setiap port seperti yang akan dilakukan hub, itu hanya mengirimkannya ke target yang dituju, sehingga mengurangi lalu lintas jaringan.

![switch](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/switches.png)

Baik *Switch* dan *Router* dapat dihubungkan satu sama lain. Kemampuan untuk melakukan ini meningkatkan redundansi (keandalan) jaringan dengan menambahkan beberapa jalur untuk diambil data. Jika satu jalan "down", jalan lain bisa digunakan. Meskipun hal ini dapat mengurangi kinerja jaringan secara keseluruhan karena paket harus memakan waktu lebih lama untuk perjalanan, tidak ada waktu henti -- harga yang harus dibayar dengan mempertimbangkan alternatifnya.

### What's router?
Adalah tugas router untuk menghubungkan jaringan dan meneruskan data di antara mereka. Ini dilakukan dengan menggunakan perutean (makanya dinamai router!).

*Routing* adalah label yang diberikan untuk proses perjalanan data melintasi jaringan. Perutean melibatkan pembuatan jalur antar jaringan sehingga data ini dapat berhasil dikirimkan.

Perutean berguna ketika perangkat dihubungkan oleh banyak jalur, seperti pada contoh diagram di bawah ini.

![router](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Intro%20LAN/Image/routing2.png)
