# 🛍️ Online Retail Order Reviews NLP Project

This project performs **Natural Language Processing (NLP)** on a large dataset of **online retail product reviews** written in **Portuguese**.
The goal is to analyze customer sentiments through **review scores** and text mining techniques like **unigrams**, **bigrams**, and **trigrams**.

It also visualizes rating distributions and frequent word patterns to better understand **customer satisfaction** and **feedback trends**.

---

## 📘 Overview

This dataset contains over **100,000 product reviews** from an online retail platform.
The analysis focuses on:

* Understanding **review score distribution** (1–5 stars)
* Cleaning and normalizing **Portuguese text**
* Tokenizing text and removing **stopwords**
* Generating and analyzing **N-grams** (Unigrams, Bigrams, Trigrams)
* Visualizing frequent patterns for positive (5-star) and negative (1-star) reviews

---

## 🧠 Key Insights

* 📊 **5-star reviews** dominate the dataset, indicating overall customer satisfaction.
* ⚠️ **1-star reviews** show recurring issues related to delivery delays and product quality.
* 🔠 Top unigrams and bigrams reveal common terms customers use in both positive and negative feedback.
* 🗣️ Portuguese-specific stopwords were removed to retain only meaningful words.
* 🎨 Visualizations provide comparative frequency distributions for **positive** and **negative** review language.

---

## ⚙️ Tools & Technologies

| Tool                                | Purpose                                               |
| ----------------------------------- | ----------------------------------------------------- |
| **Python**                          | Core programming language                             |
| **NLTK (Natural Language Toolkit)** | Tokenization, stopword removal, and N-gram generation |
| **Pandas**                          | Data manipulation and handling                        |
| **Matplotlib & Seaborn**            | Data visualization                                    |
| **UnicodeData**                     | Removing text accents for normalization               |
| **Portuguese Stopwords**            | Filtering non-informative words from reviews          |

---

## 📊 Project Workflow

### 🔹 1. Data Loading & Preprocessing

* Load dataset: `order_reviews.csv` (≈100,000 rows)
* Convert `review_creation_date` to datetime format
* Visualize **review score distribution** using pie charts and bar plots

### 🔹 2. Text Cleaning

* Convert all text to lowercase
* Remove accents using `unicodedata.normalize()`
* Tokenize text using `nltk.word_tokenize()`
* Remove Portuguese stopwords using NLTK’s corpus

### 🔹 3. N-Gram Generation

Generate:

* **Unigrams** → single words
* **Bigrams** → two-word combinations
* **Trigrams** → three-word combinations

Used for both:

* **5-star reviews** (positive sentiment)
* **1-star reviews** (negative sentiment)

### 🔹 4. Frequency Distribution Visualization

Plotted top 25 most frequent **n-grams** for both positive and negative reviews using:

```python
nltk.FreqDist(tokens).plot(25, cumulative=False, color=color)
```

---

## 📂 Project Structure

```
Online_Retail_Order_Reviews/
│
├── order_reviews_analysis.py         # Main Python analysis script
├── order_reviews.csv                 # Dataset (100k+ Portuguese reviews)
├── README.md                         # Project documentation
└── images/                           # (Optional) visualizations and n-gram plots
```

---

## 🚀 How to Run

### 🔹 Prerequisites

Install all dependencies:

```bash
pip install pandas matplotlib seaborn nltk
```

Also download NLTK datasets (only once):

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

### 🔹 Execute the Script

```bash
python order_reviews_analysis.py
```

* Pie charts and bar plots display review distributions
* N-gram frequency charts visualize word usage patterns

---

## 📈 Visualizations

1. **Pie Chart:** Distribution of review scores (1–5)
2. **Bar Graph:** Count of reviews per score on a dark grid background
3. **N-gram Frequency Graphs:**

   * Top 25 Unigrams for 5-star reviews
   * Top 25 Bigrams for 1-star reviews
   * Top 25 Trigrams for both categories

---

## 💡 Future Enhancements

* Add **sentiment polarity analysis** using TextBlob or Vader
* Translate Portuguese text for global reporting
* Implement **topic modeling (LDA)** for deeper insight into customer issues
* Deploy a **Streamlit NLP dashboard** for interactive visualization
* Integrate **word clouds** for better visual storytelling

---

## 👤 Author

**Rachakonda Ganesh**
📧 [[rachakondaganesh60@gmail.com](mailto:rachakondaganesh60@gmail.com)]
🔗 [GitHub](https://github.com/Rachakondaganesh)
🔗 [LinkedIn](https://www.linkedin.com/in/rachakonda-ganesh-2782452a8)

---

## 🏁 Conclusion

This project highlights the power of **NLP in retail analytics**, converting unstructured text data into meaningful insights.
By combining **Python**, **NLTK**, and **visualization tools**, it offers a data-driven view of customer satisfaction and recurring pain points — essential for enhancing user experience and improving product quality.
