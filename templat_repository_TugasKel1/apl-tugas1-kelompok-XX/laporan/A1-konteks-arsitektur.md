# A1. Analisis Empat Konteks Arsitektur

BAB I 
PENDAHULUAN

1.1 Gambaran Subsistem dan Layanan Inti
Subsistem Academic Management merupakan bagian dari sistem informasi yang mengelola layanan magang dan studi independen bersertifikat (MSIB) di lingkungan, Universitas Muslim Indonesia. Layanan inti yang ditugaskan mencakup lima fungsi utama:
1.	Pendaftaran: mahasiswa mendaftar program MSIB, mengunggah berkas persyaratan, dan memperoleh verifikasi dari koordinator program.
2.	Penempatan mitra: pencocokan dan pencatatan penempatan mahasiswa pada mitra industri atau lembaga penyelenggara.
3.	Logbook: pencatatan kegiatan harian atau mingguan mahasiswa selama program, beserta bukti kegiatan.
4.	Bimbingan: penjadwalan dan pencatatan sesi bimbingan antara mahasiswa, dosen pembimbing, dan pembimbing lapangan.
5.	Penilaian: pengumpulan nilai dari dosen pembimbing dan mitra, serta rekapitulasi hasil akhir untuk konversi SKS.
Pengguna utama subsistem ini adalah mahasiswa peserta, dosen pembimbing, koordinator program, dan pembimbing lapangan dari mitra. Subsistem ini juga berinteraksi dengan layanan lain di sistem induk, misalnya autentikasi pengguna dan data akademik mahasiswa. Layanan ini penting secara arsitektural karena melibatkan banyak peran dengan hak akses berbeda, data bernilai akademik yang harus akurat, dan beban yang berfluktuasi mengikuti kalender program.
1.2 Ruang Lingkup
Pembahasan dalam laporan ini dibatasi pada hal berikut.
Termasuk dalam lingkup:
-	Alur pendaftaran, penempatan mitra, logbook, bimbingan, dan penilaian pada program MSIB.
-	Analisis konteks arsitektur dan stakeholder dari subsistem tersebut (Bab II).
-	Hubungan subsistem dengan layanan lain hanya sebatas antarmuka dan ketergantungan yang memengaruhi keputusan arsitektur.
Di luar lingkup:
-	Implementasi kode dan pengujian perangkat lunak secara menyeluruh.
-	Layanan di luar subsistem ini (misalnya keuangan dan administrasi umum kampus) serta program magang di luar skema MSIB.
- Proses internal di sisi mitra industri atau penyelenggara pusat di luar interaksi dengan subsistem ini.

1.3	Sumber Data
Data dan informasi dalam laporan ini dikumpulkan beberapa sumber.
-	Pengalaman sebagai pengguna: mencoba sendiri layanannya (SIAKAD, UMI-Kalam).
 
Hanya terdapat page yang menjelaskan Magang & Studi Independen Bersertifikat (MSIB) di Kalam UMI.


