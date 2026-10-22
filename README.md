# Analisis Spasial Sebaran Penduduk Kabupaten Karawang

## Objektif Proyek
Proyek ini bertujuan untuk latihan memetakan dan menganalisis sebaran jumlah penduduk tingkat kecamatan di Kabupaten Karawang. Visualisasi ini dirancang untuk mengidentifikasi konsentrasi populasi sehingga dapat mengetahui daerah kecamatan mana yang memiliki jumlah penduduk terbanyak serta mengetahui pemetaan wilayah strategis.

## Hasil Peta Standar Kartografi 
!{Peta Karawang](./Jumlah Penduduk Karawang.jpeg)

## Metodologi, Alat & Tahapan Teknis
Proyek ini dikerjakan dengan tahapan pemrosesan data (*data processing workflow) sebagai berikut:

* **Perangkat Lunak:** QGIS
* **Data yang Digunakan:**
  * Data Spasial Batas Administrasi Kecamatan & Kabupaten Karawang.
  * Data Tabular Jumlah Penduduk Kabupaten Karawang.
  * Peta Dasar: OpenStreetMap dan GADM
* **Tahapan Teknis Pembuatan:**
* ### 1. Akuisisi dan Filtrasi Data Spasial
* **Skala Global ke Nasional:** Mengunduh data spasial batas administrasi resmi seluruh dunia melalui platform **GADM (Database of Global Administrative Areas)**.
* **Skala Regional (Indonesia):** Menyaring data GADM global untuk mengekstrack batas wilayah Indonesia.
* **Skala Lokasl (Karawang):** Melakukan query spasial pada level *Administrative 2 (Kabupaten) dan *Administrative 3 (Kecamatan) khusus untuk wilayah Kabupaten Karawang.
### 2. Pengumpulan Data Alfanumerik (Tabular)
* Mengunduh data **Jumlah Penduduk Kabupaten Karawang** dari dokumen resmi **BPS (Badan Pusat Statistik)** Kabupaten Karawang dalam bentuk csv.
### 3. Integrasi Data di QGIS (Data Input & Joining)
* Mengimpor komponen spasial (*Shapefile*) dan data tabular (CSV) ke dalam **QGIS**.
Melakukan **Attribut Joining** menggunakan kolom kunci (*Key Field*) yang sama (Nama Kecamatan) untuk mengintegrasikan data jumlah penduduk BPS ke dalam tabel atribut SHP GADM.
### 4 Klasifikasi dan Tata Letak (Symbology & Layouting)
* **Gradasi Warna:** Mengklasifikasikan sebaran penduduk menggunakan gradasi warna kuantitas agar perbedaan kepadatan antar kecamatan terlihat konstras dan informatif.
* **Layouting:** Menyusun elemen kartografi formal di QGIS, Print Layout desain sisi samping untuk peta, menyesuaikan skala batang, memperbaiki legenda warna klasifikasidan garis, serta menambahkan inset regional.
## Format Output
* **[Unduh File PDF Resolusi Tinggi](./PETA KEPENDUDUKAN KARAWANG.pdf)
