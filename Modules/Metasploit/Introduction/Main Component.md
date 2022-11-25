Saat menggunakan Metasploit Framework, Anda akan berinteraksi dengan konsol Metasploit. Anda dapat meluncurkannya dari terminal Linux Anda menggunakan perintah `msfconsole`. Konsol akan menjadi antarmuka utama Anda untuk berinteraksi dengan berbagai modul Metasploit Framework. Modul adalah komponen kecil dalam Metasploit Framework yang dibuat untuk melakukan tugas tertentu, seperti mengeksploitasi kerentanan, memindai target, atau melakukan serangan brute force.

Sebelum mendalami modul, akan sangat membantu untuk mengklarifikasi beberapa konsep berulang: kerentanan, eksploitasi, dan payload.
* Eksploitasi: Sepotong kode yang rentan yang ada pada sistem target.
* Kerentanan: Cacat desain, pengkodean, atau logika yang memengaruhi sistem target. Eksploitasi kerentanan dapat mengakibatkan terungkapnya informasi rahasia atau memungkinkan penyerang mengeksekusi kode pada sistem target.
* Payload: Eksploitasi akan memanfaatkan kerentanan. Namun, jika kita ingin exploit mendapatkan hasil yang kita inginkan (mendapatkan akses ke sistem target, membaca informasi rahasia, dll.), kita perlu menggunakan payload. Payload adalah kode yang akan dijalankan pada sistem target.

Modul dan kategori di bawah masing-masing tercantum di bawah ini. Ini diberikan untuk tujuan referensi, tetapi Anda akan berinteraksi dengan mereka melalui konsol Metasploit (msfconsole).

**Auxiliary**: Semua modul pendukung, seperti scanner, crawler, dan fuzzers, dapat ditemukan di sini.

![aux](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/aux.png)

**Encoder**: Encoder akan memungkinkan Anda untuk *encode* exploit dan payload dengan harapan signature-based antivirus melewatkannya.

Antivirus dan keamanan *signature-based* memiliki basis data ancaman yang diketahui. Mereka mendeteksi ancaman dengan membandingkan file yang mencurigakan dengan database ini dan memberikan peringatan jika ada kecocokan. Dengan demikian pembuat enkode dapat memiliki tingkat keberhasilan yang terbatas karena Antivirus dapat melakukan pemeriksaan tambahan.

![enc](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/814490c07d05616009169c80cbb173a5.png)

**Evasion**: Meskipun pembuat enkode akan meng-encode payload, tidak boleh dianggap sebagai upaya langsung untuk menghindari perangkat lunak antivirus.
Di sisi lain, modul "Evasion" akan mencobanya, dengan keberhasilan yang kurang lebih.

![eva](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/evasion.png)

**Exploit**: Eksploitasi, diatur dengan rapi oleh sistem target.

![exploit](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/exploit.png)

**NOP**: NOP (*NO Operation*) tidak melakukan apa-apa, secara harfiah.

Mereka diwakili dalam keluarga CPU Intel x86, mereka diwakili dengan 0x90, setelah itu CPU tidak akan melakukan apa pun untuk satu siklus. Mereka sering digunakan sebagai penyangga untuk mencapai ukuran muatan yang konsisten.

![nop](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/nops.png)

**Payload**: Payload adalah kode yang akan dijalankan pada sistem target.

Eksploitasi akan memanfaatkan kerentanan pada sistem target, tetapi untuk mencapai hasil yang diinginkan, kita memerlukan payload. Contohnya bisa jadi; mendapatkan shell, memuat malware atau backdoor ke sistem target, menjalankan perintah, atau meluncurkan calc.exe sebagai bukti konsep untuk ditambahkan ke laporan pengujian penetrasi. Memulai kalkulator pada sistem target dari jarak jauh dengan meluncurkan aplikasi calc.exe adalah cara yang baik untuk menunjukkan bahwa kita dapat menjalankan perintah pada sistem target.

Menjalankan perintah pada sistem target sudah merupakan langkah penting tetapi memiliki koneksi interaktif yang memungkinkan Anda mengetik perintah yang akan dijalankan pada sistem target lebih baik. Baris perintah interaktif semacam itu disebut "shell". Metasploit menawarkan kemampuan untuk mengirim payload berbeda yang dapat melakukan *open-shell* pada sistem target.

![payload](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/payloads.png)

Kamu akan menemukan tida direktori dalam payload:
1. **Singles**: Payload mandiri (tambahkan pengguna, luncurkan notepad.exe, dll.) yang tidak perlu mengunduh komponen tambahan untuk dijalankan.
2. **Stagers**: Bertanggung jawab untuk menyiapkan saluran koneksi antara Metasploit dan sistem target. Berguna saat bekerja dengan muatan bertahap. “Staged payloads” pertama-tama akan mengunggah stager pada sistem target kemudian mengunduh payload (tahapan) lainnya. Ini memberikan beberapa keuntungan karena ukuran awal payload akan relatif kecil dibandingkan dengan full payload yang dikirim sekaligus.
3. **Stages**: Diunduh oleh stager. Ini akan memungkinkan Anda untuk menggunakan payload berukuran lebih besar.

Metasploit memiliki cara halus untuk membantu Anda mengidentifikasi payload tunggal (juga disebut "inline") dan muatan bertahap.
* generic/shell_reverse_tcp
* windows/x64/shell/reverse_tcp

Keduanya adalah *reverse shell windows*. Yang pertama adalah payload inline (atau tunggal), seperti yang ditunjukkan oleh "_" antara "shell" dan "reverse". Sedangkan yang terakhir adalah staged payload, seperti yang ditunjukkan dengan tanda “/” antara “shell” dan “reverse”.

**Post**: Modul Posting akan berguna pada tahap akhir dari proses pengujian penetrasi yang tercantum di atas, post-exploitation.

![post](https://raw.githubusercontent.com/yingcrackerhades/cybersec-module/main/Modules/Metasploit/Image/post.png)

Jika Anda ingin membiasakan diri lebih jauh dengan modul-modul ini, Anda dapat menemukannya di bawah folder modul instalasi Metasploit Anda. Untuk AttackBox ini berada di bawah /opt/metasploit-framework-5101/modules
