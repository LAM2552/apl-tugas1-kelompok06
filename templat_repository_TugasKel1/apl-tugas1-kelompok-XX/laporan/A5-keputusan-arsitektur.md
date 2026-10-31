Penanggung Jawab: A.Muhammad Aditya Irawan
# A5. Keputusan Arsitektur (Architecture Decisions)

## 1. Latar Belakang & Konteks Keputusan
Subsistem **Assignment & Assessment** mengelola proses kritis dalam sistem beasiswa, mulai dari penerimaan berkas pendaftaran, verifikasi, hingga proses seleksi/penilaian oleh tim penilai dan pengumuman hasil. Keputusan arsitektur ini diambil untuk memastikan keandalan, integritas data, efisiensi pemrosesan berkas, dan transparansi penilaian.

---

## 2. ADR (Architecture Decision Records)

### ADR-01: Penerapan Microservices Architecture pada Subsistem Assessment
* **Status:** Accepted
* **Konteks:** Pemrosesan berkas pendaftaran dan kalkulasi skor seleksi memerlukan daya komputasi tinggi pada periode tertentu (misal mendekati batas akhir pendaftaran), sementara fitur pengumuman hanya membaca data secara masif.
* **Keputusan:** Memisah fungsi pendaftaran/berkas, seleksi/penilaian, dan pengumuman menjadi layanan independen (*Microservices*).
* **Konsekuensi:** 
  * (+) *Scalability* independen sesuai kebutuhan trafik layanan tertentu.
  * (+) Isolasi kegagalan (*fault tolerance*).
  * (-) Kompleksitas manajemen infrastruktur dan komunikasi antarlayanan meningkat.

---

### ADR-02: Penggunaan Object Storage Asinkron untuk Unggah Berkas
* **Status:** Accepted
* **Konteks:** Berkas pendaftaran beasiswa (PDF, KTP, Transkrip) berukuran besar dan diunggah secara simultan oleh jutaan calon penerima beasiswa.
* **Keputusan:** Menggunakan *Object Storage* (seperti MinIO / Amazon S3) yang dihubungkan melalui *Presigned URL* dan *Message Broker* (RabbitMQ / Kafka) untuk pemrosesan validasi latar belakang (*background job*).
* **Konsekuensi:**
  * (+) Mengurangi beban *web server* utama dan mempercepat waktu respon (*low latency*).
  * (+) Menjamin keamanan penyimpanan berkas pendaftaran.
  * (-) Memerlukan strategi konsistensi data secara asinkron (*eventual consistency*).

---

### ADR-03: Implementasi RBAC (Role-Based Access Control) untuk Penilaian Berkas
* **Status:** Accepted
* **Konteks:** Penilaian dan seleksi berkas beasiswa memerlukan kerahasiaan tinggi dan hanya boleh diakses oleh reviewer/assessor yang berhak.
* **Keputusan:** Menggunakan skema RBAC ketat berbasis *JWT-based Authentication & Authorization* untuk membatasi akses hak pilih berkas sesuai wilayah atau kriteria penilai.
* **Konsekuensi:**
  * (+) Memastikan privasi data pemohon beasiswa dan akuntabilitas nilai seleksi.
  * (-) Memerlukan sinkronisasi peran (*roles*) yang konsisten pada semua mikroservis.
