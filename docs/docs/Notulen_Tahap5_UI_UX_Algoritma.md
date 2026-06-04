1. Tujuan Pertemuan
Menerjemahkan Software Requirements Specification (SRS) ke dalam desain antarmuka (UI/UX) yang intuitif, serta merinci arsitektur logika Algoritma A* untuk memastikan solusi teknis terhadap bug yang telah diidentifikasi sebelumnya.
2. Hasil Perancangan UI/UX (Usability - ISO/IEC 25010)
Desain antarmuka difokuskan pada kemudahan penggunaan dalam kondisi darurat:
Tampilan Warga: Menggunakan high-contrast markers (Hijau untuk aman, Merah untuk bahaya) pada peta Leaflet.js, dilengkapi tombol aksi tunggal yang jelas ("Hitung Rute").
Tampilan Admin: Dashboard berbasis tabel dengan dropdown status jalan untuk memudahkan pembaruan data real-time.
Mitigasi BUG-02: Desain menyertakan indikator visual "Mode Offline" untuk memberi tahu pengguna bahwa peta yang ditampilkan adalah cached version.
3. Arsitektur Algoritma Inti (Dynamic Weighting)
Logika Algoritma A* (A-Star) telah dimodifikasi untuk mendukung Dynamic Weighting sebagai solusi permanen untuk BUG-01:
Biaya perjalanan (
𝑔
(
𝑛
)
g(n)) tidak lagi dihitung berdasarkan jarak fisik murni, melainkan mengambil nilai dari kolom bobot_rute pada tabel jalur_jalan di database MySQL.
Ketika Admin mengubah status_jalan menjadi 'Terendam', sistem secara otomatis menetapkan bobot_rute = 9999.
Algoritma A* akan secara matematis menghindari edge dengan bobot 9999, sehingga menghasilkan rute alternatif yang lebih panjang secara jarak, namun lebih aman secara kondisi.
4. Rencana Tindak Lanjut (Next Action)
Melanjutkan ke Minggu 6-7: Implementasi Incremental (Coding Tahap 1).
Aktivitas: Setup lingkungan XAMPP, membuat file PHP/HTML dasar, mengintegrasikan Leaflet.js, dan mengimplementasikan logika A* sederhana dengan data dummy.
Membuat branch baru di GitHub: git checkout -b feature/implementation-increment-1.
