# ADR-[001]: [Implementasi Load Balancing dan Caching Berbasis Cloud]

<!-- Salin berkas ini menjadi ADR-001-judul-singkat.md, ADR-002-... dan seterusnya. -->

- **Status:** Diterima 
- **Tanggal:** [31-10-2026]
- **Pengambil keputusan:** [Ahmad Andira Alam]

## Context
[Sistem harus mampu menangani lonjakan akses tinggi (high concurrency) saat hari-hari terakhir pendaftaran beasiswa dan pengumuman hasil seleksi. Hal ini sangat sejalan dengan konteks teknis sistem yang butuh elastisitas serta tuntutan mahasiswa agar server stabil 100% saat tenggat waktu.]

## Decision
[Kami akan menerapkan kapasitas server berbasis cloud dengan menggunakan mekanisme load balancing dan caching.]

## Consequences
[Dampak positifnya, situs tidak mengalami down atau kelambatan akses saat diserbu ribuan pendaftar. Konsekuensi negatifnya (trade-off), biaya langganan infrastruktur cloud akan meningkat.]

## Compliance
[Melakukan pengujian beban (load testing) sebelum perilisan dan pemantauan otomatis pada metrik kepadatan trafik server.]



# ADR-[002]: [Perlindungan Data Pribadi Sensitif]

<!-- Salin berkas ini menjadi ADR-001-judul-singkat.md, ADR-002-... dan seterusnya. -->

- **Status:** Diterima 
- **Tanggal:** [31-10-2026]
- **Pengambil keputusan:** [Ahmad Andira Alam]

## Context
[Sistem wajib mengamankan data pribadi sensitif (KTP, slip gaji orang tua) dengan perlindungan ketat. Selain itu, alur seleksi harus menggunakan struktur kode modular agar mudah disesuaikan jika kriteria penilaian berubah. Ini merespons kebutuhan mahasiswa atas privasi data dan standar rekayasa perangkat lunak tim pengembang.]

## Decision
[Kami akan merancang keamanan berlapis meliputi enkripsi at rest maupun in transit beserta pembatasan akses (Role-Based Access Control), dan melakukan pemisahan logika bisnis penilaian dari antarmuka pengguna.]

## Consequences
[Dampak positifnya, kerahasiaan data pribadi terjamin, manipulasi dokumen dicegah, dan pemeliharaan sistem bisa dilakukan tanpa harus merombak seluruh sistem. Trade-off-nya, tingkat kerumitan pengembangan awal akan bertambah.]

## Compliance
[Memberlakukan tinjauan kode (code review) yang ketat pada setiap modul penilaian dan menerapkan pengujian keamanan berulang.]


