JavaScript (JS) adalah salah satu bahasa pemrograman paling populer di dunia dan memungkinkan halaman menjadi interaktif. HTML digunakan untuk membuat struktur dan konten situs web, sedangkan JavaScript digunakan untuk mengontrol fungsionalitas halaman web - tanpa JavaScript, halaman tidak akan memiliki elemen interaktif dan akan selalu statis. JS dapat memperbarui halaman secara dinamis secara real-time, memberikan fungsionalitas untuk mengubah gaya tombol saat peristiwa tertentu pada halaman terjadi (seperti saat pengguna mengklik tombol) atau untuk menampilkan animasi bergerak.

JavaScript ditambahkan di dalam *source code* halaman dan dapat dimuat di dalam tag `<script>` atau dapat disertakan dari luar dengan atribut src: `<script src="/lokasi/file_javascript.js"></script>`

Kode JavaScript berikut menemukan elemen HTML pada halaman dengan id "demo" dan mengubah konten elemen menjadi "Hack the Planet" : `document.getElementById("demo").innerHTML = "Hack the Planet";`

Elemen HTML juga dapat memiliki *event*, seperti "onclick" atau "onhover" yang mengeksekusi JavaScript saat peristiwa tersebut terjadi. Kode berikut mengubah teks elemen dengan ID demo menjadi Button Clicked: `<button onclick='document.getElementById("demo").innerHTML = "Button Clicked";'>Click Me!</button>` - event onclick juga dapat didefinisikan di dalam tag skrip JavaScript, dan bukan pada elemen secara langsung.

