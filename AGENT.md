# CONTEXT

Anda adalah seorang ahli dalam bidang Data Science. Pada proyek ini, Anda akan membangun model machine learning dengan pendekatan supervised dan unsupervised learning. Anda dapat memilih dari beberapa dataset tanpa label yang kami sediakan atau mencarinya sendiri sesuai dengan preferensi masing-masing.

Langkah pertama adalah menerapkan teknik unsupervised learning, khususnya clustering, untuk menghasilkan label atau kelas pada dataset tersebut. Setelah mendapatkan label atau kelas dari proses clustering, Anda akan menggabungkan informasi ini dengan dataset asli.

Dengan dataset yang telah dilengkapi dengan label atau kelas, Anda akan menerapkan metode supervised learning, yaitu klasifikasi, untuk mengembangkan model yang mampu memprediksi kelas berdasarkan fitur yang ada. Proyek ini dirancang untuk menilai kemampuan Anda dalam mengintegrasikan kedua metode tersebut dan memecahkan masalah yang relevan dengan teknik machine learning yang telah dipelajari.

Untuk memantau progres pengerjaan, gunakan checklist pada dokumen [Tasks.md](Tasks.md).

Panduan Dataset untuk Submission Kelas
Untuk memastikan pengerjaan proyek clustering berjalan terstruktur dan sesuai standar evaluasi, peserta diwajibkan mengikuti template yang telah disediakan. Setiap langkah harus dilakukan secara sistematis dan mematuhi instruksi yang diberikan dalam template proyek. Berikut ini hal-hal yang perlu diperhatikan sebelum memulai pengerjaan projek:

- Eksekusi Notebook Disediakan pada folder `Codes/`.
- Dataset yang digunakan terdapat di file `Dataset/bank-transaction-dataset.csv`.
- Mengikuti template dalam notebook proyek sesuai struktur yang diberikan.
- Kriteria yang dapat diterima untuk pengerjaan proyek ini dapat dilihat di file `Acceptance-Criteria.md` di bagian `Criteria`. Adapun saran alur pengerjaan proyek ini dapat dilihat pada bagian `Suggested Flow` pada file `Acceptance-Criteria.md`.

![Struktur Markdown Clustering](Figures/dos-3d6b7da2729df3739319a2879bf9190120250429135517.jpeg)
Fig 1. Struktur Markdown Clustering

![Struktur Markdown Klasifikasi](Figures/dos-628a81711b46c422287030474656357620250429135517.jpeg)
Fig 2. Struktur Markdown Klasifikasi

Untuk meningkatkan kualitas dokumentasi dan memberikan pemahaman yang lebih baik terhadap proyek yang dikerjakan, peserta disarankan menambahkan penjelasan rinci pada setiap analisis dengan format berikut:

- Metode yang digunakan → Teknik atau algoritma yang diterapkan dalam tahap tersebut.
- Alasan penggunaan → Mengapa metode tersebut dipilih dan bagaimana relevansinya dengan proyek.
- Hasil yang didapat → Interpretasi hasil setelah metode diterapkan.

Ekspektasi output yang akan dihasilkan pada proyek ini adalah berpua file-file sebagai berikut:

```
BMLP_Nama-siswa.zip
├── [Clustering] Submission Akhir BMLP_username.ipynb
├── [Klasifikasi] Submission Akhir BMLP_username.ipynb
├── model_clustering.h5
├── PCA_model_clustering.h5 (Opsional)
├── decision_tree_model.h5
├── explore_<Nama Algoritma>_classification.h5 (Opsional)
├── tuning_classification.h5 (Opsional)
├── data_clustering.csv
├── data_clustering_inverse.csv (Opsional)
```
