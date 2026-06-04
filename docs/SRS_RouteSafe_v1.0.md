1. Stakeholder Analysis (BABOK - Modul 4)
Stakeholder
Peran
Kepentingan (Interest)
Tingkat Pengaruh (Power)
Warga (End-User)
Pengguna akhir aplikasi
Mendapatkan rute evakuasi tercepat dan aman, serta akses peta saat offline (tanpa sinyal).
Rendah / Tinggi
Admin (Petugas RT/Kelurahan)
Pengelola data sistem
Memvalidasi laporan warga dan mengubah status jalan (Normal/Banjir) secara real-time.
Tinggi / Tinggi
Dosen Penguji
Penilai akademis
Memastikan penerapan standar SE (SRS, RTM, Testing, Secure SDLC) dalam proyek.
Tinggi / Rendah
2. Functional Requirements (FR)
Definisi: Apa yang harus dilakukan sistem.
FR-01 (Peta Interaktif): Sistem harus mampu menampilkan peta interaktif berbasis OpenStreetMap (Leaflet.js) yang memuat marker "Zona Aman" dan "Lokasi Pengguna Saat Ini".
FR-02 (Kalkulasi Rute): Sistem harus mampu menghitung dan menampilkan rute evakuasi terpendek dari lokasi pengguna ke Zona Aman terdekat menggunakan Algoritma A* (A-Star).
FR-03 (Dynamic Weighting): Sistem harus secara otomatis menghitung ulang rute jika Admin mengubah status segmen jalan menjadi "Terendam/Banjir" (bobot jalan meningkat/dihindari).
FR-04 (Pelaporan Warga): Sistem harus menyediakan formulir bagi warga untuk melaporkan kondisi jalan (dengan pilihan: Normal, Genangan, Terendam).
3. Non-Functional Requirements (NFR)
Definisi: Bagaimana sistem harus bekerja (berdasarkan ISO/IEC 25010 - Modul 14).
NFR-01 (Performance Efficiency): Perhitungan ulang rute oleh algoritma A* harus selesai dalam waktu ≤ 2 detik.
NFR-02 (Reliability - Offline First): Aplikasi harus tetap mampu menampilkan peta dan rute terakhir yang berhasil dimuat (cached) saat koneksi internet terputus (menggunakan localStorage atau IndexedDB). (Solusi untuk BUG-02).
NFR-03 (Security): Sistem harus memvalidasi semua input dari formulir pelaporan warga di sisi server untuk mencegah serangan SQL Injection dan Cross-Site Scripting (XSS) (Penerapan Secure SDLC - Modul 12).
NFR-04 (Usability): Antarmuka harus menggunakan kontras warna tinggi (misal: Merah untuk bahaya, Hijau untuk aman) agar mudah dipahami dalam kondisi panik.
4. Requirements Traceability Matrix (RTM) Awal
Memastikan setiap kebutuhan bisnis dapat ditelusuri hingga ke pengujian (Modul 3).
Business Goal (BG)
Req ID
Deskripsi Kebutuhan
Modul Desain
Test Case ID
Status
BG-01: Meningkatkan keselamatan warga saat banjir
FR-02
Menghitung rute evakuasi terpendek
Modul Algoritma A*
TC-ALG-01
Planned
BG-01: Meningkatkan keselamatan warga saat banjir
NFR-02
Aplikasi tetap berfungsi saat offline
Modul Local Storage (JS)
TC-OFF-01
Planned
BG-02: Memastikan data jalan akurat & real-time
FR-03
Admin dapat mengubah status bobot jalan
Modul Dashboard Admin
TC-ADM-01
Planned
BG-03: Mencegah penyalahgunaan data
NFR-03
Validasi input form pelaporan
Modul Backend (PHP)
TC-SEC-01
