<div align="center">

# 🏃 Sports Footwear — Data Mining Analysis

### Analisis Pola Penjualan dan Segmentasi Konsumen
### pada Dataset Global Sports Footwear Sales 2018–2026

<br>

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.x-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)
[![Colab](https://img.shields.io/badge/Google_Colab-Ready-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com)
[![Status](https://img.shields.io/badge/Status-Completed-27AE60?style=for-the-badge&logoColor=white)]()

<br>

[📄 **Laporan Penelitian**](https://drive.google.com/drive/folders/1KeCSgFlo-1Gdv1QyqYWwTyajvajsXlzO?usp=sharing) &nbsp;·&nbsp;
[📦 **Dataset Kaggle**](https://www.kaggle.com/datasets/aliiihussain/sports-footwear-sales-and-consumer-behavior) &nbsp;·&nbsp;
[▶ **Buka di Colab**](https://colab.research.google.com/github/[USERNAME]/DataMining-SalesFootwear/blob/main/Collection%20%26%20Exploratory%20Data%20ENG.ipynb)

<br>

**Kelompok 3 &nbsp;|&nbsp; Data Warehousing & Data Mining &nbsp;|&nbsp; Universitas Bunda Mulia &nbsp;|&nbsp; Semester 4 · 2025/2026**

</div>

---

## 📋 Tentang Proyek

Proyek ini merupakan penelitian data mining berbasis **framework CRISP-DM** yang menganalisis 30.000 catatan transaksi penjualan alas kaki olahraga global dari tahun 2018 hingga 2026. Penelitian mencakup tiga domain analisis utama: penemuan pola keterkaitan antar atribut transaksi menggunakan **Apriori**, prediksi tingkat pendapatan konsumen menggunakan **Decision Tree dan Random Forest**, serta segmentasi pola transaksi menggunakan **K-Means dan DBSCAN**.

Seluruh analisis diimplementasikan dalam empat notebook Google Colab yang dapat direproduksi secara penuh. Hasil penelitian, keterbatasan metodologis, dan rekomendasi penelitian lanjutan didokumentasikan lengkap dalam laporan yang dapat diakses melalui tautan di atas.

---

## 🗂 Dataset

| Atribut | Detail |
|---------|--------|
| **Nama** | Global Sports Footwear Sales & Consumer Behavior |
| **Sumber** | Kaggle — [aliiihussain](https://www.kaggle.com/datasets/aliiihussain/sports-footwear-sales-and-consumer-behavior) |
| **Ukuran** | 30.000 baris, 18 kolom |
| **Periode** | 2018–2026 |
| **Merek** | Nike, Adidas, Puma, Reebok, ASICS, New Balance |
| **Target Variabel** | `customer_income_level` — High / Medium / Low |
| **Catatan** | Data dideskripsikan publisher sebagai *"realistic data designed for ML tasks"* |

> ⚠️ **Dataset tidak disertakan dalam repository.** Unduh langsung dari Kaggle menggunakan link di atas, lalu upload ke sesi Google Colab.

<details>
<summary><b>📂 Lihat deskripsi 18 kolom dataset</b></summary>

<br>

| Kolom | Tipe | Deskripsi |
|-------|------|-----------|
| `order_id` | string | ID unik setiap transaksi |
| `order_date` | date | Tanggal transaksi |
| `brand` | kategorikal | Merek sepatu (6 merek) |
| `model_name` | string | Nama model produk |
| `category` | kategorikal | Jenis alas kaki (Running, Basketball, dll.) |
| `gender` | kategorikal | Gender konsumen (Male, Female, Unisex) |
| `size` | numerik | Ukuran sepatu |
| `color` | kategorikal | Warna produk |
| `base_price_usd` | numerik | Harga dasar (USD) |
| `discount_percent` | numerik | Persentase diskon (0, 5, 10, 15, 20, 30) |
| `final_price_usd` | numerik | Harga akhir setelah diskon |
| `units_sold` | numerik | Jumlah unit terjual (1–4) |
| `revenue_usd` | numerik | Total pendapatan transaksi (USD) |
| `payment_method` | kategorikal | Metode pembayaran |
| `sales_channel` | kategorikal | Saluran penjualan (Online / In-Store) |
| `country` | kategorikal | Negara transaksi (6 negara) |
| `customer_income_level` | kategorikal | **Target:** High / Medium / Low |
| `customer_rating` | numerik | Rating konsumen (3.0–5.0) |

</details>

---

## 🔬 Metodologi: CRISP-DM

| Fase | Aktivitas | Output |
|------|-----------|--------|
| **1. Business Understanding** | Identifikasi masalah, tujuan analisis, pemilihan teknik mining | Rumusan masalah & kerangka analisis |
| **2. Data Understanding** | Eksplorasi distribusi, statistik deskriptif, pemeriksaan integritas | EDA report, deteksi anomali distribusi |
| **3. Data Preparation** | One-Hot Encoding (26 kolom), RobustScaler, binning harga, label encoding | Dataset siap modeling per domain |
| **4. Modeling** | Implementasi Apriori, DT, RF (+ K-Fold CV k=5), K-Means, DBSCAN | Model terlatih, 270 association rules |
| **5. Evaluation** | Accuracy, F1-macro, AUC-ROC, Silhouette, DBI, CH Index, Chi-square | Tabel perbandingan model, crosstab validasi |
| **6. Deployment** | Dokumentasi laporan, repository GitHub, notebook terpublikasi | Laporan final, repository ini |

---

## 📁 Struktur Repository

```
DataMining-SalesFootwear/
│
├── 📓 Collection & Exploratory Data ENG.ipynb
│       └── Import dataset, statistik deskriptif, visualisasi distribusi,
│           pemeriksaan missing values dan outlier
│
├── 📓 Association Rule Mining ENG.ipynb
│       └── One-Hot Encoding (26 item), Apriori (270 rules),
│           visualisasi network keterkaitan, interpretasi lift
│
├── 📓 Classification ENG.ipynb
│       └── Preprocessing, Decision Tree, Random Forest,
│           Confusion Matrix, ROC-AUC, Stratified K-Fold CV (k=5)
│
└── 📓 Clustering ENG.ipynb
        └── RobustScaler, K-Means (K=3), DBSCAN (eps=0.5),
            Silhouette/DBI/CH Index, validasi crosstab income level
```

---

## ⚙️ Algoritma & Implementasi

### 🔗 Association Rule Mining — Apriori

Setiap baris dataset diperlakukan sebagai satu unit transaksi dengan 26 item biner hasil One-Hot Encoding dari kolom `brand`, `category`, `gender`, `payment_method`, `country`, dan `sales_channel`. Pendekatan ini menghasilkan pola ko-okurens antar atribut transaksi.

| Parameter | Nilai |
|-----------|-------|
| `min_support` | 0.01 |
| `min_confidence` | 0.10 |
| Rules terbentuk | 270 |
| Lift maksimum | 1.0761 |
| Lift rata-rata | 1.0158 |

### 📊 Classification — Decision Tree & Random Forest

Prediksi `customer_income_level` (3 kelas seimbang: 33.5% / 33.3% / 33.2%) dari fitur-fitur transaksi numerik dan kategorikal.

| Metrik | Decision Tree | Random Forest |
|--------|--------------|---------------|
| Accuracy | 33.12% | **34.03%** |
| F1-macro | 0.2646 | **0.3361** |
| AUC | 0.4979 | **0.5033** |
| Train-Test Gap | 4.79% ✅ | 10.78% ⚠️ |
| K-Fold Mean Acc | 33.36% | 33.13% |

> ⚠️ Kedua model mendekati random baseline (33.33%). Korelasi Pearson seluruh fitur terhadap target ≤ 0.01, mengindikasikan ketiadaan sinyal prediktif dalam dataset ini.

### 🎯 Clustering — K-Means & DBSCAN

Segmentasi pola transaksi berdasarkan fitur numerik: `final_price_usd`, `units_sold`, `revenue_usd`, `discount_percent`, `customer_rating`, `base_price_usd`.

| Metrik | K-Means (K=3) | DBSCAN (eps=0.5) |
|--------|--------------|------------------|
| Silhouette Score | 0.2390 ⚠️ | 0.1757 ❌ |
| Davies-Bouldin Index | 1.5128 | 1.7022 |
| Calinski-Harabasz | 11391.97 | 4617.42 |
| Distribusi klaster | 8.417 / 13.283 / 8.300 | 24.997 / 5.003 |

> Silhouette < 0.25 dikategorikan sebagai struktur klaster lemah. Dataset tidak mengandung `customer_id`, sehingga klaster merepresentasikan **segmentasi pola transaksi**, bukan segmentasi pelanggan.

---

## 📈 Temuan Utama

```
ASSOCIATION RULE MINING
  ✦ 270 aturan terbentuk, namun lift maksimum 1.0761 ≈ 1.0
  ✦ Asosiasi yang ditemukan bersifat sangat lemah (lift < 1.5)
  ✦ Pola dominan: kombinasi gender + sales_channel

CLASSIFICATION
  ✦ Random Forest sedikit lebih baik secara komparatif vs Decision Tree
  ✦ Kedua model mendekati random baseline — tidak ada sinyal prediktif berarti
  ✦ AUC Decision Tree = 0.4979 < 0.5 (di bawah classifier acak)

CLUSTERING
  ✦ K-Means lebih baik dari DBSCAN pada seluruh metrik internal
  ✦ Validasi crosstab: distribusi income level per klaster ≈ 33:33:33
  ✦ Chi-square p = 0.3086 — klaster tidak berkorelasi dengan income level
```

---

## 🚀 Cara Menjalankan

**Opsi A — Google Colab (Direkomendasikan)**

1. Klik tombol **"▶ Buka di Colab"** di bagian atas README
2. Di Colab, klik ikon folder di sidebar kiri, lalu upload file dataset CSV
3. Jalankan semua cell dari atas ke bawah (`Runtime` → `Run all`)
4. Ulangi untuk setiap notebook sesuai urutan

**Opsi B — Lokal (Jupyter Notebook)**

```bash
# Clone repository
git clone https://github.com/[USERNAME]/DataMining-SalesFootwear.git
cd DataMining-SalesFootwear

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn mlxtend scipy

# Letakkan dataset CSV di folder yang sama, lalu jalankan Jupyter
jupyter notebook
```

**Urutan eksekusi yang disarankan:**
```
1. Collection & Exploratory Data  →  memahami struktur dan kualitas data
2. Association Rule Mining         →  analisis pola keterkaitan atribut
3. Classification                  →  prediksi customer_income_level
4. Clustering                      →  segmentasi pola transaksi
```

---

## 👥 Tim Peneliti

| Nama | Peran dalam Penelitian |
|------|----------------------|
| **Henry Nugraha** | Lead Researcher — Bab 3 Metodologi, Bab 4 Hasil & Pembahasan (lengkap), revisi menyeluruh seluruh bab, implementasi dan debugging seluruh notebook Python |
| **Marcelleon Kusnawan** | Bab 2 Tinjauan Pustaka, Bab 4.3 Diskusi (draft awal) |
| **Samuel Edward** | Bab 1 Pendahuluan, Bab 5 Kesimpulan & Saran, Abstrak (draft awal) |

**Dosen:** Francka Sakti Lee
**Mata Kuliah:** Data Warehousing & Data Mining
**Program Studi:** Sistem Informasi — Universitas Bunda Mulia

---

## 📚 Referensi & Tautan

| Sumber | Link |
|--------|------|
| Laporan Penelitian (Google Drive) | [Buka Dokumen](https://drive.google.com/drive/folders/1KeCSgFlo-1Gdv1QyqYWwTyajvajsXlzO?usp=sharing) |
| Dataset (Kaggle) | [Sports Footwear Sales & Consumer Behavior](https://www.kaggle.com/datasets/aliiihussain/sports-footwear-sales-and-consumer-behavior) |
| Framework CRISP-DM | [crisp-dm.eu](https://www.crisp-dm.eu) |
| Library mlxtend | [rasbt.github.io/mlxtend](https://rasbt.github.io/mlxtend) |
| Library scikit-learn | [scikit-learn.org](https://scikit-learn.org) |

---

<div align="center">

*Universitas Bunda Mulia · Program Studi Sistem Informasi · 2025/2026*

</div>
