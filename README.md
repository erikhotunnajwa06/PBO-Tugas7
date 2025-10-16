# Deskripsi
Tugas instalasi iReport dan pembuatan fitur cetak laporan pada proyek CRUD di NetBeans
# Instalasi iReport
iReport dipakai sebagai ekstensi desain JasperReports di dalam IDE dan Report Wizard dimanfaatkan untuk membangkitkan berkas .jrxml berbasis template, lengkap dengan koneksi JDBC dan kueri SQL.  Instalasi dilakukan melalui Tools → Plugins dengan paket iReport 5.6.0 dan dependensi org-jdesktop-layout, kemudian IDE direstart dan empat modul Jasper divalidasi aktif. 
# Pembuatan Laporan
Pembuatan laporan mengikuti urutan: New → Report Wizard, pilih template, tetapkan koneksi Database JDBC, isi JDBC URL, kredensial, susun Query SELECT * FROM <namatabel>, pilih kolom, lalu Finish; desain dapat disunting dan dipratinjau untuk verifikasi tampilan data.  

Integrasi ke aplikasi dilakukan dengan menambahkan tombol CETAK pada JFrame, menyertakan kode pemanggilan berkas .jasper beserta impor dan library yang diperlukan, kemudian menjalankan aplikasi, mengisi data, dan mengeksekusi tombol untuk menampilkan hasil laporan.
# Catatan
iReport Plugin di NetBeans adalah ekstensi untuk merancang dan mengelola laporan JasperReports langsung dari IDE. Plugin ini menambah editor desain laporan (.jrxml), fitur pratinjau, serta integrasi pustaka JasperReports sehingga laporan dapat dipanggil dari aplikasi Java/CRUD tanpa alat eksternal. 

Report Wizard adalah utilitas pembuat laporan berbasis template. Alur dasarnya: pilih template, tetapkan koneksi JDBC, tulis kueri SQL, pilih kolom, lalu hasilkan berkas .jrxml siap sunting dan pratinjau. Wizard mempercepat pembuatan laporan standar seperti tabel data, daftar, atau ringkasan.

Dalam konteks proyek CRUD, laporan digunakan untuk “Cetak” data dari tabel yang sama dengan operasi create–read–update–delete. Tombol Cetak pada JFrame memanggil file .jasper hasil kompilasi .jrxml dan memasok parameter atau ResultSet dari koneksi database.

Komponen pendukung yang perlu aktif di NetBeans meliputi ireport-designer, jasperreports-extensions, jasperreports-components, dan jasperserver-plugin. Instalasi dilakukan via Tools → Plugins → Downloaded, lalu restart IDE agar modul aktif.
