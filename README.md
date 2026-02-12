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

## Section 1) Software and Platform

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

NEED TO FILL IN SECTION 2 ONCE ALL OTHER PARTS OF GITHUB ARE UPLOADED

## Section 2) Repository Structure and Documentation Map

This section describes the organization of the GitHub repository and the purpose of each folder and file.

### Folder and File Descriptions

#### DATA/
Contains the raw dataset used for the project.
- Yelp Restaurant Reviews.csv: Original Yelp restaurant reviews dataset used for all exploratory analysis and modeling. This file is not manually modified.

#### OUTPUT/
Contains generated outputs from the exploratory data analysis.
- yelp_eda.Rmd: R Markdown file used to perform exploratory data analysis.
- yelp_eda.html: Rendered HTML output of the EDA.
- yelp_eda.pdf: PDF version of the EDA results.

#### MILESTONES/
Contains project milestone submissions documenting the project’s development.
- Yelp Reviews Milestone 1.pdf: Initial project proposal and design.
- Yelp Reviews Milestone 2.pdf: Refined analysis plan, EDA findings, and modeling strategy.

#### SCRIPTS/
Contains analysis and modeling code.
- yelp_sentiment_analysis.Rmd: R Markdown file containing text preprocessing, feature engineering, model training, and evaluation.
- yelp_sentiment_analysis.pdf: Rendered PDF output of the sentiment analysis and modeling results.

#### Additional Files
- Yelp Reviews Project - References.pdf: Reference material and sources used in the project.
- README.md: Provides an overview of the project, software requirements, repository structure, and instructions for reproducing results.
- DS 4002 Project 1 Presentation Slides.pdf: Final presentation slides summarizing the research question, data, methods, results, and conclusions of the project.

## Section 3) Instructions for Reproducing Results

This section provides step-by-step instructions to reproduce the exploratory analysis, modeling, and results for this project.

### Step 1: Install Required Software and Packages

- Install **R** and **RStudio**.
- Open RStudio and install all required packages listed in **Section 1** of this README.
- If any packages are missing, R will prompt you to install them when running the scripts.

### Step 2: Obtain and Place the Dataset

- Locate and download the file `Yelp Restaurant Reviews.csv` from the DATA/ folder
- The raw dataset should **not** be manually edited.

### Step 3: Run Data Loading and Cleaning Scripts

- Open the scripts in the `SCRIPTS/` folder.
- Run the script responsible for loading and cleaning the data.
- This script:
  - Reads the CSV file from the `DATA/` folder
  - Standardizes column names
  - Prepares the text and rating variables for analysis

### Step 4: Run Exploratory Data Analysis (EDA)

- Run the EDA script(s) in the `SCRIPTS/` folder.
- These scripts generate summary statistics and plots showing:
  - The distribution of Yelp star ratings
  - The distribution of review lengths
  - Frequently occurring words by star rating
- All EDA figures are saved to the `OUTPUT/` folder.

### Step 5: Run Text Preprocessing and Feature Engineering

- Run the preprocessing script(s) that clean the review text, including:
  - Lowercasing
  - Removing punctuation and numbers
  - Removing stop words
  - Filtering out dessert-related food nouns
- TF–IDF features are created, and review length is added as a numeric predictor.

### Step 6: Train Predictive Models

- Run the modeling script(s) in the `SCRIPTS/` folder to split the data into training and test sets.
- Train the following models:
  - **Logistic regression**
  - **Random forest**
- Class imbalance is addressed using class weighting or balanced sampling.

### Step 7: Evaluate Model Performance

- Run the evaluation code to compute:
  - Accuracy
  - Precision
  - Recall
  - F1 score
  - Confusion matrices
  - ROC AUC values

### Step 8: Review Final Results

- Confirm that the reproduced results align with those reported in the project documentation and presentation.
- Key findings include:
  - Stronger overall performance for the **random forest** model
  - The importance of **review length** and **sentiment-bearing words** in predicting ratings


