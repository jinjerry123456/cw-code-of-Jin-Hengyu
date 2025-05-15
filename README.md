

# 💊 Drug Sentiment Analysis Proposal – Code and Dataset

This repository contains the complete code and datasets used for the project **"Drug Sentiment Analysis Proposal Report"**, which compares different sentiment analysis methods (traditional ML, GPT, Weka, Sketch Engine) on a large-scale drug review dataset.

---

## 📁 Repository Structure
initial:
```
.
├── code.ipynb                   # Main Python notebook for data processing and analysis
├── dataset/                     # Dataset folder (compressed files)
│   ├── drugsComTest_raw.zip     # Main test dataset (required for running code.ipynb)
│   └── archive.zip              # Contains full datasets (optional)
│       ├── drugsComTest_raw.tsv
│       ├── drugsComTrain_raw.tsv
│       └── textsentiment.csv
└── README.md                    # Documentation (you are here)
```
After run
```
.
├── code.ipynb                   # Main Python notebook for data processing and analysis
├── dataset/                     # Dataset folder (compressed files)
│   ├── drugsComTest_raw.zip     # Main test dataset (required for running code.ipynb)
│   └── archive.zip              # Contains full datasets (optional)
│       ├── drugsComTest_raw.tsv
│       ├── drugsComTrain_raw.tsv
│       └── textsentiment.csv
├── diagram/                     # Auto-generated charts after running code.ipynb
├── sketch_engine_data/          # Sketch Engine files + usage tutorial
├── weka_data/                   # Weka ARFF file + usage tutorial
├── chatgpt_data/                # GPT prompt file + usage guide
└── README.md                    # Documentation (you are here)
```

---

## ▶️ How to Run

1. **Unzip Dataset**
   Unzip `dataset/drugsComTest_raw.zip` to get the dataset required by the notebook.

2. **Open the Code**
   Open `code.ipynb` in Jupyter Notebook or Google Colab.

3. **Run the Notebook**
   Execute all cells. It will:

   * Preprocess and analyze the dataset.
   * Train several ML models (Logistic Regression, Naive Bayes, etc.).
   * Generate feature importance visualizations.
   * Export results into various folders for external tools.

---

## 📊 Output Description

After successful execution, the following folders will be generated:

### `diagram/`

* Contains:

  * Data cleaning charts
  * Word frequency and distribution charts from advanced study
  * Feature importance and model evaluation plots

### `sketch_engine_data/`

* Contains:

  * `positive_reviews.txt`, `negative_reviews.txt`, and `neutral_reviews.txt` for import into Sketch Engine
  * A short tutorial explaining how to use these files in Sketch Engine

### `weka_data/`

* Contains:

  * `drug_reviews_weka.arff` – ready for use in Weka
  * A tutorial on importing and analyzing this file with Weka

### `chatgpt_data/`

* Contains:

  * `chatgpt_prompt.txt` – A prompt designed to query ChatGPT for sentiment classification
  * A guide on using ChatGPT for batch classification or analysis

---

## 📦 Datasets Summary

| File                    | Description                                            |
| ----------------------- | ------------------------------------------------------ |
| `drugsComTest_raw.tsv`  | Drug reviews test dataset                              |
| `drugsComTrain_raw.tsv` | Training dataset                                       |
| `textsentiment.csv`     | Additional labeled dataset for sentiment analysis      |

---

## 🧪 Model Outputs

* Trained and evaluated models include:

  * Logistic Regression
  * Naive Bayes
  * SVM
  * Random Forest
* Evaluation metrics: accuracy, precision, recall, F1-score
* Visualizations of top features per sentiment

---

### 🔍 Detailed Evaluation Results

**Python (scikit-learn) – Test Set (400 samples):**

| Classifier          | Accuracy | Precision | Recall | F1-Score |
| ------------------- | -------- | --------- | ------ | -------- |
| Logistic Regression | 65.12%   | 0.67      | 0.65   | 0.65     |
| Naïve Bayes         | 60.54%   | 0.62      | 0.61   | 0.61     |
| SVM (Linear Kernel) | 63.64%   | 0.65      | 0.64   | 0.64     |
| Random Forest       | 63.74%   | 0.66      | 0.63   | 0.63     |

**Weka – TF-IDF Features:**

| Model         | Accuracy | F1-Positive | F1-Neutral | F1-Negative | Notes                                         |
| ------------- | -------- | ----------- | ---------- | ----------- | --------------------------------------------- |
| Naïve Bayes   | 7.39%    | 0.670       | 0.302      | 0.485       | Sparse feature issue; 86% unclassified        |
| Random Forest | 71.60%   | 0.812       | 0.316      | 0.541       | Best overall Weka performance                 |
| J48 Tree      | 63.15%   | 0.759       | 0.335      | 0.497       | \~6,000 leaves; offers model interpretability |
| SMO (SVM)     | —        | —           | —          | —           | Very long runtime (\~4.5h); limited results   |

**Key Insights:**

* Logistic Regression (Python) and Random Forest (Weka) performed best in their respective environments.
* Weka's Naïve Bayes struggled with sparse features, while Python's implementation handled them better.
* J48 in Weka provided valuable visual interpretability.
* These results will serve as a baseline for comparison with Transformer-based (e.g., BERT) and GPT-based models in the next phase.

---

## 📋 License and Credits

This project is part of the coursework for the **XJCO2121 Data Mining** module at **SWJTU-Leeds Joint School**. Data originally sourced from [Drug Review Prediction](https://www.kaggle.com/datasets/oladayoowoeye/drug-review-prediction-sentiment-analysis?select=drugsComTest_raw.tsv).

---


