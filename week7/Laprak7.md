Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 7 (Socket)

Pada minggu ini kita akan mengetes bagaimana socket bekerja menggunakan bahasa python
Pertama-tama kita akan membuat virtual environment yang dimana akan menjadi tempat komunikasi antar client-server
Kemudian kita aktifkan venv tersebut (jarkom2)
![Foto1](../images/Screenshot%202026-04-13%20154756.png)

Pada codingan ini kita dapat mengimport library socket, kita berikan letak server kita (perangkat sendiri/localhost)
kita gunakan port 12000, kemudian deklarasikan socket tcp client, kemudian hubungkan dengan servernya, buat while loop untuk menerima input terus-menerus
Kemudian kirim pesan ke server dalam encode, buat kondisi untuk user keluar dari program ketika input exit (lower) yang dimana akan melakukan status loop false dan break, jika tidak keluar maka
terima balasan dari server, yang telah di decode, tutup koneksi server
![Foto4](../images/Screenshot%202026-04-13%20162203.png)
Untuk server kurang lebih sama, kita import library dan tentukan port server, buat socketnya dulu, ikat socketnya ke port 12000 agar bisa terhubung, dengarkan 1 antrian, lakukan loop selama server masih hidup, tunggu koneksi dari client dan decode pesannya, bila tidak ada maka keluar dari loop,  jika exit (lower) diinputkan maka server akan ditutup, jika tidak maka ubah pesan yang diterima menjadi besar (upper)
kirim balik ke server pesannya, tutup koneksi server
![Foto3](../images/Screenshot%202026-04-13%20162156.png)
Contoh simulasi TCP
![Foto2](../images/Screenshot%202026-04-13%20162148.png)

Pada UDP kita dapat melakukan import socket, dan system, kita tuliskan ip tujuan, port server, dan buat socket UDP, kita buatkan timeout agar ketika server tidak membalas maka akan menghasilkan error
loop input, jika kosong inputnya ulangi lagi, kirim pesan yang di encode ke alamat server, jika user ketik exit (lower) maka keluar dari program / exit server, dan buatkan kondisi jika user ketik keluar maka hanya akan keluar dari client, blok untuk menerima balasan, terima pesan balasan dari alamat server yang telah di decode, buat exception timeout, dan exxception untuk error yang lain, tutup socket.
![Foto7](../images/Screenshot%202026-04-13%20165524.png)
Untuk server kita dapat import socket, import system, konfigurasi server, config port servernya, buat socket UDPnya, ikat IP dan port 12000, buat loop utama server selagi server nyala, terima pesan dari client yang memiliki client addressnya juga, decode pesannya dan ubah ke huruf kecil, jika pesannya exit maka berhentikan servernya, kemudian ubah lagi ke huruf besar,tampilkan IP, port dan pesan client, kirim balik dan encode pesan dari server ke client ke alamat client, buat exception untuk error, dan tutup socket.
![Foto8](../images/Screenshot%202026-04-13%20165531.png)
Contoh simulasi UDP
![Foto6](../images/Screenshot%202026-04-13%20165513.png)