# B2. Atribut Kualitas yang Terukur


**Penanggung jawab:** Ahmad Andira Alam[cite: 1]

Berikut adalah 3 karakteristik pendorong (*Quality Attributes*) untuk subsistem **Academic Management** (Layanan magang dan studi independen/MSIB)[cite: 1]:

### 1. Kinerja (*Performance*)
* **Angka Target:** Waktu respons sistem (*response time*) maksimal 2 detik untuk memuat halaman pendaftaran dan pengisian logbook harian[cite: 1].
* **Kondisi Pengukuran:** Sistem sedang diakses dalam kondisi beban puncak (*peak load*), misalnya saat tenggat waktu pendaftaran program atau penutupan penilaian[cite: 1] dengan ribuan mahasiswa mengakses secara bersamaan (*concurrent users*).
* **Cara Mengukur:** Menggunakan perangkat lunak *Load Testing* (seperti Apache JMeter atau k6) untuk menyimulasikan lonjakan *traffic* (ribuan *request* per detik) dan mencatat rata-rata waktu respons server.

### 2. Ketersediaan (*Availability*)
* **Angka Target:** Sistem memiliki persentase ketersediaan (*uptime*) minimal 99,9% (toleransi *downtime* maksimal sekitar 43 menit per bulan).
* **Kondisi Pengukuran:** Sistem beroperasi normal pada *production environment* selama periode aktif MSIB (terutama saat masa pengisian logbook harian dan bimbingan)[cite: 1].
* **Cara Mengukur:** Menggunakan *Automated Monitoring Tools* (seperti UptimeRobot, AWS CloudWatch, atau Prometheus) yang mengirimkan *ping* atau permintaan *health-check* ke server setiap 1 menit secara terus-menerus.

### 3. Keamanan (*Security*)
* **Angka Target:** 100% data logbook dan penilaian[cite: 1] terlindungi dari akses pihak yang tidak berwenang (0 insiden kebocoran privasi atau perubahan nilai tanpa izin).
* **Kondisi Pengukuran:** Ada percobaan akses (*request*) ke *endpoint* pengubahan nilai atau pembacaan logbook dari akun/peran (*role*) yang tidak memiliki hak (misalnya mahasiswa lain mencoba melihat nilai temannya).
* **Cara Mengukur:** Menjalankan *Penetration Testing* secara berkala dan menggunakan *Automated Vulnerability Scanner* (seperti OWASP ZAP) untuk menguji sistem otorisasi dan memastikan tidak ada celah *Broken Access Control*.

