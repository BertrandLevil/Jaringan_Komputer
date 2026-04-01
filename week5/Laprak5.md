Nama: Bertrand Lianto
Nim: 103072400019
Kelas: IF-04-05
Modul: 5 (UDP)

Pada modul 5 UDP kali ini, tidak banyak yang dibahas, kita cukup mendownload sebuah folder untuk mempelajari lebih lanjut tentang protokol internet UDP.
Setelah mengunduh folder tersebut yang bertipe ZIP kita dapat mengekstraknya sehingga mendapatkan file file sebagai berikut (yang berguna untuk uji praktikum)
![Foto6](../images/Screenshot%202026-04-01%20201441.png)
Kita pilih file http-ethereal-trace-5 untuk pengujian kali ini, kita membukanya dengan Wireshark
![Foto2](../images/Screenshot%202026-03-30%20164418.png)
![Foto3](../images/Screenshot%202026-03-30%20164449.png)
Setelah file dibuka maka tampilan awalnya akan seperti ini (berisi paket-paket yang telah di capture sehingga kita tidak memerlukan untuk membuka websitenya untuk mendapatkan paket yang dimaksud)
![Foto1](../images/Screenshot%202026-03-30%20164343.png)
1. Pilih satu paket UDP yang terdapat pada trace Anda. Dari paket tersebut, berapa banyak 
“field” yang terdapat pada header UDP? Sebutkan nama-nama field yang Anda temukan!
Setelah kita membuka sebuah paket (yaitu paket pertama) maka kita akan menemukan field field berikut (4)
Source Port
Destination Port
Length
Checksum 
![Foto4](../images/Screenshot%202026-03-30%20165056.png)
2. Perhatikan informasi “content field” pada paket yang Anda pilih di pertanyaan 1. Berapa 
panjang (dalam satuan byte) masing-masing “field” yang terdapat pada header UDP? 
Setiap field berukuran 2 bytes (total header UDP = 8 bytes)
![Foto4](../images/Screenshot%202026-03-30%20165056.png)
Dapat dilihat disini bahwa masing masing berisi 2 bytes
![Foto8](../images/Screenshot%202026-04-01%20205641.png)
3. Nilai yang tertera pada ”Length” menyatakan nilai apa? Verfikasi jawaban Anda melalui 
paket UDP pada trace. 
Nilai Length = panjang total UDP header + payload/data (dalam bytes).
Verifikasi : Length = 8 (header) + jumlah byte data = 58 bytes.
Sehingga jumlah data yang dapat ditampung adalah 50 byte saja (8 byte terpakai pada header)
4. Berapa jumlah maksimum byte yang dapat disertakan dalam payload UDP? (Petunjuk: 
jawaban untuk pertanyaan ini dapat ditentukan dari jawaban Anda untuk pertanyaan 2)
Maksimum 65.527 bytes.
Karena field Length adalah 16-bit dengan nilai maksimal Length = 65.535 bytes.
Payload = 65.535 – 8 bytes (header) = 65.527 bytes.
5. Berapa nomor port terbesar yang dapat menjadi port sumber? (Petunjuk: lihat petunjuk 
pada pertanyaan 4) 
65.535 (karena Source Port juga 16-bit). Sesuai dengan nilai maksimal Length 16 bit.
6. Berapa nomor protokol untuk UDP? Berikan jawaban Anda dalam notasi heksadesimal dan 
desimal. Untuk menjawab pertanyaan ini, Anda harus melihat ke bagian ”Protocol” pada 
datagram IP yang mengandung segmen UDP.
Nomor protokol UDPnya adalah 17 atau 0x11 dalam bentuk heksadesimal
![Foto12](../images/Screenshot%202026-04-01%20212536.png)
7. Periksa pasangan paket UDP di mana host Anda mengirimkan paket UDP pertama dan paket 
UDP kedua merupakan balasan dari paket UDP yang pertama. (Petunjuk: agar paket kedua 
merupakan balasan dari paket pertama, pengirim paket pertama harus menjadi tujuan dari 
paket kedua). Jelaskan hubungan antara nomor port pada kedua paket tersebut!
Dapat dilihat disini bahwa kedua paket memiliki nomor tujuan dan pengiriman yang sesuai dengan 1 sama lain
Paket pertama Source port = 4334 Dest port = 161
Paket kedua Source port = 161 Dest port = 4334
![Foto12](../images/Screenshot%202026-04-01%20212536.png)
![Foto11](../images/Screenshot%202026-04-01%20210022.png)
Ketika kedua nomor port sesuai maka kedua paket dapat berkomunikasi dengan baik karena nomor portnya sesuai satu sama lain

<!-- ![Foto5](../images/Screenshot%202026-03-30%20165332.png) -->
<!-- ![Foto7](../images/Screenshot%202026-04-01%20201441.png) -->
<!-- ![Foto8](../images/Screenshot%202026-04-01%20205641.png) -->

