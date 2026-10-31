Penanggung jawab: Amar Farid A Toloa

# A3. Batasan Sistem

Tabel di bawah ini memuat minimal 2 batasan untuk tiap kategori (teknologi, bisnis, operasional) beserta dampaknya pada sistem layanan beasiswa.

| No | Kategori | Batasan Sistem | Dampak |
|:--:|:---|:---|:---|
| 1 | **Teknologi** | Sistem harus terintegrasi dengan layanan Single Sign-On (SSO) universitas yang sudah ada menggunakan protokol OAuth 2.0 / SAML untuk proses otentikasi akun mahasiswa. | Tim pengembang tidak dapat membangun modul otentikasi mandiri dari awal dan harus menyesuaikan alur login pengguna dengan infrastruktur keamanan pusat universitas. |
| 2 | **Teknologi** | Aplikasi berbasis web harus responsif dan kompatibel minimal pada dua versi peramban (*browser*) utama terakhir tanpa mewajibkan instalasi plugin tambahan. | Penggunaan pustaka (*library*) atau *framework* front-end dibatasi pada teknologi yang mendukung kompatibilitas lintas peramban secara optimal agar mudah diakses pendaftar dari berbagai perangkat. |
| 3 | **Bisnis** | Pengembangan dan peluncuran modul pendaftaran dan seleksi beasiswa harus selesai tepat waktu sebelum jadwal pembukaan pendaftaran periode baru dimulai. | Ruang lingkup fitur (*scope*) pada rilis pertama harus diprioritaskan hanya pada layanan inti (pendaftaran, unggah berkas, seleksi/penilaian, dan pengumuman) serta menunda fitur opsional ke tahap berikutnya. |
| 4 | **Bisnis** | Kepatuhan terhadap regulasi perlindungan data pribadi mahasiswa dan kerahasiaan dokumen syarat beasiswa (seperti slip gaji, transkrip, dll) sesuai kebijakan instansi. | Sistem wajib menerapkan aturan pembatasan akses (*Role-Based Access Control*) yang ketat sehingga hanya tim penilai/reviewer berwenang yang dapat membuka dokumen pendaftar. |
| 5 | **Operasional** | Pemeliharaan rutin (*maintenance*) dan pembaruan sistem hanya dapat dijadwalkan di luar jam sibuk akademik (seperti akhir pekan atau tengah malam). | Tim pengelola infrastruktur harus merancang mekanisme pembaruan sistem tanpa gangguan (*zero-downtime deployment*) atau membuat pengumuman pemeliharaan agar tidak mengganggu proses unggah berkas mahasiswa. |
| 6 | **Operasional** | Keterbatasan jumlah staf pengelola atau administrator IT yang siaga untuk memantau server secara langsung setiap hari. | Sistem harus dilengkapi fitur *logging* dan sistem pemberitahuan otomatis (*alerting*) via email/webhook jika terjadi lonjakan error atau kendala pada server. |
