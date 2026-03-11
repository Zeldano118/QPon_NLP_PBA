# QPon Sentiment Analysis

End-to-end NLP pipeline on **4,638 user reviews** of the [QPon](https://play.google.com/store/apps/details?id=com.qpon.platform) app (cashback & coupons) from Google Play Store. All text processing is done in Indonesian.

> Scraping → Preprocessing → BoW / N-Grams → TF-IDF → POS Tagging

## Notebooks

| # | Notebook | What it does |
|---|---|---|
| 01 | `01_scraping_tokenization.ipynb` | Scrape all reviews, tokenization baselines (Gutenberg + IndoNLU), tokenize QPon data |
| 02 | `02_preprocessing_eda.ipynb` | Clean text, remove stopwords, stem, label sentiment, visualize distributions |
| 03 | `03_bow_ngrams.ipynb` | Bag of Words, regex pattern matching, bigram/trigram analysis |
| 04 | `04_tfidf.ipynb` | TF-IDF extraction, BoW vs TF-IDF comparison, Naive Bayes & LogReg benchmark |
| 05 | `05_pos_tagging.ipynb` | POS tagging with Stanza, linguistic patterns across sentiment |

## Project Structure
QPon_NLP_PBA/
├── data/
│   ├── raw/
│   │   └── qpon_reviews_raw.csv
│   └── processed/
│       └── qpon_preprocessed.csv
├── notebooks/
│   ├── 01_scraping_tokenization.ipynb
│   ├── 02_preprocessing_eda.ipynb
│   ├── 03_bow_ngrams.ipynb
│   ├── 04_tfidf.ipynb
│   └── 05_pos_tagging.ipynb
├── README.md
└── requirements.txt

## Quick Start

**Colab (recommended):** Open any notebook and click the "Open in Colab" badge.

**Local:**
```bash
git clone https://github.com/Zeldano118/QPon_NLP_PBA.git
cd QPon_NLP_PBA
pip install -r requirements.txt
```

## Tech Stack

| | |
|---|---|
| **Scraping** | google-play-scraper |
| **NLP** | NLTK, Sastrawi, Stanza |
| **ML** | scikit-learn (CountVectorizer, TF-IDF, Naive Bayes, Logistic Regression) |
| **Data** | Pandas, NumPy |
| **Viz** | Matplotlib, Seaborn, WordCloud |

## App Info

| | |
|---|---|
| **App** | QPon |
| **App ID** | `com.qpon.platform` |
| **Reviews** | 4,638 (Indonesian) |
| **Rating split** | ~44% ★1, ~44% ★5 — heavily polarized |

## Author

**Zeldano Shan Oeffie** — 5026231118
📧 kerjaanzeldano@gmail.com · [GitHub](https://github.com/Zeldano118)
