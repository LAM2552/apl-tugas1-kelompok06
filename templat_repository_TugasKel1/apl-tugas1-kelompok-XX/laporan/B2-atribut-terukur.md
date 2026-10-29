# B2. Atribut Kualitas yang Terukur

**Penanggung jawab:** Ahmad Andira Alam

Berikut adalah 3 karakteristik pendorong (*Quality Attributes*) untuk subsistem **Layanan Beasiswa Universitas Muslim Indonesia (UMI) Makassar**. Layanan beasiswa UMI merupakan salah satu layanan yang tersedia bagi mahasiswa dan mencakup proses pendaftaran serta pengelolaan beasiswa.

### 1. Kinerja (*Performance*)

* **Angka Target:** Waktu respons sistem maksimal **2 detik** saat mahasiswa melakukan pendaftaran, mengunggah berkas, dan melihat informasi beasiswa.
* **Kondisi Pengukuran:** Sistem diuji ketika banyak mahasiswa mengakses layanan beasiswa secara bersamaan, terutama pada masa pendaftaran.
* **Cara Mengukur:** Menggunakan *Load Testing* seperti Apache JMeter atau k6 untuk mengetahui waktu respons sistem ketika menerima banyak pengguna.

### 2. Ketersediaan (*Availability*)

* **Angka Target:** Sistem memiliki tingkat ketersediaan minimal **99,9%** selama periode layanan beasiswa.
* **Kondisi Pengukuran:** Sistem dipantau selama proses pendaftaran, pengumpulan berkas, seleksi, sampai pengumuman hasil beasiswa.
* **Cara Mengukur:** Menggunakan sistem monitoring untuk mengecek apakah halaman dan layanan beasiswa dapat diakses secara berkala serta mencatat apabila terjadi *downtime*.

### 3. Keamanan (*Security*)

* **Angka Target:** **100% data pendaftar dan berkas beasiswa** hanya dapat diakses oleh pihak yang memiliki hak akses.
* **Kondisi Pengukuran:** Dilakukan pengujian dengan mencoba mengakses data atau berkas mahasiswa menggunakan akun yang tidak memiliki izin.
* **Cara Mengukur:** Melakukan *security testing* menggunakan alat seperti OWASP ZAP untuk menguji login, hak akses, pengunggahan berkas, dan perlindungan data mahasiswa.

**Catatan:** Angka target seperti 2 detik dan 99,9% merupakan **target kualitas yang digunakan dalam analisis tugas**, bukan standar resmi yang ditetapkan oleh UMI.
