hasil
Berdasarkan gambar papan tulis dari mata kuliah **Wireless dan Mobile Computing**, materi tersebut sedang membandingkan tiga arsitektur utama dalam pengembangan aplikasi mobile: **Native**, **Hybrid**, dan **PWA (Progressive Web App)**.

Berikut adalah penjelasan komprehensif menggunakan pola **PREP**:

---

## 1. Native App Development
**Point (P):**
Aplikasi Native adalah aplikasi yang dibangun khusus untuk platform spesifik (seperti Android atau iOS) menggunakan bahasa pemrograman asli platform tersebut (misalnya Kotlin/Java untuk Android, Swift untuk iOS).

**Reason (R):**
Aplikasi ini memiliki akses langsung ke API sistem operasi dan perangkat keras. Karena tidak memerlukan lapisan perantara (abstraction layer), performanya jauh lebih optimal dan mampu memanfaatkan fitur hardware secara menyeluruh.

**Example (E):**
* **Hardware Access:** Akses penuh ke NFC, Bluetooth (BT), dan Kamera dengan latensi rendah.
* **Performance:** Sangat tinggi (*High Performance*), cocok untuk aplikasi berat.
* **Usage:** Pilihan tepat untuk pengembangan Game mobile tingkat tinggi, aplikasi VR (Virtual Reality), dan AR (Augmented Reality).

**Point (P) / Result:**
Hasil akhirnya adalah aplikasi yang memberikan pengalaman pengguna (*User Experience*) paling mulus dengan responsivitas maksimal, meskipun biaya pengembangannya lebih mahal karena harus dibuat terpisah untuk tiap OS.

---

## 2. Hybrid App Development
**Point (P):**
Aplikasi Hybrid adalah kombinasi antara web app dan native app. Ia ditulis menggunakan teknologi web (HTML, CSS, JS) namun dibungkus dalam "kontainer" native agar bisa diinstal seperti aplikasi biasa.

**Reason (R):**
Hybrid menggunakan *plugin* (seperti Cordova atau Capacitor) untuk menjembatani kode web dengan fitur native perangkat. Strategi ini memungkinkan satu kode dasar (*single codebase*) berjalan di berbagai platform, yang menghemat waktu dan biaya.

**Example (E):**
* **Hardware Access:** Menggunakan *plugin* untuk mengakses fitur seperti kamera atau lokasi.
* **Performance:** Menengah (*Medium*). Lebih lambat dari Native karena ada beban dari proses *rendering* web di dalam aplikasi.
* **Usage:** Sering digunakan untuk aplikasi bisnis atau aplikasi perusahaan (*Line of Business apps*) yang tidak memerlukan grafis berat.

**Point (P) / Result:**
Hasilnya adalah efisiensi pengembangan. Anda bisa merilis aplikasi di App Store dan Play Store secara bersamaan dengan satu tim pengembang saja, meski dengan sedikit kompromi pada kecepatan transisi UI.

---

## 3. PWA (Progressive Web App)
**Point (P):**
PWA adalah situs web yang dioptimalkan agar memiliki kemampuan dan tampilan menyerupai aplikasi native, namun dijalankan langsung melalui browser tanpa perlu diinstal via App Store.

**Reason (R):**
PWA mengandalkan *Service Workers* dan *Web Manifest* untuk memungkinkan fitur seperti *offline mode* dan *push notifications*. Keunggulannya adalah aksesibilitas tinggi melalui URL dan tidak memakan ruang penyimpanan yang besar.

**Example (E):**
* **Hardware Access:** Terbatas pada API yang didukung browser (Kamera, Geolocation, Bluetooth tertentu).
* **Technology Stack:** Murni menggunakan HTML, CSS, dan JavaScript.
* **Delivery:** Diakses melalui **URL** (Web App), bukan melalui file instalasi (APK/IPA).

**Point (P) / Result:**
Hasilnya adalah kemudahan distribusi. Pengguna tidak perlu mengunduh aplikasi besar; mereka cukup membuka link dan mendapatkan pengalaman aplikasi yang ringan namun fungsional.

---

### Ringkasan Perbandingan (Berdasarkan Catatan Gambar)

| Karakteristik | Native | Hybrid | PWA |
| :--- | :--- | :--- | :--- |
| **Akses Hardware** | Maksimal (NFC, BT, Cam) | Melalui Plugin | Terbatas API Browser |
| **Performa** | Tinggi (*Height*) | Menengah (*Medium*) | Standar (*Height* di sisi Web) |
| **Distribusi** | App Store / Play Store | App Store / Play Store | URL / Browser |
| **Pilihan Tepat** | Game, VR/AR, IoT | Aplikasi Bisnis | Web App Interaktif |


Dari penjelasan di atas, pemilihan arsitektur sangat bergantung pada kebutuhan bisnis: apakah mengejar **performa** (Native), **efisiensi biaya** (Hybrid), atau **kemudahan akses** (PWA).
