# Catatan Minggu-04: Polymorphism

## Yang saya kerjakan
Pada minggu ini, saya mengerjakan polimorfisme pada class `Ruang.java`, `Laptop.java`, dan `AlatLab.java` dengan menggunakan method `hitungDenda()`. Setiap jenis aset memiliki perhitungan denda yang berbeda sesuai dengan pengalinya. Saya juga melengkapi method `cari()` pada kelas `KatalogAset` untuk mencari aset berdasarkan nama dan jenisnya. Setelah selesai, saya menjalankan pengujian menggunakan `bash scripts/uji.sh 4` dan semua 27 tes berhasil.

## Keputusan desain
Saya menerapkan method `hitungDenda()` secara terpisah pada class  `Ruang.java`, `Laptop.java`, dan `AlatLab.java` menggunakan `@Override`. Dengan cara ini, setiap class dapat memiliki hasil perhitungan denda sesuai dengan karakteristik jenis asetnya.

Pada class `KatalogAset`, saya menggunakan `for-each` untuk memeriksa setiap aset yang tersimpan. Saya memanfaatkan `contains()` untuk mencocokkan kata kunci dengan nama aset dan `toLowerCase` supaya pencarian tetap berjalan meskipun huruf yang digunakan berbeda antara huruf besar dan huruf kecil. Untuk pencarian berdasarkan jenis, saya membandingkan jenis aset dengan parameter `JenisAset` yang diberikan.

## Kendala
Saya sempat bingung menentukan langah awal pengerjaan dan memahami fungsi dari setiap kode yang harus di lengkapi. Saya juga mengalami kesulitan membedakan konsep overriding dan overloading serta cara menerapkannya pada class yang dikerjakan. Untuk mengatasinya, saya mempelajari contoh kode secara bertahap, memahami perbedaan kedua konsep tersebut, dan mencoba menjalankan pengujian untuk memastikan program berjalan dengan benar.

## Penggunaan AI
- **Alat yang dipakai:**  ChatGPT
- **Bagian yang dibantu AI:**  Pemahaman konsep overriding dan overloading serta penggunaan method `hitungDenda()` dan `cari()` pada keempat class tersebut.
- **Prompt utama:** 
1. Jelaskan langkah pengerjaan dan cara menguji Minggu-04 dan jelaskan apa perbedaan dari overriding dan overloading. 
2. Bagaimana cara menerapkan polimorfisme pada class `Ruang`, `Laptop`, dan `AlatLab`?
3. Bagaimana cara membuat dua method `cari()` dengan parameter berbeda pada class `KatalogAset`
- **Yang saya ubah atau tolak dari saran AI, dan alasannya:**  Saya mengikuti saran AI dalam memahami dan memperbaiki kode agar sesuai dengan ketentuan tugas yang diberikan.
- **Satu hal yang saya pahami lebih baik sekarang:**  Saya mulai memahami perbedaan overriding dan overloading. Overriding digunakan ketika class turunan membuat ulang method dari class induk, sedangkan overloading menggunakan nama method yang sama dengan parameter yang berbeda.

## Hasil Pengujian

```
keysha@keysha-dev:~/Documents/OOP/oop-202601-250202944$ mvn -B -ntp test "-Dgroups=week4"
[INFO] Scanning for projects...
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Build Order:
[INFO] 
[INFO] Aset-Pinjam (OOP 202601)                                           [pom]
[INFO] Aset-Pinjam Core (minggu 1-11)                                     [jar]
[INFO] Aset-Pinjam API (minggu 12-15)                                     [jar]
[INFO] 
[INFO] --------------------< id.ac.upb:asetpinjam-parent >---------------------
[INFO] Building Aset-Pinjam (OOP 202601) 0.1.0                            [1/3]
[INFO]   from pom.xml
[INFO] --------------------------------[ pom ]---------------------------------
[INFO] 
[INFO] ---------------------< id.ac.upb:asetpinjam-core >----------------------
[INFO] Building Aset-Pinjam Core (minggu 1-11) 0.1.0                      [2/3]
[INFO]   from core/pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ asetpinjam-core ---
[INFO] Copying 0 resource from src/main/resources to target/classes
[INFO] Copying 1 resource from src/main/resources to target/classes
[INFO] 
[INFO] --- compiler:3.14.1:compile (default-compile) @ asetpinjam-core ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ asetpinjam-core ---
[INFO] skip non existing resourceDirectory /home/keysha/Documents/OOP/oop-202601-250202944/core/src/test/resources
[INFO] 
[INFO] --- compiler:3.14.1:testCompile (default-testCompile) @ asetpinjam-core ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- surefire:3.5.6:test (default-test) @ asetpinjam-core ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] Running id.ac.upb.asetpinjam.Minggu04PolimorfismeTest
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.285 s -- in id.ac.upb.asetpinjam.Minggu04PolimorfismeTest
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] 
[INFO] ----------------------< id.ac.upb:asetpinjam-api >----------------------
[INFO] Building Aset-Pinjam API (minggu 12-15) 0.1.0                      [3/3]
[INFO]   from api/pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ asetpinjam-api ---
[INFO] Copying 1 resource from src/main/resources to target/classes
[INFO] Copying 0 resource from src/main/resources to target/classes
[INFO] 
[INFO] --- compiler:3.14.1:compile (default-compile) @ asetpinjam-api ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ asetpinjam-api ---
[INFO] skip non existing resourceDirectory /home/keysha/Documents/OOP/oop-202601-250202944/api/src/test/resources
[INFO] 
[INFO] --- compiler:3.14.1:testCompile (default-testCompile) @ asetpinjam-api ---
[INFO] Nothing to compile - all classes are up to date.
[INFO] 
[INFO] --- surefire:3.5.6:test (default-test) @ asetpinjam-api ---
[INFO] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[INFO] 
[INFO] -------------------------------------------------------
[INFO]  T E S T S
[INFO] -------------------------------------------------------
[INFO] 
[INFO] Results:
[INFO] 
[INFO] Tests run: 0, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] Reactor Summary for Aset-Pinjam (OOP 202601) 0.1.0:
[INFO] 
[INFO] Aset-Pinjam (OOP 202601) ........................... SUCCESS [  0.006 s]
[INFO] Aset-Pinjam Core (minggu 1-11) ..................... SUCCESS [  3.475 s]
[INFO] Aset-Pinjam API (minggu 12-15) ..................... SUCCESS [  1.986 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  6.185 s
[INFO] Finished at: 2026-11-07T15:28:10+07:00
[INFO] ------------------------------------------------------------------------
keysha@keysha-dev:~/Documents/OOP/oop-202601-250202944$ 

```
