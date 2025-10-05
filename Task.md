# Checklist Proyek Machine Learning Pemula

## Persiapan Awal
- [ ] Baca template notebook pada folder `Codes/` dan pahami struktur yang harus diikuti.
- [ ] Pastikan dataset `Dataset/bank-transaction-dataset.csv` siap digunakan dan periksa ukuran serta konsistensinya.
- [ ] Tetapkan catatan dokumentasi: jelaskan setiap analisis dengan format *Metode → Alasan → Hasil*.

## Tahap Clustering (Unsupervised Learning)

### 1. Exploratory Data Analysis (EDA)
- [ ] Load dataset dan tampilkan `head()`, `info()`, serta `describe()`.
- [ ] Visualisasikan matriks korelasi dan interpretasi awal hubungan fitur numerik.
- [ ] Plot histogram untuk seluruh fitur numerik dan kategorikal; pastikan label tidak saling tumpang tindih.

### 2. Pembersihan & Pra-pemrosesan Data
- [ ] Cek nilai hilang dengan `isnull().sum()` dan duplikasi dengan `duplicated().sum()`.
- [ ] Tangani nilai hilang (mis. `dropna()` atau `fillna()`) dan hapus duplikat (`drop_duplicates()`).
- [ ] Drop kolom ID: `TransactionID`, `AccountID`, `DeviceID`, `IPAddress`, `MerchantID`.
- [ ] Lakukan encoding fitur kategorikal (mis. `LabelEncoder`) dan scaling fitur numerik (`StandardScaler` atau `MinMaxScaler`).
- [ ] Tangani outlier (drop atau imputasi) dan lakukan binning pada 1–2 fitur numerik lalu encode hasil binning.

### 3. Pemodelan Clustering
- [ ] Gunakan dataset hasil pra-pemrosesan sebagai input.
- [ ] Jalankan Elbow Method melalui `KElbowVisualizer()` untuk menentukan jumlah cluster optimal.
- [ ] Latih model `KMeans` dengan jumlah cluster terpilih.
- [ ] Hitung dan tampilkan nilai Silhouette Score.
- [ ] Visualisasikan hasil clustering (mis. scatter plot atau pair plot).
- [ ] Simpan model dengan `joblib.dump(model_kmeans, "model_clustering")`.
- [ ] (Opsional) Bangun model berbasis PCA dan simpan sebagai `PCA_model_clustering.h5`.

### 4. Interpretasi Hasil Clustering
- [ ] Tambahkan label cluster ke dataset dan ekspor kolom target sebagai `Target`.
- [ ] Analisis karakteristik tiap cluster: minimal mean, min, max (plus mode untuk fitur kategorikal jika inverse dilakukan).
- [ ] Lakukan `inverse_transform()` pada fitur yang di-encode/scale, kemudian interpretasi ulang berdasarkan nilai asli.
- [ ] Integrasikan data inverse dengan kolom `Target` dan simpan sebagai `data_clustering_inverse.csv` bila diperlukan.

## Tahap Klasifikasi (Supervised Learning)

### 5. Persiapan Dataset Klasifikasi
- [ ] Gunakan dataset hasil clustering (kolom target `Target`), atau `data_clustering_inverse.csv` bila tersedia.
- [ ] Bagi data dengan `train_test_split()`; dokumentasikan proporsi dan random state.

### 6. Pemodelan & Evaluasi
- [ ] Latih model `DecisionTreeClassifier` dan simpan dengan `joblib.dump(decision_tree_model, "decision_tree_model.h5")`.
- [ ] Evaluasi model minimal menggunakan akurasi, precision, recall, dan F1-score.
- [ ] Eksperimen dengan ≥1 algoritma klasifikasi lain; simpan tiap model dengan pola nama `explore_<Algoritma>_classification`.
- [ ] Lakukan hyperparameter tuning pada salah satu model dan simpan sebagai `tuning_classification`.

## Dokumentasi & Finalisasi
- [ ] Ringkas temuan utama dari tahap clustering dan klasifikasi, kaitkan dengan tujuan bisnis/proyek.
- [ ] Laporkan kendala, asumsi, dan rekomendasi perbaikan data/model.
- [ ] Verifikasi ulang seluruh sel notebook berjalan tanpa error dan output sesuai kriteria.
- [ ] Siapkan artefak untuk submission: notebook final, file model `.h5`, dan dataset hasil inverse bila diminta.
