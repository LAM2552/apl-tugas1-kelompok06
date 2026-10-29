Penanggung jawab: Ahmad Andira Alam
# BAB I. Pendahuluan

<!-- Gambaran subsistem dan layanan inti yang ditugaskan, ruang lingkup, dan sumber data. -->
<!-- Penanggung jawab: [ALam] -->

## 1.1 Gambaran layanan inti
Subsistem layanan beasiswa merupakan sebuah platform perangkat lunak terintegrasi yang dirancang untuk mengelola seluruh siklus administratif program beasiswa. Layanan inti yang ditugaskan dalam subsistem ini meliputi:

1.    **Pendaftaran**

Fasilitas bagi calon penerima beasiswa untuk membuat akun dan mengisi formulir data diri.

2.    **Unggah Berkas**

Modul penyimpanan dokumen digital (dokumen persyaratan, transkrip, sertifikat) secara aman.

3.    **Seleksi dan Penilaian Berkas**

Antarmuka khusus bagi tim _reviewer_ atau panitia untuk memverifikasi keabsahan dokumen dan memberikan penilaian (skoring) berdasarkan kriteria yang ditetapkan.

4.    **Pengumuman**

Fitur distribusi informasi hasil seleksi secara serentak kepada para pendaftar melalui _dashboard_ pengguna maupun notifikasi email.

## 1.2 Ruang lingkup (3-5 kasus penggunaan)
Ruang lingkup arsitektur sistem ini mencakup perancangan antarmuka pengguna (web-based), logika bisnis untuk alur pendaftaran dan validasi otomatis, serta pengelolaan basis data relasional dan penyimpanan objek (berkas). Sistem ini dibatasi pada proses seleksi administrasi dan akademik. Arsitektur difokuskan untuk menangani _traffic_ tinggi yang bersifat musiman (menjelang _deadline_ pendaftaran).

## 1.3 Sumber data
<!-- Pengalaman pengguna, informasi publik, wawancara responden. Tanpa identitas pribadi. -->
-	Observasi terhadap sistem layanan pendaftaran beasiswa. 
-	Wawancara dengan staf bagian kemahasiswaan selaku pengelola program beasiswa (Manajer Bisnis) dan mahasiswa selaku pengguna akhir sistem.
-	Studi literatur dari buku Software Architecture in Practice (Bass et al.) dan Fundamentals of Software Architecture (Richards & Ford) terkait karakteristik pendorong arsitektur.

