Nama: Bertrand Lianto <br>
Nim: 103072400019 <br>
Kelas: IF-04-05 <br>
Modul: 14 (WIFI) <br>

Materi minggu ini kita akan membahas mengenai wifi, pertama dalam jaringan wifi, kita dapat melihat perbedaan pada spek biasanya pada angka 2.4 GHz dan 5 GHz, kita dijelaskan bahwa perbedaan diantara keduanya yaitu berada pada kekuatan dan jarak, seperti 2.4 GHz unggul dalam jangkauan koneksi sedangkan 5 GHz akan unggul dalam hal kecepatan, berguna untuk kegiatan yang membutuhkan real time seperti game atau streaming. Kemudian kita juga diberikan penjelasan terkait AP (Access Point) yang berfungsi untuk memperpanjang jangkauan wifi agar dapat dikoneksikan kepada user, dan user dapat berpindah antar Access point bila user berpindah tempat, dan device user akan otomatis menyambungkan ke access point lain terdekat bila ada <br>
Beacon frame merupakan sesuatu yang dikirim terus menerus oleh perangkat ke AP/wifi atau sebaliknya yang bertujuan untuk mengkonfirmasi keberadaan dan status perangkat seperti terhubung/tidak terhubung <br>
Dapat dilihat di wireshark bahwa kita dapat menyaring menggunakan wlan fc subtype dengan kode 0 dan 8, serta informasi bahwa beacon frame yang dikirimkan setiap 8 milisekon interval<br>
![Foto3](../images/Screenshot%202026-06-08%20155319.png)
Kita juga dapat melihat nama wifi yang digunakkan pada record wireshark yang digunakan pada parameter SSID yaitu 30 monroe st <br>
![Foto5](../images/Screenshot%202026-06-08%20155721.png)
Kemudian kita dapat melihat penangkapan paket terhadap alice.txt, dan pada file ini jelas sebuah paket memiliki informasi tambahan seperti radio, dan informasi IEEE, yang jelas tidak ada pada modul sebelumnya, karena kita belajar bahwa user tidak langsung connect ke sebuah router namun ada invisible wireless sebagai perantara jaringan <br>
![Foto6](../images/Screenshot%202026-06-08%20160544.png)
Kita juga dapat melihat informasi tambahan seperti MAC address yang digunakkan <br>
![Foto7](../images/Screenshot%202026-06-08%20160710.png)
Kemudian kita lanjut ke associate request dan respond yang akan terjadi ketika kita berpindah dari suatu AP ke AP yang lain, kita dapat menerapkan filter subtype 0 untuk memfilter sebuah request <br>
![Foto8](../images/Screenshot%202026-06-08%20161219.png)
Kita dapat melihat disini bahwa waktu dalam association request disini adalah 314 microsekon aja <br>
![Foto9](../images/Screenshot%202026-06-08%20161408.png)
Kita dapat melihat nama AP nya disini dalam parameter SSID <br>
![Foto10](../images/Screenshot%202026-06-08%20161426.png)
Kemudian kita dapat bandingkan dalam paket terakhir bahwa nama parameter SSIDnya berbeda dengan yang tadi <br>
![Foto11](../images/Screenshot%202026-06-08%20161511.png)
Kita juga dapat menggunakan filter dengan wlan.fc.subtype == 1 untuk menyaring frame 802.11, dan ternyata hanya ada 1 paket <br>
![Foto12](../images/Screenshot%202026-06-08%20161644.png)
Terakhir kita dapat menggunakan filter wlan.fc.subtype == 10 / disini menggunakan 0x0a dalam hexa untuk melihat respond yang diberikan, namun tidak ada paket respond yang terlihat dalam file zip tersebut <br>
![Foto13](../images/Screenshot%202026-06-08%20161850.png)