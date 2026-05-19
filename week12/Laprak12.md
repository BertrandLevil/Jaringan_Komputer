Nama: Bertrand Lianto <br>
Nim: 103072400019 <br>
Kelas: IF-04-05 <br>
Modul: 12 (ICMP) <br>
Pokok pembasan pada modul kali ini adalah <br>
• Pesan ICMP yang dihasilkan oleh program Ping; <br> 
• Pesan ICMP yang dihasilkan oleh program Traceroute; <br> 
• format dan isi pesan ICMP. <br>
Pertama untuk melakukan ping dalam cmd kita dapat gunakan syntax -n x, dimana x adalah angka maksimum ping, sebagai contoh disini saya menggunakan -n 10, dimana cmd akan melakukan ping sebanyak 10. dan kebetulan disini hasilnya sukses semua (tidak ada rto) <br>
![Gambar1](../images/Screenshot%202026-05-18%20154530.png)
Ketika kita menggunakan wireshark untuk mendeteksi ping dari cmd, maka kita akan mendapatkan balasan untuk setiap pingnya, sebagai contoh disini saya melakukan 4x ping maka total ada 4x request dan 4x reply. <br>
![Gambar2](../images/Screenshot%202026-05-18%20154847.png)
Kita dapat melihat disini bahwa tipe pesan ICMP pada request adalah 8 <br>
![Gambar3](../images/Screenshot%202026-05-18%20155149.png)
Sedangkan untuk tipe pesan reply adalah 0 <br>
![Gambar4](../images/Screenshot%202026-05-18%20155324.png)
Selanjutnya disini kita dapat melakukan tracert, dan menangkap paket paketnya menggunakan wireshark, ketika sebuah hop mengalami RTO (koneksi tidak dapat menjangkau) maka kita dapat melihat pesannya berupa time to live exceed, dapat disimpulkan bahwa terjadi bottle neck pada port 120 <br>
![Gambar5](../images/Screenshot%202026-05-18%20155824.png)

Berikut merupakan format umum untuk pesan dalam ICMP <br>
| Field          |   Ukuran | Fungsi                                    | <br>
| Type           |    8 bit | Menentukan jenis pesan ICMP               | <br>
| Code           |    8 bit | Menjelaskan detail dari Type              | <br>
| Checksum       |   16 bit | Mengecek kesalahan pada paket ICMP        | <br>
| Rest of Header |   32 bit | Isinya tergantung jenis pesan ICMP        | <br>
| Data           | Variabel | Data tambahan atau bagian dari paket asli | <br>
