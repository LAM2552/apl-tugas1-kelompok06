Penanggung jawab : Ahmad Andira Alam

## A1. Analisis Empat Konteks Arsitektur

Berikut adalah tabel analisis empat konteks arsitektur terhadap layanan inti beasiswa.

| **Konteks**         | **Kondisi subsistem Academic Management**                                                                                                                                                                                                                 |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Teknis              | Subsistem ini membutuhkan arsitektur dengan skalabilitas (elastisitas) tinggi berbasis _cloud_ untuk menangani lonjakan akses serentak saat batas waktu pendaftaran, serta memerlukan keamanan data yang kuat untuk melindungi dokumen pribadi mahasiswa. |
| Siklus hidup proyek | Pengembangan akan menggunakan pendekatan iteratif (_Agile_), sehingga modul pendaftaran dan unggah berkas harus dirilis lebih awal sebelum tim mulai mengembangkan modul penilaian bagi _reviewer_                                                        |
| Bisnis              | Sistem ini menjadi investasi institusi untuk mengurangi waktu pemrosesan administrasi manual, meningkatkan transparansi penilaian, dan mencegah hilangnya dokumen pelamar yang sering terjadi pada pendaftaran fisik.                                     |
| Profesional         | Arsitek dituntut untuk mengambil keputusan yang menjamin kepatuhan terhadap regulasi privasi data (misalnya UU Perlindungan Data Pribadi) sekaligus menjaga standar rekayasa perangkat lunak (_clean code_, ADR yang terdokumentasi).                     |

_Tabel 2.1 Analisis empat konteks arsitektur_

