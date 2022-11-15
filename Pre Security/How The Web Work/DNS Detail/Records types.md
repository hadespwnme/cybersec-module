### DNS Record Types
DNS bukan hanya untuk situs web, dan ada beberapa jenis catatan DNS. Kami akan membahas beberapa yang paling umum yang mungkin Anda temui.

### A Record
Catatan ini diselesaikan ke alamat IPv4, misalnya 20.205.243.166.

### AAAA Record
Catatan ini diselesaikan ke alamat IPv6, misalnya 2606:4700:20::681a:be5

### CNAME Record
Catatan ini diselesaikan ke nama domain lain, misalnya, toko online Toko Padi memiliki nama subdomain store.tokpad.com yang mengembalikan catatan CNAME store.shopify.com. Permintaan DNS lain kemudian akan dibuat ke toko.shopify.com untuk mengetahui alamat IP.

### MX Record
Catatan ini diselesaikan ke alamat server yang menangani email untuk domain yang Anda tanyakan, misalnya respons data MX untuk github.com akan terlihat seperti alt1.aspmx.l.google.com. Catatan ini juga dilengkapi dengan bendera prioritas. Ini memberitahu klien di mana untuk mencoba server, ini sangat cocok jika server utama turun dan email perlu dikirim ke server cadangan.

### TXT Record
Catatan TXT adalah bidang teks gratis tempat data berbasis teks apa pun dapat disimpan. Catatan TXT memiliki banyak kegunaan, tetapi beberapa yang umum dapat digunakan untuk mencantumkan server yang memiliki wewenang untuk mengirim email atas nama domain (ini dapat membantu memerangi spam dan email palsu). Mereka juga dapat digunakan untuk memverifikasi kepemilikan nama domain saat mendaftar ke layanan pihak ketiga.

