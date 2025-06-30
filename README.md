# 🧠 NLP Business Case: Automated Customer Reviews

## 📌 Overview

This project builds a **smart product review analysis and recommendation system** powered by Natural Language Processing (NLP) and Generative AI. It automates the end-to-end process of understanding customer sentiment, clustering products, and summarizing key insights—helping businesses make data-driven decisions and enhance product visibility.

---

## 🚀 Key Features

- **✅ Sentiment Classification**: Categorize reviews into **Positive**, **Neutral**, or **Negative**.
- **📦 Product Clustering**: Group products into **4–6 meaningful categories** using unsupervised learning.
- **🧠 Generative AI Summarization**: Summarize reviews and generate **product highlights** using Large Language Models (LLMs).
- **📇 Product Card Generation**: Create structured product summaries that can be integrated into a user interface.

---

## 🧩 Project Steps

### 🔹 Part 1: Data Preprocessing & Sentiment Label Classification

#### 🎯 Objective

Clean and prepare the Amazon review data, then classify each review into **Positive**, **Neutral**, or **Negative** categories to gain valuable insights into customer sentiment.

#### 📚 Dataset

We used Amazon product review data from Kaggle:

- `Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products.csv`
- `Datafiniti_Amazon_Consumer_Reviews_of_Amazon_Products_May19.csv`

These were merged to create a more diverse and robust dataset.

#### ⚙️ Workflow Summary

📍 _Notebook: `data_exploration_and_acquisition.ipynb`, `data_preprocessing.ipynb`_

- Load and explore both datasets
- Combine and clean the review data
- Apply sentiment labeling using rule-based or lexicon-based methods (e.g., VADER)
- Save final dataset as `cleaned_amazon_reviews_final.csv`

---

### 🔹 Part 2: Sentiment Classification with DistilBERT

#### 🎯 Objective

Use a **pretrained transformer model (DistilBERT)** to classify Amazon reviews into sentiment categories more accurately than traditional models.

#### 📂 Dataset

- `cleaned_amazon_reviews_final.csv` with:

  - `full_review` (cleaned review text)
  - `sentiment` (labeled sentiment)

#### ⚙️ Workflow Summary

📍 _Notebook: `Classification_Model_1.ipynb`_

- Load and encode sentiment labels
- Tokenize using Hugging Face’s DistilBERT tokenizer
- Fine-tune `DistilBertForSequenceClassification` on labeled reviews
- Evaluate model using accuracy and confusion matrix

✅ **Achieved 95.29% accuracy**

---

### 🔹 Part 3: Product Clustering & GPT Summarization

#### 🎯 Objective

Organize products into clusters and generate summaries and recommendations using LLMs like GPT.

#### 🛠️ Workflow Overview

1. **Clustering**

   - Dimensionality reduction with **UMAP**
   - Clustering with **KMeans** (11 clusters)
   - Relabled the Clusters in 4
   - Assign descriptive `cluster_labels` using GPT-based interpretation

2. **Product-Level Aggregation**

   - Group reviews by `name` and `brand`
   - Compute average rating, sentiment trends, and gather review samples

3. **GPT-Based Summary Generation**

   - Identify top and worst products per category
   - Output structured summaries in JSON:

4. **Product Card Generation**

   - Final outputs rendered as **Product Cards** with:

     - Product name, brand, rating
     - Review highlights and representative image
     - Category and source URL

---

## 🛠️ Tech Stack

- Python (pandas, numpy, sklearn, matplotlib, seaborn)
- Hugging Face Transformers (`DistilBERT`)
- UMAP, KMeans
- OpenAI GPT-4 API (for summarization)
- Jupyter Notebooks

---

## 📈 Results

- ✅ **95.29% accuracy** on sentiment classification using DistilBERT.
- 🔍 Products grouped into coherent clusters such as Kindle, Fire Tablets, Accessories.
- 💬 GPT-generated summaries provide actionable insights and highlight standout products.
