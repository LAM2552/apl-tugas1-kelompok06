Penanggung jawab : A.Muhammad Aditya Irawan
# B3. Tiga Struktur Arsitektur (Three Architectural Views)

## 1. Struktur Modul (Module Structure)

Deskripsi: Menggambarkan organisasi elemen kode, modul, dan dependensi logis dari sistem.

* **Diagram:** B3-struktur-modul.png (sumber: B3-struktur-modul.drawio)
* **Elemen Modul Utama:**
  i. `Registration Module`: Mengelola alur formulir pendaftaran beasiswa dan validasi data diri pemohon.
  ii. `Document Service Module`: Mengelola kompresi, penyimpanan, dan verifikasi berkas persyaratan.
  iii. `Assessment & Scoring Module`: Mengelola scoring rubric, alokasi reviewer, dan perhitungan nilai akhir seleksi.
  iv. `Announcement Module`: Mempublikasikan status kelulusan peserta.
  v. `Shared Utilities Module`: Berisi fungsi validasi, audit log, dan keamanan dasar.
* **Hubungan (Relationships):** Modul `Assessment` dan `Registration` mengimpor `Shared Utilities` ; modul `Announcement` membaca luaran dari `Assessment Module` .

## 2. Struktur Component & Connector (C&C Structure)

Deskripsi: Menggambarkan komponen runtime (proses yang berjalan) serta saluran komunikasi/konektor di antaranya.

* **Diagram:** B3-struktur-cc.png (sumber: B3-struktur-cc.drawio)
* **Komponen & Konektor Utama:**
  i. `Client Devices`: Berinteraksi dengan pengguna melalui protokol HTTP/REST API.
  ii. `API Gateway`: Mengatur routing, rate limiting, dan otentikasi token JWT.
  iii. `Microservices`: Layanan backend pemrosesan inti (Registration, Document, & Assessment Svc).
  iv. `Message Broker`: Konektor asinkron (RabbitMQ/Kafka) untuk antrean berkas.
  v. `Data Stores`: PostgreSQL Database dan Object Storage.

## 3. Struktur Alokasi (Allocation Structure)

Deskripsi: Menggambarkan bagaimana elemen perangkat lunak dipetakan ke lingkungan infrastruktur fisik atau cloud.

* **Diagram:** B3-struktur-alokasi.png (sumber: B3-struktur-alokasi.drawio)
* **Elemen Alokasi Utama:**
  i. `User Environment Layer`: Perangkat pendaftar (mahasiswa) dan tim penilai (reviewer).
  ii. `Kubernetes Cluster`: Cloud Server Node tempat pod aplikasi mikroservis dideploy.
  iii. `Storage Infrastructure`: Dedicated Object Storage Server untuk berkas.
  iv. `Database Infrastructure`: PostgreSQL Master-Replica Server Node.
<!-- Yang diminta: Struktur modul, struktur komponen dan konektor (C&C), dan struktur alokasi untuk subsistem yang sama (gambar dari folder diagram/). -->
<!-- Hapus komentar ini setelah bagian selesai. -->

