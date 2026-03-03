# QPon Sentiment Analysis

An end-to-end **Natural Language Processing** project analyzing user reviews of the **QPon** app (cashback & coupons) from the Google Play Store. The entire pipeline is built for **Indonesian language text**, covering data collection, text preprocessing, feature extraction, and linguistic analysis.

> **4,638 reviews** scraped from Google Play | **Language:** Indonesian (`lang='id'`) | **Built with:** Python, NLTK, Sastrawi, scikit-learn

---

## Objectives
- Build a complete NLP pipeline for Indonesian text from scratch
- Analyze user sentiment and linguistic patterns in QPon app reviews
- Extract actionable insights from customer feedback using statistical and machine learning methods

## App Information
| | |
|---|---|
| **App Name** | QPon |
| **Google Play** | [View on Play Store](https://play.google.com/store/apps/details?id=com.qpon.platform) |
| **App ID** | `com.qpon.platform` |
| **Review Language** | Indonesian |
| **Total Reviews** | 4,638 |

## Project Structure

```
QPon_NLP_PBA/
├── data/
│   ├── raw/                                # Raw scraped data
│   │   └── qpon_reviews_raw.csv
│   └── processed/                          # Cleaned & preprocessed data
│       └── qpon_reviews_preprocessed.csv
├── notebooks/
│   ├── 01_Scraping_Tokenisasi.ipynb        # Data collection & tokenization
│   ├── 02_Preprocessing_EDA.ipynb          # Text preprocessing & EDA
│   ├── 03_BOW.ipynb                        # Bag of Words
│   ├── 04_TFIDF.ipynb                      # TF-IDF
│   └── 05_POS_Tagging.ipynb               # POS Tagging
├── README.md
└── requirements.txt
```

## Pipeline Overview

### 1. Data Collection & Tokenization
- Scraped all QPon reviews from Google Play using `google_play_scraper` (`reviews_all()`)
- Initial exploration: rating distribution, sample reviews per rating
- Tokenization on English text (NLTK Gutenberg corpus) and Indonesian text (IndoNLU SMSA dataset)
- Applied tokenization, stemming (Sastrawi), and stopword removal on QPon reviews
- **Output:** `data/raw/qpon_reviews_raw.csv`

### 2. Text Preprocessing & Exploratory Data Analysis
- Full preprocessing pipeline: lowercasing, punctuation removal, tokenization, stopword removal, stemming
- Sentiment labeling based on ratings (1–2 = Negative, 3 = Neutral, 4–5 = Positive)
- EDA: sentiment distribution, word clouds, word frequency, temporal trends
- **Output:** `data/processed/qpon_reviews_preprocessed.csv`

### 3. Feature Extraction — Bag of Words
- Text vectorization using `CountVectorizer`
- Feature matrix construction and vocabulary analysis

### 4. Feature Extraction — TF-IDF
- Term weighting using TF-IDF
- Comparison with Bag of Words approach

### 5. Linguistic Analysis — POS Tagging
- Part-of-Speech tagging for Indonesian text
- Linguistic pattern analysis across sentiment categories

## Progress
- [x] Data Collection & Tokenization
- [ ] Text Preprocessing & EDA
- [ ] Bag of Words
- [ ] TF-IDF
- [ ] POS Tagging

## Tech Stack
| Category | Tools |
|---|---|
| **NLP & Text Processing** | NLTK, PySastrawi, Hugging Face `datasets` |
| **Web Scraping** | google-play-scraper |
| **Data Manipulation** | Pandas, NumPy |
| **Feature Extraction** | scikit-learn (CountVectorizer, TfidfVectorizer) |
| **Visualization** | Matplotlib, Seaborn, WordCloud |

## Getting Started

### Google Colab (Recommended)
Open any notebook and click the **"Open in Colab"** badge in the first cell.

### Local Setup
```bash
git clone https://github.com/Zeldano118/QPon_NLP_PBA.git
cd QPon_NLP_PBA
pip install -r requirements.txt
```

## References
- Jurafsky, D. & Martin, J.H. (2023). *Speech and Language Processing* (3rd ed.)
- Cahyawijaya, S. et al. (2020). *IndoNLU: Benchmark and Resources for Evaluating Indonesian NLP.* ACL 2020.
- Bird, S., Klein, E. & Loper, E. (2009). *Natural Language Processing with Python.* O'Reilly Media.

## Author
**Zeldano Shan Oeffie**
- Information Systems, Institut Teknologi Sepuluh Nopember (ITS)
- Course: Natural Language Processing (PBA) — Irmasari Hafidz, S.Kom., M.Sc.
- 📧 kerjaanzeldano@gmail.com
- 🔗 [GitHub](https://github.com/Zeldano118)
