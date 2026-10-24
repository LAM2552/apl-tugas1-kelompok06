# B1 — Kandidat Karakteristik Sistem

*Penanggung jawab:* [MUHAMMAD AIDIL]

## 1. Pendahuluan

Subsistem Academic Management merupakan bagian dari sistem informasi akademik Universitas Muslim Indonesia yang mendukung layanan Magang dan Studi Independen (MSIB). Sistem ini mencakup pendaftaran mahasiswa, penempatan mitra, pengisian logbook, bimbingan, dan penilaian.

Untuk menentukan karakteristik arsitektur yang penting, dilakukan identifikasi terhadap kandidat karakteristik berdasarkan kebutuhan operasional, struktural, dan lintas sektor. Setiap kandidat disertai alasan yang menjelaskan kepentingannya terhadap sistem.

## 2. Daftar Kandidat Karakteristik

| No. | Kandidat Karakteristik | Kategori | Alasan |
|---|---|---|---|
| 1 | Keamanan data dan kontrol akses | Lintas sektor | Sistem menyimpan data pribadi mahasiswa, dokumen pendaftaran, logbook, dan penilaian akademik. Akses harus dibatasi berdasarkan peran pengguna agar data terlindungi dari akses dan perubahan yang tidak sah. |
| 2 | Integritas dan konsistensi data | Struktural | Data mahasiswa, mitra, pendaftaran, logbook, bimbingan, dan penilaian saling berkaitan. Konsistensi diperlukan agar tidak terjadi ketidaksesuaian data antarbagian sistem. |
| 3 | Keandalan sistem | Operasional | Sistem harus dapat menyimpan dan menampilkan data secara benar. Gangguan atau kegagalan penyimpanan dapat menghambat pendaftaran dan menyebabkan kehilangan catatan kegiatan mahasiswa. |
| 4 | Efisiensi waktu respons | Operasional | Mahasiswa dan dosen membutuhkan akses yang memadai ketika melakukan pendaftaran, mengisi logbook, memberikan bimbingan, dan memeriksa penilaian. |
| 5 | Kemudahan penggunaan | Operasional | Sistem digunakan oleh mahasiswa, dosen pembimbing, koordinator program, dan pembimbing lapangan. Antarmuka harus mudah dipahami agar setiap pengguna dapat menjalankan tugasnya dengan benar. |
| 6 | Kemudahan pemeliharaan | Struktural | Sistem terdiri atas beberapa fungsi utama. Pemisahan modul berdasarkan tanggung jawab dapat mempermudah perbaikan kesalahan dan pengembangan fitur tanpa mengubah seluruh aplikasi. |
| 7 | Interoperabilitas | Lintas sektor | Sistem berpotensi perlu bertukar data dengan sistem akademik atau layanan lain. Format data dan mekanisme integrasi perlu dirancang agar pertukaran informasi dapat dilakukan secara konsisten dan aman. |
| 8 | Skalabilitas | Struktural | Jumlah mahasiswa, mitra, dan catatan kegiatan dapat bertambah. Arsitektur perlu mempertimbangkan kemampuan sistem untuk menangani pertumbuhan data dan jumlah pengguna. |
| 9 | Kemudahan audit dan ketertelusuran | Lintas sektor | Riwayat perubahan data penting, status pendaftaran, bimbingan, dan penilaian perlu dapat ditelusuri untuk membantu pemeriksaan serta pertanggungjawaban proses akademik. |
| 10 | Ketersediaan layanan | Operasional | Pengguna perlu mengakses layanan sesuai jadwal kegiatan MSIB. Ketersediaan yang baik membantu mengurangi hambatan saat pendaftaran, pengisian logbook, dan proses penilaian. |

## 3. Prioritas Kandidat Karakteristik

Berdasarkan fungsi dan data yang dikelola, kandidat yang diprioritaskan untuk dipertimbangkan dalam keputusan arsitektur adalah:

1. **Keamanan data dan kontrol akses**, karena sistem menangani informasi pribadi serta penilaian akademik.
2. **Integritas dan konsistensi data**, karena data antarproses MSIB saling berkaitan.
3. **Keandalan sistem**, karena kegagalan penyimpanan dapat mengganggu proses akademik.
4. **Kemudahan pemeliharaan**, karena sistem memiliki beberapa modul dengan tanggung jawab berbeda.
5. **Efisiensi waktu respons**, karena pengguna membutuhkan akses yang memadai terhadap layanan.

Prioritas tersebut merupakan hasil analisis awal berdasarkan ruang lingkup proyek. Penetapan prioritas akhir perlu dikonfirmasi melalui kebutuhan pemangku kepentingan dan keputusan arsitektur kelompok.

## 4. Kesimpulan

Sepuluh kandidat karakteristik telah diidentifikasi untuk sistem Academic Management layanan MSIB dengan mempertimbangkan kategori operasional, struktural, dan lintas sektor. Kandidat tersebut dapat digunakan sebagai dasar dalam menentukan atribut kualitas yang paling penting dan merumuskan keputusan arsitektur pada tahap berikutnya.


