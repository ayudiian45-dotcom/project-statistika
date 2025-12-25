# Tugas Analisis Statistik: Deskriptif, Korelasi, dan Regresi

## 1. Informasi Penyusun

- **Nama:** Putu Ayu Dian Melani
- **NIM:** 2515091060
- **Program Studi:** Sistem Informasi
- **Mata Kuliah:** Statistika dan Probabilitas

---
         
## 2. Deskripsi Proyek

Pada bagian ini, jelaskan secara singkat dataset yang Anda gunakan. Apa saja variabel di dalamnya? Apa tujuan dari analisis yang Anda lakukan?


> Dataset yang digunakan dalam proyek ini merupakan data data_startup_saas. Data startup Software as a Service (SaaS) yang berisi informasi kinerja dan karakteristik beberapa startup di berbagai kategori layanan. Dataset ini mencakup data mengenai nama startup, jenis atau kategori layanan yang ditawarkan, pendapatan tahunan dalam miliar rupiah, jumlah pelanggan, nilai pelanggan dalam satuan juta rupiah, serta tingkat churn pelanggan dalam persentase.

Variabel-variabel utama dalam dataset ini meliputi pendapatan tahunan, jumlah pelanggan, nilai pelanggan, dan tingkat churn. Variabel pendapatan dan jumlah pelanggan digunakan untuk menggambarkan performa bisnis startup, sementara nilai pelanggan dan tingkat churn mencerminkan loyalitas serta kualitas hubungan startup dengan pelanggannya.

Tujuan dari proyek ini adalah untuk memahami karakteristik data startup SaaS melalui analisis statistik deskriptif, menganalisis hubungan antara pendapatan tahunan dan jumlah pelanggan menggunakan analisis korelasi, serta memprediksi tingkat churn pelanggan berdasarkan variabel nilai pelanggan melalui analisis regresi. Hasil analisis diharapkan dapat memberikan gambaran mengenai faktor-faktor yang memengaruhi kinerja dan keberlanjutan startup SaaS.

---

## 3. Struktur Proyek

Proyek ini diorganisir ke dalam beberapa folder:
- `/data`: Berisi dataset mentah yang digunakan untuk analisis.
- `/scripts`: Berisi semua skrip R yang digunakan dalam analisis, diurutkan berdasarkan alur kerja.
- `/results`: Berisi output dari analisis, seperti plot, gambar, atau tabel ringkasan.

---

## 4. Cara Menjalankan Analisis

Untuk mereproduksi hasil analisis ini, ikuti langkah-langkah berikut:
1. Pastikan Anda memiliki R dan RStudio terinstal.
2. Buka proyek R ini di RStudio.
3. Instal paket yang diperlukan dengan menjalankan perintah berikut di konsol R:
   ```R
   # install.packages(c("tidyverse", "corrplot", "knitr"))
   ```
4. Jalankan skrip di dalam folder `/scripts` secara berurutan, mulai dari `01_data_preparation.R` hingga `05_analisis_regresi.R`.

---

## 5. Hasil dan Interpretasi

Di bagian ini, mahasiswa diharapkan untuk menyajikan dan menginterpretasikan hasil dari setiap tahap analisis.

### 5.1. Statistik Deskriptif
- **Ukuran Pemusatan (Mean, Median, Modus):**
  - *Tabel atau ringkasan*
    >Berdasarkan hasil analisis pada variabel Pendapatan_Tahunan_Miliar_IDR, diperoleh nilai mean sebesar 31,88, median sebesar 31,31, dan modus sebesar 1,87.

  - *Interpretasi:* Jelaskan apa arti dari nilai-nilai tersebut terkait dengan data Anda.
    > Nilai mean menunjukkan bahwa rata-rata pendapatan tahunan startup berada di sekitar 31,88 miliar rupiah. Nilai median yang hampir sama dengan mean menandakan bahwa sebaran data pendapatan relatif seimbang dan tidak terlalu condong ke salah satu sisi. Sementara itu, nilai modus yang lebih kecil menunjukkan bahwa pendapatan dengan nilai rendah cukup sering muncul dalam dataset, meskipun secara keseluruhan terdapat banyak startup dengan pendapatan yang lebih tinggi.

Secara umum, dapat disimpulkan bahwa sebagian besar startup memiliki pendapatan di kisaran menengah, dengan variasi pendapatan dari yang rendah hingga tinggi, seperti yang terlihat pada histogram.

- **Ukuran Sebaran (Standar Deviasi, Range, Kuartil):**
  - *Tabel atau ringkasan...*
  - *Interpretasi:* Jelaskan seberapa menyebar data Anda berdasarkan nilai-nilai ini.
- **Visualisasi (Histogram/Boxplot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Jelaskan wawasan apa yang Anda dapatkan dari bentuk distribusi data.

### 5.2. Uji Normalitas
- **Hasil Uji Shapiro-Wilk:**
  - *Nilai p-value...*
  - *Interpretasi:* Apakah data Anda terdistribusi normal berdasarkan hasil uji? Apa implikasinya?
- **Plot Q-Q:**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah titik-titik data mengikuti garis lurus? Apa artinya?

### 5.3. Analisis Korelasi
- **Nilai Koefisien Korelasi:**
  - *Nilai r...*
  - *Interpretasi:* Seberapa kuat dan apa arah hubungan antara dua variabel yang Anda uji? (misalnya, korelasi positif kuat, negatif lemah, atau tidak ada korelasi).
- **Visualisasi (Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah pola pada scatter plot mendukung hasil koefisien korelasi?

### 5.4. Analisis Regresi
- **Model Regresi:**
  - *Persamaan regresi: Y = b0 + b1*X*
  - *Interpretasi:* Jelaskan arti dari koefisien intercept (b0) dan slope (b1) dalam konteks data Anda.
- **Evaluasi Model (R-squared):**
  - *Nilai R-squared...*
  - *Interpretasi:* Berapa persen variasi dari variabel dependen yang dapat dijelaskan oleh model regresi Anda?
- **Visualisasi (Garis Regresi pada Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Jelaskan bagaimana garis regresi merepresentasikan hubungan antara variabel.

---

## 6. Kesimpulan

Rangkum temuan utama dari analisis Anda dalam beberapa kalimat. Apa wawasan paling penting yang Anda peroleh?
