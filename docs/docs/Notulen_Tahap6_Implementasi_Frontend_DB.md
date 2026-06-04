1. Tujuan Pertemuan
Mengimplementasikan Increment 1 dari Model Proses Incremental, yaitu mengintegrasikan antarmuka pengguna (Frontend) dengan basis data (MySQL) menggunakan library pemetaan Leaflet.js.
2. Hasil Implementasi Teknis
Arsitektur Modular (MVC Sederhana): Kode dipisahkan menjadi Models (pengambil data), Views (tampilan), dan Entry Point untuk meningkatkan Maintainability (ISO/IEC 25010).
Integrasi Database Aman: Pengambilan data menggunakan PDO Prepared Statements di dalam kelas Zone.php dan Road.php, mencegah celah SQL Injection (Sesuai Modul 12: Secure SDLC).
Visualisasi Geospasial: Berhasil merender peta OpenStreetMap, marker Zona Aman, dan polilines Jalur Jalan menggunakan Leaflet.js. Data dari MySQL disuntikkan ke JavaScript secara aman menggunakan json_encode().
Color-Coded Status: Jalur jalan dirender dengan warna dinamis (Abu-abu=Normal, Kuning=Genangan, Merah=Terendam) berdasarkan data status_jalan dari database.
3. Rencana Tindak Lanjut (Next Action)
Melanjutkan ke Minggu 7: Implementasi Algoritma Inti.
Aktivitas: Menghubungkan tombol "Hitung Rute" dengan kelas AStarAlgorithm.php yang sudah dibuat sebelumnya, sehingga sistem benar-benar dapat menghitung dan menggambar rute yang menghindari jalan berwarna merah (Terendam).
Commit perubahan ke GitHub: git add . && git commit -m "feat: integrate Leaflet map with MySQL database (Increment 1)".
