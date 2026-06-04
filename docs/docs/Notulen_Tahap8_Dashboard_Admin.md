1. Tujuan Pertemuan
Mengimplementasikan antarmuka administrator untuk mengelola data master jalan, serta menghubungkan UI dengan logika Dynamic Weighting pada Algoritma A* secara real-time.
2. Hasil Implementasi Teknis
Arsitektur MVC Sederhana: Memisahkan logika bisnis (AdminController), manipulasi data (Road Model), dan antarmuka (dashboard.php) untuk meningkatkan Maintainability (ISO/IEC 25010).
Secure Coding (Modul 12):
Menerapkan Prepared Statements pada query UPDATE untuk mencegah SQL Injection.
Melakukan validasi input ketat (in_array) pada parameter status untuk mencegah Mass Assignment atau manipulasi data ilegal.
Menggunakan htmlspecialchars() untuk mencegah serangan Cross-Site Scripting (XSS) pada output nama jalan.
Post/Redirect/Get (PRG) Pattern: Menerapkan redirect setelah form submission untuk mencegah duplicate data jika user me-refresh halaman.
3. Rencana Tindak Lanjut (Next Action)
Melanjutkan ke Minggu 9-10: Pengujian Sistem (Software Quality Engineering & Testing).
Aktivitas: Menyusun Test Plan, membuat Test Case (Positive, Negative, Edge Case) berdasarkan SRS, dan melakukan Black Box Testing untuk memastikan seluruh fitur berjalan sesuai requirement.
