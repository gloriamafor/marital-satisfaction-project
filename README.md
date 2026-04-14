# Predicting Marital Satisfaction Using Machine Learning

A data science project that explores what factors most strongly predict marital satisfaction using survey data from **7,178 married individuals across 45 countries**.

This project combines **data cleaning, exploratory data analysis, feature engineering, classification, regression, and interpretation** to answer a simple question:

> What really drives marital satisfaction?

---

## Project Overview

The goal of this project was to analyze marital satisfaction using demographic, emotional, and cultural variables, then build machine learning models to predict satisfaction.

I wanted to go beyond surface-level assumptions like age, number of children, or years married, and see whether **relationship quality**, **culture**, or **religion** had stronger influence.

---

## Dataset

The dataset includes responses from married individuals and contains four main parts:

- **Demographics**
  - age
  - sex
  - education
  - number of children
  - years married
  - material status
  - religion
  - religiosity

- **MRQ (Marriage and Relationship Questionnaire)**
  - measures relationship quality through variables like love, pride, attraction, romance, and enjoyment

- **KMSS (Kansas Marital Satisfaction Scale)**
  - a 1–7 scale measuring marital satisfaction
  - used as the main target variable in this project

- **GLOBE items**
  - measures cultural and family-related expectations

Dataset source:  
[PMC Dataset Source](https://pmc.ncbi.nlm.nih.gov/articles/PMC6923244/#_ad93_)

---

## Project Objectives

This project answers the following questions:

- Which variables best predict marital satisfaction?
- Do demographics influence satisfaction?
- Do emotional and relationship-quality factors matter most?
- Do cultural values contribute to satisfaction?
- Does religion influence satisfaction?

---

## Tech Stack

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Jupyter Notebook**

---

## Workflow

### 1. Data Cleaning
- Removed non-data header rows
- Renamed columns into cleaner labels
- Converted ordinal survey responses into numeric values
- Handled missing values using **median imputation**
- Created target variables for classification and regression

### 2. Feature Engineering
Created:
- `kmss_mean` → average marital satisfaction score
- `satisfied` → binary classification label
- `mrq_mean` → average relationship quality score
- `globe_mean` → average cultural orientation score

### 3. Exploratory Data Analysis
Performed:
- satisfaction distribution analysis
- class balance check
- boxplots and scatterplots
- correlation heatmap

### 4. Modeling
Classification models:
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Decision Tree

Regression model:
- Linear Regression

### 5. Evaluation
Classification metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Regression metrics:
- MAE
- RMSE
- R²

---

## Key Results

### Best Classification Model
**Random Forest**
- Accuracy: **0.885**
- F1-score: **0.932**
- AUC: **0.883**

### Regression Result
**Linear Regression**
- MAE: **0.707**
- RMSE: **1.011**
- R²: **0.484**

---

## Main Findings

### 1. Relationship quality was the strongest predictor
The most important variable was:

- `mrq_mean` (overall relationship quality)

Other top relationship predictors included:
- love
- pride
- romance
- attraction
- enjoyment

### 2. Demographics had weak influence
Variables like:
- age
- sex
- education
- number of children
- years married

had much less predictive power than emotional relationship variables.

### 3. Cultural values had modest influence
The GLOBE-based cultural variables contributed somewhat, but they were not among the strongest predictors.

### 4. Religion had a small overall effect
Religion had low overall feature importance compared to relationship-quality variables, although some group-level differences in average satisfaction existed.

---

## Visual Highlights

This project includes visualizations such as:

- Distribution of marital satisfaction
- Correlation heatmap
- Random Forest feature importance chart

These visuals helped show that:
- most participants were satisfied
- demographics did not strongly explain satisfaction
- emotional connection mattered the most

---

## Repository Structure
├── marital-project.ipynb
├── README.md
└── Martial satifaction_Data.csv

Access my blog here: [marital-satisfaction-blog.html](https://gloriamafor.com/projects/maritalproject/marital-satisfaction-blog.html)
