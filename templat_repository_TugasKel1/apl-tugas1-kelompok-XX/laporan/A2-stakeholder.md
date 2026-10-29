Penanggung jawab : Ahmad Andira Alam
## A2. Stakeholder

Tabel yang mendefinisikan minimal 6 stakeholder yang mewakili 5 kelompok utama yang berinteraksi dengan sistem layanan beasiswa
| **Kelompok**        | **Nama / Peran Stakeholder**        | **Kebutuhan Utama**                                                                                                               | **Ekspektasi Kualitas (Quality Attributes)**                                              | **Prioritas** |
| ------------------- | ----------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | ------------- |
| **Pengguna Akhir**  | 1. Mahasiswa (Pendaftar)            | Proses pendaftaran lancar, unggah berkas tidak gagal, dan bisa melihat hasil pengumuman dengan jelas.                             | _Usability_ (kemudahan penggunaan), _Availability_ (ketersediaan sistem saat _deadline_). | Tinggi        |
| **Pengguna Akhir**  | 2. Tim Penilai (_Reviewer_)         | Kemudahan dalam melihat dan mengunduh berkas ratusan pendaftar serta memasukkan nilai seleksi.                                    | _Performance_ (waktu muat berkas cepat), _Data Integrity_ (nilai tidak berubah/hilang).   | Tinggi        |
| **Tim Pengembang**  | 3. _Software Engineer_              | Arsitektur yang modular agar kode mudah dipahami, diuji, dan diperbarui jika ada perubahan aturan seleksi.                        | _Maintainability_, _Testability_.                                                         | Sedang        |
| **Tim Operasional** | 4. _System Administrator_           | Visibilitas terhadap kesehatan server, penggunaan _storage_ berkas, dan log apabila terjadi _error_ pada saat pendaftaran massal. | _Observability_, _Deployability_.                                                         | Sedang        |
| **Manajer Bisnis**  | 5. Direktur Kemahasiswaan / Sponsor | Laporan _real-time_ jumlah pendaftar, progres seleksi, serta sistem yang menjamin reputasi penyelenggara beasiswa.                | _Reliability_ (keandalan), _Security_ (keamanan data).                                    | Tinggi        |
| **Pihak Eksternal** | 6. Penyedia Layanan _Cloud Storage_ | Sistem harus berkomunikasi dengan API _storage_ mereka sesuai protokol standar tanpa melampaui batasan _rate limit_.              | _Interoperability_, _Security_.                                                           | Rendah        |

_Tabel 2.1 Analisis empat konteks arsitektur_
