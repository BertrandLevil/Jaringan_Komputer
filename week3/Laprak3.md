Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 3 (Pengenalan HTTP)
# Get-Response HTTP

Ketika kita sedang membrowsing atau membuka sebuah website HTTP, kita akan melakukan Request & Response dari server. Ada beberapa status code yang kita pelajari 

Kode 1xx (Informational) = Request telah diterima server 

Kode 2xx (Success) = Request berhasil 

Kode 3xx (Redirect) = Biasanya diarahkan ke laman lain terlebih dahulu 

Kode 4xx (Client error) = Kesalahan client sehingga request ditolak 

Kode 5xx (Server error) = Kesalahan server sehingga request tidak diterima 

Disini kita membuka sebuah website dapat dilihat bahwa kita telah melakukan Request dan memperoleh status code 200 yang artinya berhasil. 

 ![Foto1](../images/Screenshot%202026-03-13%20193323.png)

Contoh bila kita menghapus cache kemudian kita membuka ulang website yang sama maka kita akan memperoleh status code 3xx yang berarti di redirect. Bila terdapat gambar dalam website tersebut maka Wireshark akan menangkap paket tersebut juga. 

 ![Foto2](../images/Screenshot%202026-03-13%20193617.png)
Paket yang dikirim akan dibagi menjadi 4. Supaya apabila terjadi kesalahan pengiriman paket maka paket akan dilanjutkan dari checkpoint terakhir, tidak mengulang dari awal. <br>

<br>
Revisi praktikum penambahan modul <br>
Pertama kita akan membuka sebuah website http yang berisikan html pada modul yaitu http://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-file1.html <br>
![Foto4](../images/Screenshot%202026-06-16%20135359.png)
Kita dapat melihat pada wireshark bahwa jaringan akan melakukan get dan post, kita meminta akses kepada suatu halaman kemudian halaman website tersebut memberikan dengan kode 2xx yaitu oke, yang artinya permintaan kita disetujui <br>
![Foto3](../images/Screenshot%202026-06-16%20135351.png)
Selanjutnya kita akan membuka sebuah website yaitu http://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-file2.html <br>
![Foto5](../images/Screenshot%202026-06-16%20135441.png)
Ketika kita membuka sebuah website kemudian mereload ulang/membuka kembali dalam tempo yang sangat cepat, maka akan muncul kode 3xx not modified, artinya website tersebut dapat dibuka secara sangat cepat berkat cache <br>
![Foto5](../images/Screenshot%202026-06-16%20135515.png)
Kemudian kita akan membuka lagi website selanjutnya yaitu http://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-file3.html <br>
![Foto6](../images/Screenshot%202026-06-16%20135541.png)
Disini kita dapat melihat bahwa terdapat http get dan response seperti biasanya namun ada beberapa paket yang menampilkan TCP segment of a reassembled PDU karena halaman file yang besar dan akan dilalui proses segmentasi <br>
![Foto7](../images/Screenshot%202026-06-16%20135651.png)
Kita buka lagi link berikutnya yaitu http://gaia.cs.umass.edu/wireshark-labs/HTTP-wireshark-file4.html <br>
![Foto8](../images/Screenshot%202026-06-16%20135719.png)
Ketika kita mengklik embed linknya, maka kita akan mengalami redirect ke halaman lain, seperti ini <br>
![Foto9](../images/Screenshot%202026-06-16%20135826.png)
Tentu kita dapat melihat paket html itu sendiri <br>
![Foto10](../images/Screenshot%202026-06-16%20140713.png)
Beserta paket yang berisikan gambar pada halaman website tersebut <br>
![Foto11](../images/Screenshot%202026-06-16%20140722.png)
Terakhir kita akan pergi ke http://gaia.cs.umass.edu/wireshark-labs/protected_pages/HTTP-wireshark-file5.html  dan memasukkan sebuah username dan password secara random terlebih dahulu, yang dimana hasilnya akan ditolak dan kita harus input password ulang dengan format yang benar yaitu<br> Username: wireshark-students<br>
Password: network<br>
![Foto12](../images/Screenshot%202026-06-16%20140802.png)
Kita dapat melihat bahwa paket akan ditandai unauthorized untuk percobaan yang gagal (tidak berhasil login) dan akan mendapatkan respond 2xx ok untuk percobaan yang sukses (berhasil login) <br>
![Foto13](../images/Screenshot%202026-06-16%20140816.png)