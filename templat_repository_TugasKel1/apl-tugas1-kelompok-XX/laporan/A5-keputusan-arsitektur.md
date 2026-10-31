Penanggung Jawab: A.Muhammad Aditya Irawan
# A5 - Keputusan Arsitektur (Architecture Decision Records)

## 1.Daftar Keputusan Arsitektur (ADR)

| Kode ADR | Judul Keputusan | Status | Tanggal | Pengambil Keputusan |
| :--- | :--- | :--- | :--- | :--- |
| **ADR-001** | Implementasi Load Balancing dan Caching Berbasis Cloud | Diterima | 31-10-2026 | Ahmad Andira Alam[cite: 4] |
| **ADR-002** | Perlindungan Data Pribadi Sensitif dan Kode Modular | Diterima | 31-10-2026 | Ahmad Andira Alam[cite: 4] |

## 2. Detail Keputusan Arsitektur Utama

### 2.1 ADR-001: Implementasi Load Balancing dan Caching Berbasis Cloud
* **Status:** Diterima
* **Tanggal:** 31-10-2026
* **Pengambil Keputusan:** Ahmad Andira Alam[cite: 4]
* **Konteks & Masalah (Context):**
  Sistem harus mampu menangani lonjakan akses tinggi (*high concurrency*) saat hari-hari terakhir pendaftaran beasiswa dan pengumuman hasil seleksi[cite: 4, 5]. Hal ini sejalan dengan konteks teknis sistem yang membutuhkan elastisitas serta tuntutan mahasiswa agar server tetap stabil 100% saat tenggat waktu (*deadline*).
* **Keputusan (Decision):**
  Kami akan menerapkan kapasitas server berbasis *cloud* dengan menggunakan mekanisme *load balancing* dan *caching*.
* **Dampak & Konsekuensi (Consequences):**
  * **Dampak Positif:** Situs tidak mengalami *down* atau kelambatan akses saat diserbu ribuan pendaftar secara bersamaan.
  * **Trade-off:** Biaya langganan infrastruktur *cloud* akan meningkat.
* **Kepatuhan (Compliance):**
  Melakukan pengujian beban (*load testing*) sebelum perilisan serta pemantauan otomatis (*monitoring*) pada metrik kepadatan trafik server.

### 2.2 ADR-002: Perlindungan Data Pribadi Sensitif dan Struktur Kode Modular
* **Status:** Diterima
* **Tanggal:** 31-10-2026
* **Pengambil Keputusan:** Ahmad Andira Alam[cite: 4]
* **Konteks & Masalah (Context):**
  Sistem wajib mengamankan data pribadi sensitif (seperti KTP dan slip gaji orang tua) dengan perlindungan ketat. Selain itu, alur seleksi harus menggunakan struktur kode modular agar mudah disesuaikan jika kriteria penilaian berubah di masa depan[cite: 5]. Ini merespons kebutuhan mahasiswa atas privasi data serta standar rekayasa perangkat lunak dari tim pengembang.
* **Keputusan (Decision):**
  Kami akan merancang keamanan berlapis yang meliputi enkripsi data *at rest* maupun *in transit* beserta pembatasan akses (*Role-Based Access Control* / RBAC), serta melakukan pemisahan logika bisnis penilaian dari antarmuka pengguna (*user interface*).
* **Dampak & Konsekuensi (Consequences):**
  * **Dampak Positif:** Kerahasiaan data pribadi pendaftar terjamin, manipulasi dokumen dapat dicegah, dan pemeliharaan modul sistem dapat dilakukan tanpa harus merombak seluruh arsitektur aplikasi.
  * **Trade-off:** Tingkat kerumitan pada tahap pengembangan awal akan bertambah.
* **Kepatuhan (Compliance):**
  Memberlakukan tinjauan kode (*code review*) yang ketat pada setiap modul penilaian dan menerapkan pengujian keamanan (*security testing*) secara berulang.

## 3. Pemetaan Keputusan ke Atribut Kualitas (Quality Attributes)

| Kode ADR | Atribut Kualitas Utama | Atribut Kualitas Sekunder |
| :--- | :--- | :--- |
| **ADR-001** | Ketersediaan (*Availability*) & Skalabilitas | Efisiensi Kinerja (*Performance Efficiency*) |
| **ADR-002** | Keamanan (*Security*) | Modulartas & Pemeliharaan (*Maintainability*) |
