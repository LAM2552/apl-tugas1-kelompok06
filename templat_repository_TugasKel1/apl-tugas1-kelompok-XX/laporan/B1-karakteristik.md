# B1 — Kandidat Karakteristik Sistem

*Penanggung jawab:* [MUHAMMAD AIDIL]

## 1. Pendahuluan

Sistem Informasi Layanan Beasiswa merupakan sistem yang dirancang untuk mendukung proses pengelolaan beasiswa secara digital. Sistem ini mencakup pendaftaran mahasiswa, unggah berkas persyaratan, seleksi dan penilaian berkas, serta pengumuman hasil seleksi.

Untuk menentukan karakteristik arsitektur yang penting, dilakukan identifikasi terhadap kandidat karakteristik berdasarkan kebutuhan operasional, struktural, dan lintas sektor. Setiap kandidat disertai alasan yang menjelaskan kepentingannya terhadap sistem.

## 2. Daftar Kandidat Karakteristik

| No. | Kandidat Karakteristik | Kategori | Alasan |
|---|---|---|---|
| 1 | Keamanan data dan kontrol akses | Lintas sektor | Sistem menyimpan data pribadi dan dokumen persyaratan mahasiswa sehingga akses harus dibatasi agar tidak disalahgunakan. |
| 2 | Integritas dan konsistensi data | Struktural | Data pendaftaran, dokumen, dan hasil penilaian harus saling sesuai agar tidak terjadi kesalahan informasi. |
| 3 | Keandalan sistem | Operasional | Sistem harus mampu menyimpan dan menampilkan data dengan benar agar proses pendaftaran dan seleksi tidak terganggu. |
| 4 | Efisiensi waktu respons | Operasional | Pengguna membutuhkan akses yang cepat ketika melakukan pendaftaran, mengunggah berkas, dan melihat hasil seleksi. |
| 5 | Kemudahan penggunaan | Operasional | Sistem harus mudah dipahami oleh mahasiswa dan admin agar setiap proses dapat dilakukan dengan baik. |
| 6 | Kemudahan pemeliharaan | Struktural | Sistem perlu mudah diperbaiki dan dikembangkan apabila terdapat perubahan persyaratan atau tahapan seleksi beasiswa. |
| 7 | Interoperabilitas | Lintas sektor | Sistem berpotensi terhubung dengan sistem akademik untuk memperoleh atau memverifikasi data mahasiswa. |
| 8 | Skalabilitas | Struktural | Sistem harus mampu menangani peningkatan jumlah pendaftar dan dokumen ketika periode pendaftaran berlangsung. |
| 9 | Kemudahan audit dan ketertelusuran | Lintas sektor | Riwayat pemeriksaan berkas dan penilaian perlu dicatat agar proses seleksi dapat diperiksa kembali. |
| 10 | Ketersediaan layanan | Operasional | Sistem perlu dapat diakses selama periode pendaftaran, seleksi, dan pengumuman hasil beasiswa. |

## 3. Prioritas Kandidat Karakteristik

Dalam menentukan karakteristik pendorong arsitektur, digunakan tiga ciri sebagai alat pengujian, yaitu:
1. Penting bagi keberhasilan sistem, yaitu karakteristik memiliki pengaruh terhadap keberhasilan layanan beasiswa.
2. Dapat diukur atau diuji, yaitu karakteristik dapat diperiksa melalui indikator atau pengujian tertentu.
3. Memengaruhi keputusan arsitektur, yaitu karakteristik dapat memengaruhi rancangan, pemilihan teknologi, atau struktur sistem.
Berdasarkan ketiga ciri tersebut, dipilih tiga karakteristik yang paling penting untuk diprioritaskan:

1. Keamanan data dan kontrol akses, karena sistem mengelola data pribadi serta dokumen mahasiswa yang harus dilindungi dari akses tidak sah. Karakteristik ini dapat diuji melalui autentikasi dan pembatasan hak akses, serta memengaruhi rancangan keamanan sistem.

2. Integritas dan konsistensi data, karena data pendaftaran, dokumen persyaratan, dan hasil penilaian harus sesuai satu sama lain. Karakteristik ini dapat diuji melalui validasi data dan pemeriksaan basis data, serta memengaruhi rancangan penyimpanan dan pengelolaan data.

3. Keandalan sistem, karena sistem harus mampu menjalankan proses pendaftaran, unggah berkas, seleksi, dan pengumuman tanpa kehilangan data. Karakteristik ini dapat diuji melalui pengujian penyimpanan dan pemulihan data, serta memengaruhi rancangan pengelolaan sistem dan mekanisme pencadangan.

## 4. Kesimpulan

Berdasarkan hasil identifikasi, terdapat sepuluh kandidat karakteristik arsitektur yang relevan dengan Sistem Informasi Layanan Beasiswa. Kandidat tersebut dikelompokkan ke dalam kategori operasional, struktural, dan lintas sektor.

Dari sepuluh kandidat tersebut, tiga karakteristik yang diprioritaskan adalah keamanan data dan kontrol akses, integritas dan konsistensi data, serta keandalan sistem. Ketiganya dipilih karena memiliki pengaruh besar terhadap perlindungan data, ketepatan informasi, dan kelancaran proses layanan beasiswa.


