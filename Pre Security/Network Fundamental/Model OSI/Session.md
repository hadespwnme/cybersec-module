![session](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/session.png)

Setelah data diterjemahkan atau diformat dengan benar dari lapisan presentasi (lapisan 6), lapisan *session* (lapisan 5) akan mulai membuat koneksi ke komputer lain yang menjadi tujuan data tersebut. Ketika koneksi dibuat, sesi dibuat. Sementara koneksi ini aktif, jadi itu adalah sesi.

Lapisan *session* (lapisan 5) menyinkronkan dua komputer untuk memastikan bahwa mereka berada di halaman yang sama sebelum data dikirim dan diterima. Setelah pemeriksaan ini dilakukan, lapisan sesi akan mulai membagi data yang dikirim menjadi potongan data yang lebih kecil dan mulai mengirim potongan (paket) ini satu per satu. Pembagian ini bermanfaat karena jika koneksi terputus, hanya potongan yang belum terkirim yang harus dikirim lagi — bukan seluruh bagian data (anggap saja seperti memuat file simpanan dalam video game).

Yang perlu diperhatikan adalah bahwa sesi itu unik — artinya data tidak dapat melewati sesi yang berbeda, tetapi pada kenyataannya, hanya di setiap sesi saja.
