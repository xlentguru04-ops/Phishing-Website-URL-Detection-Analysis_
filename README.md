# A Data-Driven Analysis of Phishing Website Characteristics Using Python

## 📌 Project Overview

This project focuses on analyzing phishing and legitimate websites using Python to identify patterns and characteristics associated with suspicious websites.

The analysis includes data cleaning, exploratory data analysis (EDA), feature engineering, statistical analysis, data visualization, and predictive modeling.

The main goal is to understand how phishing websites differ from legitimate websites and identify useful features for phishing detection.

## 🎯 Project Objectives

1. Analyze URL and domain lengths of phishing and legitimate websites.
2. Compare special characters and suspicious URL patterns.
3. Perform statistical analysis of subdomains.
4. Analyze URL similarity and website title-matching scores.
5. Compare website features such as titles, favicons, and descriptions.
6. Examine HTTPS usage, redirects, and other security-related indicators.
7. Identify meaningful patterns through statistical analysis and visualization.
8. Build and evaluate a classification model for phishing detection.

## 📂 Dataset Information

- **Dataset Name:** PhiUSIIL Phishing URL Dataset
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset)
- **Original Dataset:** 235,795 records
- **Dataset Used:** 49,999 records
- **Columns in Analysis:** 56
- **Missing Values:** 0
- **Duplicate Records:** 0
- **Target Column:** `label`

### Target Label Distribution

| Website Type | Records | Percentage |
|---|---:|---:|
| Phishing (0) | 20,625 | 41.25% |
| Legitimate (1) | 29,374 | 58.75% |

## 🛠️ Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 🔍 Data Cleaning and Preprocessing

The dataset was inspected and prepared before analysis.

The following steps were performed:

- Checked dataset structure and data types.
- Verified missing values and duplicate records.
- Examined numerical and categorical columns.
- Checked outliers using the IQR method.
- Created a new feature called `URLLengthCategory`.
- Validated the final dataset before analysis.

Outliers were analyzed but not automatically removed because extreme values may contain useful information about suspicious websites.

## 📊 Exploratory Data Analysis and Statistical Analysis

The analysis focused on comparing phishing and legitimate websites using different URL and website characteristics.

The following areas were analyzed:

- URL and domain length distribution
- Special characters in URLs
- Number of subdomains
- URL similarity and title-matching scores
- Website title, favicon, and description availability
- HTTPS usage and URL redirects
- Correlation between numerical features

## 🔑 Key Findings and Insights

### 1. URL and Domain Length

Phishing websites had an average URL length of **42.14**, compared with **26.28** for legitimate websites.

The average domain length was also higher for phishing websites, at **23.70**, compared with **19.28**.

**Insight:** Longer URLs and domains can be useful warning signs when analyzing suspicious websites.

### 2. Special Characters

Phishing URLs contained an average of **3.43 special characters**, while legitimate URLs contained **1.24**.

**Insight:** Phishing websites tend to use more special characters in their URLs.

### 3. Subdomain Analysis

Phishing websites had an average of **1.18 subdomains**, compared with **1.16** for legitimate websites.

**Insight:** The difference is small, so subdomain count alone is not a strong indicator of phishing.

### 4. Similarity and Title Matching

Legitimate websites had higher domain-title matching scores.

- Phishing websites: **19.76**
- Legitimate websites: **75.44**

**Insight:** Low domain-title matching scores can help identify suspicious websites.

### 5. Website Features

Website titles were present in:

- **64.80%** of phishing websites
- **99.87%** of legitimate websites

Website descriptions were present in:

- **4.22%** of phishing websites
- **73.65%** of legitimate websites

**Insight:** Legitimate websites generally contain more complete website information.

### 6. URL Redirects

The average number of redirects was:

- Phishing websites: **0.15**
- Legitimate websites: **0.12**

**Insight:** Redirect behavior can support phishing analysis, but the difference is small.

## 🤖 Predictive Analysis

A Logistic Regression classification model was developed to identify phishing and legitimate websites.

The dataset was divided into training and testing sets using an 80:20 split.

### Model Performance

| Metric | Result |
|---|---:|
| Accuracy | 99.98% |
| Precision (Phishing) | 100% |
| Recall (Phishing) | 99.95% |
| F1-Score (Phishing) | 99.98% |

### Additional Model Validation

Four selected features were removed to check whether the model still performed well:

- `URLSimilarityIndex`
- `TLDLegitimateProb`
- `DomainTitleMatchScore`
- `URLTitleMatchScore`

After removing these features, the model achieved **99.92% accuracy**.

These results show strong performance on the analyzed dataset. However, further testing with independent data and checks for potential data leakage are needed before real-world deployment.

## 💡 Business Insights and Recommendations

The analysis suggests that phishing detection should consider multiple website characteristics instead of relying on a single feature.

Key recommendations:

- Examine unusual URL lengths and special-character patterns.
- Consider URL similarity and website title-matching scores.
- Analyze website content features such as titles, favicons, and descriptions.
- Do not assume a website is safe simply because it uses HTTPS.
- Use multiple features together to support phishing detection.
- Validate classification models using independent and newer website data.

## 🚀 Future Enhancements

- Test the model on additional phishing datasets.
- Compare Logistic Regression with other machine learning algorithms.
- Evaluate model performance on newly collected websites.
- Develop a simple phishing URL detection application.
- Improve model reliability through additional validation.

## 🔗 Google Colab Notebook

[View Project Notebook](https://colab.research.google.com/drive/1g4Q4mjd2it1fsyvSGNNGkFCE7-9xz2VP?usp=sharin)

## ✅ Conclusion

This project analyzed phishing and legitimate websites using Python.

The analysis identified useful differences in URL length, special characters, similarity scores, and website features.

A Logistic Regression model also achieved strong classification performance on the test dataset.

Overall, the project demonstrates how data analysis and machine learning can help identify suspicious website characteristics and support phishing detection.

---

**Author:** Gurucharan S  
**Project:** AI-Driven Data Analytics – Final Project
