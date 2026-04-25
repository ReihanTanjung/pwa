hasil
Berdasarkan catatan pada papan tulis tersebut, berikut adalah penjelasan komprehensif mengenai manajemen memori dan siklus hidup aplikasi pada Sistem Operasi Mobile menggunakan pola **PREP**.

---

## Manajemen State Aplikasi: Foreground, Background, dan Cache

### 1. Point (Titik Utama)
Dalam sistem operasi mobile (seperti Android atau iOS), aplikasi dikelola berdasarkan tingkat prioritas aktivitasnya untuk mengoptimalkan penggunaan RAM yang terbatas. Papan tulis tersebut membagi kondisi aplikasi menjadi tiga kategori utama: **Foreground**, **Background**, dan **Cache (Inactive)**.

### 2. Reason (Alasan/Logika)
Sistem operasi mobile harus memastikan bahwa aplikasi yang sedang digunakan pengguna mendapatkan sumber daya (CPU dan RAM) yang maksimal. Jika memori penuh, sistem akan menggunakan mekanisme **"Killer Priority"** untuk menghentikan proses yang dianggap tidak penting (berada di state terendah) agar sistem tidak *crash*.


### 3. Example (Contoh & Detail Teknis)
Berdasarkan visualisasi pada gambar, berikut adalah rincian setiap state:

* **Foreground (High Priority):**
    * **Karakteristik:** Aplikasi yang sedang berinteraksi langsung dengan pengguna.
    * **Aktivitas:** Mengetik pesan, menonton video, atau bermain game.
    * **Status:** Tidak akan dihentikan oleh sistem kecuali dalam kondisi sangat kritis.
* **Background (Medium Priority):**
    * **Karakteristik:** Aplikasi tidak terlihat di layar tetapi masih menjalankan tugas tertentu.
    * **Aktivitas:** Mendownload file, memutar musik di balik layar, atau sinkronisasi data.
    * **Risiko:** Jika sistem membutuhkan memori lebih, aplikasi ini berada di urutan berikutnya untuk "dibersihkan".
* **Cache / Inactive (Low Priority):**
    * **Karakteristik:** Aplikasi yang sudah dibuka tetapi tidak sedang melakukan tugas apa pun.
    * **Aktivitas:** Hanya tersimpan di RAM agar saat dibuka kembali prosesnya lebih cepat (Resume).
    * **Eksekusi:** Ini adalah target utama "Killer Priority" jika RAM menipis.

**Komponen Pendukung Lainnya:**
* **Provider:** Mengatur bagaimana data dibagikan antar aplikasi (misalnya WhatsApp mengambil kontak dari buku telepon).
* **Memory Management (WM/FBE/EDA):**
    * **FBE (File-Based Encryption):** Mengamankan data pada level file.
    * **EDA:** Terkait dengan arsitektur berbasis event (Event-Driven Architecture) dalam menangani request query.


### 4. Point (Hasil/Kesimpulan)
Hasil dari manajemen ini adalah efisiensi penggunaan baterai dan performa perangkat. Dengan membagi aplikasi ke dalam tingkatan prioritas (Foreground > Background > Cache), sistem operasi dapat memberikan pengalaman pengguna yang mulus tanpa hambatan (*lag*), sembari secara cerdas menutup aplikasi yang tidak produktif melalui mekanisme *Request Query* ke sistem memori.

---

**Ringkasan Teknis Tambahan dari Gambar:**
* Terdapat grafik persentase baterai (**BT**) yang menunjukkan konsumsi daya pada level tertentu (misal: 10% vs 9%).
* Alur **Request Query** menunjukkan bagaimana aplikasi meminta akses ke data melalui lapisan OS sebelum akhirnya dieksekusi atau diberikan izin akses memori.
