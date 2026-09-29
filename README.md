# Stroke Prediction - Logistic Regression

## Deskripsi

Proyek machine learning untuk memprediksi kemungkinan terjadinya stroke menggunakan metode **Logistic Regression**.

Dataset yang digunakan adalah **Stroke Prediction Dataset** yang berisi informasi mengenai karakteristik pasien seperti usia, hipertensi, penyakit jantung, kadar glukosa, BMI, status merokok, dan beberapa variabel kategorikal lainnya.

## Tujuan

Membangun model klasifikasi menggunakan Logistic Regression untuk memprediksi apakah seorang pasien mengalami stroke atau tidak.

## Dataset

Dataset terdiri dari **5.110 data dengan 12 variabel**.

Target:

- `stroke = 0` → tidak mengalami stroke
- `stroke = 1` → mengalami stroke

Beberapa variabel prediktor:

- `age`
- `gender`
- `hypertension`
- `heart_disease`
- `ever_married`
- `work_type`
- `Residence_type`
- `avg_glucose_level`
- `bmi`
- `smoking_status`

## Proses Analisis

### 1. Exploratory Data Analysis

- Melihat struktur dan tipe data
- Statistik deskriptif
- Melihat distribusi variabel
- Memeriksa distribusi target
- Memeriksa outlier

### 2. Data Cleaning

- Menangani missing value pada `bmi` menggunakan median
- Memeriksa data duplikat
- Memeriksa tipe data
- Memeriksa kategori pada variabel kategorikal

### 3. Preprocessing

- Encoding variabel kategorikal
- Standardisasi variabel numerik menggunakan `StandardScaler`
- Membagi data menjadi training dan testing
- Menggunakan `stratify` untuk mempertahankan proporsi kelas

### 4. Modeling

Model yang digunakan:

**Logistic Regression**

Karena jumlah data antara kelas `stroke = 0` dan `stroke = 1` tidak seimbang, model menggunakan:

```python
class_weight='balanced'