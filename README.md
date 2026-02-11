# DS-4002-Project1
# Yelp Reviews Sentiment Analysis (DS 4002 Project 1)

This repository contains our end-to-end data science project using Yelp restaurant reviews to (1) explore how review language and review length relate to star ratings and (2) build a predictive model that classifies reviews as **Negative (1–3 stars)** vs. **Positive (4–5 stars)**.

## Repository Contents (What’s in here)
At a high level, this repo includes:
- The **raw Yelp reviews dataset** (CSV)
- **EDA outputs** (plots + summary findings)
- **Modeling code** (text cleaning, TF–IDF features, train/test split, logistic regression + random forest)
- **Results artifacts** (metrics, confusion matrices, feature importance)
- **Presentation slides** (PDF export)

---

## 1) Software and Platform

### Software
- **R** (RStudio recommended)

### Platform
- **macOS (Mac)**

### Required R Packages
Install these packages before running the code:
- `tidyverse`
- `readr`
- `dplyr`
- `tidyr`
- `stringr`
- `janitor`
- `tidytext`
- `caret`
- `randomForest`
- `lubridate`
- `knitr`
- `rmarkdown`

(If you run into a missing-package error, install whatever package the error message names.)


3) Instructions to Reproduce Results (Step-by-Step)

Follow these steps to reproduce the key results from this project, including exploratory data analysis, model training, evaluation, and feature importance.

Step 0 — Install R and required packages

Install R and RStudio (recommended).

Open RStudio and run:

install.packages(c(
  "tidyverse", "readr", "dplyr", "tidyr", "stringr", "janitor",
  "tidytext", "caret", "randomForest", "lubridate",
  "knitr", "rmarkdown"
))

Step 1 — Place the dataset in the repository

Download or locate the file Yelp Restaurant Reviews.csv.

Place the file in the DATA/ folder at the top level of the repository.

Do not modify the raw data file.

Step 2 — Run data loading and cleaning scripts

Open RStudio and set your working directory to the project root.

Navigate to the SCRIPTS/ folder.

Run the script responsible for loading and cleaning the data.
This script standardizes column names and prepares the review text and rating variables.

Step 3 — Run exploratory data analysis (EDA)

Run the EDA script(s) in the SCRIPTS/ folder.

These scripts generate:

Distribution of Yelp star ratings

Distribution of review lengths

Word frequency plots by star rating

All EDA figures are saved to the OUTPUT/ folder.

Step 4 — Preprocess text and engineer features

Run the text preprocessing and feature engineering script(s).

This step includes:

Lowercasing text

Removing punctuation and numbers

Removing stop words

Filtering out dessert-related food nouns

Tokenizing review text

TF–IDF features are created, and review length is added as a numeric predictor.

Step 5 — Train predictive models

Run the modeling script(s) in the SCRIPTS/ folder.

The data is split into training and test sets.

Train:

A logistic regression model (with class weighting)

A random forest model (with balanced sampling)

Step 6 — Evaluate model performance

Run the evaluation code to compute:

Accuracy

Precision, recall, and F1 score

Confusion matrices

ROC AUC (via cross-validation)

Model evaluation results and plots are saved to the OUTPUT/ folder.

Step 7 — Verify reproduced results

Confirm that the reproduced results align with those reported in the project documentation and presentation, including stronger performance for the random forest model and the importance of review length and sentiment-bearing words.

---



