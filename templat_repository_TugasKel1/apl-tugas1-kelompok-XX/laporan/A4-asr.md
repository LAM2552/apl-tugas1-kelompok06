Penanggung Jawab: Amar Farid A Toloa

# A4. Kebutuhan Signifikan (ASR)


Tabel di bawah ini memuat minimal 3 Kebutuhan Signifikan Secara Arsitektural (ASR) beserta alasan signifikansinya terhadap sistem layanan beasiswa.

| No | Kategori ASR | Deskripsi Kebutuhan Signifikan (ASR) | Alasan Signifikansi Arsitektural |
|:--:|:---|:---|:---|
| 1 | **Performance / Kinerja** | Sistem harus mampu menangani lonjakan akses tinggi secara bersamaan (*high concurrency*) saat hari-hari terakhir pendaftaran beasiswa dan pengumuman hasil seleksi. | Kebutuhan ini sangat krusial untuk menentukan kapasitas *server*, penerapan *load balancing*, serta mekanisme *caching* agar situs tidak mengalami *down* atau kelambatan akses saat diserbu ribuan pendaftar. |
| 2 | **Security & Data Integrity / Keamanan** | Sistem wajib mengamankan data pribadi sensitif pendaftar serta dokumen persyaratan yang diunggah (seperti KTP, transkrip nilai, slip gaji orang tua) dengan enkripsi ketat dan pembatasan akses (*Role-Based Access Control*). | Aspek arsitektur keamanan harus dirancang berlapis (baik enkripsi *at rest* maupun *in transit*) guna menjaga kerahasiaan data pribadi dan mencegah manipulasi dokumen atau hasil penilaian oleh pihak yang tidak berwenang. |
| 3 | **Maintainability & Extensibility / Pemeliharaan & Skalabilitas** | Modul alur seleksi dan penilaian berkas harus dirancang dengan struktur kode yang modular agar mudah disesuaikan jika ada perubahan kriteria atau bobot penilaian beasiswa di periode berikutnya. | Pemilihan pola arsitektur perangkat lunak yang modular (seperti pemisahan logika bisnis penilaian dari antarmuka pengguna) akan mempermudah pengembang dalam melakukan pemeliharaan dan pembaruan aturan seleksi tanpa harus merombak seluruh sistem
