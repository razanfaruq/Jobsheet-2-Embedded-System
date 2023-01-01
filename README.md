# Jobsheet-2-Embedded-System
### Protokol Komunikasi dan Sensor

#### I. Teori Dasar

#### II. Alat dan Bahan
1) ESP32
2) Breadboard
3) Kabel jumper
4) Sensor DHT 11, RFID
5) LED (5) dan Push Button (3)
6) Servo
7) Resistor 330,1K, 10K Ohm (@ 3)

#### III. Percobaan
A. ESP32 Capacitive Touch Sensor
1. Hubungkan kabel jumper Male-to-Female pada Pin D4 ESP32.
2. Buka Arduino IDE dan upload script program berikut ke ESP32.
3. Buka serial monitor untuk melihat raw data. Ubah tampilan serial monitor menjadi Serial Plotter pada menu Tools > Serial Plotter.
4. Sentuh ujung kabel jumper dan amati yang terjadi, kemudian dokumentasikan hasilnya.

https://user-images.githubusercontent.com/118172386/210176940-9379fa47-5f6d-48b4-be05-3bcb7f090ab9.mp4

5. Buatlah rangkaian seperti gambar berikut ini.

![Capture](https://user-images.githubusercontent.com/118172386/210176511-fb0ebc7f-b9d3-48d6-81f8-9485c106a67b.JPG)

6. Buatlah program agar LED menyala ketika sensor disentuh, dan LED akan mati ketika sensor tidak disentuh.

https://user-images.githubusercontent.com/118172386/210176946-69aacff1-a9b8-4e62-b929-6505c69aed3a.mp4

7. Buatlah program agar ketika sensor disentuh, LED menyala Blink.

https://user-images.githubusercontent.com/118172386/210176952-3934080d-971a-4a50-b4bb-0fe4edc5041a.mp4

8. Buatlah program agar ketika LED menyala, maka pada Serial Monitor akan menampilkan angka yang akan bertambah setiap kali sensor disentuh.

https://user-images.githubusercontent.com/118172386/210176965-2d7e3e59-5b90-4a05-a6d1-56638aaa6c6b.mp4

9. Tambahkan 2 LED sehingga pada rangkaian terdapat 3 LED. Buatlah program agar ketika sensor disentuh, LED menyala menjadi running LED. Nyala running LED tersebut adalah bergerak dari kiri ke kanan, kemudian kanan ke kiri secara kontinyu.

https://user-images.githubusercontent.com/118172386/210176971-ba4b2d5c-479d-42dc-98a8-4c9a1222cdaf.mp4

B. Mengakses Sensor DHT 11 (Single Wire / BUS)
1. Buatlah rangkaian seperti pada Gambar di bawah ini.

![Capture1](https://user-images.githubusercontent.com/118172386/210176993-aa6f9ec7-1e31-4744-9142-512187b4f331.JPG)

2. Install library sensor DHT 11 melalui Sketch > Include Library > Manage Libraries. Ketikkan DHT pada kolom pencarian, pilih library yang akan diinstall seperti pada Gambar berikut ini. Kemudian install juga Adafruit Unified Sensor menggunakan cara yang sama.

![Capture2](https://user-images.githubusercontent.com/118172386/210177155-9a2899b1-3d41-4c36-af22-96a39126e299.JPG)

![Capture3](https://user-images.githubusercontent.com/118172386/210177166-4d0cc5f0-4b79-43e8-ba95-4dca0eb3649e.JPG)

3. Buatlah program seperti pada script di bawah ini untuk mengakses sensor DHT11. Kemudian upload program tersebut pada ESP32 dan dokumentasikan hasilnya.


https://user-images.githubusercontent.com/118172386/210177103-f327b3c7-3cb0-4c24-9776-689b5335c925.mp4


4. Buatlah program agar ketika suhu rungan mencapai 30 derajat celcius, maka ESP32 akan menyalakan LED Merah dan buzzer secara beep (blink). Apabila suhu dibawah 30 derajat, ESP32 akan mematikan buzzer dan menyalakan LED berbentuk running LED seperti pada Percobaan A. Kemudian dokumentasikan hasilnya.


https://user-images.githubusercontent.com/118172386/210177110-3f43c712-037e-4da7-956d-de7e9f8f29da.mp4



C. Mengakses Sensor RFID (SPI Communication)
1. Buatlah rangkaian seperti pada gambar di bawah ini.
![Capture](https://user-images.githubusercontent.com/118172386/210177261-08eb49ed-e1b0-437e-875e-44a4d1fe0cd4.JPG)

2. Install Library MFRC522 dari Library Manager.
3. Kemudian buatlah program seperti pada script berikut ini.
4. Dekatkan kartu atau Tag RFID ke RFID Reader. Amati dan analisis cara kerja programnya.
5. Buatlah program agar Tag RFID yang terbaca sebelumya dapat digunakan untuk hak akses. Apabila Tag RFID didekatkan pada Reader, maka LED Hijau akan menyala, servo akan bergerak ke kanan (lalu kembali ke posisi semula setelah 3 detik) dan di Serial Monitor akan tertampil pesan “Akses Diterima, Silahkan Masuk”. Apabila Tag RFID tidak dikenali, maka LED Merah akan menyala, servo tidak bergerak dan di Serial Monitor akan tertampil pesan “Akses Ditolak”. Gunakan Tag RFID lain untuk mencoba.
6. Amati yang terjadi, analisis dan dokumentasikan hasilnya.


https://user-images.githubusercontent.com/118172386/210177272-1841bddc-b41c-46e8-94ad-e5b0b76a9eaa.mp4

