Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 4 (DNS)
Pengertian DNS
Dns adalah Domain Name System yang bertujuan untuk mengubah alamat domain (manusia) menjadi alamat ip (komputer) ibarat media translasi
Contoh Pertama disini kita memiliki syntax yaitu nslookup www.mit.edu yang artinya menampilkan seluruh alamat ip dari domain mit.edu
![Foto1](../images/Screenshot%202026-03-30%20155121.png)
Selanjutnya kita memiliki syntax yaitu nslookup -type=NS mit.edu yang dimana bertujuan untuk menunjukkan server resmi yang mengelola domain tersebut
![Foto2](../images/Screenshot%202026-03-30%20155317.png)
Selanjutnya kita memiliki syntax nslookup www.aiit.or.kr bitsy.mit.edu yang bertujuan untuk mengecek apakah dns server bitsy.mit.edu mengetahui mengenai domain www.aiit.or.kr atau belum. Pada kasus ini hasilnya timeout.
![Foto4](../images/Screenshot%202026-03-30%20155713.png)
Selanjutnya kita memiliki syntax ipconfig /all. Syntax ini bertujuan untuk menampilkan seluruh jaringan yang ada di perangkat kita, dan hasilnya pasti akan sangat banyak sekali
![Foto5](../images/Screenshot%202026-03-30%20160059.png)
Selanjutnya kita memiliki syntax ipconfig /all > networkinfo.txt yang berfungsi seperti ipconfig /all namun menyimpan hasil jaringannya ke sebuah file yang bernama networkinfo dengan format txt
![Foto6](../images/Screenshot%202026-03-30%20160345.png)
![Foto7](../images/Screenshot%202026-03-30%20160508.png)
Selanjutnya kita memiliki syntax ipconfig /displaydns yang berfungsi menampilkan cache dns dari query yang sudah tersimpan, sehingga pencarian akan menjadi lebih cepat
![Foto9](../images/Screenshot%202026-03-30%20160729.png)
![Foto8](../images/Screenshot%202026-03-30%20160633.png)
Terakhir kita dapat melakukan ipconfig /flushdns untuk menghapus cache dns yang tersimpan
![Foto10](../images/Screenshot%202026-03-30%20160743.png)
Kita dapat melihat ip kita masing masing pada terminal, ipv4 Address
![Foto11](../images/Screenshot%202026-03-30%20161018.png)
Jika kita pergi ke WireShark kita dapat melihat hasil penangkapan jaringan dan memfilternya menggunakan ip kita sendiri yang tadi sudah kita dapatkan dari terminal
![Foto12](../images/Screenshot%202026-03-30%20161132.png)
Selanjutnya kita dapat membuka sebuah website seperti pada contoh ini adalah www.ietf.org
![Foto13](../images/Screenshot%202026-03-30%20161330.png)
Kemudian kita dapat memfilter tangkapan jaringan tersebut dengan menggunakan ip dan nama website yang dituju (kata mengandung nama website) namun disini ada typo dalam syntax, namun kita dapat melihat syntax yang benar pada contoh berikutnya pada filter mit
![Foto15](../images/Screenshot%202026-03-30%20162307.png)
Contoh syntax filter query yang benar
![Foto16](../images/Screenshot%202026-03-30%20162431.png)
Kita juga dapat melihat protokol internet yang digunakan serta port asal dan tujuan dari sebuah paket
![Foto17](../images/Screenshot%202026-03-30%20162637.png)


