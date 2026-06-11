# DataMining-SalesFootwear

Implementasi teknik data mining pada dataset **Global Sports Footwear Sales (2018–2026)** menggunakan framework **CRISP-DM**. Penelitian ini mencakup tiga domain analisis: Association Rule Mining, Classification, dan Clustering.

**Kelompok 3 | Data Warehousing & Data Mining | Universitas Bunda Mulia | Semester 4 2025/2026**

---

## Dataset

| Atribut | Detail |
|---------|--------|
| Sumber | Kaggle — [Sports Footwear Sales & Consumer Behavior](https://www.kaggle.com/datasets/aliiihussain/sports-footwear-sales-and-consumer-behavior) |
| Ukuran | 30.000 baris, 18 kolom |
| Periode | 2018–2026 |
| Target | `customer_income_level` (High / Medium / Low) |

> Dataset tidak disertakan dalam repository. Unduh langsung dari link Kaggle di atas, lalu upload ke sesi Google Colab sebelum menjalankan notebook.

---

## Struktur Repository

```
DataMining-SalesFootwear/
├── README.md
├── Collection & Exploratory Data ENG.ipynb
├── Association Rule Mining ENG.ipynb
├── Classification ENG.ipynb
└── Clustering ENG.ipynb
```

Jalankan notebook sesuai urutan di atas.

---

## Metode dan Algoritma

| Domain | Algoritma | Library |
|--------|-----------|---------|
| Association Rule Mining | Apriori | `mlxtend` |
| Classification | Decision Tree, Random Forest | `scikit-learn` |
| Clustering | K-Means, DBSCAN | `scikit-learn` |
| Evaluasi Klasifikasi | Stratified K-Fold CV (k=5) | `scikit-learn` |
| Framework Metodologi | CRISP-DM | — |

---

## Ringkasan Hasil

| Metode | Metrik Utama | Nilai |
|--------|-------------|-------|
| Apriori | Jumlah rules / Lift maksimum | 270 rules / 1,0761 |
| Decision Tree | Accuracy / AUC | 33,12% / 0,4979 |
| Random Forest | Accuracy / F1-macro | 34,03% / 0,3361 |
| K-Means (K=3) | Silhouette Score / DBI | 0,2390 / 1,5128 |
| DBSCAN (eps=0.5) | Silhouette Score | 0,1757 |

> Catatan: Akurasi klasifikasi mendekati random baseline (33,33%) untuk masalah tiga kelas seimbang, konsisten dengan korelasi Pearson ≤ 0,01 antara seluruh fitur dan target variabel. Pembahasan lengkap tersedia di laporan penelitian.

---

## Cara Menjalankan

1. Buka [Google Colab](https://colab.research.google.com/)
2. Upload atau buka notebook dari repository ini
3. Upload file dataset (`global_sports_footwear_sales_2018_2026.csv`) ke sesi Colab
4. Jalankan seluruh cell dari atas ke bawah
5. Ulangi untuk setiap notebook sesuai urutan

---

## Tim Peneliti

| Nama | Peran |
|------|-------|
| Henry Nugraha | Data Analysis, Modeling, Dokumentasi |
| Marcelleon Kusnawan | Data Analysis, Tinjauan Pustaka |
| Samuel Edward | Data Analysis, Visualisasi |

**Dosen Pembimbing:** Francka Sakti Lee
**Mata Kuliah:** Data Warehousing & Data Mining
**Program Studi:** Sistem Informasi, Universitas Bunda Mulia
