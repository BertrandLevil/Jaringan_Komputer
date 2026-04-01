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

1. Jalankan nslookup untuk mendapatkan alamat IP dari server web di Asia. Berapa alamat IP 
Alamat IP dari server web tersebut adalah  10.217.7.77
![Fotosoal1.1](../images/Screenshot%202026-03-31%20110855.png)
server tersebut? 
2. Jalankan nslookup agar dapat mengetahui server DNS otoritatif untuk universitas di Eropa. 
Server DNS otoritatif untuk universitas di Eropa dapat dilihat pada gambar berikut
![Fotosoal1.2](../images/Screenshot%202026-03-31%20110912.png)
3. Jalankan nslookup untuk mencari tahu informasi mengenai server email dari Yahoo! Mail 
Melalui salah satu server yang didapatkan di pertanyaan nomor 2. Apa alamat IP-nya? 
Alamat IP nya adalah sebagai berikut Addresses:  
          98.136.96.76
          98.136.96.75
          67.195.204.73
          98.136.96.74
          67.195.228.94
          67.195.228.110
          67.195.228.109
          67.195.204.79
![Fotosoal1.3](../images/Screenshot%202026-03-31%20111303.png)

1. Cari pesan permintaan DNS dan balasannya. Apakah pesan tersebut dikirimkan melalui UDP 
atau TCP? 
Pesan tersebut dikirim melalui UDP dapat dilihat pada internet protocol di bawah ini
![FotoSoal2.1](../images/Screenshot%202026-03-31%20112224.png)
2. Apa port tujuan pada pesan permintaan DNS? Apa port sumber pada pesan balasannya?
Port Tujuan dari permintaan DNS dan Port Sumber dari pesan balasannya sama yaitu 3163
![FotoSoal2.2a](../images/Screenshot%202026-03-31%20112253.png)
![FotoSoal2.2b](../images/Screenshot%202026-03-31%20112304.png)
3. Pada pesan permintaan DNS, apa alamat IP tujuannya? Apa alamat IP server DNS lokal anda 
(gunakan ipconfig untuk mencari tahu)? Apakah kedua alamat IP tersebut sama?
Alamat tujuan permintaan DNS adalah 128.238.29.23 Sedangkan Ip server dns lokal saya adalah 10.218.0.253, yaitu IP kita berbeda
![Fotosoal2.3](../images/Screenshot%202026-03-31%20112639.png) 
4. Periksa pesan permintaan DNS. Apa “jenis” atau ”type” dari pesan tersebut? Apakah pesan 
permintaan tersebut mengandung ”jawaban” atau ”answers”? 
Pesan tersebut cuma menampilkan answer 0 
![Fotosoal2.4](../images/Screenshot%202026-03-31%20112733.png)
5. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau ”answers” yang terdapat di 
dalamnya? Apa saja isi yang terkandung dalam setiap jawaban tersebut? 
Ya, isi yang terkandung adalah Nama, Tipe, Class, Time to live, Data length, dan address pada jawaban tersebut
![Fotosoal2.5](../images/Screenshot%202026-03-31%20112841.png)
6. Perhatikan paket TCP SYN yang selanjutnya dikirimkan oleh host Anda. Apakah alamat IP 
pada paket tersebut sesuai dengan alamat IP yang tertera pada pesan balasan DNS?
Ya, sesuai (karena browser langsung connect ke IP yang baru didapat dari DNS) 
![Fotosoal2.6](../images/Screenshot%202026-03-31%20113130.png)
7. Halaman web yang sebelumnya anda akses (http://www.ietf.org) memuat beberapa 
gambar. Apakah host Anda perlu mengirimkan pesan permintaan DNS baru setiap kali ingin 
mengakses suatu gambar?
Tidak ada DNS query baru. Browser sudah tahu IP dari DNS sebelumnya (DNS cache + same domain)
![Fotosoal2.7](../images/Screenshot%202026-03-31%20113219.png)

1. Apa port tujuan pada pesan permintaan DNS? Apa port sumber pada pesan balasan DNS?
Ya, keduanya sama port tujuan dari permintaan dan juga port sumber pada pesan balasan yaitu 53
![Fotosoal3.1a](../images/Screenshot%202026-03-31%20114837.png) 
![Fotosoal3.1b](../images/Screenshot%202026-03-31%20114852.png)
2. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut 
merupakan default alamat IP server DNS lokal Anda?
Alamat IP yang dituju dari permintaan DNS adalah 128.238.29.22 dan alamat IPnya tentu tidak akan sama dengan server dns lokal
![Fotosoal3.2](../images/Screenshot%202026-03-31%20114934.png) 
3. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan 
tersebut mengandung ”jawaban” atau ”answers”?
Pesan tersebut hanya mengandung answer 0 (tidak ada jawaban)
![Fotosoal3.3](../images/Screenshot%202026-03-31%20115008.png) 
4. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau “answers” yang terdapat di 
dalamnya. Apa saja isi yang terkandung dalam setiap jawaban tersebut? 
Ya, dapat dilihat isinya dalam screenshot ini sebagai berikut
![Fotosoal3.4](../images/Screenshot%202026-03-31%20115029.png)

1. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut 
merupakan default alamat IP server DNS lokal Anda? 
Alamat IP pesan permintaan DNS tersebut dikirimkan ke 10.217.7.77 dan akan sama karena tidak menggunakan server lain
2. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan 
tersebut mengandung ”jawaban” atau ”answers”? 
Jenis/Type = NS (Name Server query)
Mengandung answers? = Tidak (permintaan selalu 0 answers)
3. Periksa pesan balasan DNS. Apa nama server MIT yang diberikan oleh pesan balasan? 
Apakah pesan balasan ini juga memberikan alamat IP untuk server MIT tersebut?
Pesan balasan memberikan 3 nama server (Name Servers) MIT :
bitsy.mit.edu
strawb.mit.edu
w20ns.mit.edu
Ya, pesan balasan juga memberikan alamat IP untuk ketiga server tersebut. Dapat dilihat pada gambar
![Fotosoal4](../images/Screenshot%202026-03-31%20115911.png)

1. Ke alamat IP manakah pesan permintaan DNS dikirimkan? Apakah alamat IP tersebut 
merupakan default alamat IP server DNS lokal Anda? 
Tidak dapat mengetahui ip DNS permintaan DNS kita dikirimkan
2. Periksa pesan permintaan DNS. Apa ”jenis” atau ”type” dari pesan tersebut? Apakah pesan 
tersebut mengandung ”jawaban” atau ”answers”? 
Tidak ada answer
3. Periksa pesan balasan DNS. Berapa banyak ”jawaban” atau “answers” yang terdapat di 
dalamnya. Apa saja isi yang terkandung dalam setiap jawaban tersebut? 
Tidak ada answer
Tidak dapat menjawab semua soal diatas karena pasti akan menghasilkan timeout
Dapat dilihat pada gambar berikut 
![Fotosoal5](../images/Screenshot%202026-03-31%20120551.png)