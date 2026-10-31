Penanggung jawab : A.Muhammad Aditya Irawan
# B3 - Tiga Struktur Arsitektur (Three-View Architecture)

## 1. Struktur Modul (Module Structure)
Struktur modul menggambarkan bagaimana sistem didekomposisi menjadi unit-unit kode atau modul fungsional yang lebih kecil serta relasi ketergantungannya (*dependency*).

* **Penjelasan Modul Utama:**
  * **Modul Pendaftaran (`Auth & Registration Module`):** Mengelola data akun pengguna, validasi formulir data diri calon pendaftar beasiswa.
  * **Modul Manajemen Berkas (`File Storage & Management Module`):** Menangani proses *upload*, enkripsi, dan penyimpanan dokumen persyaratan (transkrip, sertifikat) secara aman.
  * **Modul Seleksi & Penilaian (`Assessment Module`):** Menyediakan antarmuka dan logika bisnis bagi *reviewer* / panitia untuk memberikan skor dan verifikasi kelayakan berkas.
  * **Modul Pengumuman & Notifikasi (`Notification & Announcement Module`):** Mengelola distribusi hasil seleksi secara serentak ke *dashboard* pengguna dan pengiriman notifikasi email.

---

## 2. Struktur C&C / Component & Connector (Runtime View)
Struktur *Component & Connector* menunjukkan elemen-elemen runtime (komponen yang aktif saat sistem berjalan) dan bagaimana mereka saling berinteraksi melalui konektor komunikasi (seperti HTTP Request, gRPC, atau Event Bus).

* **Penjelasan Alur Interaksi Runtime:**
  * **Client / Frontend (React App):** Berinteraksi langsung dengan *API Gateway*.
  * **API Gateway:** Bertindak sebagai titik masuk tunggal (*single entry point*) yang merutekan permintaan pengguna ke layanan mikro yang bersangkutan.
  * **Layanan Pendaftaran & Layanan Berkas:** Memproses data masuk dan menyimpan serta mengambil file dari *Cloud Object Storage*.
  * **Layanan Penilaian:** Berkomunikasi dengan basis data utama untuk merekam hasil skoring *reviewer*.
  * **Database & Message Broker:** Tempat penyimpanan data terpusat dan pengiriman pesan asinkron untuk notifikasi email.

---

## 3. Struktur Alokasi (Allocation Structure)
Struktur alokasi memetakan elemen-elemen software (modul atau komponen) ke dalam unsur lingkungan eksternal seperti infrastruktur fisik, server, lingkungan deployment (Vercel/Cloud), maupun tim pengembang.

* **Penjelasan Alokasi Infrastruktur:**
  * **Frontend Deployment:** Antarmuka berbasis web dideploy menggunakan platform **Vercel** yang terintegrasi dengan repositori GitHub[cite: 4].
  * **Backend & Microservices:** Ditempatkan pada server cloud terpusat (Docker Container / Cloud VM).
  * **Storage Allocation:** Dokumen digital (berkas persyaratan beasiswa) dialokasikan ke layanan *Cloud Object Storage* yang aman.
  * **Database Allocation:** Basis data relasional dialokasikan pada Managed Database Instance untuk menjamin integritas data pendaftar dan nilai seleksi.
