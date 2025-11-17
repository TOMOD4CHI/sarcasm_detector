
# Sarcasm Detector

Machine Learning Mini-Project – CI1 –

##  Project Overview

This project focuses on automatically detecting whether an English tweet is **sarcastic** or **non-sarcastic**, using classical Machine Learning techniques for text classification.

The dataset used is **iSarcasmEval_En**, a real dataset used in international NLP competitions.
The goal is to build a full ML pipeline: data exploration, preprocessing, vectorization, model training, evaluation, and final inference.

---

##  Dataset

Source: [https://github.com/iabufarha/iSarcasmEval](https://github.com/iabufarha/iSarcasmEval)

Two CSV files were provided:

| File                 | Purpose                               |
| -------------------- | ------------------------------------- |
| `train.En.csv`       | Model training & validation           |
| `task_A_En_test.csv` | Final testing with the selected model |

Relevant columns:

* **tweet** — The input text.
* **sarcastic** — Target label (`1` sarcastic, `0` non-sarcastic).

Optional columns such as `rephrase`, `sarcasm`, `irony`, etc., were not used for training but may assist in analysis.

---

## 🧪 Workflow Summary

### 1. Exploratory Data Analysis (EDA)

* Basic inspection (`head()`, `info()`, `describe()`).
* Class distribution analysis.
* Tweet length (words/characters).
* Visualizations:

  * Histograms of class distribution.
  * Text length distribution.
  * WordClouds for sarcastic vs non-sarcastic tweets.

### 2. Text Preprocessing

Steps included:

* Lowercasing
* Removing punctuation, URLs, mentions, hashtags
* Removing stopwords
* Optional: lemmatization
* Creating a clean text column: `text_clean`

### 3. Vectorization

Different numerical representations were tested:

* **TF-IDF Vectorizer**
* Bag-of-Words
* (Optional): word embeddings (e.g., BERT)

### 4. Machine Learning Models

At least five models were trained and compared, including:

* Logistic Regression
* Support Vector Machine (SVM)
* Random Forest
* Naive Bayes
* K-Nearest Neighbors (KNN)

For each model:

* Train/test split
* Training
* Evaluation using:

  * Accuracy
  * Precision
  * Recall
  * F1-score
* Confusion matrix visualization

### 5. Model Comparison

All model metrics were summarized in a comparison table.
The best model was selected according to its overall performance (especially F1-score).

### 6. Final Testing

* The best model was applied to `task_A_En_test.csv`.
* The model and predictions were saved for reuse.

---

## 📈 Results

The project produced:

* Visualizations (EDA, word clouds, confusion matrices)
* A full comparison of ML algorithms
* Selection and justification of the best-performing model
* Final predictions on test data

---

##  Repository Structure

```
├── data/
│   ├── train.En.csv
│   ├── task_A_En_test.csv
│
├── notebooks/
│   ├── sarcasm_detection.ipynb
│   ├── sarcasm_detection.html
│
│
├── README.md
```

---

##  Conclusion

This project demonstrates a complete machine-learning workflow for text classification.
After testing several models, the chosen algorithm achieved the best balance between accuracy and generalization, making it the final solution used for inference on the test dataset.

Possible extensions include:

* Using transformer-based models (BERT)
* Handling sarcasm using contextual embeddings
* Improving preprocessing with better linguistic features
---

##  Author
Project developed as part of the **Machine Learning** course (CI1),
