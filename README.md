

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

## 📋 License and Credits

This project is part of the coursework for the **XJCO2121 Data Mining** module at **SWJTU-Leeds Joint School**. Data originally sourced from [Drug Review Prediction](https://www.kaggle.com/datasets/oladayoowoeye/drug-review-prediction-sentiment-analysis?select=drugsComTest_raw.tsv).

---


