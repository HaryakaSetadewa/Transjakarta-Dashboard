# Transjakarta 2024 Service Coverage Dashboard

Analisis Spasial Distribusi Halte Bus dan Aksesibilitas Layanan Transjakarta di Jakarta

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat\&logo=powerbi\&logoColor=black)
![ArcGIS](https://img.shields.io/badge/ArcGIS-2C7AC3?style=flat\&logo=arcgis\&logoColor=white)

---

## Tentang Project

Project ini lahir dari ketertarikan saya terhadap isu aksesibilitas transportasi publik di Jakarta. Sebagai kota metropolitan dengan populasi yang sangat padat, pertanyaan yang saya ingin jawab bukan sekadar *"berapa banyak halte yang ada?"*, melainkan *"apakah halte-halte tersebut benar-benar bisa dijangkau oleh warga?"*

Dengan menggabungkan **analisis spasial di ArcGIS** dan **visualisasi interaktif di Power BI**, saya membangun dashboard yang tidak hanya menampilkan angka, tetapi menceritakan realita ketimpangan akses transportasi antar wilayah di Jakarta.

---

## Objective

* **Coverage Mapping:** Memetakan seberapa luas cakupan layanan Transjakarta di tingkat kelurahan secara spasial.
* **Accessibility Measurement:** Mengukur akses nyata warga berdasarkan jarak berjalan kaki ke halte terdekat.
* **Gap Identification:** Mengidentifikasi kelurahan dengan aksesibilitas kritis yang membutuhkan intervensi prioritas.
* **Strategic Recommendation:** Menyusun rekomendasi berbasis data untuk peningkatan layanan Mikrotrans dan integrasi TOD.

---

## Skills \& Tech Stack

|Tool|Fungsi|
|-|-|
|**ArcGIS**|Pemrosesan data geospasial, kalkulasi walking distance ke halte terdekat, dan analisis service area buffer 500m|
|**Power BI Desktop**|Pembuatan dashboard interaktif dengan Shape Map, conditional formatting, dan DAX measures|
|**DAX**|Kalkulasi coverage rate per kelurahan, segmentasi kategori akses, dan dynamic KPI metrics|

---

## Alur Kerja: Dari Data Spasial ke Dashboard

Saya tidak hanya mengimpor data mentah ke Power BI. Ada proses analisis spasial yang menjadi fondasi dari seluruh visualisasi ini:

**1. Spatial Processing di ArcGIS**
Data titik lokasi halte Transjakarta diproses untuk menghasilkan dua output utama:

* **Coverage Rate per kelurahan** — persentase area kelurahan yang berada dalam radius layanan halte
* **Walking Distance per kelurahan** — jarak berjalan kaki dari centroid kelurahan ke halte terdekat

**2. Data Integration ke Power BI**
Hasil output spasial dari ArcGIS digabungkan dengan data administrasi kelurahan Jakarta, kemudian dimuat ke Power BI untuk divisualisasikan.

**3. Dashboard Development**
Dua halaman dashboard dibangun dengan pendekatan *clean design* — mengutamakan keterbacaan data tanpa elemen visual yang berlebihan.

---

## Dashboard Pages

### Page 1 — Overview

Memberikan gambaran makro distribusi layanan Transjakarta di seluruh Jakarta.

<img width="1274" height="715" alt="image" src="https://github.com/user-attachments/assets/89f20627-29bb-4629-9e02-51ee915c3cb1" />


**Summary**
Halaman ini berfungsi sebagai *service pulse* jaringan Transjakarta, menjawab pertanyaan mendasar: apakah distribusi 258 halte yang ada sudah mencerminkan pemerataan layanan, ataukah masih terpusat di area tertentu saja?

**Visual \& KPI:**

* **4 KPI Cards** — Total Bus Stops, Total Villages, Avg Coverage Rate, Low Coverage Villages
* **Choropleth Map** — Peta Jakarta dengan gradasi warna coverage rate per kelurahan (0%–100%)
* **Donut Chart** — Distribusi proporsi kelurahan berdasarkan kategori coverage (Low / Medium / High)
* **Bar Chart** — Coverage rate per kecamatan, disusun dari tertinggi ke terendah
* **Stat Cards** — Key findings dan strategic goals dalam format visual yang ringkas

**Key Findings:**

* **82%** kelurahan masih berada di kategori coverage rendah hingga sedang
* Distribusi halte sangat terkonsentrasi di pusat kota, menciptakan ketimpangan spasial yang signifikan
* Rata-rata coverage rate hanya **25.09%** — jauh di bawah target minimum 40%

---

### Page 2 — Accessibility \& Walking Analysis

Mengukur aksesibilitas *real* warga berdasarkan jarak berjalan kaki ke halte terdekat.

<img width="1278" height="719" alt="image" src="https://github.com/user-attachments/assets/2d0b66fc-a232-4ccc-86a5-61d90bddfce3" />


**Summary**
Coverage rate menunjukkan seberapa luas area yang terlayani, tetapi tidak menjawab pertanyaan yang lebih penting: *seberapa jauh warga harus berjalan untuk sampai ke halte?* Halaman ini hadir untuk menjawab gap tersebut.

**Visual \& KPI:**

* **3 KPI Cards** — Avg Walking Distance, Max Walking Distance, % Villages Beyond 500m
* **Histogram** — Distribusi walking distance seluruh kelurahan dengan penanda threshold 500m
* **Bar Chart** — Top kelurahan dengan akses terburuk (jarak berjalan kaki terpanjang)
* **Shape Map** — Peta Jakarta dengan warna berdasarkan kategori aksesibilitas

**Kategori Aksesibilitas:**

|Kategori|Jarak|Keterangan|
|-|-|-|
|Accessible|≤ 500m|Dalam jangkauan nyaman|
|Moderate|500m – 1km|Masih terjangkau namun perlu perhatian|
|Not Accessible|> 1km|Membutuhkan intervensi prioritas|

---

## Key Insights \& Rekomendasi

Berdasarkan analisis spasial yang telah dilakukan, berikut temuan dan rekomendasi strategis yang dihasilkan:

**1. Coverage ≠ Accessibility**
Angka coverage rate yang tinggi di suatu kecamatan tidak selalu berarti warga dapat dengan mudah mengakses halte. Beberapa kelurahan memiliki coverage rate sedang namun walking distance yang sangat jauh — menunjukkan bahwa halte yang ada tidak terdistribusi secara optimal di dalam wilayah tersebut.

**2. Ketimpangan Spasial yang Sistematis**
Kelurahan-kelurahan di pinggiran Jakarta secara konsisten menunjukkan coverage rendah sekaligus walking distance yang tinggi. Ini bukan anomali, melainkan pola yang perlu ditangani secara struktural.

**3. Prioritas Intervensi**
Kelurahan dengan coverage di bawah **10%** dan walking distance di atas **1km** seharusnya menjadi prioritas utama ekspansi rute Mikrotrans — bukan wilayah yang sudah memiliki akses baik.

**4. Potensi TOD**
Kelurahan dengan kepadatan tinggi namun aksesibilitas rendah adalah kandidat ideal untuk pengembangan integrasi *first/last-mile* berbasis Transit-Oriented Development.

---

## Author

**Putu Haryaka Seta Dewa**

* GitHub: [@HaryakaSetadewa](https://github.com/HaryakaSetadewa)

