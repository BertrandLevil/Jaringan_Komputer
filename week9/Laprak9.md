Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 9 (Web Server)

Pertama kita review ulang mengenai osi layer yaitu bagaimana jaringan bekerja <br>
step 1 yaitu data dikirimkan dalam bentuk bit (0/1) melalui media fisik <br>
step 2 yaitu pengaturan untuk mengirim antar device / jaringan lokal <br>
step 3 menentukan jalur pengantaran <br>
step 4 mengatur koneksi dan keandalan data <br>
step 5 mengatur sesi komunikasi <br>
step 6 mengatur format data <br>
step 7 layer yang berinteraksi langsung dengan client <br>
![OsiLayer](../images/The-7-Layers-of-the-OSI-Model--1536x787.png)

Web server adalah bagaimana cara kita memvisualisasikan sebuah data langsung kepada client melalui browser <br>
Sehingga web server termasuk pada osi layer nomor 7 <p>

Selanjutnya kita langsung membuat sebuah file index.html dengan isian singkat untuk ditampilkan bila alamat web server diakses dengan sesuai <br>
![HTML](../images/Screenshot%202026-04-28%20115357.png)

Disini kita mempunyai sebuah skeleton code dari web server yang dapat kita kembangkan <br>
![Skeleton](../images/Screenshot%202026-04-28%20113542.png)

Setelah kita perbaiki skeleton code tadi kita dapat melihat codenya menjadi seperti ini, tujuan dari code ini mengupload file index.html ke website kita dengan port 6789 dan menampilkan 404 not found bila tidak berhasil, serta code ini hanya dapat menangani 1 klien saja <br> 
![Img1](../images/Screenshot%202026-04-28%20114224.png)

Bila kita menggunakan thread yang memungkinkan multi klien dapat mengakses web server yang sama kita dapat menggunakan code ini, kedua code kurang lebih berjalan sama persis hanya saja berbeda di jumlah klien yang dapat ditangani <br>
![Img2](../images/Screenshot%202026-04-28%20114213.png)

Kita langsung run kedua codingan tersebut <br>
![Img3](../images/Screenshot%202026-04-28%20114159.png)

![Img4](../images/Screenshot%202026-04-28%20114120.png)

Hasilnya menampilkan 404 not found apabila ada kesalahan dalam server atau tidak index.html atau alamat server yang diakses tidak sesuai (bukan index.html) <br>
![Img5](../images/Screenshot%202026-04-28%20114033.png)

Ini yang akan muncul ketika codingan berjalan sesuai <br>
![Img6](../images/Screenshot%202026-04-28%20114019.png)