# Aspect-Based Sentiment Analysis (ABSA) on App Store & Google Play Reviews

This project implements an end-to-end **Aspect-Based Sentiment Analysis (ABSA)** pipeline using **Large Language Models (LLMs)**. The system extracts *aspects* from app reviews (e.g., “UI”, “performance”, “pricing”, “ads”) and classifies the **sentiment for each aspect** individually. It supports data from both the **Apple App Store** and **Google Play Store**.

---

## Project Features

### 1. Data Collection
- Scrapes reviews from the App Store and Google Play Store.
- Handles metadata such as review text, rating, and date.
- Works for any app (e.g., Spotify, Instagram).

### 2. LLM-Based Aspect Extraction
- Uses Google Gemini API.
- Custom prompt engineering to extract all meaningful aspects.
- Ensures structured JSON output.

### 3. LLM-Based Sentiment Classification
- Assigns Positive, Neutral, or Negative sentiment to **each aspect**.
- Handles mixed-sentiment reviews effectively.

### 4. Baseline Model (VADER)
- Implements VADER for comparison.
- Highlights advantages of LLMs vs traditional sentiment analysis.

### 5. Evaluation
- Semantic similarity scoring.
- LLM-as-a-Judge evaluation.
- Frequency analysis and sentiment distribution.

### 6. Visualization
- Plots for aspect frequencies.
- Sentiment distribution charts.
- Review-by-review sentiment overviews.

---

## Requirements

Install required packages:

```bash
pip install google-generativeai umap-learn pandas numpy matplotlib seaborn scikit-learn
```

## Methodology

1.  **Scraping Reviews**
    * Custom functions fetch reviews, ratings, and metadata.

2.  **Prompt Engineering**
    * Carefully crafted prompts ensure consistent aspect extraction.
    * Output is always structured JSON for easy parsing.

3.  **ABSA Pipeline**
    * Fetch raw reviews
    * Extract aspects
    * Classify sentiment per aspect
    * Store results in a structured dataframe

4.  **Baseline Comparison**
    * VADER is used for traditional sentiment scoring.
    * Comparison shows LLM strength in multi-aspect interpretation.

5.  **Evaluation**
    * Includes:
        * Semantic evaluation
        * LLM-as-Judge scoring
        * Aspect coverage analysis
