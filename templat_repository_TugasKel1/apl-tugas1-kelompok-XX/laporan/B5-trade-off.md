# B5. Analisis Trade-off


**Penanggung jawab:** [MUHAMMAD AIDIL]

## 1. Pendahuluan

Analisis trade-off merupakan proses menganalisis hubungan antara dua atau lebih karakteristik sistem yang dapat saling memengaruhi ketika diterapkan secara bersamaan. Dalam pengembangan subsistem Academic Management untuk layanan Magang dan Studi Independen (MSIB) di Universitas Muslim Indonesia, analisis ini diperlukan untuk menentukan keputusan desain yang sesuai dengan kebutuhan pengguna dan kemampuan tim pengembang.

Analisis trade-off dilakukan dengan mempertimbangkan karakteristik sistem, dampak dari setiap alternatif, serta keputusan yang diambil untuk menjaga keseimbangan antara kualitas sistem dan kebutuhan operasional.

## 2. Analisis Pasangan Karakteristik

### 2.1 Keamanan (Security) dan Kemudahan Penggunaan (Usability)

**Hubungan antar-karakteristik**

Keamanan dan kemudahan penggunaan merupakan dua karakteristik yang dapat saling memengaruhi. Penerapan keamanan yang ketat, seperti autentikasi dan pembatasan hak akses, dapat melindungi data mahasiswa serta informasi penilaian akademik. Namun, proses autentikasi yang terlalu rumit dapat menyulitkan pengguna ketika mengakses sistem.

Sebaliknya, proses akses yang terlalu sederhana dapat meningkatkan kemudahan penggunaan, tetapi berisiko mengurangi perlindungan terhadap data akademik.

Dalam sistem Academic Management, mahasiswa perlu mengakses pendaftaran dan logbook, sedangkan dosen pembimbing, koordinator program, serta pembimbing lapangan membutuhkan akses sesuai tugas dan kewenangannya.

**Keputusan yang diambil**

Sistem menerapkan autentikasi pengguna dan pengaturan hak akses berdasarkan peran atau *Role-Based Access Control* (RBAC). Antarmuka dibuat sederhana, sedangkan proses autentikasi dirancang agar tetap mudah digunakan tanpa mengurangi perlindungan data.

**Alasan keputusan**

Keputusan ini diambil untuk menjaga keamanan data pribadi dan akademik sekaligus mempertahankan kemudahan akses bagi setiap pengguna. Keamanan tetap menjadi prioritas, tetapi penerapannya perlu dirancang agar tidak menimbulkan hambatan penggunaan yang tidak perlu.

### 2.2 Kinerja (Performance Efficiency) dan Keandalan (Reliability)

**Hubungan antar-karakteristik**

Kinerja dan keandalan dapat saling memengaruhi dalam pengelolaan data sistem. Optimalisasi proses penyimpanan dan pengambilan data dapat mempercepat waktu respons aplikasi. Namun, apabila optimasi dilakukan tanpa memperhatikan validasi dan konsistensi data, risiko kesalahan penyimpanan dapat meningkat.

Sebaliknya, pemeriksaan dan pemrosesan tambahan untuk menjaga keandalan dapat menambah waktu pemrosesan apabila tidak dirancang secara efisien.

Dalam sistem Academic Management, hubungan ini penting ketika mahasiswa melakukan pendaftaran, mengisi logbook, dan ketika dosen mengakses atau memasukkan penilaian.

**Keputusan yang diambil**

Sistem dirancang menggunakan pengelolaan basis data yang terstruktur, validasi data, dan proses penyimpanan yang menjaga konsistensi informasi. Optimasi kinerja dilakukan melalui perancangan kueri yang efisien dan pengelolaan akses data sesuai kebutuhan.

**Alasan keputusan**

Keputusan ini bertujuan menjaga waktu respons tetap memadai tanpa mengorbankan ketepatan data akademik. Data yang benar dan tersimpan dengan baik lebih penting daripada peningkatan kecepatan yang berisiko menimbulkan kesalahan.

### 2.3 Kemudahan Pemeliharaan (Maintainability) dan Kinerja (Performance Efficiency)

**Hubungan antar-karakteristik**

Kemudahan pemeliharaan dan kinerja dapat saling memengaruhi melalui struktur aplikasi. Pemisahan sistem menjadi modul yang jelas dapat mempermudah pengembangan, pengujian, dan perbaikan kesalahan. Namun, pemisahan yang tidak dirancang dengan baik dapat menambah komunikasi antarmodul dan menyebabkan proses aplikasi menjadi kurang efisien.

Sebaliknya, pengoptimalan kinerja yang terlalu berfokus pada satu bagian kode dapat membuat struktur aplikasi lebih sulit dipahami dan dipelihara.

**Keputusan yang diambil**

Sistem direkomendasikan menggunakan arsitektur monolitik modular dengan pemisahan fungsi pendaftaran, penempatan mitra, logbook, bimbingan, dan penilaian. Setiap modul memiliki tanggung jawab yang jelas, sedangkan proses yang sering digunakan tetap dirancang secara efisien.

**Alasan keputusan**

Pendekatan ini sesuai untuk proyek mahasiswa karena mempermudah pembagian tugas, pengujian, dan pemeliharaan tanpa menambah kompleksitas infrastruktur yang tidak diperlukan. Kinerja tetap diperhatikan melalui perancangan modul dan akses data yang efisien.

## 3. Ringkasan Keputusan Trade-off

| No. | Pasangan Karakteristik | Potensi Konflik | Keputusan |
|---|---|---|---|
| 1 | Keamanan dan kemudahan penggunaan | Perlindungan ketat dapat menambah langkah akses pengguna. | Menerapkan autentikasi dan RBAC dengan antarmuka yang sederhana. |
| 2 | Kinerja dan keandalan | Optimasi kecepatan yang tidak tepat dapat meningkatkan risiko kesalahan data. | Mengutamakan konsistensi data dan melakukan optimasi proses secara terukur. |
| 3 | Kemudahan pemeliharaan dan kinerja | Pemisahan modul yang tidak tepat dapat menambah beban pemrosesan. | Menggunakan arsitektur monolitik modular dengan batas modul yang jelas. |

## 4. Kesimpulan

Analisis trade-off pada sistem Academic Management menunjukkan bahwa keamanan, kemudahan penggunaan, kinerja, keandalan, dan kemudahan pemeliharaan perlu dipertimbangkan secara seimbang.

Keputusan yang direkomendasikan adalah menerapkan keamanan berbasis peran dengan antarmuka sederhana, menjaga konsistensi data sambil mengoptimalkan kinerja, serta menggunakan arsitektur monolitik modular untuk mendukung pemeliharaan sistem.

Keputusan tersebut merupakan rekomendasi awal yang perlu disesuaikan dengan kebutuhan sistem dan diselaraskan dengan dokumen keputusan arsitektur A5. Tujuannya adalah menghasilkan sistem layanan MSIB yang aman, andal, mudah digunakan, dan dapat dikembangkan sesuai kebutuhan.

