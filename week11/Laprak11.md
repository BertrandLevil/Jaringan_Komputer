Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 11 (DHCP)
DHCP atau Dynamic Host Configuration Protocol adalah protokol jaringan yang digunakan untuk memberikan konfigurasi IP secara otomatis kepada perangkat dalam jaringan. <br>
Biasanya mencakup <br>
IP Address
Subnet Mask
Default Gateway
DNS Server
Lease Time atau masa berlaku IP <br>
Plus Minus DHCP<br>
Plus konfigurasi ip otomatis, cepat, efisien, mempermudah mobilitas, mengurangi kesalahan konfigurasi IP, mencegah konflik, memasyikan IP valid<br>
Minus Bergantung pada server, potensi konflik jika salah konfigurasi, Keamanan lebih rendah<br>
Konfigurasi IP pada server dhcp dapat dilihat pada setting network, properties dari IPv4, dapat dilihat pada gambar di bawah sebagai berikut<br>
![Foto1](../images/Screenshot%202026-05-11%20153843.png)
Kita juga dapat melihat konfigurasi IP kita di dalam cmd dengan menggunakan syntax ipconfig yang dapat menampilkan subnet mask, gateway, ipv4 address itu sendiri, dapat dilihat pada gambar berikut <br>
![Foto2](../images/Screenshot%202026-05-11%20153946.png)
Terakhir kita akan membahas DORA yang berarti, discover, offer, request, acknowledge.<br>
Discover Pertama client akan bertanya apakah ada DHCP server? <br>
Offer Kemudian server membalas dengan memberikan IP 192.168.1.10 (contoh)<br>
Request Selanjutnya klien akan berkata seperti demikian "Saya ingin memakai IP 192.168.1.10" untuk meminta penggunaan ke server <br>
Acknowledge Terakhir DHCP server mengirim pesan DHCP Acknowledge sebagai konfirmasi bahwa IP tersebut resmi diberikan kepada client<br>
![Foto3](../images/Screenshot%202026-05-11%20160052.png)