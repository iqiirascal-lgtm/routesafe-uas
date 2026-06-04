1. Tujuan Pertemuan
Mengintegrasikan prinsip keamanan ke dalam siklus hidup pengembangan perangkat lunak (Secure SDLC) dan melakukan analisis ancaman (Threat Modeling) pada fitur kritis aplikasi RouteSafe sesuai standar Modul 12.
2. Penerapan Shift Left Security
Keamanan telah dirancang sejak fase awal (Shift Left), mencakup:
Privacy by Design: Data lokasi GPS pengguna diproses secara lokal (client-side) dan tidak disimpan di server tanpa persetujuan eksplisit.
Secure Coding Standard: Rencana penggunaan Prepared Statements untuk mencegah SQL Injection dan password_hash() untuk manajemen kredensial.
3. Hasil Threat Modeling (Metode STRIDE)
Analisis ancaman telah dilakukan pada fitur "Pelaporan Warga & Dashboard Admin". Enam kategori ancaman (STRIDE) telah diidentifikasi dan dipasangkan dengan mitigasi spesifik:
Spoofing & Elevation of Privilege: Dimitigasi melalui implementasi Role-Based Access Control (RBAC) dan manajemen sesi yang aman.
Tampering & Information Disclosure: Dimitigasi melalui validasi input ketat (server-side) dan enkripsi transmisi data.
Repudiation: Dimitigasi dengan pencatatan audit log (user_id, timestamp) pada setiap transaksi data.
Denial of Service (DoS): Dimitigasi dengan rencana penerapan Rate Limiting pada endpoint publik.
4. Keselarasan dengan OWASP Top 10
Mitigasi yang dirancang telah dipetakan untuk mengatasi kerentanan umum seperti Broken Access Control (A01), Injection (A03), dan Authentication Failures (A07).
5. Rencana Tindak Lanjut (Next Action)
Melanjutkan ke Minggu 5: Perancangan Antarmuka (UI/UX) & Arsitektur Algoritma.
Aktivitas: Membuat Wireframe antarmuka menggunakan Bootstrap 5 dan mendetailkan pseudo-code atau alur logika Algoritma A* dengan dynamic weighting.
Membuat branch baru di GitHub: git checkout -b feature/ui-wireframe.
