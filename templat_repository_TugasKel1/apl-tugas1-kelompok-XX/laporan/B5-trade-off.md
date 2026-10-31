# B5. Analisis Trade-off


**Penanggung jawab:** [MUHAMMAD AIDIL]

## 1. Pendahuluan

Analisis trade-off merupakan proses menganalisis hubungan antara dua karakteristik arsitektur yang saling memengaruhi, ketika peningkatan satu karakteristik dapat memberikan dampak terhadap karakteristik lainnya. Pada Sistem Informasi Layanan Beasiswa, analisis ini diperlukan untuk menentukan prioritas dalam pengambilan keputusan arsitektur agar sistem dapat berjalan secara optimal.

Beberapa karakteristik yang saling memengaruhi perlu dipertimbangkan, terutama dalam proses pendaftaran, unggah berkas, seleksi dan penilaian, serta pengumuman hasil beasiswa.
## 2. Analisis Pasangan Karakteristik

Pasangan Karakteristik	Dampak Trade-off
1.	Keamanan dan Kinerja	Penerapan autentikasi, enkripsi, dan pemeriksaan hak akses dapat meningkatkan keamanan data, tetapi menambah proses sehingga berpotensi memperlambat waktu respons sistem.
2.	Ketersediaan dan Keamanan	Penerapan pembatasan akses dan pemeriksaan keamanan yang ketat dapat menambah tahapan sebelum pengguna mengakses sistem. Hal ini dapat memengaruhi kemudahan akses, tetapi tetap diperlukan untuk melindungi data beasiswa.
3.	Skalabilitas dan Kemudahan Pemeliharaan	Penambahan kapasitas server dan komponen sistem dapat membantu menangani peningkatan jumlah pendaftar, tetapi dapat membuat pengelolaan dan pemeliharaan sistem menjadi lebih kompleks.

## 3. Ringkasan Keputusan Trade-off

| No. | Pasangan Karakteristik | Potensi Konflik | Keputusan |
|---|---|---|---|
| 1 | Keamanan dan kemudahan penggunaan | Perlindungan ketat dapat menambah langkah akses pengguna. | Menerapkan autentikasi dan RBAC dengan antarmuka yang sederhana. |
| 2 | Kinerja dan keandalan | Optimasi kecepatan yang tidak tepat dapat meningkatkan risiko kesalahan data. | Mengutamakan konsistensi data dan melakukan optimasi proses secara terukur. |
| 3 | Kemudahan pemeliharaan dan kinerja | Pemisahan modul yang tidak tepat dapat menambah beban pemrosesan. | Menggunakan arsitektur monolitik modular dengan batas modul yang jelas. |

## 4. Kesimpulan

Berdasarkan analisis trade-off, terdapat tiga pasangan karakteristik yang saling memengaruhi dalam Sistem Informasi Layanan Beasiswa, yaitu keamanan dan kinerja, ketersediaan dan keamanan, serta skalabilitas dan kemudahan pemeliharaan.

Dalam pengambilan keputusan arsitektur, keamanan menjadi prioritas utama karena sistem mengelola data pribadi, dokumen persyaratan, dan hasil seleksi mahasiswa. Namun, karakteristik lainnya tetap perlu diperhatikan agar sistem dapat memberikan layanan yang cepat, tersedia, dan mudah dikembangkan.

