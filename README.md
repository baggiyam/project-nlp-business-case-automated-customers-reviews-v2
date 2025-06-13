# Project NLP | Business Case: Automated Customer Reviews

# Project-Overview

This project builds a product review website powered by NLP models that aggregate customer feedback from multiple sources. It helps businesses:

Analyze review sentiment
Organize products into meaningful categories
Recommend top products effectively using AI
 # Main Features

Sentiment Classification: Categorize reviews as Positive, Neutral, or Negative.
Product Category Clustering: Group products into 4–6 meaningful categories.
Generative AI Summarization & Recommendations: Summarize reviews and recommend top products with Large Language Models (LLMs).

#Project Steps

Part 1: Data Preprocessing and Sentimanet Lable Clasifications

Objective:
Identify and preprocess the dataset by cleaning the Amazon product reviews, then classify each review into Positive, Neutral, or Negative sentiment categories. This classification helps businesses gain insights into customer opinions and improve decision-making based on sentiment trends.

Dataset:
Amazon Datset from https://www.kaggle.com/datasets/datafiniti/consumer-reviews-of-amazon-products/data
Methodology:

Extract TF-IDF features (top 5000) from review text.
Train a Support Vector Machine (SVM) classifier with balanced class weights.
Results:

Achieved 85.68% accuracy.
Output file contains reviews with predicted sentiments and confidence scores.
Output:
product_reviews_sentiment_and_confidence.csv — reviews plus predicted sentiment and confidence.

How to Run:

Upload 1429_1.csv.
Run the notebook sentiment_analysis_tfidf_svm.ipynb.