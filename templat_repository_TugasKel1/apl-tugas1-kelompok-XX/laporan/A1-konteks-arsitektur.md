Penanggung jawab : Ahmad Andira Alam
# BAB II. Konteks Dan Keputusan Arsitektur

## A1. Analisis Empat Konteks Arsitektur

Tabel 2.1 merangkum kondisi subsistem Academic Management pada empat konteks arsitektur.

|**Konteks**|**Kondisi subsistem Academic Management**|
|---|---|
|Teknis|Layanan web modular (pendaftaran, penempatan mitra, logbook, bimbingan, penilaian) dengan basis data relasional terpusat. Harus terintegrasi dengan SIAKAD kampus dan menyimpan dokumen (laporan, bukti logbook). Beban puncak terjadi saat pendaftaran dan saat penilaian akhir.|
|Siklus hidup proyek|Dikembangkan iteratif per batch karena aturan MSIB sering berubah. Perlu strategi migrasi data antarbatch, rilis yang aman, dan dokumentasi arsitektur agar mudah diserahkan ke tim berikutnya.|
|Bisnis|Mendukung kelancaran program MSIB, konversi SKS, akuntabilitas penilaian, dan hubungan dengan mitra industri. Batasannya adalah anggaran kampus yang terbatas dan kepatuhan pada ketentuan penyelenggara program.|
|Profesional|Tim kecil (umumnya mahasiswa atau staf kampus) dengan keahlian beragam dan pergantian anggota yang tinggi. Karena itu perlu standar kode, teknologi yang mudah dipelihara, serta perlindungan data pribadi (UU PDP) dan integritas nilai.|

_Tabel 2.1 Analisis empat konteks arsitektur_

