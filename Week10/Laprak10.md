Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 10 (IP)

IP Address adalah alamat unik yang digunakan untuk mengidentifikasi perangkat dalam jaringan (internet atau LAN). IP setiap perangkat pasti berbeda didalam jaringan yang sama, namun tidak menutup kemungkinan untuk 2 perangkat berbeda memiliki IP yang sama diluar jaringan yang sama. <BR>
![IMG1](../images/Screenshot%202026-05-04%20153514.png)
Kita disini melakukan jalur (hop) yang dilewati paket menuju sebuah website, kita menggunakan syntax tracert untuk melakukan tracking, kita juga dapat melihat berapa lama sebuah respond diantara setiap hop, sebagai contoh disini kita akan menuju website gaia.cs.umass.edu dengan sekitar 28x hop termasuk server request timeout. <BR>
![IMG2](../images/Screenshot%202026-05-04%20154800.png)
Contoh tracking website yang lain: <BR>
![IMG6](../images/Screenshot%202026-05-05%20000921.png)
Kemudian kita juga mempelajari beberapa istilah seperti <BR>
ICMP (Internet Control Message Protocol) <BR>
Digunakan untuk komunikasi error & status <BR>
Contoh: ping <BR>
MTU (Maximum Transmission Unit) <BR>
Ukuran maksimum paket data yang bisa dikirim tanpa fragmentasi <BR>
Contoh umum: 3000 bytes <BR>
TTL (Time To Live) <BR>
Batas jumlah hop sebelum paket dibuang <BR>
Dipakai oleh traceroute <BR>
Kemudian disini kita dapat mengecek sebuah ICMP dari sebuah file yang telah disediakan <BR>
![IMG3](../images/Screenshot%202026-05-04%20155646.png)
Kita dapat melihat TTLnya adalah 11 <BR>
![IMG4](../images/Screenshot%202026-05-04%20160007.png)
Dan di paket tersebut ternyata tidak ada fragmentasi yang offset. <BR>
![IMG5](../images/Screenshot%202026-05-04%20160235.png)
Maka dari itu kita coba untuk melakukan ping google.com -l 2000 untuk memaksa kita mengirim 2000 bytes yang memaksa untuk terjadinya fragmentasi <BR>
![IMG7](../images/Screenshot%202026-05-05%20001445.png)
Ini adalah salah satu contoh penangkapan IPv6 dengan melakukan ping -6 ::1 <BR>
![IMG8](../images/Screenshot%202026-05-05%20002325.png)