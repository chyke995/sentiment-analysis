# sentiment-analysis
This project performs sentiment analysis on book reviews using R. It involves data preprocessing, tokenization, visualization, and sentiment scoring with lexicon-based methods. The goal is to extract insights from reviews, determine sentiment scores, and analyze patterns in word usage and sentiment trends.
# Sentiment Analysis of Book Reviews

## Author: Chijioke Obiakor

**Date:** February 19, 2025

## Project Overview

This project performs sentiment analysis on book reviews using R. It involves data preprocessing, tokenization, visualization, and sentiment scoring with lexicon-based methods. The goal is to extract insights from reviews, determine sentiment scores, and analyze patterns in word usage and sentiment trends.

## Table of Contents

- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Installation and Setup](#installation-and-setup)
- [Project Workflow](#project-workflow)
- [Key Findings](#key-findings)
- [Conclusion](#conclusion)

## Technologies Used

This project is implemented in **R** using the following libraries:

- `tm`, `tidytext`, `ggplot2`, `wordcloud`, `syuzhet`, `dplyr`, `tibble`, `textstem`, `textdata`, `tidyr`, `Matrix`, `topicmodels`, `stringr`, `reshape2`, `LDAvis`, `jsonlite`, `spacyr`, `NLP`, `proxy`, `igraph`, `textTinyR`

## Dataset

- **Source:** CSV file containing book reviews.
- **Format:** Includes book title, review text, ratings, and other metadata.
- **Preprocessing:** Removal of missing values, selection of relevant columns, and data sampling.

## Installation and Setup

1. Install necessary R packages (if not already installed):
   ```r
   install.packages(c("tm", "tidytext", "ggplot2", "wordcloud", "syuzhet", "dplyr", "tibble", "textstem", "textdata", "tidyr", "Matrix", "topicmodels", "stringr", "reshape2", "LDAvis", "jsonlite","spacyr","NLP","proxy","igraph","textTinyR"))
   ```
2. Load the required libraries:
   ```r
   for (lib in libraries) {
     library(lib, character.only=TRUE)
   }
   ```
3. Load the dataset:
   ```r
   review_df <- as_tibble(read.csv("C:/Users/Dell/Downloads/MS4S09_CW_Book_Reviews.csv", stringsAsFactors = FALSE))
   ```

## Project Workflow

### 1. Data Preprocessing

- Selects relevant columns and removes missing values.
- Filters books with more than 50 reviews.
- Samples a subset of books for analysis.

### 2. Text Tokenization and Cleaning

- **Word Tokenization:** Converts text into individual words.
- **Stopword Removal and Lemmatization:** Cleans data for better analysis.
- **Bigram Tokenization:** Extracts common word pairs.

### 3. Data Visualization

- **Word Frequency Analysis:** Displays the most common words in reviews.
- **Word Cloud:** Highlights frequently occurring words.
- **Bigram Analysis:** Identifies commonly used word pairs.
- **Sentiment Score Distribution:** Box plots and histograms show sentiment trends.

### 4. Sentiment Analysis

- Uses **Bing** and **AFINN** lexicons to assign sentiment scores.
- Compares sentiment scores with book ratings.
- Identifies best and worst reviews.
- Performs emotion analysis using **NRC** lexicon.

## Key Findings

1. **Correlation Between Sentiment Scores and Ratings:**
   - Weak positive correlation between sentiment scores and ratings.
   - Sentiment scores alone do not fully determine user ratings.
2. **Word Choice Impact:**
   - Some positive reviews received negative sentiment scores due to specific word usage.
3. **Sentiment Consistency:**
   - Strong correlation between Bing and AFINN lexicon sentiment scores.
4. **Emotion Analysis:**
   - Different books evoke varying levels of emotions (anger, joy, sadness, etc.).

## Conclusion

The project highlights the importance of sentiment analysis in understanding book reviews. While lexicon-based methods provide valuable insights, limitations exist due to word misclassification. Future improvements may include:

- Implementing machine learning models for sentiment classification.
- Using context-aware NLP techniques to enhance accuracy.
- Expanding the dataset for more diverse insights.

This project serves as a foundational step in leveraging sentiment analysis for book reviews, providing valuable data-driven insights for readers and publishers alike.



