# Tutorial
Sebelum membahas tutorialnya, mari kita ketahui sejarah dari filter instagram ini. Program instagram filter sudah ada sejak awal 2018 dengan status program sebagai closed beta program tahap 1, dimana hanya "beberapa" orang saja yang bisa membuat filter instagram, lalu pada pertengahan 2018 sudah masuk ke tahap 2 dimana peserta closed beta program menjadi lebih banyak dengan syarat melakukan pendaftaran terlebih dahulu sebagai calon closed beta program instagram filter samapai pada bulan oktober/november 2018, pada bulan selanjutnya filter instagram sudah menjadi public dimana semua orang bisa membuat filter instagram tanpa harus melakukan pendaftaran terlebih dahulu seperti pada masa closed beta program, dengan syarat bahwa mereka memiliki akun facebook untuk diunggah ke facebook atau akun facebook dan instagram jika ingin diunggah ke instagram.

Setelah tahu sejarahnya, saatnya kita mengetahui tahapan-tahapan sederhana dari pembuatan filter instagram. Mari kita siapkan terlebih dahulu beberapa bahan yang ingin digunakan.

## Alat dan bahan
- Spark AR Studio
- Gambar kacamata ( unduh sampel )
- Gambar topi ( unduh sampel )

## Syarat & Ketentuan
- Aplikasi Spark AR Studio hanya mendukung pada sistem operasi Windows 10 64-bit atau MacOS
- Memiliki minimal RAM sebesar 4GB ( Rekomendasi 8GB )
- Jika ingin mengunggahnya ke Instagram, kamu harus mengintegrasikan Akun Instagram Kamu Ke Akun - - Facebook Personal/Fanspage (halaman)

## Tahapan Menghubungkan Akun Instagram Ke Akun Facebook Pribadi
1. Buka aplikasi Instagram
2. Tap pada menu pengaturan dan lanjut tap pada menu akun

![Tahapan Menghubungkan Akun Instagram Ke Akun Facebook Pribadi #1](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(29).png?raw=true)

3. Tap pada menu akun tertaut dan lanjut tap pada opsi facebook

![Tahapan Menghubungkan Akun Instagram Ke Akun Facebook Pribadi #2](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(30).png?raw=true)

4. Masukan email dan kata sandi akun facebook kamu dan jika sudah maka hasilnya akan seperti dibawah

![Tahapan Menghubungkan Akun Instagram Ke Akun Facebook Pribadi #3](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(31).png?raw=true)

5. Selesai

## Mengenal dan Membuat Projek di Spark AR Studio
1. Unduh dan install aplikasi Spark AR Studio
2. Buka aplikasi Spark AR Studio dan kamu akan diminta untuk melakukan login akun facebook, silahkan isi email dan password pada form yang tersedia

![Form login Spark AR Studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(1).png?raw=true)

3. Buat projek baru dengan cara klik tombol plus ( + ) seperti pada gambar dibawah

![Buat project baru di aplikasi Spark AR Studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(2).png?raw=true)

4. Kamu akan melihat halaman utama dari aplikasi Spark AR Studio, Mari kita pahami setiap bagian dari aplikasi Spark AR Studio

![Tampilan Project Baru Spark AR](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(3).png?raw=true)

> Hijau: Beberapa tombol untuk mengatur jalannya filter, mengatur preview video

> Merah: Bagian scene yang berfungsi untuk memberikan informasi apa aja objek yang ada pada filter, dan layer berfungsi untuk mengatur fungsi layer pada setiap objek

> Kuning: Proses compile projek seperti export, upload, debugging dan report aplikasi

> Biru: Bagian untuk menyimpan kumpulan assets seperti gambar, audio, spritesheets image, material, 3d, dll

> Ungu: Bagian preview filter dari segi developer

> Pink: Bagian properties dimana merupakan informasi pengaturan lanjut terkait objek yang di seleksi baik itu objek di bagian scene, layer dan assets

## Membuat Projek Sederhana
1. Buat projek baru di Spark AR Studio seperti pada informasi diatas
2. Siapkan assets assets yang dibutuhkan, jika tidak punya kamu bisa mengunduh contoh assets yang sudah disediakan
3. Klik pada tombol add assets -> import from computer dan pilih assets ( 3d, image, audio ) yang ingin kamu masukan, pada kasus ini kita masukan gambar kacamata dan topi

![Melakukan import file assets (gambar, audio, 3d, dll) ke project Spark AR Studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(4).png?raw=true)

4. Pada proses import gambar ke aplikasi, seleksi kedua texture ( gambar ) dan klik pada checkbox no compression pada bagian properties

![Mengaktifkan no compression agar gambar tidak blur saat di export menjadi filter](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(5).png?raw=true)

> untuk apa sih no compression? jika no compression tidak di centang, maka gambar kamu nanti ketika digunakan oleh orang lain maka gambar tersebut akan di kompres dan membuat gambar menjadi blur, termasuk sebaliknya, jadi? lebih baik mana? sudah jelas no compressionnya di centang

5. Texture sudah kita import, sekarang kita buat objek material karena kita tidak bisa langsung memasangkan texture kedalam sebuah objek yang nanti muncul pada filter, caranya klik pada tombol add assets -> material

![Menambahkan material baru](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(6).png?raw=true)

6. Berikan nama material sesuai keinginanmu, pada bagian properties kamu ubah shader type ke flat, lalu ubah texture menjadi topi, dan terakhir uncheck pada checkbox use depth test yang tersembunyi pada bagian advanced render options

![Memberikan pengaturan pada material](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(8).png?raw=true)

> Kenapa memilih flat? Shader type pada Spark AR Studio ada berbagai macam jenisnya, yaitu standard yang jenisnya sama seperti pemberian material pada aplikasi 3d editing yang dimana bergantung pada posisi lighting dari segi 3d, flat yang jenisnya warna datar yang sesuai seperti gambar aslinya dan tidak bergantung pada pencahayaan, physically-based biasanya digunakan pada material yang sudah diatur pada sebuah objek 3d (menggunakan material bawaan objek 3d tersebut), face paint yang hasilnya sama seperti cat warna yang hasilnya seperti cat wajah, dan masih banyak lagi

> kenapa use depth test harus di uncheck? karena udt akan membuat objek objek pada filter mengikuti hirarki 3d modeling, jika udt di ceklis maka objek yang berada dibelakang layer kamera akant tidak terlihat pada preview filternya, bukan hanya itu, bagian transparan pada png tidak akan transparan jika udt di ceklis.

7. Lakukan hal serupa pada langkah 6 untuk texture kacamata
8. Sekarang kita masuk ke bagian utama proses pembuatan filternya, klik kanan pada objek focal distance -> add -> Face Tracker

![Penambahan objek face tracker pada Spark AR Studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(10).png?raw=true)

> Kenapa harus di focal distance? Focal distance merupakan bagian utama dari urutan objek pada filter, jika kamu menyimpan objek dengan parents-nya adalah focal distance, maka objek itu akan ada di posisi utama filter dan mengikuti arah depan kamera, sedangkan jika kamu menyimpannya diluar focal distance, maka objek yang disimpan berada di luar posisi utama filter

9. Jika sudah, klik kanan pada objek face tracker yang sudah kamu tambahkan sebelumnya pada tahap 8 lalu klik add -> plane

![Penambahan objek plane pada parent face tracker](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(11).png?raw=true)

10. Klik pada objek plane tersebut dan di bagian properties kamu klik material dan pilih material yang kamu inginkan

![Memberikan material pada objek plane](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(13).png?raw=true)

11. Jika sudah, maka objek plane akan sesuai dengan material yang kamu pilih, tetapi posisinya masih tidak sesuai dengan seharusnya, untuk memperbaiki itu kamu bisa menggunakan fitur transformasi di bagian preview filter dengan mengklik tombol transformasi, scaling, rotation di bagian atas layar preview, pastikan objek plane sudah sesuai dengan posisi seharusnya

![Proses pencocokan posisi, ukuran, rotasi pada objek plane](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/transformation.gif?raw=true)

> tips tambahan: jika objek yang kamu inginkan merupakan bagian dari suatu wajah ( kacamata, topi, topeng, dll ) penulis sarankan untuk memberikan nilai posisi Z -0.005 sampai -0.015 agar posisinya tepat menempel muka

12. Silahkan kamu atur semua plane dengan material yang kamu inginkan sampai pas dengan apa yang kamu inginkan
13. Selesai ^_^

## Proses Export dan Upload
1. Jika projek SparkAR kamu sudah siap untuk diunggah ke instagram ataupun facebook, kamu simpan/save terlebih dahulu projek kamu dengan cara klik pada menu file -> save lalu beri nama projek sesuai keinginan kamu

![Menyimpan projek spark ar studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(18).png?raw=true)

2. Selanjutnya yaitu mengekspor projeknya menjadi file arexport dimana file inilah yang akan diunggah ke instagram/facebook nanti, caranya yaitu klik pada menu file -> upload and export

![mengekspor projek spark ar studio](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(20).png?raw=true)

3. Lalu kamu klik pada tombol export disudut kiri bawah tampilan, dan atur lokasi penyimpanan yang kamu inginkan

![Menyimpan file arexport ke komputer](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(19).png?raw=true)

4. Atau, kamu bisa langsung mengunggahya secara otomatis pada aplikasi SparkAR ke layanan SparkARHub, dengan cara yang sama seperti pada tahap 2, lalu dilanjut dengan mengklik tombol upload yang berada disudut kanan bawah, dan sebelumnya pastikan terlebih dahulu bahwa kamu mencentang pada checkbox publish a new effect

![Upload langsung file export ke SparkARHub](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(21).png?raw=true)

> SparkARHub adalah sebuah situs panel yang dirancang untuk mengatur semua filter yang kamu unggah baik itu ke facebook maupun ke instagram, di situs itulah kamu mengatur setiap filter yang kamu unggah, seperti mengunggah filter baru, mengubah, menghapus, dll

> Terdapat 2 pilihan checkbox jika kamu ingin mengunggahnya langsung filter dari aplikasi SparkAR ke SparkARHub, yaitu publish a new effect untuk mengunggah filter baru dan update an existing effect untuk mengganti file arexport lama dengan yang baru pada filter yang pernah diunggah sebelumnya

5. Selanjutnya adalah kamu harus mengatur beberapa informasi yang diminta pada situs SparkARHub, yaitu memberi nama, video demo, icon, kategori dan keterangan pada filter

![Memasukan informasi informasi yang dibutuhkan untuk mempublish filter](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(24).png?raw=true)

> Nama: masukan judul dari filter kamu

> File: merupakan file arexport yang kamu buat, jika kamu mengklik tombol upload, maka form file akan otomatis terisi, tetapi jika kamu mengklik tombol export, maka form file harus kamu isi secara manual

> Platform: merupakan target dimana filter akan di publish, ada facebook, instagram dan facebook ads

> Pemilik: merupakan akun/fanspage facebook tempat filter itu diunggah

> Akun Instagram: form ini akan muncul jika kamu memilih platform instagram untuk filter kamu

> Kategori: merupakan kategori tentang filter kamu, pada kasus filter ini merupakan karegori selfie dan tampilan

> Kata Kunci: untuk membantu orang orang dalam mencari filter kamu nanti pada menu pencarian filter

> Video Demo: merupakan contoh video penggunaan filter kamu, cara membuatnya akan dibahas dibagian akhir postingan ini

> Icon: merupakan icon yang akan muncul pada saat pengguna ingin memilih filter, cara membuatnya akan dibahas dibagian akhir postingan ini

> Tanggal Penerbitan: jika kamu ingin memberikan schedule publish pada filter ini, kamu pilih pada "Tanggal dan waktu yang diatur" dan pilih tanggalnya, tetapi jika kamu ingin mempublishnya secepat mungkin, kamu klik pada "Sesegera mungkin", tetapi jika kamu mengunggahnya secara terjadwal, pastikan kamu memberi jangka waktu minimal 10 hari dari target jadwal kamu, karena akan ada proses masa review selama 1–10 hari.

> Instruksi untuk peninjau: merupakan catatan cara penggunaan filter untuk nanti diberikan kepada tim reviewer dari Spark AR Studio, berikan informasi sedetail mungkin agar terhindar dari penolakan filter.

6. Jika semua sudah diisi, kamu klik tombol publish
7. Selesai, sekarang kamu hanya perlu menunggu proses konfirmasi dari tim reviewer facebook
Kamu setidaknya perlu menunggu antara 1–10 hari untuk menunggu apakah filter kamu disetujui oleh SparkAR atau tidaknya, jika filter kamu ditolak, mereka akan memberikan informasi/alasan kenapa filter kamu ditolak, sehingga informasi itu bisa menjadi acuan bagi kamu untuk memperbaiki filter kamu

![Proses pending menunggu verifikasi dari pihak Spark AR](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(28).png?raw=true)

## Tips Membuat Icon Menarik Untuk Filter
Kamu pasti akan diminta di panel Spark AR Studio Hub untuk memasukan icon filter untuk filter kamu, ada beberapa peraturan yang wajib kamu ketahui untuk membuat icon filter ini, berikut ini beberapa peraturan yang cukup penting dan sering dilanggar oleh pembuat filter pemula
- menggunakan foto artis/orang lain sebagai icon filter kamu
- menggunakan icon yang tidak berhubungan sama sekali dengan filter
- terdapat unsur kekerasan/sara/narkotika/obat obatan/minuman dewasa/dll pada icon tersebut

Demi menghindari pelanggaran tersebut, dibawah ini ada contoh sederhana untuk pembuatan icon filter, karena saya membuat filter kacamata dan topi, maka saya membuat icon seperti dibawah.

![icon sederhana untuk filter](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(25).png?raw=true)

## Cara Membuat VideoDemo
Bagaimana cara membuat video demo sedangkan kamu saja belum bisa mengugnakan filter itu? Sebenarnya bisa, kamu hanya perlu membuat sebuah url demo filter kamu, berikut ini caranya
1. Dibagian layar proses compile ( kotak kuning pada pengenalan tampilan sparkar ) kamu klik pada icon yang berbentuk hp yang disamping kirinya ada panah yang mengarah ke kanan
2. akan muncul sub menu send to app, dan kamu klik pada tombol send pada bagian instagram ( bisa juga ke facebook, tapi lebih mudah di instagram )

![Membuat video demo dengan mendapatkan url preview filternya](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(26).png?raw=true)

3. kamu tunggu proses pembuatan url demonya, jika sudah selesai kamu akan mendapatkan url demo filter kamu, dan kamu juga akan mendapatkan notifikasi filter preview ke akun instagram yang terhubung dengan akun facebook kamu, kamu bisa mengaksesnya dari kedua cara tersebut

![Mendapatkan url preview filternya](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(27).png?raw=true)

![Mendapatkan notifikasi di aplikasi instagram](https://github.com/zFz0000/TopiDanKacamataSparkAR/blob/main/tutorial-image/tutorial-image%20(32).png?raw=true)

4. Setelah kamu mengaksesnya, kamu akan mendapatkan tampilan langsung dari filter kamu, buatlah video kamu menggunakan filter tersebut minimal 5 detik dan kamu save video tersebut
5. Video yang sudah kamu save, bisa kamu unggah ke situs sparkarhub sebagai syarat untuk mengunggah filter baru secara publik

> Jika video demo ditolak oleh pihak SparkAR, kamu bisa mengakalinya dengan cara melakukan konversi video tersebut ke format mp4, meskipun video kamu sudah berekstensi mp4, kamu tetap harus mengkonversinya dengan menggunakan layanan layanan konversi yang tersedia di internet, atau bisa menggunakan aplikasi pihak ketiga.

## Unduh Projek Yang Sudah Jadi
[Unduh Disini](https://github.com/zFz0000/TopiDanKacamataSparkAR/archive/main.zip)
