Penanggung jawab : A.Muhammad Aditya Irawan
# B3. Tiga Struktur Arsitektur (Three Architectural Views)


## 1. Struktur Modul (Module Structure)

**Deskripsi:** Menggambarkan organisasi elemen kode, modul, dan dependensi logis dari sistem.
* **Elemen Modul Utama:**
  1. Registration Module: Mengelola alur formulir pendaftaran beasiswa dan validasi data diri pemohon.
  2. Document Service Module: Mengelola kompresi, penyimpanan, dan verifikasi berkas persyaratan.
  3. Assessment & Scoring Module: Mengelola *scoring rubric*, alokasi *reviewer*, dan perhitungan nilai akhir seleksi.
  4. Announcement Module: Mempublikasikan status kelulusan peserta.
  5. Shared Utilities Module: Berisi fungsi validasi, *audit log*, dan keamanan dasar.
* **Hubungan (Relationships):** Modul `Assessment` dan `Registration` mengimpor `Shared Utilities`; modul `Announcement` membaca luaran dari `Assessment Module`.


## 2. Struktur Component & Connector (C&C Structure)

**Deskripsi:** Menggambarkan komponen *runtime* (proses yang berjalan) serta saluran komunikasi/konektor di antaranya.
* **Komponen & Konektor Utama:**
  1. **Client Devices (Browser / Mobile):** Berinteraksi dengan pengguna melalui protokol HTTP/REST API.
  2. **API Gateway:** Mengatur *routing*, *rate limiting*, dan otentikasi token JWT.
  3. **Microservices (Registration, Document, & Assessment Svc):** Layanan *backend* pemrosesan inti.
  4. **Message Broker (RabbitMQ/Kafka):** Konektor asinkron untuk mengelola antrean unggah berkas.
  5. **Data Stores (PostgreSQL & Object Storage):** Tempat penyimpanan data terstruktur dan berkas dokumen.


## 3. Struktur Alokasi (Allocation Structure)

**Deskripsi:** Menggambarkan bagaimana elemen perangkat lunak dipetakan ke lingkungan infrastruktur fisik atau *cloud*.
* **Elemen Alokasi Utama:**
  1. **User Environment Layer:** Perangkat pendaftar (mahasiswa) dan tim penilai (reviewer).
  2. **Kubernetes Cluster (Cloud Server Node):** Tempat *pod* aplikasi mikroservis dideploy.
  3. **Storage & Database Node:** Server terpisah untuk *Managed Database* (PostgreSQL) dan *Object Storage* berkas.
<!-- Yang diminta: Struktur modul, struktur komponen dan konektor (C&C), dan struktur alokasi untuk subsistem yang sama (gambar dari folder diagram/). -->
<!-- Hapus komentar ini setelah bagian selesai. -->

