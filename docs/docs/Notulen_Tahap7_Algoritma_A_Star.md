1. Tujuan Pertemuan
Mengimplementasikan logika Algoritma A* (A-Star) pada sisi klien (JavaScript) untuk menghitung rute evakuasi, serta melakukan debugging terhadap integrasi data dari database MySQL.
2. Hasil Implementasi Teknis
Algoritma A Berfungsi:* Sistem berhasil menghitung rute terpendek dari lokasi pengguna ke Zona Aman terdekat.
Dynamic Weighting (Solusi BUG-01): Algoritma berhasil membaca bobot rute dari database. Jalur dengan status "Terendam" (bobot 9999) secara otomatis dihindari, memaksa algoritma mencari jalur alternatif yang lebih aman.
Debugging Tipe Data: Mengatasi error TypeError: lat.toFixed is not a function dengan menerapkan type casting (parseFloat()) pada data koordinat DECIMAL yang dikirim dari PHP, memastikan komputasi matematika JavaScript berjalan akurat.
3. Evaluasi Kualitas (ISO/IEC 25010)
Functional Suitability: Fitur inti (kalkulasi rute aman) berjalan sesuai requirement.
Performance Efficiency: Perhitungan rute dilakukan secara client-side dalam waktu < 1 detik (sangat efisien).
4. Rencana Tindak Lanjut (Next Action)
Melanjutkan ke Minggu 8: Implementasi Dashboard Admin.
Aktivitas: Membuat antarmuka admin untuk mengubah status jalan secara real-time langsung dari web (tanpa perlu membuka phpMyAdmin), sehingga fitur Dynamic Weighting dapat didemonstrasikan secara interaktif.
