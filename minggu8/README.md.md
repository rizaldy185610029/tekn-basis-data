# LAPORAN PRAKTIKUM TEKNOLOGI BASIS DATA PER-8

# LISTING latihan
![Gambar 1](gambar_1.jpg) ![Gambar 2](gambar_2.jpg) ![Gambar 3](gambar_3.jpg) ![Gambar 4](gambar_4.jpg) ![Gambar 5](gambar_5.jpg) 
![Gambar 6](gambar_6.jpg) ![Gambar 7](gambar_7.jpg) ![Gambar 8](gambar_8.jpg) ![Gambar 9](gambar_9.jpg) ![Gambar 10](gambar_10.jpg)
![Gambar 11](gambar_11.jpg) ![Gambar 12](gambar_12.jpg) ![Gambar 13](gambar_13.jpg) ![Gambar 14](gambar_14.jpg) ![Gambar 15](gambar_15.jpg)
![Gambar 16](gambar_16.jpg) ![Gambar 17](gambar_17.jpg) ![Gambar 18](gambar_18.jpg) ![Gambar 19](gambar_19.jpg) 


# PEMBAHASAN
# Lima Menit Pertama
![Gambar 1](gambar_1.jpg)
Perintah pertama membuat instance Graph bernama graph, yang dengan demikian menyediakan referensi ke data yang Anda inginkan untuk dilalui GREMLIN. Sayangnya, memiliki grafik tidak memberikan GREMLIN konteks yang cukup untuk melakukan pekerjaannya. Anda juga memerlukan sesuatu yang disebut TraversalSource, yang dihasilkan oleh perintah kedua. TraversalSource memberikan informasi tambahan kepada GREMLIN (seperti strategi traversal untuk diterapkan dan mesin traversal untuk digunakan) yang memberinya panduan tentang cara menjalankan perjalanannya di sekitar Grafik.
Ada beberapa cara untuk membuat TraversalSource. Contoh di atas menggunakan gaya tertanam dan merupakan pendekatan terbatas untuk bahasa menggunakan Java Virtual Machine (JVM). Metode lain serupa dalam bentuk, tetapi bukan fokus tutorial ini. Lihat Dokumentasi Referensi untuk informasi lebih lanjut tentang berbagai cara menghubungkan dengan GREMLIN.

![Gambar 2](gambar_2.jpg)
Dapatkan semua simpul dalam Grafik. Dapatkan simpul dengan pengidentifikasi unik "1". Dapatkan nilai properti nama pada titik dengan pengidentifikasi unik "1". Dapatkan tepi dengan label "tahu" untuk titik dengan pengidentifikasi unik "1". Dapatkan nama-nama orang yang memiliki simpul dengan pengidentifikasi unik "1" "tahu". Perhatikan bahwa ketika seseorang menggunakan outE (). InV () seperti yang ditunjukkan pada perintah sebelumnya, ini dapat disingkat menjadi just out () (mirip dengan inE (). OutV () dan in () untuk tepi yang masuk). Dapatkan nama orang-orang vertex "1" tahu siapa yang berusia di atas 30.

# Lima belas Menit Selanjutnya
![Gambar 3](gambar_3.jpg)

