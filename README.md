# 📰 Fake News Detection Using Machine Learning

## 📌 Project Overview

This project aims to build a machine learning model that classifies news articles as **Fake** or **Real** based on their textual content. The model leverages Natural Language Processing (NLP) techniques and is deployed via a user-friendly Streamlit web application.

---

## 🗂️ Dataset

- **Source**: [Kaggle - Fake and Real News Dataset](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- **Files**:
  - `Fake.csv`: Fake news articles
  - `True.csv`: Real news articles
- **Columns Used**: `title`, `text`, `label`

---

## 🧹 Data Preprocessing

- Combined `title` and `text` into a `content` field
- Cleaned the text:
  - Lowercased
  - Removed punctuation, stopwords, and URLs
- Transformed text into numerical features using **TF-IDF Vectorization**

---

## 🤖 Model Training

Three models were developed and evaluated:

| Model               | Accuracy |
|--------------------|----------|
| Logistic Regression| ~95%     |
| Random Forest      | ~96%     |
| XGBoost            | ~97%     |

**XGBoost** performed best and was used as a benchmark.

---

## 📊 Visualizations

- **Class distribution**: Bar chart of Fake vs Real
- **Word clouds**: Frequent words in Fake and Real news
- **Confusion matrices**
- **ROC-AUC Curves** comparing models

---

## 💻 Streamlit App Features

The interactive app includes:

- 📥 Input box for pasting news text
- ⚙️ Model prediction output: FAKE or REAL
- 📊 Word clouds for fake and real news articles
- 🧠 Model performance summary

To run locally:

```bash
pip install -r requirements.txt
streamlit run fake_news_app.py
