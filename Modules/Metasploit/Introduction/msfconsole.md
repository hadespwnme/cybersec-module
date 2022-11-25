Seperti yang disebutkan sebelumnya, konsol akan menjadi antarmuka utama Anda di Metasploit Framework. Anda dapat meluncurkannya menggunakan perintah `msfconsole` di terminal Linux atau dimanapun tempat Metasploit Framework diinstal.

![msfconsole](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/msfconsole.png)

Setelah diluncurkan, Anda akan melihat baris perintah berubah menjadi msf5 (atau msf6 tergantung pada versi Metasploit yang terinstal). Konsol Metasploit (msfconsole) dapat digunakan seperti shell baris perintah biasa, seperti yang Anda lihat di bawah. Perintah pertama adalah `ls` yang mencantumkan isi folder tempat Metasploit diluncurkan menggunakan perintah `msfconsole`.

![msf-ls](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/msf-ls.png)

Metasploit mendukung sebagian besar perintah Linux, termasuk clear (untuk menghapus layar terminal), tetapi tidak akan memungkinkan Anda untuk menggunakan beberapa fitur dari baris perintah biasa (misalnya tidak mendukung pengalihan output), seperti yang terlihat di bawah ini.

![>](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/msf-%3E.png)

Fitur penting msfconsole adalah dukungan penyelesaian tab. Ini akan berguna nanti saat menggunakan perintah Metasploit atau berurusan dengan modul. Misalnya, jika Anda mulai mengetik `he` dan menekan tombol tab, Anda akan melihatnya selesai secara otomatis untuk perintah `help`.

Msfconsole dikelola oleh konteks; ini berarti bahwa kecuali ditetapkan sebagai variabel global, semua pengaturan parameter akan hilang jika Anda mengubah modul yang telah Anda putuskan untuk digunakan. Pada contoh di bawah ini, kami telah menggunakan eksploitasi ms17_010_eternalblue, dan kami telah menetapkan parameter seperti `RHOSTS`. Jika kita beralih ke modul lain (mis. Port scanner), kita perlu mengatur nilai RHOSTS lagi karena semua perubahan yang kita buat tetap dalam konteks eksploit ms17_010_eternalblue.

Mari kita lihat contoh di bawah ini untuk lebih memahami fitur ini. Kita akan menggunakan eksploitasi MS17-010 "Eternalblue" untuk tujuan ilustrasi.

Setelah Anda mengetik perintah `use exploit/windows/smb/ms17_010_eternalblue`, Anda akan melihat command line prompt berubah dari msf6 menjadi “msf6 exploit(windows/smb/ms17_010_eternalblue)”. "EternalBlue" adalah eksploit yang diduga dikembangkan oleh Badan Keamanan Nasional AS (N.S.A.) untuk kerentanan yang memengaruhi server SMBv1 pada banyak sistem Windows. SMB (Server Message Block) banyak digunakan di jaringan Windows untuk berbagi file dan bahkan untuk mengirim file ke printer. EternalBlue dibocorkan oleh kelompok penjahat siber "Shadow Brokers" pada April 2017. Pada Mei 2017, kerentanan ini dieksploitasi di seluruh dunia dalam serangan ransomware WannaCry.

![eteb](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/eternalblue.png)

Modul yang akan digunakan juga dapat dipilih dengan perintah `use` diikuti dengan nomor di awal baris hasil pencarian.

Meskipun prompt telah berubah, Anda akan melihat bahwa kami masih dapat menjalankan perintah yang disebutkan sebelumnya. Ini berarti kami tidak "memasukkan" folder seperti yang biasanya Anda harapkan di baris perintah sistem operasi.

![ls](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/etb-ls.png)

Prompt memberi tahu kita bahwa kita sekarang memiliki kumpulan konteks tempat kita akan bekerja. Anda dapat melihatnya dengan mengetikkan perintah `show options`.

![show](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/etb-show.png)

Ini akan mencetak opsi yang terkait dengan exploit yang telah kita pilih sebelumnya. Perintah show options akan memiliki output yang berbeda tergantung pada konteks yang digunakan. Contoh di atas menunjukkan bahwa exploit ini mengharuskan kita untuk mengatur variabel seperti RHOSTS dan RPORT. Di sisi lain, modul `post-exploitation` mungkin hanya membutuhkan kita untuk menyetel ID SESI (lihat tangkapan layar di bawah). Sesi adalah koneksi yang ada ke sistem target yang akan digunakan modul pasca-eksploitasi.

![post-show](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/post-show.png)

Perintah `show` dapat digunakan dalam konteks apa pun diikuti dengan jenis modul (auxiliary, payload, exploit, dll) untuk membuat daftar modul yang tersedia. Contoh di bawah mencantumkan payload yang dapat digunakan dengan eksploitasi ms17-010 Eternalblue.

![payload](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/payloads.png)

Jika digunakan dari prompt msfconsole, perintah show akan mencantumkan semua modul.

Perintah `use` dan `show options` yang telah kita lihat sejauh ini identik untuk semua modul di Metasploit.

Anda dapat meninggalkan konteks menggunakan perintah `back`.


