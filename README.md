# 📊 Analisis Sentimen Ulasan QPon — NLP Pipeline (Bahasa Indonesia)

Proyek end-to-end **Natural Language Processing** untuk menganalisis sentimen ulasan pengguna aplikasi **QPon** (cashback & kupon) dari Google Play Store. Seluruh pipeline dikerjakan dalam Bahasa Indonesia, mulai dari data collection hingga feature extraction dan POS tagging.

> 📌 **Dataset:** 4.638 ulasan pengguna QPon | **Bahasa:** Indonesia (`lang='id'`) | **Tools:** Python, NLTK, Sastrawi, scikit-learn

---

## 🎯 Tujuan Proyek
- Mengimplementasikan pipeline NLP lengkap untuk teks Bahasa Indonesia
- Menganalisis sentimen dan pola linguistik dalam ulasan aplikasi QPon
- Mengekstrak insight dari feedback pengguna menggunakan metode statistik dan machine learning

## 📱 Informasi Aplikasi
| | |
|---|---|
| **Nama** | QPon |
| **Google Play** | [QPon di Play Store](https://play.google.com/store/apps/details?id=com.qpon.platform) |
| **App ID** | `com.qpon.platform` |
| **Bahasa Ulasan** | Indonesia |

## 📁 Struktur Proyek
```
QPon_NLP_PBA/
├── data/
│   ├── raw/                                # Data mentah hasil scraping
│   │   └── qpon_reviews_raw.csv
│   └── processed/                          # Data setelah preprocessing
│       └── qpon_reviews_preprocessed.csv
├── notebooks/
│   ├── 01_Scraping_Tokenisasi.ipynb        # Week 1: Scraping + Tokenisasi
│   ├── 02_Preprocessing_EDA.ipynb          # Week 2: Preprocessing + EDA
│   ├── 03_BOW.ipynb                        # Week 3: Bag of Words
│   ├── 04_TFIDF.ipynb                      # Week 4: TF-IDF
│   └── 05_POS_Tagging.ipynb               # Week 5: POS Tagging
├── README.md
└── requirements.txt
```

## 🚀 Tahapan Proyek

### Week 1 — Scraping + Tokenisasi
`01_Scraping_Tokenisasi.ipynb`
- Scraping seluruh ulasan QPon dari Google Play menggunakan `reviews_all()`
- Eksplorasi awal: distribusi rating, contoh ulasan per rating
- Tokenisasi teks Inggris (Korpus Gutenberg / NLTK) dan Indonesia (IndoNLU SMSA / Hugging Face)
- Demo tokenisasi, stemming (Sastrawi), dan stopword removal pada ulasan QPon
- **Output:** `data/raw/qpon_reviews_raw.csv` (4.638 ulasan)

### Week 2 — Preprocessing + EDA
`02_Preprocessing_EDA.ipynb`
- Preprocessing: lowercase, hapus tanda baca, tokenisasi, stopwords, stemming
- Sentiment labeling: rating 1-2 = Negatif, 3 = Netral, 4-5 = Positif
- EDA: distribusi sentimen, word cloud, word frequency, tren waktu
- **Output:** `data/processed/qpon_reviews_preprocessed.csv`

### Week 3 — Bag of Words
`03_BOW.ipynb`
- Feature extraction menggunakan CountVectorizer
- Analisis feature matrix dari teks ulasan

### Week 4 — TF-IDF
`04_TFIDF.ipynb`
- Feature extraction menggunakan TF-IDF
- Perbandingan hasil dengan Bag of Words

### Week 5 — POS Tagging
`05_POS_Tagging.ipynb`
- Part-of-Speech tagging untuk Bahasa Indonesia
- Analisis pola linguistik per sentimen

## ✅ Progress
- [x] Week 1: Scraping + Tokenisasi
- [ ] Week 2: Preprocessing + EDA
- [ ] Week 3: Bag of Words
- [ ] Week 4: TF-IDF
- [ ] Week 5: POS Tagging

## 🛠️ Tech Stack
| Kategori | Tools |
|---|---|
| **NLP** | NLTK, PySastrawi, Hugging Face datasets |
| **Scraping** | google-play-scraper |
| **Data** | Pandas, NumPy |
| **Feature Extraction** | scikit-learn (CountVectorizer, TF-IDF) |
| **Visualisasi** | Matplotlib, Seaborn, WordCloud |

## ⚙️ Instalasi
```bash
git clone https://github.com/Zeldano118/QPon_NLP_PBA.git
cd QPon_NLP_PBA
pip install -r requirements.txt
```

## 📚 Referensi
- Jurafsky & Martin, *Speech and Language Processing* (3rd ed., 2023)
- Cahyawijaya et al., *IndoNLU: Benchmark and Resources for Evaluating Indonesian NLP* (ACL 2020)
- Bird et al., *Natural Language Processing with Python* (NLTK Book, 2009)

## 👤 Author
**Zeldano Shan Oeffie**
- NRP: 5026231118
- Program Studi: Sistem Informasi, Institut Teknologi Sepuluh Nopember
- Mata Kuliah: Pengolahan Bahasa Alami (PBA) — Irmasari Hafidz
- 📧 kerjaanzeldano@gmail.com
- 🔗 [GitHub](https://github.com/Zeldano118)
