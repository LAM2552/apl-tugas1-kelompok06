Penanggung jawab: Amar Farid A Toloa

# A3. Batasan Sistem

Tabel 2.2 memuat 2 batasan untuk tiap kategori (teknologi, bisnis, operasional), disertai dampaknya
## 1. Batasan Teknologi (Technology Constraints)
* **Batasan 1:** Sistem harus terintegrasi dengan layanan Single Sign-On (SSO) universitas yang sudah ada menggunakan protokol OAuth 2.0 / SAML.
  * **Dampak:** Tim pengembang tidak dapat membangun sistem autentikasi mandiri dari awal dan harus menyesuaikan alur login dengan infrastruktur keamanan pusat universitas.
* **Batasan 2:** Aplikasi harus dibangun berbasis web yang responsif dan kompatibel minimal pada dua versi peramban (*browser*) utama terakhir tanpa memerlukan instalasi perangkat lunak tambahan.
  * **Dampak:** Penggunaan pustaka (*library*) atau *framework* front-end dibatasi pada teknologi yang mendukung kompatibilitas lintas peramban dengan baik.

## 2. Batasan Bisnis (Business Constraints)
* **Batasan 1:** Pengembangan dan peluncuran modul MSIB harus selesai sebelum jadwal periode pendaftaran mahasiswa semester baru dimulai (tenggat waktu ketat).
  * **Dampak:** Ruang lingkup fitur (*scope*) pada rilis pertama dibatasi hanya pada layanan inti (pendaftaran, penempatan, *logbook*, bimbingan, penilaian) dan menunda fitur tambahan/pendukung ke fase berikutnya.
* **Batasan 2:** Kepatuhan terhadap regulasi perlindungan data pribadi mahasiswa dan mitra industri sesuai kebijakan universitas dan hukum yang berlaku.
  * **Dampak:** Sistem wajib menerapkan enkripsi data sensitif (baik saat transit maupun *at rest*) dan pembatasan akses (*role-based access control*) yang ketat bagi admin, dosen pembimbing, dan mentor mitra.

## 3. Batasan Operasional (Operational Constraints)
* **Batasan 1:** Pemeliharaan rutin (*maintenance*) dan pembaruan sistem hanya dapat dilakukan di luar jam operasional akademik utama (yakni pada akhir pekan atau tengah malam).
  * **Dampak:** Tim DevOps harus merancang arsitektur sistem yang mendukung proses *zero-downtime deployment* atau penjadwalan *backup* otomatis yang efisien agar tidak mengganggu aktivitas pengguna.
* **Batasan 2:** Keterbatasan jumlah staf administrator IT universitas yang tersedia untuk menangani pemantauan infrastruktur harian secara langsung.
  * **Dampak:** Sistem harus dilengkapi dengan fitur *logging* dan sistem *alerting* otomatis (misalnya notifikasi ke webhook/email) jika terjadi kegagalan layanan (*server down* atau *error* fatal).

