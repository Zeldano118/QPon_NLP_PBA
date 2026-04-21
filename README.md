# QPon Sentiment Analysis

End-to-end NLP pipeline on **4,638 user reviews** of the [QPon](https://play.google.com/store/apps/details?id=com.qpon.platform) app (cashback & coupons) from Google Play Store. All text processing is done in Indonesian.

> Scraping → Preprocessing → BoW / N-Grams → TF-IDF → POS Tagging

---

## Project Notebooks

The main pipeline lives in `notebooks/`. Each notebook builds on the previous one.

| # | Notebook | What it does |
|---|---|---|
| 01 | `01_scraping_tokenization.ipynb` | Scrape all reviews, tokenization baselines (Gutenberg + IndoNLU), tokenize QPon data |
| 02 | `02_preprocessing_eda.ipynb` | Clean text, remove stopwords, stem, label sentiment, visualize distributions |
| 03 | `03_bow_ngrams.ipynb` | Bag of Words, regex pattern matching, bigram/trigram analysis |
| 04 | `04_tfidf.ipynb` | TF-IDF extraction, BoW vs TF-IDF comparison, Naive Bayes & LogReg benchmark |
| 05 | `05_pos_tagging.ipynb` | POS tagging with Stanza, linguistic patterns across sentiment |

---

## Assignments

Weekly NLP assignments in `assignments/`. These follow a different structure from the main project — they're shorter, more focused exercises. Most of them need `df_qpon_rev.csv` (located in `assignments/data/`), which is the raw scraped data from Week 2.

### Week 2 — Scraping & Preprocessing

| File | Description | Needs CSV? |
|---|---|---|
| `1_Week2_Scrapping_QPon.ipynb` | Scrape QPon reviews from Google Play, basic stats, TextBlob sentiment, frequency chart, stopword removal (Sastrawi + English) | No (generates its own CSV) |
| `2_Week2_Preprocessing_QPon.ipynb` | Load the scraped CSV, Indonesian stopword list, top 50 frequent words analysis | Yes — upload `df_qpon_rev.csv` |

Run scrapping first, then preprocessing.

### Week 3 — EDA, BoW & Regex

| File | Description | Needs CSV? |
|---|---|---|
| `1_week3_eda.ipynb` | Full EDA: score distribution, review trends over time, word frequency top 30, word clouds (positive vs negative) | Yes |
| `2_week3_yearly.ipynb` | Reviews per year, score distribution by year, word clouds | Yes |
| `3_week3_bow_regex.ipynb` | Bag of Words (3 step process on 50 sampled reviews), regex pattern matching for positive & negative insights | Yes |

### Week 4 — TF-IDF

| File | Description | Needs CSV? |
|---|---|---|
| `1_week4_tfidf_summarization.ipynb` | TF-IDF text summarization on 3 articles: Manchester (EN), Danantara (ID), flood news (ID) | No (text is in the notebook) |
| `2_week4_tfidf_classification.ipynb` | TF-IDF sentiment classification with 5 classifiers (SVM, LogReg, NB, XGBoost, RandomForest) | Yes |
| `3_week4_tfidf_custom.ipynb` | Custom TF-IDF implementation (from Wittline/tf-idf GitHub) applied to QPon reviews | Yes |

### Week 5 — Text Embedding & Keyword Extraction

| File | Description | Needs CSV? |
|---|---|---|
| `week5_text_embedding.ipynb` | Keyword extraction (TF-IDF, RAKE, TextRank), N-gram analysis, regex keyword variations, Sentence-BERT embeddings, clustering & PCA visualization | Yes |

### How is this different from the main project?

The `notebooks/` folder is the full QPon sentiment analysis pipeline — everything connects end to end, from raw scraping to POS tagging. The `assignments/` folder contains standalone exercises that explore specific NLP techniques in isolation. Some overlap exists (both do EDA, both do TF-IDF), but the assignments follow a different format and scope.

---

## Project Structure

```
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
├── assignments/
│   ├── data/
│   │   └── df_qpon_rev.csv
│   ├── week 2/
│   │   ├── 1_Week2_Scrapping_QPon.ipynb
│   │   └── 2_Week2_Preprocessing_QPon.ipynb
│   ├── week 3/
│   │   ├── 1_week3_eda.ipynb
│   │   ├── 2_week3_yearly.ipynb
│   │   └── 3_week3_bow_regex.ipynb
│   ├── week 4/
│   │   ├── 1_week4_tfidf_summarization.ipynb
│   │   ├── 2_week4_tfidf_classification.ipynb
│   │   └── 3_week4_tfidf_custom.ipynb
│   └── week 5/
│       └── week5_text_embedding.ipynb
├── README.md
└── requirements.txt
```

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
| **Embeddings** | sentence-transformers (Sentence-BERT) |
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
