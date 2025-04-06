🎬 Movie Review Sentiment Analysis

This project performs sentiment analysis on movie reviews scraped from platform **Rotten Tomatoes**. It uses Natural Language Processing (NLP) and Machine Learning to classify reviews as **Positive**, **Neutral**, or **Negative** and visualize trends in genres, ratings, and sentiment.

---

## 📌 Project Structure

### 🔹 1. Web Scraping
- Scraped movie reviews, ratings, and metadata using `BeautifulSoup` and `Selenium`
- Stored data in a CSV format

### 🔹 2. Data Cleaning
- Removed null values, duplicates, and non-English characters
- Normalized ratings (e.g., from 1–5 scale to 1–10)
- Preprocessed text:
  - Lowercasing
  - Removing punctuation, stopwords
  - Tokenization and optional stemming/lemmatization

### 🔹 3. Feature Engineering
- Transformed text using `TF-IDF` / `CountVectorizer` (up to 5000 features)
- Encoded sentiment labels (Positive, Neutral, Negative)

### 🔹 4. Model Training
- Split data into `train` and `test` sets (80/20)
- Trained and evaluated:
  - **Logistic Regression** 🔥
  - **Naive Bayes**
- Metrics:
  - Accuracy
  - Precision, Recall, F1-Score

### 🔹 5. Evaluation
- Compared models using classification reports
- Logistic Regression showed best performance (Accuracy ≈ 98%)

### 🔹 6. Visualization
- Used `Matplotlib` and `Seaborn` for:
  - Rating distributions
  - Sentiment trends over time
- Built an interactive dashboard in **Power BI**

---

## 📈 Results

| Model              | Accuracy | F1 (Positive) | F1 (Neutral) | F1 (Negative) |
|--------------------|----------|---------------|--------------|---------------|
| Logistic Regression| 0.98     | 0.99          | 0.96         | 0.95          |
| Naive Bayes        | 0.93     | 0.95          | 0.86         | 0.81          |

- **Conclusion**: Logistic Regression generalized well; Naive Bayes underfitted.
- **Insight**: Positive reviews often praise *acting* and *storyline*. Negative reviews focus on *predictability* and *pacing*.

---

## 🛠️ Tech Stack

- Python 3.x
- BeautifulSoup, Selenium
- Pandas, NumPy
- Scikit-learn, NLTK
- Matplotlib, Seaborn
- Power BI (Dashboard)

---

## 📂 Files in This Project

| File/Folder         | Description                                  |
|---------------------|----------------------------------------------|
| `scraped_data.csv`  | Cleaned dataset with reviews, ratings        |
| `notebooks/`        | Jupyter Notebooks for analysis               |
| `models/`           | Saved ML models (optional)                   |
| `powerbi/`          | Power BI .pbix file                          |
| `README.md`         | Project documentation                        |

---


