# Tasks

## Persiapan

- [x] Siapkan environment Python (virtualenv/conda) dan pastikan dependensi, termasuk `scikit-learn==1.7.0`, sudah terpasang.
- [x] Tinjau notebook template pada folder `Codes/` untuk memahami struktur pengerjaan yang harus diikuti.
- [x] Baca ulang deskripsi proyek di `AGENT.md` dan kriteria penilaian pada `Acceptance-Criteria.md` agar seluruh langkah selaras dengan ekspektasi.

## Eksplorasi Data (Kriteria 1)

- [ ] Muat dataset `Dataset/bank-transaction-dataset.csv` dan tampilkan output `head()`, `info()`, serta `describe()`.
- [ ] Buat matriks korelasi dan interpretasi singkat terhadap relasi fitur utama.
- [ ] Visualisasikan distribusi fitur numerik dan kategorikal (histogram) dengan label yang terbaca jelas.

## Pembersihan & Pra-pemrosesan (Kriteria 2)

- [ ] Periksa nilai hilang dan duplikat menggunakan `isnull().sum()` dan `duplicated().sum()`.
- [ ] Tangani nilai hilang (drop atau imputasi) dan hapus entri duplikat jika ditemukan.
- [ ] Hapus kolom ID (`TransactionID`, `AccountID`, `DeviceID`, `IPAddress`, `MerchantID`).
- [ ] Lakukan encoding fitur kategorikal dengan `LabelEncoder` dan scaling fitur numerik menggunakan `MinMaxScaler` atau `StandardScaler`.
- [ ] Lakukan penanganan outlier (drop atau imputasi) dan, bila relevan, lakukan binning pada 1–2 fitur numerik lalu encode hasilnya.

## Pemodelan Clustering (Kriteria 3)

- [ ] Jalankan Elbow Method (`KElbowVisualizer`) untuk menentukan jumlah cluster optimal.
- [ ] Latih model K-Means pada data yang sudah diproses dan simpan menggunakan `joblib.dump(model_clustering)`.
- [ ] Hitung Silhouette Score dan visualisasikan hasil cluster untuk evaluasi awal.
- [ ] (Opsional Advanced) Bangun model PCA, bandingkan hasilnya, dan simpan dengan `joblib.dump(model, "PCA_model_clustering.h5")`.

## Interpretasi Hasil Clustering (Kriteria 4)

- [ ] Sajikan visualisasi hasil clustering dan analisis deskriptif (min, max, mean) tiap cluster.
- [ ] Jelaskan karakteristik setiap cluster berdasarkan fitur yang dominan.
- [ ] Lakukan inverse transform pada fitur yang di-scaling/encoding, lengkapi deskripsi dengan nilai mode untuk fitur kategorikal.
- [ ] Simpan dataset terklaster (pra-inverse) beserta label cluster ke `data_clustering.csv`.
- [ ] Gabungkan data yang sudah di-inverse dengan label cluster (`Target`) dan ekspor ke `data_clustering_inverse.csv`.

## Pemodelan Klasifikasi (Kriteria 5)

- [ ] Gunakan dataset berlabel (`Target`) untuk melakukan `train_test_split()`.
- [ ] Latih model Decision Tree dan simpan menggunakan `joblib.dump(decision_tree_model, "decision_tree_model.h5")`.
- [ ] Uji algoritma klasifikasi lain, tampilkan metrik akurasi, presisi, recall, dan F1-score; simpan model eksplorasi (`joblib.dump` dengan pola `explore_<algoritma>_classification`).
- [ ] (Opsional Advanced) Lakukan hyperparameter tuning pada salah satu model dan simpan hasilnya (`joblib.dump(tuning_model, "tuning_classification")`).

## Dokumentasi & Finalisasi

- [ ] Ekspor notebook clustering ke `[Clustering] Submission Akhir BMLP_username.ipynb` dan notebook klasifikasi ke `[Klasifikasi] Submission Akhir BMLP_username.ipynb`.
- [ ] Pastikan notebook mengikuti struktur template (unsupervised lalu supervised) dan seluruh sel menampilkan output yang diminta.
- [ ] Tambahkan penjelasan metode, alasan pemilihan, dan ringkasan hasil pada setiap analisis sesuai format yang disarankan.
- [ ] Verifikasi ulang semua file output (`joblib`, notebook, dan CSV) berada di lokasi yang diminta dan dapat dibaca evaluator.
- [ ] Kemasi seluruh berkas output ke `BMLP_Nama-siswa.zip` mengikuti struktur pada bagian `Ekspektasi Output` di `AGENT.md`.
- [ ] Lakukan pengecekan akhir sebelum submission (re-run notebook, bersihkan warning/error, update catatan penting).
