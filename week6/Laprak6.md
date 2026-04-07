Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 6 (TCP)

Pada praktikum minggu ini pertama-tama kita disuruh untuk membuka sebuah website yang berisi banyak tulisan yang dapat kita simpan dalam file bentuk txt
![Foto1](../images/Screenshot%202026-04-06%20152558.png)
Lalu kita menyimpan file tersebut ke dalam perangkat dengan nama alice.txt setelah itu kita membuka sebuah website lagi disini, untuk mengupload file alice.txt yang telah kita unduh tadi
![Foto2](../images/Screenshot%202026-04-06%20152616.png)
Tampilan berhasil pada layar website bila upload kita telah berhasil dan diterima server
![Foto3](../images/Screenshot%202026-04-06%20152828.png)
Selanjutnya kita buka WireShark kita untuk melihat jaringan yang berkomunikasi
![Foto4](../images/Screenshot%202026-04-06%20153238.png)
Dapat dilihat disini bahwa paket file tadi yang kita upload sebenarnya dipecah menjadi berbagai segmen ketika mengupload (ciri khas protokol internet TCP)
![Foto5](../images/Screenshot%202026-04-06%20153414.png)
1. Berapa alamat IP dan nomor port TCP yang digunakan oleh komputer klien (sumber) untuk 
mentransfer file ke gaia.cs.umass.edu? Cara paling mudah menjawab pertanyaan ini adalah 
dengan memilih sebuah pesan HTTP dan meneliti detail paket TCP yang digunakan untuk 
membawa pesan HTTP tersebut.
Kita dapat melihat IP dan nomor port dari sumber seperti berikut, yaitu 10.218.15.24 dan 55626
![Foto6](../images/Screenshot%202026-04-06%20154117.png)
2. Apa alamat IP dari gaia.cs.umass.edu? Pada nomor port berapa ia mengirim dan menerima 
segmen TCP untuk koneksi ini? 
Kita dapat melihatnya pada screenshot ini pada Destination IP dan Destination port, yaitu 128.119.245.12 dan 80
![Foto7](../images/Screenshot%202026-04-06%20154140.png)
3. Berapa alamat IP dan nomor port TCP yang digunakan oleh komputer klien Anda (sumber) 
untuk mentransfer  ke gaia.cs.umass.edu?
Alamat IP saya adalah  10.217.7.77 seperti pada cmd ini dan port yang digunakan adalah 55626
![Foto9](../images/Screenshot%202026-04-06%20154349.png)
1. Berapa nomor urut segmen TCP SYN yang digunakan untuk memulai sambungan TCP antara 
komputer klien dan gaia.cs.umass.edu? Apa yang dimiliki segmen tersebut sehingga 
teridentifikasi sebagai segmen SYN? 
Nomor urut SYN adalah 1
Segmen teridentifikasi sebagai SYN karena flag SYN = 1 dan ACK = 0 (ini adalah segmen pembuka koneksi / 3-way handshake)
![Foto10](../images/Screenshot%202026-04-06%20154908.png)
2. Berapa nomor urut segmen SYNACK yang dikirim oleh gaia.cs.umass.edu ke komputer klien 
sebagai balasan dari SYN? Berapa nilai dari field Acknowledgement pada segmen SYNACK? 
Bagaimana gaia.cs.umass.edu menentukan nilai tersebut? Apa yang dimiliki oleh segmen  
sehingga teridentifikasi sebagai segmen SYNACK? 
Nomor urut SYNACK adalah 213
Nilai acknowledgement berarti 23 + 1 = 24
Gaia menentukan nilai tersebut karena setiap flag SYN mengonsumsi 1 nomor urut.
Segmen teridentifikasi sebagai SYNACK karena SYN = 1 dan ACK = 1.
![Foto11](../images/Screenshot%202026-04-06%20155107.png)
3. Berapa nomor urut segmen TCP yang berisi perintah HTTP POST? Perhatikan bahwa untuk 
menemukan perintah POST, Anda harus menelusuri content field milik paket di bagian 
bawah jendela Wireshark, kemudian cari segmen yang berisi "POST" di bagian field DATA
nya. 
Nomor urut = 199 seperti terlihat pada gambar
![Foto8](../images/Screenshot%202026-04-07%20230414.png)
4. Anggap segmen TCP yang berisi HTTP POST sebagai segmen pertama dalam koneksi TCP. 
Berapa nomor urut dari enam segmen pertama dalam TCP (termasuk segmen yang berisi 
HTTP POST)? Pada jam berapa setiap segmen dikirim? Kapan ACK untuk setiap segmen 
diterima? Dengan adanya perbedaan antara kapan setiap segmen TCP dikirim dan kapan 
acknowledgement-nya diterima, berapakah nilai RTT untuk keenam segmen tersebut? 
Berapa nilai EstimatedRTT setelah penerimaan setiap ACK? (Catatan: Wireshark memiliki 
fitur yang memungkinkan Anda untuk memplot RTT untuk setiap segmen TCP yang dikirim. 
Pilih segmen TCP yang dikirim dari klien ke server gaia.cs.umass.edu pada jendela "daftar
paket yang ditangkap". Kemudian pilih: Statistics->TCP Stream Graph- >Round Trip Time 
Graph). 
Nomor urut 6 segmen pertama adalah 565+1460x5 = 7865
![Foto14](../images/Screenshot%202026-04-06%20160229.png)
nilai RTT (Waktu ACK diterima - Waktu segmen terkirim sekitar 300 MS) = Nilai estimasi
Kita dapat melihat statistik RTT langsung dari WireShark seperti berikut
![Foto13](../images/Screenshot%202026-04-06%20155823.png)
5. Berapa panjang setiap enam segmen TCP pertama?
Panjangnya ada 565 dan 1460, bila di total 7865 panjangnya
![Foto14](../images/Screenshot%202026-04-06%20160229.png)
6. Berapa jumlah minimum ruang buffer tersedia yang disarankan kepada penerima dan 
diterima untuk seluruh trace? Apakah kurangnya ruang buffer penerima pernah 
menghambat pengiriman? 
Sesuai pada nilai window disini yaitu 5840, Tidak karena buffer tidak memengaruhi kecepatan pengiriman
![Foto15](../images/Screenshot%202026-04-06%20160428.png)
7. Apakah ada segmen yang ditransmisikan ulang dalam file trace? Apa yang anda periksa (di 
dalam file trace) untuk menjawab pertanyaan ini? 
Dapat dilihat pada gambar ini bahwa tidak ada segmen yang dikirimkan ulang
![Foto16](../images/Screenshot%202026-04-06%20160722.png)
8. Berapa banyak data yang biasanya diakui oleh penerima dalam ACK? Dapatkah anda 
mengidentifikasi kasus-kasus di mana penerima melakukan ACK untuk setiap segmen yang 
diterima? 
Kita ambil contoh nilai ACKnya yaitu 7866 ke 9013 berarti nilai yang di ACK sekaligus adalah 1147 byte, ya kalau ada selisih nomor ACKnya
![Foto17](../images/Screenshot%202026-04-06%20161017.png)
9. Berapa throughput (byte yang ditransfer per satuan waktu) untuk sambungan TCP? 
Jelaskan bagaimana Anda menghitung nilai ini. 
Dapat dilihat pada gambar ini bahwa average Throughput nya berkisaran antara 170-270 kbps, nilai didapat dari diagram throughput langsung
![Foto18](../images/Screenshot%202026-04-06%20161126.png)
Tambahan untuk grafik sequence number dari steven
![Foto19](../images/Screenshot%202026-04-06%20161447.png)