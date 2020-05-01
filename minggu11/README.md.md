# LAPORAN PRAKTIKUM TEKNOLOGI BASIS DATA PER-11

# LISTING latihan
![Gambar 1](gambar_1.jpg) ![Gambar 2](gambar_2.jpg) ![Gambar 3](gambar_3.jpg) ![Gambar 4](gambar_4.jpg) ![Gambar 5](gambar_5.jpg) 
![Gambar 6](gambar_6.jpg) ![Gambar 7](gambar_7.jpg) ![Gambar 8](gambar_8.jpg) ![Gambar 9](gambar_9.jpg) ![Gambar 10](gambar_10.jpg)


# PEMBAHASAN
# Installing the Library
![Gambar 1](gambar_1.jpg) ![Gambar 2](gambar_2.jpg) ![Gambar 3](gambar_3.jpg)
pip menggunakan argumen -m ke perintah Python, untuk memastikan Python mana yang menjadi target instal (sesuai tip ini dari Raymond Hettinger). Anda akan melihat beberapa output yang menunjukkan keberhasilan. Kami akan bekerja melalui beberapa fungsi pustaka Python menggunakan REPL, sehingga kami dapat memasukkan perintah dan segera melihat hasilnya. Mari kita mulai REPL sekarang, dan impor InfluxDBClient dari pustaka python-influxdb untuk memastikan itu dipasang.

# Membuat Koneksi
![Gambar 4](gambar_4.jpg)
Langkah selanjutnya adalah membuat instance baru dari InfluxDBClient (API docs), dengan informasi tentang server yang ingin kita akses. Masukkan perintah berikut di REPL Anda, ganti nilai host dan port dengan URL / alamat IP dan port host InfluxDB yang sesuai. Dalam hal ini, kami berjalan secara lokal di port default.

![Gambar 5](gambar_5.jpg)
Dengan menggunakan fungsi get_list database () dari klien.Di samping database telegraf dan _internal yang saya miliki pada instalasi saya. Akhirnya, kami akan mengatur klien untuk menggunakan basis data ini.

# Memasukkan Data
![Gambar 6](gambar_6.jpg) ![Gambar 7](gambar_7.jpg)
Database untuk menulis data, dan klien kami terkonfigurasi dengan benar, saatnya untuk memasukkan beberapa data! Kami akan menggunakan metode write_points () klien kami untuk melakukannya (API docs). Metode ini mengambil daftar poin dan beberapa parameter tambahan termasuk "ukuran bets", yang memberi kita kemampuan untuk memasukkan data dalam batch sebagai lawan dari semuanya sekaligus. Ini bisa bermanfaat jika Anda memasukkan data dalam jumlah besar. Metode write_points () memiliki argumen yang disebut poin, yang merupakan daftar kamus, dan berisi poin yang akan ditulis ke database. Mari kita buat beberapa sampel data sekarang dan masukkan. Pertama, mari kita tambahkan tiga poin dalam format JSON ke variabel yang disebut json_body.
Ini menunjukkan "acara sikat" untuk sikat gigi pintar kami; masing-masing terjadi sekitar jam 8 pagi, ditandai dengan nama pengguna orang yang menggunakan sikat gigi dan ID dari sikat itu sendiri (sehingga kita dapat melacak berapa lama setiap kepala sikat telah digunakan untuk), dan memiliki bidang yang berisi bagaimana lama pengguna menguasainya, dalam detik.
Karena kita sudah memiliki set basis data kita, dan input default untuk write_points () adalah JSON, kita dapat memanggil metode itu menggunakan variabel json_body kita sebagai satu-satunya argumen.
Anda akan melihat respons True sedang dikembalikan oleh fungsi jika operasi penulisan telah berhasil. Jika Anda membuat aplikasi, Anda ingin pengumpulan data ini menjadi otomatis, menambahkan poin ke basis data setiap kali pengguna berinteraksi.

# Meminta Data
![Gambar 8](gambar_8.jpg)
Kita coba menjalankan beberapa permintaan untuk mendapatkannya kembali. Kami akan menggunakan objek klien yang sama seperti yang kami gunakan untuk menulis data, kecuali kali ini kami akan menjalankan kueri di InfluxDB dan mendapatkan kembali hasilnya menggunakan fungsi kueri () klien kami () (dokumen API).
![Gambar 9](gambar_9.jpg)
Fungsi query () mengembalikan objek ResultSet (API Documents), yang berisi semua data hasil bersama dengan beberapa metode kenyamanan. Permintaan kami meminta semua pengukuran dalam database sampel pyex kami, dikelompokkan berdasarkan pengguna. Anda dapat menggunakan parameter .raw untuk mengakses respons JSON mentah dari InfluxDB.
![Gambar 10](gambar_10.jpg)
Jika Anda tertarik melacak jumlah waktu yang digunakan kepala sikat individual, Anda bisa mengganti kueri baru yang mengelompokkan poin berdasarkan brushId, lalu ambil durasi masing-masing poin tersebut dan tambahkan ke jumlah. Pada titik tertentu Anda dapat memberi tahu pengguna Anda bahwa sudah waktunya untuk mengganti.







