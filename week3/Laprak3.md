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
Paket yang dikirim akan dibagi menjadi 4. Supaya apabila terjadi kesalahan pengiriman paket maka paket akan dilanjutkan dari checkpoint terakhir, tidak mengulang dari awal. 

 ![Foto3](../images/Screenshot%202026-03-13%20193741.png)
 Bagi Website yang membutuhkan Username dan Password maka kita juga dapat melihat perbedaannya apabila login info yang kita berikan valid/tidak valid. 

 Ini contoh apabila Password/Username yang diberikan tidak valid (Unauthorized). 

 ![Foto4](../images/Screenshot%202026-03-12%20134536.png)
 Ini contoh apabila Password/Username yang diberikan valid (OK). 

 ![Foto5](../images/Screenshot%202026-03-12%20134557.png)