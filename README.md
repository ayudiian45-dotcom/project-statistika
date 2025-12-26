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

> Variabel-variabel utama dalam dataset ini meliputi pendapatan tahunan, jumlah pelanggan, nilai pelanggan, dan tingkat churn. Variabel pendapatan dan jumlah pelanggan digunakan untuk menggambarkan performa bisnis startup, sementara nilai pelanggan dan tingkat churn mencerminkan loyalitas serta kualitas hubungan startup dengan pelanggannya.

> Tujuan dari proyek ini adalah untuk memahami karakteristik data startup SaaS melalui analisis statistik deskriptif, menganalisis hubungan antara pendapatan tahunan dan jumlah pelanggan menggunakan analisis korelasi, serta memprediksi tingkat churn pelanggan berdasarkan variabel nilai pelanggan melalui analisis regresi. Hasil analisis diharapkan dapat memberikan gambaran mengenai faktor-faktor yang memengaruhi kinerja dan keberlanjutan startup SaaS.

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
    > Berdasarkan hasil analisis pada variabel Pendapatan_Tahunan_Miliar_IDR, diperoleh nilai mean sebesar 31,88, median sebesar 31,31, dan modus sebesar 1,87.

  - *Interpretasi:* Jelaskan apa arti dari nilai-nilai tersebut terkait dengan data Anda.
    > Nilai mean menunjukkan bahwa rata-rata pendapatan tahunan startup berada di sekitar 31,88 miliar rupiah. Nilai median yang hampir sama dengan mean menandakan bahwa sebaran data pendapatan relatif seimbang dan tidak terlalu condong ke salah satu sisi. Sementara itu, nilai modus yang lebih kecil menunjukkan bahwa pendapatan dengan nilai rendah cukup sering muncul dalam dataset, meskipun secara keseluruhan terdapat banyak startup dengan pendapatan yang lebih tinggi.

    > Secara umum, dapat disimpulkan bahwa sebagian besar startup memiliki pendapatan di kisaran menengah, dengan variasi pendapatan dari yang rendah hingga tinggi, seperti yang terlihat pada histogram.

- **Ukuran Sebaran (Standar Deviasi, Range, Kuartil):**
  - *Tabel atau ringkasan...*
    > "Standar Deviasi dari Pendapatan_Tahunan_Miliar_IDR : 19.79"
    > "Range dari Pendapatan_Tahunan_Miliar_IDR : 1 - 66.89 = 65.89"
    > "Ringkasan 5 Angka untuk Pendapatan_Tahunan_Miliar_IDR :"
    >  Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    >  1.00   14.31   31.30   31.88   49.04   66.89 
  - *Interpretasi:* Jelaskan seberapa menyebar data Anda berdasarkan nilai-nilai ini.
    > Standar Deviasi = 19,79.
    > Nilai standar deviasi sebesar 19,79 menunjukkan bahwa data pendapatan tahunan cukup menyebar dari nilai rata-ratanya (mean = 31,88). Artinya, pendapatan tiap data tidak terlalu berdekatan, melainkan memiliki variasi yang cukup besar antar perusahaan/objek yang diamati.
    > Range (Jangkauan Data).Range dihitung dari selisih nilai maksimum dan minimum:
    > Range = 66,89 − 1,00 = 65,89
    > Nilai range yang besar (65,89) menunjukkan bahwa terdapat perbedaan pendapatan yang sangat jauh antara data terendah dan data tertinggi. Ini menandakan penyebaran data yang luas.
    > Ringkasan 5 Angka (Five-Number Summary)
    > Minimum (1,00) → Pendapatan terendah dalam data
    > Kuartil 1 / Q1 (14,31) → 25% data berada di bawah nilai ini
    > Median (31,30) → Nilai tengah data
    > Kuartil 3 / Q3 (49,04) → 75% data berada di bawah nilai ini
    > Maksimum (66,89) → Pendapatan tertinggi dalam data
    > Selisih antara Q1 dan Q3 cukup besar, yang menunjukkan bahwa 50% data tengah juga cukup menyebar, bukan terkonsentrasi pada satu nilai tertentu.
    > Data Pendapatan_Tahunan_Miliar_IDR memiliki penyebaran yang cukup besar. Hal ini terlihat dari nilai standar deviasi sebesar 19,79 dan range sebesar 65,89 yang menunjukkan adanya perbedaan pendapatan yang cukup jauh antara nilai terendah dan tertinggi. Selain itu, ringkasan lima angka menunjukkan bahwa data tidak terkonsentrasi pada satu nilai tertentu, sehingga variasi pendapatan antar data tergolong tinggi.
    
- **Visualisasi (Histogram/Boxplot):**
  - *Sematkan gambar plot dari folder /results...*
    ![alt text](results/histogram_Pendapatan_Tahunan_Miliar_IDR.png)
    ![alt text](results/boxplot_Pendapatan_Tahunan_Miliar_IDR.png)
  - *Interpretasi:* Jelaskan wawasan apa yang Anda dapatkan dari bentuk distribusi data.
    > Berdasarkan histogram Pendapatan_Tahunan_Miliar_IDR, terlihat bahwa data menyebar cukup merata di seluruh rentang nilai. Nilai mean (31,88) dan median (31,30) yang hampir sama menunjukkan bahwa distribusi data cenderung simetris dan tidak condong ke salah satu sisi. Hal ini sesuai dengan bentuk histogram yang tidak memperlihatkan kemiringan yang ekstrem.
   > Selain itu, nilai standar deviasi sebesar 19,79 menunjukkan bahwa meskipun pusat data berada di sekitar 31 miliar IDR, penyebaran data dari nilai tersebut cukup besar. Kondisi ini terlihat pada histogram yang menunjukkan data tersebar dari pendapatan rendah hingga tinggi. Dengan demikian, distribusi data dapat dikatakan seimbang, namun memiliki variasi pendapatan yang relatif tinggi.

### 5.2. Uji Normalitas
- **Hasil Uji Shapiro-Wilk:**
  - *Nilai p-value...*
    > "--- Hasil Uji Normalitas Shapiro-Wilk ---"

     >      Shapiro-Wilk normality test

>     data:  data_bersih[[kolom_uji]]
>     W = 0.94664, p-value = 1.497e-14
  - *Interpretasi:* Apakah data Anda terdistribusi normal berdasarkan hasil uji? Apa implikasinya?
    > "Interpretasi: p-value = 0 <= 0.05. Data kemungkinan besar TIDAK terdistribusi normal."
    > Hasil uji Shapiro–Wilk menunjukkan bahwa data tidak terdistribusi normal, sehingga pemilihan metode analisis statistik selanjutnya perlu disesuaikan agar hasil yang diperoleh tetap valid dan dapat dipertanggungjawabkan.
- **Plot Q-Q:**
  - *Sematkan gambar plot dari folder /results...*
    > 
  - *Interpretasi:* Apakah titik-titik data mengikuti garis lurus? Apa artinya?
    > Berdasarkan Q–Q Plot untuk variabel Pendapatan_Tahunan_Miliar_IDR, terlihat bahwa titik-titik data tidak sepenuhnya mengikuti garis lurus (garis diagonal merah). Pada bagian tengah, beberapa titik masih relatif mendekati garis, namun pada bagian kuantil rendah dan kuantil tinggi terlihat penyimpangan yang cukup jelas.
    > Pola titik yang melengkung (tidak linear) menunjukkan bahwa distribusi data menyimpang dari distribusi normal. Penyimpangan ini menandakan bahwa data memiliki bentuk distribusi yang tidak simetris atau memiliki ekor yang berbeda dari distribusi normal.

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
