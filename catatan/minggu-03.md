# Catatan Minggu-03: Inheritance

## Yang saya kerjakan
Saya melengkapi class, yaitu `Ruang.java`, `Laptop.java`, dan `AlatLab.java`. Saya mengubah bagian yang ditugaskan, seperti menambahkan field, konstruktor, getter, serta menyesuaikan validasi dan method `getJenis()` pada masing-masing kelas.

## Keputusan desain
Saya menempatkan atribut umum di class induk `Aset`, sedangkan atribut khusus ditempatkan di masing-masing class turunan. Saya menggunakan super (kode, nama) untuk memanggil konstruktor induk dan `getJenis()` untuk membedakan jenis aset. Inheritance kurang tepat jika objek tidak memiliki hubungan pewarisan, seperti infomasi lokasi penyimpanan yang sesuai menggunakan komposisi.

## Kendala
Saya mengalami error saat pengujian Maven karena tipe data `getJenis()` tidak sesuai dan terdapat kesalahan penulisan variabel `tingkatRisiko`. Saya memperbaikinya dengan menyesuaikan tipe data dan nama variabel.

## Penggunaan AI
- **Alat yang dipakai:** ChatGPT

- **Bagian yang dibantu AI:** Membantu melengkapi dan memeriksa kode pada class `Ruang.java`, `Laptop.java`, dan `AlatLab.java`, serta menemukan bagian kode yang mengalami error.

- **Yang saya ubah atau tolak dari saran AI, dan alasannya:** Saya memperbaiki kode sesuai intruksi yang diberikan dan memastikan setiap jenis aset memiliki validasi yang benar.

- **Satu hal yang saya pahami lebih baik sekarang:** Saya memahami bahwa inheritance memungkinkan class turunan menggunakan atribut dan method dari class induk, serta mengikuti aturan yang sudah ditentukan oleh class induk. 

## Hasil Pengujian

```
keysha@keysha-dev:~/Documents/OOP/oop-202601-250202944$ mvn -B -ntp test "-Dgroups=week3"
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
[INFO] Running id.ac.upb.asetpinjam.Minggu03HierarkiTest
[INFO] Tests run: 8, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.456 s -- in id.ac.upb.asetpinjam.Minggu03HierarkiTest
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
[INFO] Aset-Pinjam (OOP 202601) ........................... SUCCESS [  0.005 s]
[INFO] Aset-Pinjam Core (minggu 1-11) ..................... SUCCESS [  3.419 s]
[INFO] Aset-Pinjam API (minggu 12-15) ..................... SUCCESS [  2.057 s]
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  6.173 s
[INFO] Finished at: 2026-11-07T07:14:47+07:00
[INFO] ------------------------------------------------------------------------
keysha@keysha-dev:~/Documents/OOP/oop-202601-250202944$ 
```
