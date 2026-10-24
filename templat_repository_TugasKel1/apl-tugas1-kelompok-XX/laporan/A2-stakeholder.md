BAB II 
KONTEKS DAN KEPUTUSAN ARSITEKTUR

A1. Analisis Empat Konteks Arsitektur

Tabel 2.1 merangkum kondisi subsistem Academic Management pada empat konteks arsitektur.
| **Konteks**         | **Kondisi subsistem Academic Management**                                                                                                                                                                                                                                         |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Teknis              | Layanan web modular (pendaftaran, penempatan mitra, logbook, bimbingan, penilaian) dengan basis data relasional terpusat. Harus terintegrasi dengan SIAKAD kampus dan menyimpan dokumen (laporan, bukti logbook). Beban puncak terjadi saat pendaftaran dan saat penilaian akhir. |
| Siklus hidup proyek | Dikembangkan iteratif per batch karena aturan MSIB sering berubah. Perlu strategi migrasi data antarbatch, rilis yang aman, dan dokumentasi arsitektur agar mudah diserahkan ke tim berikutnya.                                                                                   |
| Bisnis              | Mendukung kelancaran program MSIB, konversi SKS, akuntabilitas penilaian, dan hubungan dengan mitra industri. Batasannya adalah anggaran kampus yang terbatas dan kepatuhan pada ketentuan penyelenggara program.                                                                 |
| Profesional         | Tim kecil (umumnya mahasiswa atau staf kampus) dengan keahlian beragam dan pergantian anggota yang tinggi. Karena itu perlu standar kode, teknologi yang mudah dipelihara, serta perlindungan data pribadi (UU PDP) dan integritas nilai.    |

_Tabel 2.1 Analisis empat konteks arsitektur_



A2. Stakeholder 

Tabel 2.2 memuat stakeholder register dari lima kelompok: pengguna akhir, tim pengembang, tim operasional, manajer bisnis, dan pihak eksternal.
| **No** | **Stakeholder**                          | **Kelompok**    | **Kebutuhan utama**                                                | **Ekspektasi kualitas**                                          | **Prioritas** |
| ------ | ---------------------------------------- | --------------- | ------------------------------------------------------------------ | ---------------------------------------------------------------- | ------------- |
| 1      | Mahasiswa peserta MSIB                   | Pengguna akhir  | Daftar, isi logbook, lihat jadwal bimbingan dan nilai dengan mudah | Usability, ketersediaan tinggi saat tenggat, responsif di ponsel | Tinggi        |
| 2      | Dosen pembimbing                         | Pengguna akhir  | Memantau logbook, memberi catatan bimbingan, menginput nilai       | Kemudahan penggunaan, akurasi data, notifikasi tepat waktu       | Tinggi        |
| 3      | Tim pengembang                           | Tim pengembang  | Arsitektur jelas, kebutuhan stabil, kode mudah diubah              | Modifiability, testability, dokumentasi                          | Tinggi        |
| 4      | Tim operasional (admin sistem, helpdesk) | Tim operasional | Deployment sederhana, monitoring, backup, penanganan insiden       | Reliability, observability, recoverability                       | Sedang        |
| 5      | Koordinator MSIB / prodi                 | Manajer bisnis  | Rekap penempatan, laporan progres dan nilai untuk konversi SKS     | Akurasi data, laporan tepat waktu, kontrol akses                 | Tinggi        |
| 6      | Pimpinan fakultas/universitas            | Manajer bisnis  | Program berjalan baik, mendukung akreditasi, biaya terkendali      | Keandalan layanan, kepatuhan, efisiensi biaya                    | Sedang        |
| 7      | Kemendikbudristek (penyelenggara MSIB)   | Pihak eksternal | Pelaporan sesuai ketentuan program                                 | Kepatuhan dan akurasi data                                       | Sedang        |

Tabel 2.2 Stakeholder register

