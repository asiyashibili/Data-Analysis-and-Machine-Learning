# Data Analysis and Machine Learning Projects (Tasks 1–8)

## Overview

This repository contains eight data analysis and machine learning tasks completed using Python. The projects cover data cleaning, exploratory data analysis (EDA), data visualization, customer segmentation, natural language processing, regression, classification, and fraud detection.

The objective of this project collection is to apply analytical and machine learning techniques to different datasets, identify meaningful patterns, evaluate model performance, and communicate findings through visualizations and statistical summaries.

## Technologies and Tools

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn, Plotly
- **Machine Learning:** Scikit-learn
- **Natural Language Processing:** TF-IDF, TextBlob
- **Data Preparation:** Missing-value treatment, duplicate removal, feature engineering, encoding, scaling
- **Development Environment:** Jupyter Notebook

## Project Tasks

### Task 1: Retail Sales Analysis

**Objective:** Analyze retail transactions to understand sales performance, customer demographics, product categories, and sales trends over time.

**Dataset:** `retail_sales_dataset.csv`

**Work performed:**
- Inspected dataset structure, data types, missing values, and descriptive statistics.
- Analyzed sales by product category, gender, and customer age.
- Examined monthly and quarterly sales trends.
- Created visualizations to communicate sales patterns and comparisons.
- Investigated relationships between transaction variables.

**Key findings:**
- Electronics recorded the highest total sales among the three product categories, at 156,905.
- May 2023 was the highest-sales month, with 53,150 in sales.
- The fourth quarter of 2023 recorded the highest quarterly sales, at 126,190.
- Female customers contributed higher total sales than male customers in this dataset.
- The correlation between unit price and total transaction amount was approximately 0.85.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Plotly

### Task 2: Online Retail Customer Segmentation

**Objective:** Segment customers based on purchasing behaviour using Recency, Frequency, and Monetary (RFM) analysis and K-Means clustering.

**Dataset:** `Online Retail.xlsx`

**Work performed:**
- Investigated missing values and duplicate records.
- Removed records without customer IDs and filtered transactions with non-positive quantities or unit prices.
- Calculated transaction amounts.
- Created RFM features to represent how recently, how frequently, and how much customers purchased.
- Scaled RFM features and applied K-Means clustering.
- Used an elbow plot to help select the number of clusters.
- Compared customer groups using their RFM profiles and visualizations.

**Key findings:**
- The analysis produced four customer clusters.
- One cluster contained customers with particularly high purchase frequency and monetary value.
- Another cluster showed relatively low purchase frequency and spending, with longer times since the last purchase.
- The resulting profiles can help explore customer retention and engagement strategies.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

### Task 3: Titanic Dataset Cleaning and Preprocessing

**Objective:** Prepare the Titanic test dataset for further analysis or machine learning by improving data quality and consistency.

**Dataset:** `test.csv`

**Work performed:**
- Inspected the dataset structure, missing values, and duplicate records.
- Checked selected numerical columns for invalid values.
- Imputed missing Age and Fare values using the median.
- Replaced missing Cabin values with `"Unknown"`.
- Standardized whitespace and text-column data types.
- Investigated potential numerical outliers using the IQR method.
- Exported the cleaned dataset as `cleaned_titanic.csv`.

**Key findings:**
- The original dataset contained 418 rows and 11 columns.
- Age, Fare, and Cabin contained missing values.
- The cleaned dataset retained all 418 rows and had no remaining missing values or duplicate rows.

**Tools:** Pandas, NumPy

**Note:** This task focused on data cleaning and preprocessing. It did not train a survival prediction model because the test dataset does not contain the survival target.

### Task 4: Airline Tweet Sentiment Analysis

**Objective:** Classify airline-related tweets as negative, neutral, or positive using natural language processing and machine learning.

**Dataset:** `Tweets.csv`

**Work performed:**
- Examined the distribution of tweet sentiment labels.
- Prepared text data for modelling.
- Converted text into numerical features using TF-IDF.
- Trained and evaluated Multinomial Naive Bayes and Logistic Regression classifiers.
- Compared model accuracy and classification performance.

**Key findings:**
- The dataset contained 14,640 tweets.
- Negative tweets formed the largest sentiment category.
- Multinomial Naive Bayes achieved approximately 72.81% accuracy.
- Logistic Regression achieved approximately 78.83% accuracy and performed better by accuracy on this evaluation.

**Tools:** Pandas, NumPy, Scikit-learn, TF-IDF, Matplotlib, Seaborn

### Task 5: House Price Prediction

**Objective:** Build a regression model to estimate house sale prices from property-related features.

**Dataset:** `train.csv`

**Work performed:**
- Explored the housing dataset and prepared features for modelling.
- Encoded categorical variables using one-hot encoding.
- Split the data into training and testing sets.
- Trained a Linear Regression model.
- Evaluated predictions using Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared.

**Key findings:**
- The dataset contained 1,460 house records.
- The model achieved an R-squared value of approximately 0.8498 on the test set.
- The test RMSE was approximately 33,937, in the target price's units.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

### Task 6: Red Wine Quality Classification

**Objective:** Use physicochemical wine measurements to classify wine quality into grouped categories.

**Dataset:** `winequality-red.csv`

**Work performed:**
- Loaded and explored the dataset.
- Prepared wine-quality categories by grouping quality scores into Low, Medium, and High.
- Prepared features for classification and applied scaling where required.
- Trained and compared Random Forest, Support Vector Classifier (SVC), and Stochastic Gradient Descent (SGD) classifiers.
- Evaluated model accuracy and classification metrics.
- Examined feature importance for the Random Forest model.

**Key findings:**
- The dataset contained 1,599 red wine samples.
- Random Forest achieved approximately 75.31% accuracy.
- SVC achieved approximately 66.56% accuracy.
- SGD Classifier achieved approximately 59.69% accuracy.
- Random Forest had the highest accuracy among the three evaluated models.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

### Task 7: Credit Card Fraud Detection

**Objective:** Identify potentially fraudulent credit card transactions in a highly imbalanced dataset and compare classification models.

**Dataset:** `creditcard.csv`

**Work performed:**
- Examined the dataset and the distribution of fraudulent and legitimate transactions.
- Prepared the data for modelling and applied scaling.
- Used SMOTE on the training data to address class imbalance.
- Trained Logistic Regression and Random Forest models.
- Compared precision, recall, and ROC-AUC to understand the trade-offs between detecting fraud and generating false alarms.

**Key findings:**
- The dataset contained 284,807 transactions, including 492 fraudulent transactions.
- Logistic Regression achieved approximately 91.84% fraud recall, with 5.49% precision and a ROC-AUC of 0.973.
- Random Forest achieved approximately 80.61% fraud recall, with 84.04% precision and a ROC-AUC of 0.962.
- Logistic Regression detected a larger proportion of fraudulent transactions, while Random Forest produced a much higher proportion of correct fraud alerts among its positive predictions.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SMOTE

### Task 8: Google Play Store App Analysis

**Objective:** Explore app characteristics, ratings, installs, pricing, and user-review sentiment to identify patterns in the Google Play Store dataset.

**Datasets:** `googleplaystore.csv`, `googleplaystore_user_reviews.csv`

**Work performed:**
- Cleaned and explored app and user-review datasets.
- Analyzed app categories, ratings, installs, and free-versus-paid distribution.
- Examined app pricing and calculated estimated revenue using price and reported installs.
- Analyzed review sentiment using TextBlob.
- Compared sentiment patterns across app categories.
- Created visualizations, including an interactive Plotly chart.

**Key findings:**
- The cleaned app dataset contained 10,358 rows.
- The average app rating was approximately 4.21.
- The cleaned review dataset contained 29,692 rows.
- TextBlob classified 19,015 reviews as positive, 6,321 as negative, and 4,356 as neutral.
- The FAMILY category contained the largest number of apps in the dataset.
- The relationship between app size and installs was very weak, with a correlation of approximately 0.05.

**Tools:** Pandas, NumPy, Matplotlib, Seaborn, Plotly, TextBlob

**Note:** Revenue calculated from listed price and reported installs is an estimate, not verified actual revenue. Dataset anomalies and missing information should be considered when interpreting the results.

## Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- Descriptive statistics and correlation analysis
- Grouping, aggregation, and feature engineering
- Time-based sales analysis
- Data visualization and interpretation
- RFM analysis and K-Means clustering
- Text preprocessing and TF-IDF feature extraction
- Regression modelling and evaluation
- Classification and model comparison
- Handling imbalanced datasets using SMOTE
- Evaluation using precision, recall, RMSE, R-squared, and ROC-AUC
- Translating analytical results into potential business insights

## Repository Structure

The notebooks are organized by task. Each notebook contains the code and analysis for its respective dataset.

```text
.
├── README.md
├── Task 1 - Retail Sales Analysis.ipynb
├── Task 2 - Customer Segmentation.ipynb
├── Task 3 - Titanic Data Cleaning.ipynb
├── Task 4 - Airline Sentiment Analysis.ipynb
├── Task 5 - House Price Prediction.ipynb
├── Task 6 - Wine Quality Classification.ipynb
├── Task 7 - Credit Card Fraud Detection.ipynb
└── Task 8 - Google Play Store Analysis.ipynb
```

*The filenames above are illustrative. Replace them with your actual notebook filenames if they differ.*

## Conclusion

These eight tasks provided practical experience in analysing different types of data and applying Python-based analytical and machine learning techniques. The collection ranges from exploratory analysis and data preparation to customer segmentation, text classification, regression, and fraud detection.

The projects demonstrate a developing foundation in data analytics, statistical thinking, visualization, and machine learning. Further improvements can include more systematic model validation, additional evaluation metrics, deeper investigation of data-quality issues, and clearer presentation of findings.

---

**Author:** Asiya B  
**Focus Areas:** Data Analytics | Business Analytics | Python | Machine Learning
