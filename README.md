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

# Part 1: Data Preprocessing and Sentimanet Lable Clasifications

Objective:
Identify and preprocess the dataset by cleaning the Amazon product reviews, then classify each review into Positive, Neutral, or Negative sentiment categories. This classification helps businesses gain insights into customer opinions and improve decision-making based on sentiment trends.

Dataset:
Amazon Datset from https://www.kaggle.com/datasets/datafiniti/consumer-reviews-of-amazon-products/data and combained Two data sets () with the same column name to obtain a large dataset


# Part 2 :Implements a sentiment classification pipeline using DistilBERT:

Data loading and preprocessing
Label encoding for sentiment classes
Model training with Hugging Face Transformers
Evaluation metrics (accuracy, confusion matrix, classification report)
Visualization of results
Key metrics:

Validation Accuracy: 95.29%

# Part 3 :Generative GPT-3 Model (Generative GPT3 model.ipynb)

https://colab.research.google.com/assets/colab-badge.svg

Generates product category summaries using GPT-3.5-turbo:

Product clustering by category
Prompt engineering for structured JSON output
GPT-3 API integration
Result enrichment with product images
JSON output generation
Sample output structure:

