# Catatan Minggu-05: Abstraction

## Yang saya kerjakan
Pada minggu 5, saya mengubah kelas Aset menjadi abstract class dan mengimplementasikan method `bisaDipinjam()`. Saya juga mengimplementasikan interface AturanDenda pada kelas `DendaFlat` dan `DendaProgresif`. Denda flat menggunakan perhitungan dari `aset.hitungDenda()`, sedangkan denda progresif memberikan tambahan denda berdasarkan jumlah hari keterlambatan.

## Keputusan desain
Saya menggunakan abstract class pada Aset karena kelas tersebut menjadi dasar bagi beberapa jenis aset, seperti Ruang, Alatlab dan Laptop. Saya menggunakan interface AturanDenda agar aturan perhitungan denda dapat memiliki implementasi yang berbeda. Untuk denda progresif, saya menggunakan rumus denda flat ditambah jumlah hari keterlambatan kuadrat dikalikan 1.000.

## Kendala
Kendala yang saya temui adalah memahami perbedaan abstract class dan interface serta cara menerapkannya pada kode. Selain itu, saya mengalami kesulitan dalam menentukan rumus denda progresif agar sesuai dengan aturan yang telah ditentukan. Saya mengatasi hal tersebut dengan mempelajari kembali struktur kelas dan interface yang sudah tesedia, serta mencoba menentukan rumus yang membuat denda besar seiring bertambahnya hari keterlambatan.

## Penggunaan AI
- **Alat yang dipakai:**  ChatGPT
- **Bagian yang dibantu AI:**  Kelas Aset, DendaFlat, dan DendaProgresif.
- **Prompt utama:**  
1. Bagaimana cara mengubah class Aset menjadi abstract class?
2. Bagaimana cara mengimplementasikan interface AturanDenda pada `DendaFlat` dan `DendaProgresif`?
3. Bagaimana cara menerapkan dan membedakan abstract class dan interface pada program java, khususnya pada kelas Aset, DendaFlat dan DendaProgresif?

- **Yang saya ubah atau tolak dari saran AI, dan alasannya:**  Saya menyesuaikan kode yang diberikan dengan struktur program dan ketentuan tuas yang sudah tersedia.
- **Satu hal yang saya pahami lebih baik sekarang:** Saya memahami perbedaan abstract class dan interface. Abstract class digunakan sebagai kelas turunan, sedangkan interface digunakan untuk menetapkan perilaku yang harus diimplementasikan oleh kelas.
