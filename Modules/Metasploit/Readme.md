Metasploit adalah framework eksploitasi yang paling banyak digunakan. Metasploit adalah alat yang ampuh yang dapat mendukung semua fase keterlibatan dalam *penetration testing*, mulai dari *infomation gathering* hingga *post-exploitation*.

Metasploit mempunyai dua versi:
* **Metasploit pro**: Versi komersial yang memfasilitasi otomatisasi dan pengelolaan tugas. Versi ini memiliki *Graphic User Interface* (GUI).
* **Metasploit Framework**: Versi *open source* yang bekerja menggunakan *command line*. Modul ini akan fokus pada versi ini, diinstal pada distribusi Linux untuk *penetration testing* yang paling umum digunakan.

Metasploit Framework adalah seperangkat alat yang memungkinkan *information gathering, scanning,  exploitation, exploit development, post-exploitation*, dan banyak lagi. Sementara penggunaan utama *Metasploit Framework* berfokus pada domain pengujian penetrasi, itu juga berguna untuk penelitian kerentanan dan pengembangan eksploit.

Komponen utama Kerangka Metasploit dapat diringkas sebagai berikut;
1. **msfconsole**: *command-line* antarmuka utama
2. **Modules**: Mendukung modul seperti exploit, scanner, payload, dll.
3. **Tools**: Alat mandiri yang akan membantu dalam hal *vulnerability research, vulnerability assessment*, atau *penetration testing*. Beberapa alat ini adalah `msfvenom`, `pattern_create` dan `pattern_offset`. Kami akan membahas msfvenom dalam modul ini, tetapi pattern_create dan pattern_offset adalah alat yang berguna dalam mengeksploitasi pengembangan yang berada di luar cakupan modul ini.

