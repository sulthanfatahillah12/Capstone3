# Capstone3

## README.md

### Prediksi Customer Churn di Perusahaan E-Commerce

Ini adalah proyek untuk membangun model Machine Learning untuk memprediksi pelanggan yang berisiko **churn** (kehilangan pelanggan) pada sebuah perusahaan e-commerce.

---

### Latar Belakang Masalah

Perusahaan e-commerce menghadapi masalah **customer churn** yang menyebabkan penurunan pendapatan dan peningkatan biaya akuisisi pelanggan baru. Saat ini, perusahaan menggunakan dua strategi yang tidak efisien:

* **Treat All**: Memberikan penawaran retensi kepada semua pelanggan, yang menyebabkan biaya membengkak karena menargetkan pelanggan yang tidak akan churn.
* **Treat None**: Tidak melakukan intervensi, yang mengakibatkan hilangnya pelanggan yang churn tanpa upaya untuk mempertahankannya.

Proyek ini bertujuan untuk mengatasi inefisiensi tersebut dengan pendekatan berbasis data.

---

### Tujuan Proyek

Tujuan utama dari proyek ini adalah untuk mengembangkan model Machine Learning yang dapat:

* Memprediksi pelanggan yang memiliki risiko tinggi untuk churn.
* Memungkinkan tim marketing untuk menargetkan upaya retensi secara lebih spesifik dan efisien.
* Mengoptimalkan penggunaan anggaran pemasaran.
* Mengurangi total biaya gabungan dari retensi dan akuisisi pelanggan.

---

### Metodologi

Proyek ini mengikuti alur kerja Data Science yang mencakup beberapa tahapan:

1.  **Data Understanding**: Memahami struktur dataset dan deskripsi fitur-fitur seperti `Tenure`, `WarehouseToHome`, `SatisfactionScore`, `MaritalStatus`, dan `CashbackAmount`.
2.  **Data Cleaning**: Menghapus data duplikat dan memeriksa *missing value* pada fitur-fitur seperti `Tenure`, `WarehouseToHome`, dan `DaySinceLastOrder`.
3.  **Modeling**: Membangun model klasifikasi untuk memprediksi probabilitas churn pelanggan.
4.  **Model Evaluation**: Menggunakan **F-3 Score** sebagai metrik evaluasi utama. Metrik ini dipilih karena model bertujuan untuk menekan False Negative (memprediksi pelanggan akan loyal, padahal sebenarnya churn) untuk mengurangi biaya akuisisi tanpa mengabaikan False Positive (memprediksi pelanggan akan churn, padahal loyal).

---

### Fitur Dataset

Dataset yang digunakan berisi informasi tentang pelanggan e-commerce dengan fitur-fitur berikut:

* `Tenure`: Lama waktu pelanggan menjadi bagian dari perusahaan.
* `WarehouseToHome`: Jarak antara gudang dan rumah pelanggan.
* `NumberOfDeviceRegistered`: Jumlah perangkat yang terdaftar.
* `PreferedOrderCat`: Kategori pesanan yang paling sering dipilih.
* `SatisfactionScore`: Skor kepuasan pelanggan.
* `MaritalStatus`: Status pernikahan pelanggan.
* `NumberOfAddress`: Jumlah alamat yang terdaftar.
* `Complaint`: Indikasi adanya keluhan.
* `DaySinceLastOrder`: Jumlah hari sejak pesanan terakhir.
* `CashbackAmount`: Rata-rata cashback dalam sebulan terakhir.
* `Churn`: Variabel target (0 = Loyal, 1 = Churn).

---

### Libraries yang Digunakan

Proyek ini dikembangkan menggunakan bahasa pemrograman Python dengan pustaka-pustaka berikut:

* `pandas`: Untuk manipulasi dan analisis data.
* `numpy`: Untuk operasi numerik.
* `matplotlib` & `seaborn`: Untuk visualisasi data.
* `scikit-learn`: Untuk pre-processing data, seleksi fitur, dan berbagai model Machine Learning (seperti `LogisticRegression`, `DecisionTreeClassifier`, `RandomForestClassifier`, dan `XGBClassifier`).
* `imblearn`: Untuk menangani ketidakseimbangan data.
