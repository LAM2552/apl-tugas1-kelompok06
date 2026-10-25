Penanggung jawab : A.Muhammad Aditya Irawan
# B3. Tiga Struktur Desain

Dokumen ini menjelaskan subsistem Academic Management berdasarkan tiga sudut pandang (*view structures*):

## 1. Module View Structure (Struktur Modul)
Menjelaskan bagaimana kode dan modul perangkat lunak diorganisasikan secara logis.
* **Layered Architecture Pattern:**
  * **Presentation Layer:** Antarmuka berbasis web/mobile untuk Mahasiswa, Dosen Pembimbing, Koordinator, dan Pembimbing Lapangan.
  * **Application / Business Logic Layer:** Modul Pendaftaran, Penempatan Mitra, Logbook, Bimbingan, dan Penilaian.
  * **Data Access Layer:** Service layer yang menangani query ke database dan komunikasi API ke sistem induk UMI.

## 2. Component-and-Connector (C&C) View Structure (Struktur Komponen & Konektor)
Menjelaskan elemen-elemen sistem saat berjalan (*runtime*) dan cara mereka berinteraksi.
* **Komponen Utama:**
  * **API Gateway:** Pintu masuk tunggal yang menangani autentikasi/otorisasi request.
  * **Academic Management Core Services:** 
    * *Enrollment Service* (Pendaftaran)
    * *Placement Service* (Penempatan Mitra)
    * *Logbook Service* (Pencatatan harian & bukti)
    * *Mentorship Service* (Bimbingan & penjadwalan)
    * *Grading Service* (Penilaian & rekapsulasi SKS)
  * **External Services:** Sistem Autentikasi Induk & Database Akademik UMI.
* **Konektor:** REST API (HTTP/HTTPS) dan JSON Web Token (JWT) untuk pengiriman pesan antar-komponen.

## 3. Allocation View Structure (Struktur Alokasi)
Menjelaskan pemetaan komponen perangkat lunak ke infrastruktur fisik/lingkungan eksekusi.
* **Deployment & Hardware Allocation:**
  * **Web Application Server:** Di-deploy dalam kontainer (Docker/Kubernetes) untuk kemudahan *scaling*.
  * **Database Cluster:** Database Relasional (PostgreSQL/MySQL) di-host secara terpisah untuk keandalan data.
  * **Object Storage:** Digunakan khusus menyimpan dokumen pendaftaran dan file bukti logbook.
<!-- Penanggung jawab: [nama] -->
<!-- Yang diminta: Struktur modul, struktur komponen dan konektor (C&C), dan struktur alokasi untuk subsistem yang sama (gambar dari folder diagram/). -->
<!-- Hapus komentar ini setelah bagian selesai. -->

