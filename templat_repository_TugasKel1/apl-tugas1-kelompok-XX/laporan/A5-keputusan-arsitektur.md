Penanggung Jawab: A.Muhammad Aditya Irawan

# A5. Keputusan Arsitektur

## 1. Pemilihan Gaya Arsitektur: Microservices vs Monolith Modular
* **Keputusan**: Menggunakan pendekatan **Modular Monolith** pada tahap awal, dengan rancangan yang siap dipecah menjadi **Microservices** di masa depan.
* **Alasan (Rationale)**: 
  * Layanan MSIB memiliki modul yang erat kaitannya (pendaftaran, penempatan, logbook, penilaian). Monolith modular memudahkan pengelolaan transaksi data (seperti validasi kuota penempatan mitra dengan pendaftaran mahasiswa) tanpa kompleksitas komunikasi jaringan yang tinggi di awal.
  * Memungkinkan tim untuk memisahkan domain logika kode dengan jelas per modul.

## 2. Strategi Pengelolaan Basis Data (Database Strategy)
* **Keputusan**: Menggunakan basis data relasional (**PostgreSQL**).
* **Alasan (Rationale)**: 
  * Data akademik dan operasional MSIB (seperti relasi mahasiswa, dosen pembimbing, mitra industri, logbook, dan nilai) menuntut integritas data yang tinggi (*ACID compliance*).
  * Relasi antar entitas (misalnya: satu mahasiswa memiliki banyak logbook dan satu dosen penilai) sangat optimal dikelola menggunakan *Relational Database Management System* (RDBMS).

## 3. Mekanisme Autentikasi dan Otorisasi
* **Keputusan**: Menggunakan **JSON Web Token (JWT)** dengan kontrol berbasis peran (*Role-Based Access Control - RBAC*).
* **Alasan (Rationale)**: 
  * Sistem MSIB melibatkan berbagai aktor dengan hak akses berbeda secara jelas, yaitu: Mahasiswa, Dosen Pembimbing, Mitra Industri, dan Admin Pusat.
  * JWT bersifat *stateless*, sehingga memudahkan skalabilitas server saat terjadi lonjakan akses (misalnya saat periode pendaftaran serentak).

## 4. Pengelolaan Berkas Pendukung (Logbook & Dokumen Penilaian)
* **Keputusan**: Menggunakan penyimpanan berbasis *Object Storage* (seperti AWS S3 atau MinIO) yang terpisah dari basis data utama.
* **Alasan (Rationale)**: 
  * Dokumen lampiran seperti laporan magang, sertifikat, dan bukti logbook berukuran besar. Menyimpannya langsung di database akan menurunkan performa kueri. Penyimpanan objek memberikan akses unduh/unggah yang lebih cepat dan aman.
<!-- Penanggung jawab: [nama] -->
<!-- Yang diminta: Minimal 2 ADR (Title, Status, Context, Decision, Consequences, Compliance). Ringkasan di sini, ADR lengkap di folder adr/. -->
<!-- Hapus komentar ini setelah bagian selesai. -->

