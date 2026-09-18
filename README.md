# UK Employment and Mean Pay Analysis

A Python data science project exploring UK employment and mean pay by industry using exploratory data analysis, data preprocessing, linear regression and K-Means clustering.

## Project Overview

This project investigates patterns in UK employment and mean pay data from 2014 to 2025. The analysis combines exploratory visualisation with supervised and unsupervised machine learning to examine changes over time, evaluate a simple forecasting approach and identify structure in employment/pay observations.

Rather than focusing only on model performance, the project also evaluates model limitations through backtesting and comparison with simple baselines.

## Analysis

The notebook covers:

- **Data cleaning** – identifies the true worksheet headers, converts dates and numeric variables, and prepares the employment and mean-pay datasets.
- **Exploratory data analysis** – examines UK employment trends and compares mean pay across higher- and lower-paying industries.
- **Data preprocessing** – handles missing observations using forward filling and demonstrates Z-score standardisation.
- **Linear regression** – predicts June 2025 mean pay using historical time trends for the UK aggregate and individual industries.
- **Backtesting and baselines** – evaluates whether the regression model improves on simpler forecasting approaches.
- **K-Means clustering** – groups employment and mean-pay observations after standardisation, with the number of clusters assessed using the elbow method and silhouette scores.

## Key Findings

The exploratory analysis shows long-term changes in employment and clear differences in mean pay across industries.

For the UK aggregate June 2025 prediction, the linear regression model predicted **£3,226.85** compared with an actual value of **£3,291.00**, an absolute error of **£64.15**.

Across industries, prediction performance varies, showing that a simple linear time trend does not capture every sector equally well. The additional backtesting and baseline comparison provides a more realistic assessment of the model than relying on a single held-out month.

The clustering analysis uses employment and mean pay together to identify groups of similar observations. The notebook also discusses an important limitation: because both variables change over time, some cluster separation may reflect temporal progression rather than distinct underlying economic groups.

## Tools and Technologies

- Python
- pandas
- NumPy
- Matplotlib
- scikit-learn
- openpyxl
- Jupyter Notebook

## Repository Structure

```text
uk-employment-pay-analysis/
├── uk_employment_mean_pay_analysis.ipynb
├── README.md
├── requirements.txt
├── data/
└── figures/
```

The source Excel dataset can be placed in the project directory using the filename expected by the notebook, or the `DATA_FILE` configuration value can be updated to point to its location.

## Methods

**Supervised learning:** Linear Regression  
**Unsupervised learning:** K-Means Clustering  
**Model evaluation:** MAE, RMSE, backtesting and baseline comparison  
**Cluster evaluation:** Elbow Method and Silhouette Score  
**Preprocessing:** Forward filling and Z-score standardisation

## Limitations

The regression model is intentionally simple and primarily captures a linear time trend. Economic and industry pay data may contain seasonality, structural changes and other factors that a single time variable cannot represent.

The clustering analysis is exploratory rather than causal. Cluster membership should therefore be interpreted as similarity in the selected employment and pay features, not as evidence of predefined economic categories.

## Data Availability

The dataset used for this analysis was provided for university coursework and is not included in this repository. The notebook contains the outputs required to review the analysis.

## Purpose

This project demonstrates practical skills in data cleaning, exploratory analysis, visualisation, preprocessing, supervised learning, unsupervised learning and critical model evaluation using real-world-style economic data.
