hasil :
Berikut penjelasan yang lebih rapi dan formal menggunakan pola **PREP (Point – Reason – Example – Point)**:

---

## **Point (Inti Pembahasan)**

Gambar pada papan tulis membahas tentang **mekanisme kerja sistem operasi mobile (Android)** dalam mengelola:

* proses aplikasi (foreground dan background),
* penggunaan memori,
* cache,
* serta alur request dan prioritas aplikasi.

Fokus utamanya adalah bagaimana sistem menjaga performa perangkat tetap optimal saat banyak aplikasi berjalan.

---

## **Reason (Penjelasan Detail)**

1. **Foreground dan Background Process**
   Aplikasi dibagi menjadi dua kondisi utama:

* **Foreground**: aplikasi yang sedang digunakan secara aktif oleh pengguna.
* **Background**: aplikasi yang tidak sedang digunakan tetapi masih berjalan.

Aplikasi di background biasanya berada dalam kondisi *inactive*, namun tetap disimpan agar bisa dibuka kembali dengan cepat.

---

2. **Manajemen Memori**
   Sistem operasi mengatur penggunaan RAM agar tidak terjadi overload.
   Beberapa konsep yang terlihat di papan:

* **Working Memory (WM)**: memori aktif yang sedang digunakan.
* **Cache**: penyimpanan sementara untuk aplikasi yang tidak aktif.
* **EDA (Event Driven Architecture)**: sistem bekerja berdasarkan event atau permintaan pengguna.

Jika memori penuh, sistem akan menghapus aplikasi yang memiliki prioritas rendah terlebih dahulu.

---

3. **Cache dan Prioritas Proses**
   Setiap aplikasi memiliki tingkat prioritas:

* Prioritas tinggi: aplikasi di foreground
* Prioritas rendah: aplikasi di background atau cache

Cache berfungsi untuk menyimpan data sementara sehingga aplikasi dapat dibuka kembali tanpa memulai dari awal. Namun, cache dapat dihapus jika sistem membutuhkan ruang memori.

---

4. **Struktur Data Aplikasi**
   Pada diagram terdapat contoh aplikasi seperti IG, WA, dan WB.
   Setiap aplikasi memiliki:

* **Database**: penyimpanan data utama
* **Cache**: data sementara
* **Metadata**: informasi tambahan terkait aplikasi

Hal ini menunjukkan bahwa setiap aplikasi memiliki struktur penyimpanan data yang terpisah namun dikelola oleh sistem.

---

5. **Request Queue (Antrian Proses)**
   Sistem menggunakan mekanisme antrian untuk memproses permintaan dari aplikasi.
   Setiap request diproses secara berurutan, dan waktu pemrosesan dapat berbeda tergantung:

* prioritas aplikasi,
* kondisi memori,
* status aplikasi (aktif atau tidak).

---

6. Intent dan Provider (Konsep Android)

*  Intent**: mekanisme komunikasi antar aplikasi atau antar komponen dalam aplikasi.
* **Provider**: digunakan untuk berbagi data antar aplikasi.

Ini menunjukkan bahwa aplikasi tidak berdiri sendiri, tetapi dapat saling terhubung melalui sistem operasi.

---

Example (Contoh Kasus)

Misalnya pengguna membuka beberapa aplikasi secara berurutan:

1. Membuka Instagram → menjadi foreground (prioritas tinggi).
2. Berpindah ke WhatsApp → WhatsApp menjadi foreground, Instagram menjadi background.
3. Membuka browser → sistem mengatur ulang prioritas.

Jika memori masih cukup, semua aplikasi tetap tersimpan.
Namun jika memori penuh, aplikasi dengan prioritas rendah (misalnya Instagram di cache) akan dihapus.

Saat aplikasi dibuka kembali:

* Jika masih di cache → proses lebih cepat.
* Jika sudah dihapus → aplikasi akan dimuat ulang dari awal.

---

## **Point (Kesimpulan)**

Sistem operasi mobile bekerja dengan mengatur **prioritas proses, penggunaan memori, dan antrian request** untuk memastikan kinerja perangkat tetap stabil.
Aplikasi yang aktif akan diprioritaskan, sementara aplikasi yang tidak aktif dikelola melalui cache atau dihentikan sesuai kebutuhan sistem.
