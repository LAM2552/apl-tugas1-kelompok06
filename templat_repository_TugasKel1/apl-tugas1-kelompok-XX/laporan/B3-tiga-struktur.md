Penanggung jawab : A.Muhammad Aditya Irawan

# B3. Tiga Struktur Arsitektur

## 1. Struktur Modul (Module Structure)
Struktur modul menggambarkan bagaimana sistem didekomposisi menjadi unit-unit unit kode atau modul fungsional yang lebih kecil berdasarkan domain layanannya.

* **Modul Pendaftaran & Seleksi**: Bertanggung jawab atas proses pendaftaran mahasiswa, pengisian berkas persyaratan, dan seleksi awal.
* **Modul Penempatan Mitra**: Mengelola data mitra industri, kuota posisi magang, serta proses *matching* atau penempatan mahasiswa ke mitra.
* **Modul Aktivitas & Logbook**: Menangani pencatatan harian/mingguan kegiatan mahasiswa (*logbook*) serta catatan bimbingan dengan dosen/mentor industri.
* **Modul Penilaian & Konversi**: Mengelola komponen penilaian dari mentor industri dan dosen pembimbing, serta rekapitulasi nilai akhir magang.

## 2. Struktur Komponen dan Konektor (Component-and-Connector Structure)
Struktur ini menunjukkan aspek runtime sistem, yaitu bagaimana komponen-komponen perangkat lunak berinteraksi satu sama lain saat aplikasi sedang berjalan.

* **Frontend Client (UI Layer)**: Antarmuka berbasis web/mobile yang diakses oleh mahasiswa, dosen, dan mitra. Berkomunikasi menggunakan protokol HTTP/REST.
* **API Gateway / Router**: Titik masuk tunggal (*single entry point*) yang menerima seluruh permintaan dari client, melakukan verifikasi token JWT, dan merutekan ke layanan yang sesuai.
* **Core Service Layer (Backend)**: Kumpulan layanan bisnis (Service MSIB) yang memproses logika pendaftaran, manajemen logbook, hingga kalkulasi penilaian.
* **Database & Storage Server**: Komponen penyimpanan data terstruktur (PostgreSQL) untuk transaksi utama dan *Object Storage* untuk dokumen laporan serta lampiran logbook.

## 3. Struktur Alokasi (Allocation Structure)
Struktur alokasi memetakan elemen-elemen software ke lingkungan eksternal (perangkat keras, tim pengembang, atau infrastruktur jaringan).

* **Alokasi Perangkat Keras (Deployment Environment)**: 
  * Aplikasi Backend dideploy ke dalam *Cloud Container* (menggunakan Docker/Kubernetes) untuk memastikan ketersediaan layanan yang tinggi (*high availability*).
  * Basis data berjalan pada server *managed database* terpisah yang memiliki sistem *backup* berkala.
* **Alokasi Tim Pengembang (Team Allocation)**: 
  * Tim dibagi berdasarkan modul fungsional (misal: Sub-tim pengembang modul pendaftaran & penempatan, Sub-tim pengembang logbook & penilaian, serta Tim infrastruktur/DevOps).
<!-- Penanggung jawab: [nama] -->
<!-- Yang diminta: Struktur modul, struktur komponen dan konektor (C&C), dan struktur alokasi untuk subsistem yang sama (gambar dari folder diagram/). -->
<!-- Hapus komentar ini setelah bagian selesai. -->

