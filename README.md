# Analisis Sentimen Ulasan QPon
## Gambaran Proyek
Proyek NLP untuk menganalisis sentimen ulasan pengguna aplikasi
**QPon** (cashback & kupon) dari Google Play Store.
Bahasa ulasan: Indonesia (`lang='id'`).
## Informasi Aplikasi
- **Nama:** QPon
- **Google Play:** https://play.google.com/store/apps/details?id=com.qpon.android
- **App ID:** com.qpon.android
## Mata Kuliah
Pengolahan Bahasa Alami (PBA) - Sistem Informasi ITS
Dosen: Irmasari Hafidz
## Struktur Proyek
| Folder | Isi |
|--------|-----|
| `data/raw/` | Data ulasan mentah hasil scraping |
| `data/processed/` | Data setelah preprocessing |
| `notebooks/` | Notebook Colab per minggu |
## Progress
- [x] Week 1: Scraping QPon Reviews + Tokenisasi & Konsep NLP
- [ ] Week 2: Preprocessing Lengkap + EDA
- [ ] Week 3: Bag of Words (BoW)
- [ ] Week 4: TF-IDF
- [ ] Week 5: POS Tagging
## Dataset
- Sumber: Google Play Store (QPon)
- Bahasa: Indonesia
- Sentiment labeling: Rating 1-2 = Negatif, 3 = Netral, 4-5 = Positif
## Tools
Python, NLTK, PySastrawi, google-play-scraper, pandas, scikit-learn
