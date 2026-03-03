# 📊 Analisis Sentimen Ulasan QPon
## 📊 Gambaran Umum
Repositori ini berisi analisis menyeluruh terhadap ulasan pengguna aplikasi **QPon**
(cashback & kupon)
dari Google Play Store, dilakukan melalui pipeline NLP lengkap menggunakan **Bahasa
Indonesia**.
## 📊 Informasi Aplikasi
- **Nama Aplikasi:** QPon
- **Link Google Play:** [QPon di Play
Store](https://play.google.com/store/apps/details?id=com.qpon.platform)
- **App ID:** `com.qpon.platform`
- **Bahasa Ulasan:** Indonesia (`lang='id'`)
## 📊 Identitas
- **Nama:** [Nama Kamu]
- **NRP:** [NRP Kamu]
- **Mata Kuliah:** Pengolahan Bahasa Alami (PBA)
- **Dosen:** Irmasari Hafidz
- **Program Studi:** Sistem Informasi, ITS
## 📊 Struktur Proyek
```
QPon_NLP_PBA/
├── data/
│ ├── raw/ # Data mentah hasil scraping
│ │ └── qpon_reviews_raw.csv
│ └── processed/ # Data setelah preprocessing
│ └── qpon_reviews_preprocessed.csv
├── notebooks/
│ ├── 01_Scraping_Tokenisasi.ipynb # Week 1: Scraping + Tokenisasi
│ ├── 02_Preprocessing_EDA.ipynb # Week 2: Preprocessing + EDA
│ ├── 03_BOW.ipynb # Week 3: Bag of Words
│ ├── 04_TFIDF.ipynb # Week 4: TF-IDF
│ └── 05_POS_Tagging.ipynb # Week 5: POS Tagging
├── README.md
└── requirements.txt
```
## 📊 Tahapan Proyek
### 1. Scraping + Tokenisasi (Week 1)
Notebook: `01_Scraping_Tokenisasi.ipynb`
- Scraping seluruh ulasan QPon dari Google Play (`reviews_all()`)
- Eksplorasi awal: distribusi rating, contoh ulasan per rating
- Tokenisasi teks Inggris (Korpus Gutenberg / NLTK)
- Tokenisasi teks Indonesia (Dataset IndoNLU SMSA / Hugging Face)
- Tokenisasi pada ulasan QPon + demo stemming & stopword removal
- Output: `data/raw/qpon_reviews_raw.csv`
### 2. Preprocessing + EDA (Week 2)
Notebook: `02_Preprocessing_EDA.ipynb`
- Preprocessing: lowercase, hapus tanda baca, tokenisasi, stopwords, stemming (Sastrawi)
- Sentiment labeling berdasarkan rating (1-2=Negatif, 3=Netral, 4-5=Positif)
- EDA: distribusi sentimen, word cloud, word frequency, tren waktu
- Output: `data/processed/qpon_reviews_preprocessed.csv`
### 3. Bag of Words (Week 3)
Notebook: `03_BOW.ipynb`
- Implementasi CountVectorizer
- Feature matrix dari teks ulasan
### 4. TF-IDF (Week 4)
Notebook: `04_TFIDF.ipynb`
- Implementasi TF-IDF
- Perbandingan dengan BOW
### 5. POS Tagging (Week 5)
Notebook: `05_POS_Tagging.ipynb`
- Part-of-Speech tagging untuk Bahasa Indonesia
- Analisis pola linguistik per sentimen
## ✅ Progress
- [x] Week 1: Scraping + Tokenisasi
- [ ] Week 2: Preprocessing + EDA
- [ ] Week 3: Bag of Words
- [ ] Week 4: TF-IDF
- [ ] Week 5: POS Tagging
## 📊 Teknologi
- **Python 3.x**
- **NLTK**: Tokenisasi, stopwords, korpus Gutenberg
- **PySastrawi**: Stemming & stopwords Bahasa Indonesia
- **google-play-scraper**: Scraping ulasan Google Play
- **Hugging Face datasets**: Dataset IndoNLU SMSA
- **Pandas & NumPy**: Manipulasi data
- **Scikit-learn**: Feature extraction (BOW, TF-IDF)
- **Matplotlib / Seaborn**: Visualisasi
## 📊 Instalasi
```bash
# Clone repository
git clone https://github.com/[your-username]/QPon_NLP_PBA.git
cd QPon_NLP_PBA
# Install dependencies
pip install -r requirements.txt
```

## 📊 Referensi
- Jurafsky & Martin, *Speech and Language Processing* (3rd ed., 2023)
- Cahyawijaya et al., *IndoNLU: Benchmark and Resources for Evaluating Indonesian NLP* (ACL
2020)
- Bird et al., *Natural Language Processing with Python* (NLTK Book, 2009)
