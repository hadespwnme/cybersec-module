![transport](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Model%20OSI/Image/transport.png)

Layer 4 dari model OSI memainkan peran penting dalam mentransmisikan data melalui jaringan dan bisa sedikit sulit untuk dipahami. Ketika data dikirim antar perangkat, itu mengikuti salah satu dari dua protokol berbeda yang diputuskan berdasarkan beberapa faktor:
* TCP
* UDP

Mari kita mulai dengan TCP. **T**ransmision **C**ontrol **P**rotocol(TCP). Potensi sesuai dengan namanya, protokol ini dirancang dengan mempertimbangkan keandalan dan jaminan. Protokol ini mencadangkan koneksi konstan antara dua perangkat untuk jumlah waktu yang diperlukan untuk mengirim dan menerima data.

Tidak hanya itu, tetapi TCP juga memasukkan pengecekan kesalahan ke dalam desainnya. Pemeriksaan kesalahan adalah bagaimana TCP dapat menjamin bahwa data yang dikirim dari potongan kecil di lapisan sesi (lapisan 5) kemudian telah diterima dan dipasang kembali dalam urutan yang sama.

Mari kita rangkum kelebihan dan kekurangan TCP pada tabel di bawah ini:

|Keuntungan|Kekurangan|
|:--------:|:--------:|
|Menjamin keakuratan data|Membutuhkan koneksi yang andal antara kedua perangkat. Jika satu potongan kecil data tidak diterima, maka seluruh potongan data tidak dapat digunakan|
|Mampu menyinkronkan dua perangkat untuk mencegah satu sama lain dibanjiri data.|Koneksi yang lambat dapat menghambat perangkat lain karena koneksi akan disimpan di komputer penerima sepanjang waktu.|
|Melakukan lebih banyak proses untuk keandalan.|TCP is significantly slower than UDP because more work has to be done by the devices using this protocol.|
