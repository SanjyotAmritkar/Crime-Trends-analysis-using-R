# Crime Trends Analysis (2020–Present)

A data-driven exploration of U.S. crime patterns from 2020 onward, focused on identifying trends, predicting criminal activity, and classifying crimes using machine learning and statistical modeling.


## Dataset Overview

- **Source**: [Kaggle – Crime Trends (2020–Present)](https://www.kaggle.com/datasets/sonawanelalitsunil/crime-trends-2020present/data)
- **Records**: 5,000 sampled from 2.5 million+
- **Time Span**: Jan 2020 to recent months
- **Format**: Structured CSV with demographic, spatial, and incident-level features

---

## Preprocessing Highlights

- Cleaned column names using `janitor::clean_names`
- Removed duplicates and handled missing values
- Imputed categorical data using frequency/mode-based logic
- Parsed and standardized date formats
- Removed invalid age values and outliers
- Final dataset saved as `final_data.csv`

---

## Research Questions & Models

### 1️⃣ **Predicting Crime Frequency**  
*Regression on area-crime pairs*

- Models: XGBoost, Random Forest, Ridge Regression
- Best R²: **0.6818** (XGBoost)
- Use: Forecasting crime volume across regions

### 2️⃣ **Clustering Crime Profiles**  
*K-Means clustering of states/cities based on crime type intensity*

- Optimal `k`: 4 (via Elbow and Silhouette methods)
- Result: Grouped locations by dominant crime categories
- Use: Policy planning and regional profiling

### 3️⃣ **Classifying Violent vs. Non-Violent Crimes**  
*Binary classification from structured features*

- Models: Logistic Regression, Random Forest, Decision Tree, XGBoost
- Best Accuracy: **76.65%**
- Best ROC-AUC: **0.8331** (Logistic Regression)
- Use: Automated triage and real-time crime flagging

---

## Exploratory Data Analysis (EDA)

- Temporal trends (monthly/yearly)
- Geographic heatmaps and area-wise comparisons
- Demographics (victim gender, age, race)
- Crime type distributions and status analysis
- Correlation matrix and multivariable insights

---

## Tools & Technologies

- **Language**: R
- **Libraries**: `tidyverse`, `ggplot2`, `caret`, `xgboost`, `randomForest`, `janitor`, `lubridate`, `cluster`
- **Methods**: Regression, Classification, Clustering, Data Cleaning, Visualization

---

## Key Takeaways

- Historical crime data can effectively predict future crime frequencies
- Machine learning models show high potential for crime classification and pattern discovery
- Insights are actionable for law enforcement, public policy, and community engagement

---

## Limitations & Future Work

- Lack of narrative/textual crime data for NLP-based analysis
- Potential for geospatial modeling and inclusion of socioeconomic variables
- Handling class imbalance and outlier effects in sparse categories

---
