# DS-4002-Project1
# Yelp Reviews Sentiment Analysis (DS 4002 Project 1)

This repository contains all parts of out data science project where we used Yelp restaurant reviews to (1) explore how review language and review length relate to star ratings and (2) build a predictive model that classifies reviews as **Negative (1–3 stars)** vs. **Positive (4–5 stars)**.

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
- **Yelp Restaurant Reviews.csv:** Original Yelp restaurant reviews dataset used for all exploratory analysis and modeling. This file is not manually modified.

#### OUTPUT/
Contains generated outputs from the exploratory data analysis.
- **yelp_eda.Rmd:** R Markdown file used to perform exploratory data analysis.
- **yelp_eda.html:** Rendered HTML output of the EDA.
- **yelp_eda.pdf:** PDF version of the EDA results.

#### MILESTONES/
Contains project milestone submissions documenting the project’s development.
- **Yelp Reviews Milestone 1.pdf:** Initial project proposal and design.
- **Yelp Reviews Milestone 2.pdf:** Refined analysis plan, EDA findings, and modeling strategy.

#### SCRIPTS/
Contains analysis and modeling code.
- **yelp_sentiment_analysis.Rmd:** R Markdown file containing text preprocessing, feature engineering, model training, and evaluation.
- **yelp_sentiment_analysis.pdf:** Rendered PDF output of the sentiment analysis and modeling results.

#### Additional Files
- **Yelp Reviews Project - References.pdf:** Reference material and sources used in the project.
- **README.md:** Provides an overview of the project, software requirements, repository structure, and instructions for reproducing results.
- **DS 4002 Project 1 Presentation Slides.pdf:** Final presentation slides summarizing the research question, data, methods, results, and conclusions of the project.

## Section 3) Instructions for Reproducing Results

This section provides step-by-step instructions to reproduce the exploratory analysis, modeling, and results for this project.

### Step 1: Install Required Software and Packages

- Install **R** and **RStudio**.
- Open RStudio and install all required packages listed in **Section 1** of this README.
- If any packages are missing, R will prompt you to install them when running the scripts.

### Step 2: Obtain and Place the Dataset

- Locate and download the file `Yelp Restaurant Reviews.csv` from the DATA/ folder
- The raw dataset should **not** be manually edited.

### Step 3: Run exploratory data analysis (EDA)

Open the file `OUTPUT/yelp_eda.Rmd` in RStudio and run it from top to bottom.  
This file contains all code used to perform exploratory data analysis, including:
- Distribution of Yelp star ratings  
- Distribution of review lengths  
- Word frequency plots by star rating  

The rendered EDA outputs are saved as `yelp_eda.html` and `yelp_eda.pdf` in the `OUTPUT/` folder.

### Step 4: Preprocess text and engineer features

Open the file `SCRIPTS/yelp_sentiment_analysis.Rmd` in RStudio and run the preprocessing sections of the file.  
This script performs all text preprocessing and feature engineering steps, including:
- Cleaning and standardizing review text  
- Removing stop words and non-informative terms  
- Filtering out dessert-related food nouns  
- Tokenizing text and creating TF–IDF features  
- Computing review length as an additional numeric feature  

All preprocessing steps are contained within this file and do not require running any additional scripts.

### Step 5: Train predictive models

Continue running `SCRIPTS/yelp_sentiment_analysis.Rmd` to train and evaluate predictive models.  
This file:
- Splits the data into training and test sets  
- Trains a logistic regression model and a random forest model  
- Uses binary classification (1–3 stars as negative, 4–5 stars as positive)  
- Evaluates model performance using accuracy, precision, recall, F1 score, confusion matrices, and ROC AUC  

Model results and figures generated during this step correspond to those reported in the project documentation and presentation.

### Step 6: Review Final Results

- Confirm that the reproduced results align with those reported in the project documentation and presentation.
- Key findings include:
  - Stronger overall performance for the **random forest** model
  - The importance of **review length** and **sentiment-bearing words** in predicting ratings


