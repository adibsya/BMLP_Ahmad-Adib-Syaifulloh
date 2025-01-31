# Proyek Clustering dan Klasifikasi Pelanggan

## 📚 **Deskripsi Proyek**
Proyek ini bertujuan untuk mengelompokkan pelanggan ke dalam beberapa cluster berdasarkan karakteristik mereka menggunakan *unsupervised learning* (clustering) dan membangun model klasifikasi untuk memprediksi cluster pelanggan berdasarkan fitur yang tersedia menggunakan *supervised learning*. Dataset yang digunakan adalah `Customers.csv`, yang berisi informasi seperti usia, pendapatan tahunan, skor pengeluaran, dan lainnya.

---

## 🔍 **Langkah-Langkah Proyek**

### **1. Clustering (Unsupervised Learning)**
- **Algoritma:** K-Means
- **Tujuan:** Mengelompokkan pelanggan ke dalam beberapa cluster berdasarkan pola data.
- **Evaluasi:** 
  - Metode Elbow digunakan untuk menentukan jumlah cluster optimal.
  - Silhouette Score dihitung untuk mengevaluasi kualitas clustering.
- **Hasil:** Dataset berhasil dikelompokkan ke dalam beberapa cluster, memberikan wawasan tentang segmen pelanggan.

### **2. Klasifikasi (Supervised Learning)**
- **Algoritma:**
  - Logistic Regression
  - Random Forest
- **Tujuan:** Membangun model klasifikasi untuk memprediksi cluster pelanggan berdasarkan fitur yang tersedia.
- **Evaluasi:**
  - Akurasi dan F1-Score digunakan untuk mengukur performa model.
  - Confusion matrix dibuat untuk menganalisis kesalahan prediksi.
- **Hasil:** Model mampu memprediksi cluster pelanggan dengan performa yang baik.

---

## 📁 **Struktur Repository**
Berikut adalah struktur file dalam proyek ini:
- `Clustering_Proses.ipynb`: Notebook Python untuk proses clustering.
- `Klasifikasi_Proses.ipynb`: Notebook Python untuk proses klasifikasi.
- `Customers.csv`: Dataset awal yang digunakan dalam proyek.
- `Customers_with_Clusters.csv`: Dataset hasil clustering dengan label cluster baru.
- `Output_Prediksi.csv`: Hasil prediksi klasifikasi, memuat label prediksi untuk data uji.

---

## 📊 **Evaluasi Model**

### **Clustering**
- **Algoritma:** K-Means
- **Jumlah Cluster Optimal:** Ditentukan menggunakan metode Elbow dan Silhouette Score.
- **Silhouette Score:** Memberikan gambaran kualitas clustering.

### **Klasifikasi**
- **Model yang Digunakan:**
  - Logistic Regression
  - Random Forest
- **Metrik Evaluasi:**
  - Akurasi dan F1-Score menunjukkan performa model yang sangat baik pada data uji.
  - Confusion matrix membantu menganalisis kesalahan prediksi (jika ada).

---

## ✨ **Langkah-Langkah Utama**

1. **Memahami Dataset**: Mengeksplorasi dataset awal (`Customers.csv`) untuk memahami struktur data dan distribusinya.
2. **Preprocessing Data**:
   - Encoding fitur kategorikal seperti *Gender* dan *Profession* menggunakan Label Encoding.
   - Normalisasi data numerik menggunakan StandardScaler agar memiliki skala yang seragam.
3. **Clustering dengan K-Means**:
   - Menentukan jumlah cluster optimal menggunakan metode Elbow dan Silhouette Score.
   - Melakukan clustering dan menambahkan label cluster ke dataset asli.
4. **Klasifikasi Cluster**:
   - Membagi data menjadi training set dan test set.
   - Melatih model Logistic Regression dan Random Forest menggunakan data latih.
   - Mengevaluasi performa model pada data uji.
5. **Visualisasi Hasil**:
   - Menggunakan PCA untuk mereduksi dimensi data dan memvisualisasikan hasil clustering dalam dua dimensi.
6. **Menyimpan Hasil**:
   - Menyimpan dataset dengan label cluster baru ke file `Customers_with_Clusters.csv`.
   - Menyimpan hasil prediksi klasifikasi ke file `Output_Prediksi.csv`.

---

## 💡 **Rekomendasi Tindakan Lanjutan**
Berdasarkan hasil evaluasi:
1. Jika precision atau recall rendah pada kelas tertentu, pertimbangkan untuk menyeimbangkan dataset menggunakan teknik seperti SMOTE atau oversampling.
2. Jika model mengalami overfitting, lakukan tuning hyperparameter lebih lanjut atau gunakan algoritma lain seperti Gradient Boosting (XGBoost, LightGBM).
3. Tambahkan lebih banyak data jika performa model belum memuaskan, terutama untuk kelas minoritas.

---

## ✨ **Kontributor**
Proyek ini dikembangkan oleh:
- Nama: Ahmad Adib Syaifulloh
- Email: ahmadadibsyaifulloh@gmail.com
- Username Dicoding : adib_syaa

---

## 🛠️ **Cara Menjalankan Proyek**
1. Pastikan Anda memiliki Python 3.x terinstal di komputer Anda.
2. Instal pustaka yang diperlukan dengan menjalankan perintah berikut:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn
   ```
3. Jalankan notebook Python (`Clustering_Proses.ipynb` dan `Klasifikasi_Proses.ipynb`) secara berurutan untuk melakukan clustering dan klasifikasi.
4. Hasil clustering akan disimpan di file `Customers_with_Clusters.csv`, sedangkan hasil prediksi klasifikasi akan disimpan di file `Output_Prediksi.csv`.

---

## 📂 **Referensi Dataset**
Dataset yang digunakan dalam proyek ini adalah `Customers.csv`, yang berisi informasi tentang pelanggan seperti usia, pendapatan tahunan, skor pengeluaran, pekerjaan, pengalaman kerja, dan ukuran keluarga.

--- 

Proyek ini dirancang untuk memberikan wawasan tentang bagaimana mengintegrasikan metode unsupervised learning (clustering) dengan supervised learning (klasifikasi) dalam analisis data pelanggan.
