# LAPORAN PRAKTIKUM TEKNOLOGI BASIS DATA PER-10

# LISTING latihan
![Gambar 1](gambar_1.jpg) ![Gambar 2](gambar_2.jpg) ![Gambar 3](gambar_3.jpg) ![Gambar 4](gambar_4.jpg) ![Gambar 5](gambar_5.jpg) 
![Gambar 6](gambar_6.jpg) ![Gambar 7](gambar_7.jpg) ![Gambar 8](gambar_8.jpg) ![Gambar 9](gambar_9.jpg) ![Gambar 10](gambar_10.jpg)
![Gambar 11](gambar_11.jpg) ![Gambar 12](gambar_12.jpg) ![Gambar 13](gambar_13.jpg) ![Gambar 14](gambar_14.jpg) ![Gambar 15](gambar_15.jpg)


# PEMBAHASAN
# Instalasi InfluxDB
![Gambar 1](gambar_1.jpg) ![Gambar 2](gambar_2.jpg) ![Gambar 3](gambar_3.jpg) ![Gambar 4](gambar_4.jpg) ![Gambar 5](gambar_5.jpg) 
![Gambar 6](gambar_6.jpg)
Disini cara untuk melakukan instalasi influxDB menggunakan ubuntu.

# Membuat DataBase
![Gambar 7](gambar_7.jpg)
Menjalankan influx akan memulai CLI dan secara otomatis terhubung ke instance InfluxDB lokal (dengan asumsi Anda telah memulai server dengan start layanan influxdb atau dengan menjalankan influxd secara langsung).

![Gambar 8](gambar_8.jpg)
Instalasi baru InfluxDB tidak memiliki basis data (terlepas dari sistem _internal), jadi membuatnya adalah tugas pertama kami. Anda dapat membuat database dengan pernyataan CREATE DATABASE <db-name> InfluxQL, di mana <db-name> adalah nama database yang ingin Anda buat. Nama-nama basis data dapat berisi karakter unicode apa pun selama string tersebut dikutip ganda. Nama juga dapat dibiarkan tanda kutip jika hanya berisi huruf, digit, atau garis bawah ASCII dan tidak dimulai dengan angka.

![Gambar 9](gambar_9.jpg)
Sekarang setelah database mydb dibuat, SHOW DATABASES untuk menampilkan semua database .

![Gambar 10](gambar_10.jpg)
Tidak seperti SHOW DATABASES, sebagian besar pernyataan InfluxQL harus beroperasi terhadap basis data tertentu. Anda dapat secara eksplisit memberi nama database dengan setiap permintaan, tetapi CLI memberikan pernyataan kenyamanan, USE <db-name>, yang secara otomatis akan mengatur database untuk semua permintaan yang akan dibuat.

# Menulis dan menjelajahi data
![Gambar 11](gambar_11.jpg)
Untuk memasukkan titik data seri waktu tunggal ke dalam InfluxDB menggunakan CLI, masukkan INSERT diikuti oleh titik.

![Gambar 12](gambar_12.jpg)
Suatu titik dengan nama pengukuran host dan wilayah cpu dan tag kini telah ditulis ke basis data, dengan nilai terukur 0,64.

![Gambar 13](gambar_13.jpg)
Mari kita coba menyimpan tipe data lain, dengan dua bidang dalam pengukuran yang sama.

![Gambar 14](gambar_14.jpg)
Untuk mengembalikan semua bidang dan tag dengan kueri, Anda dapat menggunakan operator *.

![Gambar 15](gambar_15.jpg)
InfluxQL memiliki banyak fitur dan kata kunci yang tidak tercakup di sini, termasuk dukungan untuk Go-style regex.
Menggunakan * tanpa klausa LIMIT pada database besar dapat menyebabkan masalah kinerja. Anda dapat menggunakan Ctrl + C untuk membatalkan permintaan yang terlalu lama untuk merespons.

# TUGAS























