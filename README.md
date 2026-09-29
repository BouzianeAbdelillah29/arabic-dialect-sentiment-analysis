# Arabic Dialect Sentiment Analysis

Sentiment analysis for Arabic dialects — **Master's thesis (2023–2025)**, University of Saad Dahlab, Blida, Algeria.

## Overview

Classifying sentiment in dialectal Arabic social media comments is a hard NLP problem: rich morphology, non-standard spelling, and heavy dialectal variation. This project tackles it on 4,128 COVID-related Arabic comments, comparing classical and neural approaches across three text representations — reaching **~89% test accuracy**.

## Dataset

`data/train_araCovid_sentiment.tsv` — 4,128 Arabic comments labeled by sentiment class.

## Approach

1. **Exploration & preprocessing** (`notebooks/01_data_exploration.ipynb`) — cleaning and normalization of dialectal text, exploratory analysis: sentiment distribution, text-length distributions per class
2. **Bag-of-Words** (`notebooks/02_bag_of_words.ipynb`) — BoW features with scikit-learn, XGBoost and Keras classifiers → up to ~88% accuracy
3. **TF-IDF** (`notebooks/03_tfidf.ipynb`) — TF-IDF features with the same classifier suite → up to ~89% accuracy
4. **Word2Vec + AraVec** (`notebooks/04_word2vec_aravec.ipynb`) — pre-trained AraVec Arabic embeddings with neural classifiers → up to ~88% accuracy

## Results

| Representation     | Best test accuracy |
|--------------------|--------------------|
| Bag-of-Words       | ~88%               |
| TF-IDF             | ~89%               |
| Word2Vec (AraVec)  | ~88%               |

TF-IDF features with tuned classifiers performed best on this dataset.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook
```

Then open the notebooks in order, starting with `01_data_exploration.ipynb`.

## Tech stack

Python, pandas, NumPy, scikit-learn, NLTK, TensorFlow/Keras, XGBoost, Gensim (AraVec), matplotlib, seaborn.

## Thesis

The full thesis document is available in `docs/Sentiment_Analysis_Thesis_final.docx`.

## Author

**Abdelillah Bouziane** — AI Engineer
- GitHub: [@BouzianeAbdelillah29](https://github.com/BouzianeAbdelillah29)
- LinkedIn: [Bouziane Abdelillah](https://www.linkedin.com/in/bouziane-abdelillah-802678435/)
- Email: bouziane.abdelillah.2002@gmail.com
