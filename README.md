"# dish_based-resturant-recmondtion-system-using-Ai-"
# 🍽️ TASTE AI: Dish-Level Restaurant Recommendation Using Aspect-Based Sentiment Analysis

**Institution:** Sakarya University, Department of Software Engineering  
**Course:** SWE402 - Senior Design Project  

---

## 📖 Project Overview

### The Problem
Traditional online review platforms (like Google Maps or Yelp) evaluate restaurants based on **overall star ratings**. This creates a significant information gap: a restaurant might have a 4.5-star rating, but a specific dish might be terrible. Conversely, a 3-star restaurant might serve the best *Adana Kebap* in the city. To find out which dishes are actually good, users are forced to manually read hundreds of unstructured, lengthy customer reviews.

### The Solution: TASTE AI
**TASTE AI** shifts the paradigm from coarse, review-level grading to **fine-grained, dish-level recommendation**. By leveraging **Aspect-Based Sentiment Analysis (ABSA)**, the system automatically reads thousands of customer reviews, breaks them down into sentence-level opinions, links them to specific menu items, and evaluates the sentiment for each dish. 

The project culminates in a complete ecosystem: an offline AI processing pipeline, a dynamic web dashboard, and a conversational chatbot assistant.

---

## 🏗️ System Architecture

The project is built on a highly decoupled, three-layer architecture:

1. **Input Data Layer:** * Raw Google Maps reviews scraped via Apify.
   * Structured menu metadata (dish names, prices, categories) from 5 local restaurants in Sakarya.
2. **Core Processing Pipeline:** * Data Cleaning $\rightarrow$ Sentence Segmentation $\rightarrow$ Hybrid Entity Matching $\rightarrow$ Subjectivity Filtering $\rightarrow$ Deep Learning Inference (mBERT) $\rightarrow$ Confidence-Weighted Ranking.
3. **Application Layer:** * A Flask REST API backend serving a responsive web interface and a deterministic, rule-based natural language Chatbot.

---

## 🚀 How to Run the Project (Getting Started)

The project is divided into an offline data/AI pipeline (Jupyter Notebooks) and an online application (Flask API). Follow these steps to execute the pipeline from scratch.

### Prerequisites
Ensure you have Python 3.8+ installed, then install the required dependencies:
```bash
pip install pandas numpy pyarrow transformers datasets evaluate scikit-learn rapidfuzz langdetect torch tqdm flask
