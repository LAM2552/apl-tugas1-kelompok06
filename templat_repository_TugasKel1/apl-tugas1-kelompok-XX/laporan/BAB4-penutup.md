# BAB IV. Penutup

<!-- Kesimpulan dan saran. Penanggung jawab: [nama] -->

## 4.1 Kesimpulan
  Berdasarkan perancangan arsitektur subsistem Layanan Beasiswa Universitas Muslim Indonesia (UMI) Makassar yang telah diuraikan pada bab-bab sebelumnya, dapat ditarik beberapa kesimpulan utama sebagai berikut:
1.	Subsistem Layanan Beasiswa membutuhkan arsitektur dengan tingkat skalabilitas dan ketersediaan (Availability) yang tinggi untuk mengatasi lonjakan akses (traffic) yang bersifat musiman, khususnya menjelang batas waktu pendaftaran. 
2.	Keamanan (Security) menjadi prioritas utama yang harus didahulukan dibandingkan dengan kinerja, mengingat sistem ini mengelola data pribadi sensitif serta dokumen persyaratan mahasiswa (KTP, slip gaji, transkrip). Arsitektur dirancang dengan perlindungan berlapis melalui enkripsi dan Role-Based Access Control (RBAC). 
3.	Implementasi Cloud Object Storage beserta mekanisme load balancing diputuskan (ADR-001) sebagai solusi untuk menjamin stabilitas server dan mempercepat proses unggah berkas tanpa membebani server lokal kampus. 
4.	Struktur arsitektur dibangun dengan pendekatan modular (Module Structure) yang memisahkan logika bisnis penilaian dari antarmuka pengguna, guna memudahkan pemeliharaan sistem (Maintainability) apabila terjadi perubahan kriteria seleksi beasiswa di masa depan. 


## 4.2 Saran
  Dalam rangka pengembangan dan penyempurnaan sistem informasi layanan beasiswa ini, penulis memberikan beberapa saran:
1.	Bagi Tim Pengembang: Disarankan untuk selalu memantau metrik performa secara berkala (seperti load testing) guna memastikan waktu respons tetap berada di bawah target maksimal 2 detik, serta memastikan uptime sistem terjaga di angka 99,9% saat periode pendaftaran berlangsung. 
2.	Bagi Institusi (Manajer Bisnis): Diperlukan alokasi anggaran yang memadai untuk biaya langganan infrastruktur cloud secara berkesinambungan, yang merupakan konsekuensi (trade-off) dari keputusan mengutamakan stabilitas dan keamanan data pelamar. 
3.	Pengembangan Lanjutan: Sebaiknya dilakukan evaluasi pasca-implementasi secara rutin dengan melibatkan pengguna akhir (mahasiswa dan tim penilai) agar sistem antarmuka (front-end) terus disesuaikan demi meningkatkan kemudahan penggunaan (usability) tanpa mengorbankan standar keamanan yang telah ditetapkan.
