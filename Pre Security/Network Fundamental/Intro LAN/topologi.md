# Local Area Network (LAN) Topologies
Selama bertahun-tahun, telah terjadi eksperimen dan implementasi berbagai desain jaringan. Mengacu pada jaringan, ketika kita merujuk pada istilah "topologi", kita sebenarnya mengacu pada desain atau tampilan jaringan yang ada. Mari kita bahas kelebihan dan kekurangan topologi tersebut di bawah ini.

### Topologi bintang / Star topologies 
Premis utama topologi bintang adalah bahwa perangkat terhubung secara individual melalui perangkat jaringan pusat seperti switch atau hub. Terlepas dari biayanya, topologi ini adalah yang paling umum ditemukan saat ini karena keandalan dan skalabilitasnya.

Setiap informasi yang dikirim ke perangkat dalam topologi ini dikirim melalui perangkat pusat yang terhubung. Mari kita telusuri beberapa kelebihan dan kekurangan topologi ini di bawah ini:

Karena lebih banyak pemasangan kabel & pembelian peralatan jaringan khusus diperlukan untuk topologi ini, itu lebih mahal daripada topologi lainnya. Namun, meskipun biaya tambahan, ini memberikan beberapa keuntungan yang signifikan. Misalnya, topologi ini sifatnya jauh lebih terukur, yang berarti sangat mudah untuk menambahkan lebih banyak perangkat karena permintaan jaringan meningkat.

Sayangnya, semakin besar skala jaringan, semakin banyak pemeliharaan yang diperlukan agar jaringan tetap berfungsi. Ketergantungan yang meningkat pada pemeliharaan ini juga dapat membuat pemecahan masalah menjadi lebih sulit. Selain itu, topologi star masih rentan terhadap kegagalan - meskipun berkurang. Misalnya, jika perangkat keras terpusat yang menghubungkan perangkat gagal, perangkat ini tidak lagi dapat mengirim atau menerima data. Untungnya, perangkat keras terpusat ini seringkali kuat.

![star]()

### Bus Topologies
Jenis koneksi ini bergantung pada koneksi tunggal yang dikenal sebagai *backbone cable*. Jenis topologi ini mirip dengan "daun" dari pohon dalam artian bahwa perangkat (*daun*) berasal dari tempat cabang berada di kabel ini. Karena semua data yang ditujukan untuk setiap perangkat berjalan di sepanjang kabel yang sama, sangat cepat rentan menjadi lambat dan macet jika perangkat dalam topologi secara bersamaan meminta data. Kemacetan ini juga menghasilkan pemecahan masalah yang sangat sulit, menjadi sulit karena untuk mengidentifikasi perangkat mana yang mengalami masalah dengan data yang semuanya berjalan di sepanjang rute yang sama.

Namun, dengan ini dikatakan, topologi bus adalah salah satu topologi yang lebih mudah dan lebih hemat biaya untuk diatur karena biayanya, seperti pemasangan kabel atau peralatan jaringan khusus yang digunakan untuk menghubungkan perangkat ini.

Terakhir, kelemahan lain dari topologi bus adalah hanya ada sedikit "kelebihan" jika terjadi kegagalan. Kerugian ini terjadi karena ada satu titik kegagalan di sepanjang *backbone cable*. Jika kabel ini putus, perangkat tidak dapat lagi menerima atau mengirimkan data di sepanjang bus.

![bus]()
