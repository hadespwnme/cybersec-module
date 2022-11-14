*User Datagram Protocol* (UDP) adalah protokol lain yang digunakan untuk mengkomunikasikan data antar perangkat.

Tidak seperti saudaranya TCP, UDP adalah protokol stateless yang tidak memerlukan koneksi konstan antara dua perangkat untuk mengirim data. Misalnya, *Three-way handshake* tidak terjadi, juga tidak ada sinkronisasi antara kedua perangkat.

Ingat beberapa perbandingan yang dibuat tentang dua protokol ini di folder  "Model OSI". Yaitu, UDP digunakan dalam situasi di mana aplikasi dapat mentolerir kehilangan data (seperti streaming video atau obrolan suara) atau dalam skenario di mana koneksi yang tidak stabil bukanlah tujuan akhir. Tabel yang membandingkan kelebihan dan kekurangan UDP terletak di bawah ini:

|Kelebihan|Kekurangan|
|:-------:|:--------:|
|UDP lebih cepat dari TCP|UDP tidak perduli data terkirim atau tidak|
|UDP meninggalkan aplikasi (perangkat lunak pengguna) untuk memutuskan apakah ada kendali atas seberapa cepat paket dikirim.|Ini cukup fleksibel untuk pengembang perangkat lunak dalam pengertian ini.|
|UDP tidak mencadangkan koneksi berkelanjutan pada perangkat seperti halnya TCP.|Ini berarti bahwa koneksi yang tidak stabil menghasilkan pengalaman yang buruk bagi pengguna.|

Seperti disebutkan, tidak ada proses yang terjadi dalam menyiapkan koneksi antara dua perangkat. Artinya tidak ada mempertimbangkan apakah data diterima atau tidak, dan tidak ada perlindungan seperti yang ditawarkan oleh TCP, seperti integritas data.

Paket UDP jauh lebih sederhana daripada paket TCP dan memiliki header yang lebih sedikit. Namun, kedua protokol berbagi beberapa header standar, yang dijelaskan dalam tabel di bawah ini:

|HEADER|Penjelasan|
|:----:|:--------:|
|Time To Live(TTL)|Bidang ini menetapkan waktu kedaluwarsa untuk paket, sehingga tidak menyumbat jaringan Anda jika tidak pernah berhasil mencapai host atau *escape*!|
|*Source Address*|Alamat IP perangkat dari mana paket dikirim, sehingga data tahu ke mana harus kembali.|
|*Destination Address*|Alamat IP perangkat yang menjadi tujuan pengiriman paket sehingga data tahu ke mana harus pergi selanjutnya.|
|*Source Port*|Nilai ini adalah port yang dibuka oleh pengirim untuk mengirim paket TCP. Nilai ini dipilih secara acak (keluar dari port 0-65535 yang belum digunakan pada saat itu).|
|*Destination Port*|Nilai ini adalah nomor port yang dijalankan aplikasi atau layanan di host jarak jauh (yang menerima data); misalnya, server web berjalan di port 80. Berbeda dengan port sumber, nilai ini tidak dipilih secara acak.|
|DATA|Header ini adalah tempat penyimpanan data, yaitu byte dari file yang sedang dikirim.|

Selanjutnya, kita akan membahas bagaimana proses koneksi melalui UDP berbeda dari sesuatu seperti TCP. Kita harus ingat bahwa UDP itu stateless. Tidak ada pengakuan yang dikirim selama koneksi.

Gambardi bawah ini menunjukkan koneksi UDP normal antara Alice dan Bob. Dalam kehidupan nyata, ini akan berada di antara dua perangkat.

![udphanshake](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Pre%20Security/Network%20Fundamental/Packets%20%26%20frames/Image/udpshake-1.png)
