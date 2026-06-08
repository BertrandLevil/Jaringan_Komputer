Nama: Bertrand Lianto <br>
Nim: 103072400019 <br>
Kelas: IF-04-05 <br>
Modul: 13 (ARP & Ethernet) <br>

Definisi ARP secara sederhana adalah 
ARP (Address Resolution Protocol) adalah sebuah protokol dalam jaringan komputer yang berfungsi untuk mengaitkan alamat IP (Internet Protocol) dengan alamat fisik perangkat, yang dikenal sebagai alamat MAC (Media Access Control). Protokol ini memungkinkan perangkat dalam jaringan untuk menemukan alamat MAC yang sesuai dengan alamat IP yang diberikan, sehingga komunikasi data dapat dilakukan dengan benar<br>

Untuk memulai praktikum kita pertama melakukan syntax arp -d * dalam terminal untuk menghapus semua cache arp sehingga kita dapat menangkap ARP dengan lebih baik <br>
![Foto1](../images/Screenshot%202026-06-05%20134956.png)
Kemudian buka wireshark, terutama pada menu analyze -> enabled protocols kita uncheck opsi untuk ipv4 dan buka sebuah halaman random sebagai contoh disini kita membuka https://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-lab-file3.html <br>
![Foto2](../images/Screenshot%202026-06-05%20135308.png)
Karena kita masih belum dapat melihat arp broadcast diantara ribuan paket yang ada kita dapat melakukan filter arp pada search dan dapat dilihat disini bahwa arp akan bertanya seperti siapa yang punya ip xxx.xxx.0.1? beritau pada xxx.xxx.0.3 agar dapat berkomunikasi lebih lanjut, kita juga dapat melihat semua alamat MAC yang tersedia <br>
![Foto3](../images/Screenshot%202026-06-05%20135914.png)
