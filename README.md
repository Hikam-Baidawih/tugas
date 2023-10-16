# APLIKASI DETEKSI BENDA
  Dalam era teknologi yang terus berkembang, aplikasi detektor objek telah menjadi salah satu inovasi yang paling menarik. Aplikasi ini memanfaatkan kecerdasan buatan untuk mengenali dan melacak objek dalam gambar atau video. Dengan kemampuan ini, aplikasi detektor objek membawa dampak besar pada berbagai bidang, termasuk pengenalan wajah, keamanan, peningkatan efisiensi industri, dan banyak lagi. Kali ini saya akan mebahas tentang aplikasi detektor objek yang dibuat oleh salah satu pengguna akun gitHub yaitu datitran.

akun gitHub: https://github.com/datitran 

link project datitran: https://github.com/datitran/object_detector_app

link Artikel: https://towardsdatascience.com/building-a-real-time-object-recognition-app-with-tensorflow-and-opencv-b7a2b4ebdc32

## alasan membuat program
Google baru saja merilis "Tensorflow object detection API" mereka, yang mana ini merupakan fondasi utama untuk membuat aplikasa detektor benda. Perilisan API yang baru ini meliputi:

- Beberapa model pre-trained (terutama dengan fokus pada model ringan, sehingga mereka dapat berjalan di perangkat seluler
- contoh notebook Jupyter dengan salah satu model yang sudah dirilis
- Beberapa skrip yang sangat berguna yang dapat digunakan untuk pelatihan ulang model, misalnya, pada himpunan data Anda sendiri.

## Cara mendemonstrasikan Aplikasi detektor benda
Pertama, kita dapat  menarik TensorFlow dan kemudian melihat notebook yang mereka rilis juga. ini pada dasarnya dapat berjalan menggunakan model pre-trained mereka. Dalam contoh mereka, mereka menggunakan model "SSD dengan Mobilenet" tetapi Anda juga dapat mengunduh beberapa model pre-trained lainnya tentang apa yang mereka sebut "kebun binatang model deteksi Tensorflow". Model-model tersebut dilatih pada dataset COCO dan bervariasi tergantung pada kecepatan model (lambat, sedang dan cepat) dan kinerja model (mAP — presisi rata-rata rata-rata).

Apa yang harus kita lakukan selanjutnya adalah menjalankan program. program ini sebenarnya didokumentasikan dengan baik. ini urutan yang harus kita lakukan:

- Impor paket yang diperlukan seperti TensorFlow, PIL dll.
- Tentukan beberapa variabel misalnya jumlah kelas, nama model, dll.
- Unduh model beku (.pb — protobuf) dan muat ke memori
- Memuat beberapa kode pembantu, misalnya indeks ke penerjemah label
- Kode deteksi itu sendiri pada dua gambar uji
- Menghapus bagian unduhan model
- PIL tidak diperlukan karena aliran video di OpenCV sudah dalam array numpy (PIL juga merupakan overhead yang sangat besar khususnya saat menggunakannya untuk membaca dalam gambar alias aliran video)
- Tidak ada pernyataan "dengan" untuk sesi TensorFlow karena ini adalah overhead yang sangat besar terutama ketika sesi dimulai setelah setiap streaming Kemudian, saya menggunakan OpenCV untuk menghubungkannya dengan webcam saya.

## Kesimpulan
  API yang baru dirilis ini berjalan cukup rapih dan sederhana, tapi ada beberapa hal yang membuat pengguna merasa tidak puas terhadap kinerjanya salah satunya adalah FPS Ratenya yang masih rendah dan ada beberapa hambatan pada OpenCV, tetapi ada beberapa solusi alternatif seperti menggunakan WebRTC. Namun ini berbasis web, dan masih ada beberapa hal lain yang perlu diperbaiki
