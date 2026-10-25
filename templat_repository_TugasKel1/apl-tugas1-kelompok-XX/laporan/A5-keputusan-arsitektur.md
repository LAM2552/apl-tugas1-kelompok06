Penanggung Jawab: A.Muhammad Aditya Irawan

# A5. Keputusan Arsitektur dan ADR

## ADR-01: Arsitektur Berbasis Layanan (Microservices / Modular Architecture)
* **Status:** Accepted
* **Konteks:** Subsistem Academic Management memiliki beban berfluktuasi mengikuti kalender program MSIB (misal: lonjakan lalu lintas saat pendaftaran dan akhir penilaian).
* **Keputusan:** Memisahkan modul utama (Pendaftaran, Penempatan, Logbook, Bimbingan, Penilaian) menjadi layanan independen yang berkomunikasi via RESTful API / Message Queue.
* **Konsekuensi:** 
  * (+) *Scalability* tinggi, modul Logbook dan Pendaftaran dapat diskalakan secara terpisah saat trafik meningkat.
  * (-) Kompleksitas operasional dan integrasi antar subsistem bertambah.

## ADR-02: Integrasi Layanan Autentikasi dan Data Akademik Terpusat
* **Status:** Accepted
* **Konteks:** Sistem harus berinteraksi dengan layanan induk untuk otentikasi pengguna (SSO/OAuth2) dan sinkronisasi data akademik.
* **Keputusan:** Menggunakan OAuth2 / JWT untuk integrasi autentikasi dan memanfaatkan API Gateways untuk akses data akademik terpusat.
* **Konsekuensi:** 
  * (+) Menjaga integritas hak akses untuk 4 peran berbeda (Mahasiswa, Dosen, Koordinator, Pembimbing Lapangan).
  * (-) Bergantung pada ketersediaan sistem utama UMI.

## ADR-03: Penyimpanan Objek Terpisah untuk Bukti Logbook dan Berkas Persyaratan
* **Status:** Accepted
* **Konteks:** Mahasiswa mengunggah berkas persyaratan dan bukti logbook dalam jumlah besar.
* **Keputusan:** Menggunakan Object Storage (misal: S3/Cloud Storage) terpisah dari database utama (Relational Database).
* **Konsekuensi:** 
  * (+) Ukuran database utama tetap terkontrol, performa query data teks/nilai tetap cepat.
  * (-) Perlu mekanisme enkripsi dan manajemen keamanan akses URL berkas.
<!-- Penanggung jawab: [nama] -->
<!-- Yang diminta: Minimal 2 ADR (Title, Status, Context, Decision, Consequences, Compliance). Ringkasan di sini, ADR lengkap di folder adr/. -->
<!-- Hapus komentar ini setelah bagian selesai. -->

