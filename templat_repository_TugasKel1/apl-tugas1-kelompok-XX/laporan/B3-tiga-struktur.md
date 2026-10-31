Penanggung jawab : A.Muhammad Aditya Irawan
# B3. Tiga Struktur Arsitektur (Three Architectural Views)

## 1. Struktur Modul (Module Structure)
*Deskripsi:* Menggambarkan organisasi elemen kode, modul, dan dependen logis dari sistem.

* **Diagram:** `B3-struktur-modul.png` (sumber: `B3-struktur-modul.drawio`)
* **Elemen Modul Utama:**
  1. `Registration Module`: Mengelola alur formulir pendaftaran beasiswa.
  2. `Document Service Module`: Mengelola kompresi, penyimpanan, dan verifikasi berkas.
  3. `Assessment & Scoring Module`: Mengelola *scoring rubric*, alokasi reviewer, dan perhitungan nilai akhir seleksi.
  4. `Announcement Module`: Mempublikasikan status kelulusan peserta.
  5. `Shared Utilities Module`: Berisi fungsi validasi, audit log, dan keamanan dasar.
* **Hubungan (Relationships):** Modul `Assessment` dan `Registration` mengimpor `Shared Utilities`; `Announcement` membaca luaran dari `Assessment Module`.

## 2. Struktur Component & Connector (C&C Structure)
*Deskripsi:* Menggambarkan komponen *runtime* (proses yang berjalan) serta saluran komunikasi/konektor di antaranya.

* **Diagram:** `B3-struktur-cc.png` (sumber: `B3-struktur-cc.drawio`)
* **Komponen & Konektor Utama:**
  1. **Client / Web Gateway (Browser/Mobile):** Berinteraksi dengan pengguna via HTTP/REST API.
  2. **API Gateway:** Mengatur *routing*, *rate limiting*, dan otentikasi JWT.
  3. **Assessment Service Component:** Layanan *backend* pemrosesan penilaian dan seleksi.
  4. **Document Storage Component:** Menyimpan berkas dokumen beasiswa.
  5. **Message Broker Connector (RabbitMQ/Kafka):** Menghubungkan proses pengunggahan berkas secara asinkron ke servis verifikasi.
  6. **Database Connector (PostgreSQL):** Menyimpan data terstruktur (nilai, status pendaftaran, pengumuman).

## 3. Struktur Alokasi (Allocation Structure)
*Deskripsi:* Menggambarkan bagaimana elemen perangkat lunak dipetakan ke lingkungan fisik/infrastruktur (hardware, cloud, deployment nodes).

* **Diagram:** `B3-struktur-alokasi.png` (sumber: `B3-struktur-alokasi.drawio`)
* **Elemen Alokasi Utama:**
  1. **User Devices Node:** Browser/HP Pendaftar & Tim Reviewer Penilai.
  2. **Kubernetes Cluster (Cloud / Server Node):**
     * Pod `Registration App`
     * Pod `Assessment Engine`
     * Pod `Announcement API`
  3. **Managed Storage Node:** Dedicated Object Storage Server untuk dokumen.
  4. **Database Cluster Node:** Server Master-Replica PostgreSQL untuk keamanan data hasil seleksi.
<!-- Penanggung jawab: [nama] -->
<!-- Yang diminta: Struktur modul, struktur komponen dan konektor (C&C), dan struktur alokasi untuk subsistem yang sama (gambar dari folder diagram/). -->
<!-- Hapus komentar ini setelah bagian selesai. -->

