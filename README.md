# EEG Signal Classification: Interictal Epileptiform Discharges (IEDs) Detection

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange.svg)](https://scikit-learn.org/)
[![Signal Processing](https://img.shields.io/badge/Signal%20Processing-FFT-green.svg)]()

## 📌 Deskripsi Proyek
Proyek ini berfokus pada penerapan pemrosesan sinyal digital (Digital Signal Processing) dan algoritma *Machine Learning* untuk menganalisis data *time-series* yang kompleks. Secara spesifik, proyek ini mengidentifikasi gelombang *Interictal Epileptiform Discharges* (IEDs) pada rekaman *Electroencephalogram* (EEG) untuk membedakan aktivitas otak normal dan indikasi epilepsi secara otomatis. 

Alur kerja (*pipeline*) pemrosesan data dalam proyek ini dapat diadaptasi untuk berbagai masalah analisis data sensor dan *time-series* di industri lainnya.

## 🚀 Fitur Utama & Alur Kerja (*Data Pipeline*)
1. **Pra-pemrosesan Data (Data Preprocessing):** Membersihkan, memotong, dan mensegmentasi data sinyal EEG mentah ke dalam jendela waktu (interval) tertentu.
2. **Ekstraksi Fitur dengan FFT:** Mengubah data sinyal dari domain waktu (time-domain) ke domain frekuensi menggunakan rumusan matematis *Fast Fourier Transform* (FFT) untuk menemukan pola magnitudo yang tersembunyi.
3. **Reduksi Dimensi (PCA):** Menerapkan *Principal Component Analysis* (PCA) untuk mereduksi dimensi matriks fitur frekuensi yang berukuran besar menjadi 10 komponen utama (*Principal Components*) tanpa menghilangkan informasi krusial, sehingga mencegah *overfitting* dan mempercepat komputasi.
4. **Klasifikasi (K-NN):** Membangun model prediktif menggunakan algoritma *K-Nearest Neighbors* (K-NN) dengan mengoptimalkan perhitungan jarak *Euclidean* pada nilai ketetanggaan optimal (K=18).

## 🛠️ Teknologi & Perangkat (*Tech Stack*)
* **Bahasa Pemrograman:** Python
* **Data Manipulation & Math:** NumPy, Pandas, SciPy
* **Machine Learning:** Scikit-Learn
* **Data Visualization:** Matplotlib, Seaborn

## 📊 Hasil & Evaluasi Kinerja
Model ini dilatih dan diuji menggunakan dataset yang terdiri dari 230 sampel (184 data latih dan 46 data uji). Evaluasi menggunakan *Confusion Matrix* menghasilkan metrik performa berikut:
* **Akurasi Keseluruhan (Accuracy):** **91%**
* **Presisi (Precision):** 95% (Normal) | 88% (Epilepsi)
* **Recall:** 88% (Normal) | 95% (Epilepsi)

Hasil ini membuktikan bahwa kombinasi FFT dan algoritma klasifikasi dasar yang dioptimalkan mampu menghasilkan tingkat keandalan yang tinggi dalam memproses sinyal fluktuatif.

## 📂 Struktur Direktori
```text
├── data/                   # Dataset 
├── notebooks/              # Jupyter Notebook berisi eksperimen dan Exploratory Data Analysis (EDA)
└── README.md               # Dokumentasi proyek
 
