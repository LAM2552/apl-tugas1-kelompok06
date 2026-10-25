Penanggung Jawab: Amar Farid A Toloa

# A4. Kebutuhan Signifikan (ASR)


Tabel 2.4 di bawah ini memuat minimal 3 Kebutuhan Signifikan Secara Arsitektural (ASR) beserta alasan signifikansinya terhadap sistem layanan MSIB.

| No | Kategori ASR | Deskripsi Kebutuhan Signifikan (ASR) | Alasan Signifikansi Arsitektural |
|:--:|:---|:---|:---|
| 1 | **Performance / Kinerja** | Sistem harus mampu menangani lonjakan akses tinggi (*high concurrency*) secara bersamaan, terutama pada periode pembukaan pendaftaran dan pengisian *logbook* massal oleh mahasiswa. | Kebutuhan ini berdampak langsung pada pemilihan arsitektur *backend*, penggunaan *load balancer*, serta strategi *caching* agar sistem tidak mengalami *down* atau *latency* yang tinggi saat trafik membludak. |
| 2 | **Security / Keamanan** | Sistem wajib mengamankan data pribadi mahasiswa, dokumen transkrip, serta penilaian mitra industri dengan standar enkripsi yang kuat dan kontrol akses berbasis peran (*Role-Based Access Control*). | Hal ini krusial secara arsitektural karena menyangkut privasi data sensitif dan integritas akademik, sehingga memerlukan perancangan lapisan keamanan (*security layers*) yang ketat pada tingkat API dan basis data. |
| 3 | **Interoperability / Integrasi** | Sistem harus dapat terintegrasi secara *real-time* atau berkala dengan sistem eksternal seperti layanan SSO universitas dan basis data mitra industri/platform MSIB pusat. | Kebutuhan ini menuntut perancangan arsitektur berbasis layanan (seperti RESTful API atau *microservices/modular monolith*) yang fleksibel agar komunikasi antar-sistem dapat berjalan stabil tanpa mengganggu modul internal. |
