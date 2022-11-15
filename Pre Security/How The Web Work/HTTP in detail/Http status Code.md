### HTTP Status Codes
Pada tugas sebelumnya, Anda mempelajari bahwa saat server HTTP merespons, baris pertama selalu berisi kode status yang menginformasikan klien tentang hasil permintaan mereka dan juga kemungkinan cara menanganinya. Kode status ini dapat dipecah menjadi 5 rentang berbeda:

|Kisaran|Penjelasan|
|:-----:|:--------:|
|100-199 - Information Responses| Ini dikirim untuk memberi tahu klien bahwa bagian pertama dari permintaan mereka telah diterima dan mereka harus terus mengirimkan sisa permintaan mereka. Kode-kode ini tidak lagi sangat umum.|
|200-299 - Success|Kisaran kode status ini digunakan untuk memberi tahu klien bahwa permintaan mereka berhasil.|
|300-399 - Redirection|Ini digunakan untuk mengarahkan permintaan klien ke sumber daya lain. Ini dapat berupa halaman web yang berbeda atau situs web yang berbeda sama sekali.|
|400-499 - Client Errors|Digunakan untuk memberi tahu klien bahwa ada kesalahan dengan permintaan mereka.|
|500-599 - Server Errors|Ini dicadangkan untuk kesalahan yang terjadi di sisi server dan biasanya menunjukkan masalah yang cukup besar dengan server yang menangani permintaan tersebut.|

### Status code http yang umum
Ada banyak kode status HTTP yang berbeda dan itu belum termasuk fakta bahwa aplikasi bahkan dapat mendefinisikannya sendiri, kami akan membahas respons HTTP paling umum yang mungkin Anda temui:

|code|Penjelasan|
|:--:|:--------:|
|200 - OK| Permintaan telah sukses|
|201 - Created|Sumber daya telah dibuat (misalnya pengguna baru atau entri blog baru).|
|301 - Permanent Redirect| Ini mengarahkan browser klien ke halaman web baru atau memberi tahu mesin pencari bahwa halaman tersebut telah pindah ke tempat lain dan sebagai gantinya mencari di sana.|
|302 - Temporary Redirect|Mirip dengan pengalihan permanen di atas, tetapi seperti namanya, ini hanya perubahan sementara dan dapat berubah lagi dalam waktu dekat.|
|400 - Bad Request|Ini memberi tahu browser bahwa ada sesuatu yang salah atau hilang dalam permintaan mereka. Ini terkadang dapat digunakan jika sumber daya server web yang diminta mengharapkan parameter tertentu yang tidak dikirim oleh klien.|
|401 - Not Authorised|Saat ini Anda tidak diizinkan untuk melihat sumber daya ini sampai Anda memiliki otorisasi dengan aplikasi web, paling sering dengan nama pengguna dan kata sandi.|
|403 - Forbidden|Anda tidak memiliki izin untuk melihat sumber daya ini baik Anda masuk ataupuun tidak.|
|405 - Method Not Allowed|
